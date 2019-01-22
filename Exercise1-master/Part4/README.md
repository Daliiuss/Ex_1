Part 4: Finally some code
--------------------

Implement this in C, Python and Go:


    global shared int i = 0

    main:
        spawn thread_1
        spawn thread_2
        join all threads (wait for them to finish)
        print i

    thread_1:
        do 1_000_000 times:
            i++
    thread_2:
        do 1_000_000 times:
            i--
            

### Delivery
In this exercise you should take advantage of the starter code found in the subdirectories corresponding to the three different programming languages. Fill out the missing code and make sure your program is working before committing and pushing the changes to your repository.

Finally, create a new file called RESULT.md inside this directory explaining what happens and why. Remember to add, commit and push the new file.

#include <pthread.h>
#include <stdio.h>

void *i=1;

void *Thread1()
{
    int count1 = 0;
    while (count1<1000000)
    {
        count1++;
        i++;
    }
    return (void *) i;
}
void *Thread2()
{
    int count2 = 0;
    while (count2<1000000)
    {
        count2++;
        i--;
    }
    return (void *) i;
}

int main()
{
   pthread_t tid1;
   pthread_t tid2;

   pthread_create(&tid1, NULL, Thread1, NULL);
   pthread_create(&tid2, NULL, Thread2, NULL);

   printf("%d\n",(int)i);

   pthread_join(tid1, &i);
   pthread_join(tid2, &i);

   printf("%d\n",(int)i);

   return 0;
}









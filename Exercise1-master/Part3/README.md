# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 Concurrency - when multiple processes work "at the same time". Multiple processes shares one thread and uses interuptions/time gaps to process data
 
 Parallelism - when multiple processes work at the same time. Multiple processes uses multiple threads to process data at the same time
 
 Difference: Concurrency uses interuptions/switches between processes on single thread while parallelism uses multiple threads for multiple processes 
 
 ### Why have machines become increasingly multicore in the past decade?
 1. Number of software using multiple processes started to rise
 2. Better performance in data processing
 3. Multiple processes running at the same time
 4. Preventing data loss, by runing crucial processes without disruption on seperate threads
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 
 Saves resources and helps optimizing systems which has less cores
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 
 It depends on the size of the software. It might get harder to organize timing in big projects which will consume programmers time
 
 ### What are the differences between processes, threads, green threads, and coroutines?

 Green threads are user-based threads which run in software (not OS)
 Thread is run by OS
 Coroutines are concurrency threads which are based on queues. Shares the same thread.
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > pthread_create() - starts new thread within the process thread
 
 >threading.Thread() - (thread) 
 
 >go - (Coroutine)
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > It locks multiple threads and allows only one thread to run
 
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > multiprocessing, opening module in other process
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > maximum of allowed threads for a program

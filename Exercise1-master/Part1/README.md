Part1: Thinking about elevators
---------------------------

Not for handing in, just for thinking about. Talk to other groups, assistants, or even people who have taken the course in previous years.

Brainstorm some techniques you could use to prevent a user from being hopelessly stranded, waiting for an elevator that will never arrive. Think about the [worst-case](http://xkcd.com/748/) behaviour of the system.

 - What if the software controlling one of the elevators suddenly crashes?"
 1. Multithreading. Using main loop to check wheather thread is terminated. 
 2. If terminated then restart. Receive lost orders from other elevators that keeps all orders stored. If no network conn. then go    to nearest floor?
 3.
 
 - What if it doesn't crash, but hangs?
 1. I'm alive message with checks / Error message / Assumption that it might be dead
 2. 
 
 - What if a message between machines is lost?
 1. Use order list to call last order
 2. if there is no conn. with other elevators, stop at the nearest floor?
 3. 
 
 - What if the network cable is suddenly disconnected? Then re-connected?
 1. We try to implement a connection check s.t. we know the difference between a software crash in one elevator and network disc. 
 2. 
 
 - What if a user of the system is being a troll?
 1. 
 
 - What if the elevator car never arrives at its destination?
1. check if elevator arrived using sensors/ timing
2. if it haven't arrived in the destination

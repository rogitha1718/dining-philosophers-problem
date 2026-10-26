EX NO 6 – Dining Philosophers Problem
Aim
To implement and study the Dining Philosophers Problem.
Domain / Use Case
Concurrent road resource sharing – each car needs two adjacent roads (like a philosopher needs two forks).
Files
File	Description
`ex6_dining_philosophers.c`	Dining Philosophers using one mutex per road
`ex6_output.png`	Program output
Description
For N cars, car `i` locks `road[i]`, then `road[(i+1) % N]`, moves through, and releases both. Each car runs in its own thread.
Compile and run
```bash
gcc ex6_dining_philosophers.c -o dining_philosophers -pthread
./dining_philosophers
```
Enter the number of cars (maximum 20).
Output
![Output](ex6_output.png)
Definition
Dining Philosophers Problem – philosophers sit around a table sharing forks and each needs two forks to eat. Poor allocation can cause deadlock, starvation or indefinite waiting; mutexes and semaphores coordinate access to the shared forks.
Result
Successfully implemented the concepts of the Dining Philosophers Problem.

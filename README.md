# philosopher

The goal of this project is to think and resolve the problem of dining philosopher using mutex.  
The philosopher can be in several state but once at a time :  
&emsp; - 🤔 think.   
&emsp; - 🍔 eat.   
&emsp; - 😴 sleep.   
&emsp; - ✝️ dead.    

The programe takes 4 or 5 arguments : 
- `number of philo` : The number of philo 
- `time to die` : If the philo is not eating after this time he will die of starving. The time is in milliseconds.
- `time to eat` : Time while the philo is eating. The time is in milliseconds.
- `time to sleep` : Time while the philo is sleeping. The time is in milliseconds.
- `number of time each pihilosophers must eat` : not mandatory but if used, stop the programe when each philosophers have eaten this time.

At the beginning of the program all even philosophers will wait 10 milliseconds before starting. This prevents us of deadlock. If all the philosophers start at the same time they will all take their forks and stay blocked.  
Then all the threads will work at the same time. They will try to take the two forks. Then eat and finally think. If one of them doesn't eat before `time to die`, he dies and the program stops.  
Each philosophers have two forks. The left fork is his own and the right fork belongs to the philosopher at his right.  
If `number of time each philosophers must eat` is used, the program will stop if the condition is met. But if a phisolopher is starving the program will stop.

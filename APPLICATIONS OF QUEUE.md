# Exp.No:40  
## APPLICATIONS OF QUEUE

---

### AIM  
To prove that a Given n processes with their burst times, the task is to find average waiting time and average turn around time using FCFS scheduling algorithm. First in, first out (FIFO), also known as first come, first served (FCFS), is the simplest scheduling algorithm. 
Here we are considering that arrival time for all processes is 0. How to compute below times in Round Robin using a program?

Completion Time: Time at which process completes its execution.
Turn Around Time: Time Difference between completion time and arrival time.
Turn Around Time = Completion Time – Arrival Time
Waiting Time(W.T): Time Difference between turn around time and burst time. Waiting Time = Turn Around Time – Burst Time
---

### ALGORITHM  

1. Start the program.  
2. Define the function `CalculateWaitingTime(at, bt, N)`.  
3. Initialize a list `wt` of size `N` with all values set to 0.  
4. Set `wt[0] = 0` for the first process.  
5. Print the table header: "P.No.", "Arrival Time", "Burst Time", "Waiting Time".  
6. Print the values for the first process.  
7. For each process from index `1` to `N-1`:  
   - Calculate `wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i]`.  
   - Print the process number, arrival time, burst time, and waiting time.  
8. Initialize `total_waiting_time = 0`.  
9. Add up all waiting times.  
10. Calculate average waiting time as `average = total_waiting_time / N`.  
11. Print the average waiting time.  
12. Get burst times as input from the user for 5 processes.  
13. Call `CalculateWaitingTime()` with `at`, `bt`, and `N`.  
14. End the program.

---

### PROGRAM  

```
# Python3 program for implementation
# of FCFS scheduling

# Function to find the waiting
# time for all processes
def findWaitingTime(processes, n,
					bt, wt):

	# waiting time for
	# first process is 0
	wt[0] = 0

	# calculating waiting time
	for i in range(1, n ):
		wt[i] = bt[i - 1] + wt[i - 1]

# Function to calculate turn
# around time
def findTurnAroundTime(processes, n,
					bt, wt, tat):

	# calculating turnaround
	# time by adding bt[i] + wt[i]
	for i in range(n):
		tat[i] = bt[i] + wt[i]

# Function to calculate
# average time
def findavgTime( processes, n, bt):

	wt = [0] * n
	tat = [0] * n
	total_wt = 0
	total_tat = 0

	# Function to find waiting
	# time of all processes
	findWaitingTime(processes, n, bt, wt)

	# Function to find turn around
	# time for all processes
	findTurnAroundTime(processes, n,
					bt, wt, tat)

	# Display processes along
	# with all details
	print( "Processes Burst time " +
				" Waiting time " +
				" Turn around time")

	# Calculate total waiting time
	# and total turn around time
	
	
	for i in range(0,n):
	    total_wt+=wt[i]
	    total_tat+=tat[i]
	    print("", str(i+1), " ", str(bt[i]), "", str(wt[i]), "  ", str(tat[i]), " ")
	
	print( "Average waiting time = "+
				str(total_wt / n))
	print("Average turn around time = "+
					str(total_tat / n))

# Driver code
if __name__ =="__main__":
	
	# process id's
	processes = [ 1, 2, 3]
	n = len(processes)

	# Burst time of all processes
	t0=int(input())
	t1=int(input())
	t2=int(input())
	burst_time = [t0,t1,t2]

	findavgTime(processes, n, burst_time)



```

### OUTPUT:
<img width="1267" height="447" alt="image" src="https://github.com/user-attachments/assets/fd32f088-69b1-4d9d-9c9d-2e27bde490cb" />
### RESULT
Thus a python program for the given has been programmed and executed successfully.


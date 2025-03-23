DESCRIPTION:
To calculate the average waiting time using the FCFS algorithm first the waiting
time of the first process is kept zero and the waiting time of the second process is the
burst time of the first process and the waiting time of the third process is the sum of the
burst times of the first and the second process and so on. After calculating all the waiting
times the average waiting time is calculated as the average of all the waiting times. FCFS
mainly says first come first serve the algorithm which came first will be served first.
ALGORITHM:
Step 1: Start the process
Step 2: Accept the number of processes in the ready Queue
Step 3: For each process in the ready Q, assign the process name and the burst time Step
4: Set the waiting of the first process as ‗0‘and its burst time as its turnaround time Step
5: for each process in the Ready Q calculate
a). Waiting time (n) = waiting time (n-1) + Burst time (n-1) b).
Turnaround time (n)= waiting time(n)+Burst time(n)
Step 6: Calculate
a) Average waiting time = Total waiting Time / Number of process
b) Average Turnaround time = Total Turnaround Time / Number of process
Step 7: Stop the process

CODE:

#include <stdio.h>
#include <conio.h>

int main() {
    int bt[20], wt[20], tat[20], i, n;
    float wtavg, tatavg;

    clrscr();

    printf("\nEnter the number of processes -- ");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        printf("\nEnter Burst Time for Process %d -- ", i);
        scanf("%d", &bt[i]);
    }

    wt[0] = wtavg = 0;
    tat[0] = tatavg = bt[0];

    for (i = 1; i < n; i++) {
        wt[i] = wt[i - 1] + bt[i - 1];
        tat[i] = tat[i - 1] + bt[i];
        wtavg += wt[i];  // Use += for cleaner addition
        tatavg += tat[i]; // Use += for cleaner addition
    }

    printf("\t PROCESS \tBURST TIME \t WAITING TIME\t TURNAROUND TIME\n");
    for (i = 0; i < n; i++) {
        printf("\n\t P%d \t\t %d \t\t %d \t\t %d", i, bt[i], wt[i], tat[i]);
    }

    printf("\nAverage Waiting Time -- %f", wtavg / n);
    printf("\nAverage Turnaround Time -- %f", tatavg / n);
    getch();
    return 0; // Added return 0 for good practice
}
DESCRIPTION:
To calculate the average waiting time in the shortest job first algorithm the sorting of
the process based on their burst time in ascending order then calculate the waiting time of
each process as the sum of the bursting times of all the process previous or before to that
process.
ALGORITHM:
Step 1: Start the process
Step 2: Accept the number of processes in the ready Queue
Step 3: For each process in the ready Q, assign the process id and accept the CPU
burst time
Step 4: Start the Ready Q according the shortest Burst time by sorting according to
lowest to highest burst time.
Step 5: Set the waiting time of the first process as ‗0‘ and its turnaround time as its burst
time.
Step 6: Sort the processes names based on their Burt time
Step 7: For each process in the ready queue,
calculate
a) Waiting time(n)= waiting time (n-1) + Burst time (n-1)
b) Turnaround time (n)= waiting time(n)+Burst time(n)
Step 8: Calculate
c) Average waiting time = Total waiting Time / Number of process
d)Average Turnaround time = Total Turnaround Time / Number of process
Step 9: Stop the process

SOURCE CODE :
#include <stdio.h>
#include <conio.h>

int main() {
    int p[20], bt[20], wt[20], tat[20], i, k, n, temp;
    float wtavg, tatavg;

    clrscr();

    printf("\nEnter the number of processes -- ");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        p[i] = i;
        printf("Enter Burst Time for Process %d -- ", i);
        scanf("%d", &bt[i]);
    }

    for (i = 0; i < n; i++) {
        for (k = i + 1; k < n; k++) {
            if (bt[i] > bt[k]) {
                temp = bt[i];
                bt[i] = bt[k];
                bt[k] = temp;
                temp = p[i];
                p[i] = p[k];
                p[k] = temp;
            }
        }
    }

    wt[0] = wtavg = 0;
    tat[0] = tatavg = bt[0];

    for (i = 1; i < n; i++) {
        wt[i] = wt[i - 1] + bt[i - 1];
        tat[i] = tat[i - 1] + bt[i];
        wtavg = wtavg + wt[i];
        tatavg = tatavg + tat[i];
    }

    printf("\n\t PROCESS \tBURST TIME \t WAITING TIME\t TURNAROUND TIME\n");
    for (i = 0; i < n; i++) {
        printf("\n\t P%d \t\t %d \t\t %d \t\t %d", p[i], bt[i], wt[i], tat[i]);
    }

    printf("\nAverage Waiting Time -- %f", wtavg / n);
    printf("\nAverage Turnaround Time -- %f", tatavg / n);
    getch();
    return 0; // Added return 0; for good practice
}
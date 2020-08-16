//MUHAMMAD AZHAN HANNAN BIN MOHD ABDUL AZIZ
//1719583
//OPERATING SYSTEM SECTION 3

#include<iostream>
using namespace std;

	struct Process
	{
   int ccode;     // course code
   int duration;      // class duration
   int priority;  //priority
   int arrival_time;   //prefered arrival time
	};
	
	// courses CSC2201 with priority 2 for 3 hours with prefered to start first, 
	// CSC3401 with priority 3 for 2 hours prefered to start second, 
	// and CSC1103 with priority 1 for 1 hour 
	Process proc[] = {{2201,3,2,1}, {3401, 2, 3,2}, {1103, 1,1,3}};

// function to find the waiting time for all processes
void findWaitingTime(int processes[], int n, int bt[], int wt[])
{
    // waiting time for first process will be 0
    wt[0] = 0;
 
    // calculating waiting time
    for (int i = 1; i < n ; i++)
    {
        wt[i] =  bt[i-1] + wt[i-1];
    }
}
 
// function to calculate turn around time
void findTurnAroundTime( int processes[], int n, int bt[], int wt[], int tat[])
{
    // calculating turnaround time by adding
    // bt[i] + wt[i]
    for (int i = 0; i < n ; i++)
    {
        tat[i] = bt[i] + wt[i];
    }
}
 
// function to calculate average time
void findAverageTime( int processes[], int n, int bt[])
{
    int wt[n], tat[n], total_wt = 0, total_tat = 0;
 
    // function to find waiting time of all processes
    findWaitingTime(processes, n, bt, wt);
 
    // function to find turn around time for all processes
    findTurnAroundTime(processes, n, bt, wt, tat);
 
    // display processes along with all details
    cout << "\n Class  "<< " Burst time  "<< " Waiting time  " << " Turn around time\n" <<endl;
 
    // calculate total waiting time and total turn around time
    for (int i = 0; i <n ; i++)
    {
        total_wt = total_wt + wt[i];
        total_tat = total_tat + tat[i];
        cout << "   " << proc[i].ccode << " \t" << bt[i] <<" \t   "<< wt[i] <<"\t\t  " << tat[i] <<endl<<endl;
    }
 
 	cout <<"===============================================================" <<endl;
    cout << "\nAverage waiting time = "<< (float)total_wt / (float)n;
    cout << "\nAverage turn around time = "<< (float)total_tat / (float)n <<endl;
    cout << "\n===============================================================" <<endl;
}



int main ()
{
	cout << "\n===============================================================" <<endl;
	cout <<"MUHAMMAD AZHAN HANNAN BIN MOHD ABDUL AZIZ | 1719583 | Section 3" << endl;
	cout <<"FIRST COME FIRST SERVE ALGORITHM" << endl;
	cout <<"===============================================================" <<endl;
	
	// process ids
    int processes[] = { 1, 2, 3};
    int n = sizeof processes / sizeof processes[0];
 
    // burst time of all processes
    int  burst_time[] = {3, 2, 1};
 
    findAverageTime(processes, n,  burst_time);
    
    return 0;
}

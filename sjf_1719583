//MUHAMMAD AZHAN HANNAN BIN MOHD ABDUL AZIZ
//1719583
//OPERATING SYSTEM SECTION 3
#include<iostream>
using namespace std;
struct Process
	{
   int ccode;     // course code
   int duration;  // class duration
   int priority;  //priority
   int arrival_time;   //prefered arrival time
	};
	
	// courses CSC2201 with priority 2 for 3 hours with prefered to start first, 
	// CSC3401 with priority 3 for 2 hours prefered to start second, 
	// and CSC1103 with priority 1 for 1 hour 
	Process proc[] = {{2201,3,2,1}, {3401, 2, 3,2}, {1103, 1,1,3}};
	
int main(){
	
	cout << "\n===============================================================" <<endl;
	cout <<"MUHAMMAD AZHAN HANNAN BIN MOHD ABDUL AZIZ | 1719583 | Section 3" << endl;
	cout <<"SHORTEST JOB FIRST SCHEDULING ALGORITHM" << endl;
	cout <<"===============================================================" <<endl;
	int bt[20],p[20],wt[20],tat[20],i,j,n,total=0,pos,temp, temp2;
    float avg_wt,avg_tat;
    n = 3; //initialize process into 3 class
   
    for(i = 0; i<n ; i++){
    bt[i] = proc[i].duration;
	}
	
	//sorting burst time in ascending order using selection sort
    for(i=0;i<n;i++)
    {
        pos=i;
        for(j=i+1;j<n;j++)
        {
            if(bt[j]<bt[pos])
                pos=j;
        }
 
        temp=bt[i];
        bt[i]=bt[pos];
        bt[pos]=temp;
 
        temp2=proc[i].ccode;
        proc[i].ccode=proc[pos].ccode;
        proc[pos].ccode=temp2;
    }
    
	wt[0]=0;            //waiting time for first process will be zero
 
    //calculate waiting time
    for(i=1;i<n;i++)
    {
        wt[i]=0;
        for(j=0;j<i;j++)
            wt[i]+=bt[j];
 
        total+=wt[i];
    }
 
    avg_wt=(float)total/n;      //average waiting time
    total=0;
	
    cout << "\nClass" << "\tBurst Time" << "\tWaiting Time" << "\tTurnaround Time" << endl; 
    
    
    for(i=0;i<n;i++)
    {
        tat[i]=bt[i]+wt[i];     //calculate turnaround time
        total+=tat[i];
        cout << "\n"<<proc[i].ccode<<"\t\t"<<bt[i]<<"\t\t"<< wt[i]<<"\t\t"<<tat[i] << endl;
    }
 
    avg_tat=(float)total/n;     //average turnaround time
    
    cout << "\n====================================" <<endl;
    cout << "\nThe class scheduling is as below :" <<endl;
    cout << endl;
 	for(i=0;i<n;i++)
	cout<<proc[i].ccode<<" \t";
	cout<<endl;
    
    cout << "\n===============================================================" <<endl;
    cout << "\nAverage Waiting Time= " << avg_wt << endl;
    cout << "Average Turnaround Time= " << avg_tat << endl;
	cout << "\n===============================================================" <<endl;
}	

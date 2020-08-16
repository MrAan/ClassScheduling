# Introduction

Praise to the Almighty, I have completed my project on the CPU scheduling algorithm. I have been tasked to finished this project by 17 of August 2020. We delivered this project to test our understanding in the CPU scheduling algorithm which is under the topic of Uniprocessor Scheduling. At first, I have listed some other CPU scheduling such as Round Robin, Highest Response Ratio Next (HRRN), and also Feedback (FB). Round Robin and Feedback scheduling algorithm are preemptive, which is may be interrupted while HRRN is non-preemptive (cannot be interrupted). But after taking some calculation. I have decided to use Shortest Job First Scheduling Algorithm and Shortest Remaining Time algorithm.

As mention above, I have choose 2 algorithms which are:

Shortest Remaining Time Scheduling Algorithm (SRTF)
Shortest Job First Scheduling Algorithm (SJF)
SRTF is preemptive while SJF is a non-pre-emptive. But for SRTF, the decision mode of preemptive is only at the arrival. SRTF the process with the shortest expected remaining process time. A process may be preempted when another process becomes ready. As for the SJF, the scheduling selects the process with the shortest expected processing time and does not preempt the process.

# Consideration

For this project, my consideration in on to find the most optimum algorithm that can suit the task which is for the class scheduling. The first idea that came up in my mind is SJF. This is because SJF is non-preemptive. Imagine the situation of conducting a class. It is unusual to held a class and then pause the class after 30 min to give other classes continue their subject and pass the time back to the previous subject. I consider is as a rare method for conducting a class and I never experience it. So, I came up with the idea to proceed the class until the end which is a non-pre-emptive decision mode and align with the SJF method.

I have stated above regarding the rare method of teaching which is, pause a class session and pass it to another class and then continue again for the class. Even though I said that it is a rare method of teaching but, it may be a perfect way of teaching for some students. As for me, I knew that if I am learning, I need to take a break for a while or change to another topic which can give move time for my brain to process and at the same time, processing new knowledge. I believe that there is also a student who usual with that type of learning. That is why I choose the SRTF scheduling for my project.

# Analysis

In this section, I will give my analysis of my algorithm that I have chosen and make comparison with the FCFS scheduling.

## FCFS

As we know, FCFS scheduling is a non-preemptive decision mode. It means that it will not allow any task or process to interrupt until it finished the first task. The FCFS scheduling will ignore the burst time, and only focusing on the arrival time. It will not follow any rules of priority. As for FCFS, this is the most straight forward method and have no consideration of priority. As for the result of my programming, the result is as below.

Average waiting time = 2.66667
Average turn around time = 4.66667

For the scheduling, the class flow will be as below:

2201 < 3401 < 1103

Among the 3 algorithms, FCFS take the longest time for average waiting time and also the turnaround time which make it the less preferable algorithm for the class scheduling.

## Algo2

My second algorithm is the SRTF scheduling algorithm. We know that supposedly SRTF will that the shortest remaining time of process or service time and also consider that arrival time. That is why SRTF is specified as the pre-emptive decision mode. I would not say that SRTF is the fairest but SRTF indeed is optimum to be used and good for time management. As for the result is as below:

Average waiting time =1.33333
Average Turnaround time =3.33333

By using the SRTF, as we can above, we manage to reduce the average waiting time into half as compared to FCFS. How this can be happen? SRTF will prioritize the process that has lesser remaining time. If the current process has a higher processing time, the SRTF scheduling algorithm will pre-empt it and allow the process that has lesser remaining time. And this will allow the process to be done faster than FCFS.

The scheduling can be seen below:
2201 1103 3401

## Algo3

The last one is the SJF scheduling algorithm. From my view, I can say that the SJF scheduling algorithm is almost the same as SRTF. The only difference is SJF is non-pre-emptive while SRTF is pre-emptive. It means that SJF cannot be interrupted during the whole process of scheduling. It will not entertain another process as long as the current process is not finished. Even though it is similar with FCFS that categories as the same decision mode; nonpreemptive, SJF is much better than FCFS. FCFS will finish a process that arrived first, SJF did the same too. What differs is after finished the first task, SJF will look for another task that has lesser processing time while FCFS will straightforward do the next job without consider the processing time. That is how SJF can cut more average waiting time compared to FCFS. This is the result of my SJF scheduling algorithm:

Average Waiting Time= 1.33333
Average Turnaround Time= 3.33333

As you can see, it is the same same as SRTF but the average waiting time is half of the FCFS. It is shown that SJF is more preferable to use as compared to FCFS.

But for the class scheduling, since my algorithm ignore the arrival time, you can see the result as below:
1103 3401 2201

Since class 1103 has the shortest expected processing time, SJF chooses to process it first and continue by the next class. But if we consider the arrival time. It should be that class 2201 will start first, continued by 1103 since it has the shortest processing time and followed by 3401.


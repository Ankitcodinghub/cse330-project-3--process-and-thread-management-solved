# cse330-project-3--process-and-thread-management-solved
**TO GET THIS SOLUTION VISIT:** [CSE330 Project 3- Process and Thread Management Solved](https://www.ankitcodinghub.com/product/cse330-operating-systems-project-3-process-and-thread-management-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;120774&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;5&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (5 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE330  Project 3- Process and Thread Management Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (5 votes)    </div>
    </div>
<h1>Brief Summary</h1>
Process and thread management is a key responsibility given to modern operating systems. The operating system is responsible for creating, scheduling, and terminating processes running within a computer. Nearly every computer used today has multiple processors, which are used to run computations in parallel to improve performance. However, it must be stated that programs which use multiple processors must handle issues which arise from concurrency in order to ensure robustness. To achieve software robustness, many multithreaded processes today use shared memory regions, which must be managed to ensure concurrency violations don’t occur.

<h1>1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Background Information</h1>
In this project, your task is to write a kernel module to calculate the total elapsed time of all the processes that belong to a given user in the system. To demonstrate the efficiency and challenges associated with multithreaded systems, you will model this task as a form of the classic <em><sub>producer-consumer </sub></em>problem.

<ul>
<li>The producers and consumers of this project will be kernel threads in your module.</li>
<li>A producer thread will find processes that belong to a given user and add the process information to a shared buffer.</li>
<li>Consumers remove process information from the shared buffer, calculate the elapsed time that these processes have run, and output the total elapsed time to the kernel’s log.</li>
<li>sudo apt update</li>
<li>sudo apt install git</li>
<li>git clone -b PTM https://github.com/ASTERISC-Teaching/cse330-public.git</li>
</ul>
Directory breakdown. The repository contains the following directories:

<ul>
<li><sub>process_gen: </sub>Contains code which produces processes for project.</li>
<li>c: Kernel module which will contain the implementation.</li>
<li>testcase_outputs: Screenshots of expected test case output.</li>
<li><sub>sample_code: </sub>Sample code which offers examples as to how threads/semaphores are used.</li>
<li><sub>sh: </sub>Script that allows you to run a test.</li>
</ul>
<table width="623">
<tbody>
<tr>
<td width="116">Important note</td>
<td width="507"></td>
</tr>
<tr>
<td colspan="2" width="623">•&nbsp;&nbsp; This document only contains high-level instructions for completing this project; they are NOT EXACT step-by-step instructions. You MUST figure out the steps on your own.

•&nbsp;&nbsp; This project requires you to use the kernel (Linux v6.6.9) you compiled in project #1. If you are changing your group, it is okay to get the VM disk from your previous group and use it.

•&nbsp;&nbsp; Remember to add debug statements inside the kernel module (e.g., using printk) to see what your code is doing and debug the operations. This applies to all steps of the project.

•&nbsp;&nbsp; Using semaphores (explained in section 2) incorrectly in this project can cause your kernel to hang (e.g., due to a deadlock). If it does, simply restart your virtual machine, and find where the kernel module was stuck.

•&nbsp;&nbsp; We provide you all testcases but it is your job to understand what these testcases are doing.

•&nbsp;&nbsp; The TAs/Instructor will not help you complete the bonus parts. That is totally on you.

•&nbsp;&nbsp; If your assignment does not compile or your upload is corrupted, you will get a zero. Always double-check your submission.
</td>
</tr>
</tbody>
</table>
<h1>2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Prerequisite Knowledge</h1>
In this section, we will provide short details regarding three core concepts you will use to build this project: <em>kernel threads, semaphores, and task list</em>. If you are not familiar with using any of these concepts, please refer to the attached reading and lecture slides for further study.

<h2>Kernel Threads</h2>
To create and start the kernel threads, you can use the kthread_run() function.

<table width="624">
<tbody>
<tr>
<td width="624">/*

threadfn is the function to run in the thread; data is the data pointer for threadfn; namefmt is the name for the thread.

It returns a pointer to the thread’s task_struct if the thread creation is successful or ERR_PTR(-ENOMEM) if it fails.*/

struct task_struct *kthread_run(int (*threadfn)(void *data), void *data, *const char *namefmt, …)
</td>
</tr>
</tbody>
</table>
1

2

3

4

5

6

7

Example code to create a kernel thread:

<table width="624">
<tbody>
<tr>
<td width="624">#include &lt;linux/kthread.h&gt;

// the function to run in the thead static int kthread_func(void *arg) {

// Thread Code

}

// Create and run a thread that executes “kthread_func” ts1 = kthread_run(kthread_func, NULL, “thread-1”);
</td>
</tr>
</tbody>
</table>
1

2

3

4

5

6

7

8

9

To stop a kernel thread, you need to use kthread_stop. It sets end_flag for thread k to return TRUE. The thread k can check its end_flag using kthread_should_stop and determine if it should stop.

<table width="624">
<tbody>
<tr>
<td width="400">// stop the kernel thread pointed by task_struct k kthread_stop(struct task_struct *k)

// when kthread_stop() is called, this function will kthread_should_stop(void)
</td>
<td width="53">return</td>
<td width="171">true</td>
</tr>
</tbody>
</table>
1

2

3

4

5

Semaphores are a type of lock. Recall that locks are used to regulate threads executing within a code region, and synchronize the reading and writing of the shared data.

Use these in areas which contain <em><sub>critical code</sub></em>, such as when threads read and write to the shared buffer.

<table width="335">
<tbody>
<tr>
<td width="92"></td>
<td width="243">Kernel Semaphore</td>
</tr>
<tr>
<td width="92">Define</td>
<td width="243">struct semaphore &lt;name&gt;;</td>
</tr>
<tr>
<td width="92">Initialize</td>
<td width="243">sema_init(&amp;&lt;name&gt;, BUFFER_SIZE);</td>
</tr>
<tr>
<td width="92">Wait</td>
<td width="243">down(&amp;&lt;name&gt;);</td>
</tr>
<tr>
<td width="92">Post</td>
<td width="243">up(&amp;&lt;name&gt;);</td>
</tr>
</tbody>
</table>
Table 1: Functions Related To Kernel Semaphores The following code snippet explains how to use semaphores:

<table width="624">
<tbody>
<tr>
<td width="624">// Defines a semaphore with a given name struct semaphore name;

// a function to initialize a semaphore static inline void sema_init(struct semaphore *sem, int val)

// acquire a lock structure void down(struct semaphore *sem)

// release a loc void up(struct semaphore *sem)
</td>
</tr>
</tbody>
</table>
1

2

3

4

5

6

7

8

9 10

11

An example of how to use semaphores and regulate a critical section:

<table width="624">
<tbody>
<tr>
<td width="624">#include &lt;linux/semaphore.h&gt; // Semaphore Definition struct semaphore empty; // define a semaphore named ’empty’ sema_init(&amp;empty, 5); // init the semaphore as 5

// if the thread works in an infinite loop, this is how it knows when to stop.

Check (4) module_exit for more information.

while (!kthread_should_stop())

{ if (down(&amp;empty)) break; // exit
</td>
</tr>
</tbody>
</table>
1

2

3

4

5

6

7

8

9

<table width="624">
<tbody>
<tr>
<td width="624">// Beginning Critical section ….

….

// End of Critical Section up(&amp;empty) // signal the semaphore
</td>
</tr>
</tbody>
</table>
10

11

12

13

14

Suggested reading(s)

Please refer to the sample code to see how semaphores work: <a href="https://github.com/ASTERISC-Teaching/cse330-public/tree/PTM/sample_code/down_up">Semaphore Sample Cod</a><a href="https://github.com/ASTERISC-Teaching/cse330-public/tree/PTM/sample_code/down_up"><sub>e </sub></a>Further Reading for using semaphores: <a href="https://cs162.org/static/proj/pintos-docs/docs/synch/semaphores/#:~:text=%E2%80%9CDown%E2%80%9D%20or%20%E2%80%9CP%E2%80%9D,waiting%20thread%2C%20if%20any).">Synchronization and Semaphore</a><a href="https://cs162.org/static/proj/pintos-docs/docs/synch/semaphores/#:~:text=%E2%80%9CDown%E2%80%9D%20or%20%E2%80%9CP%E2%80%9D,waiting%20thread%2C%20if%20any)."><sub>s</sub></a>

<h1>Task List</h1>
The Linux kernel stores all of the active processes in a circular doubly linked list called “task list”. Each element in the task list is a process descriptor of the struct type task_struct which contains all of the information about a process. The figure below illustrates the task list and its task_struct entries.

The task_struct contains the process’ PID in pid and the process’ user’s UID in cred-&gt;uid.val

<table width="624">
<tbody>
<tr>
<td width="348">struct task_struct *task; task-&gt;pid // PID of the process task-&gt;cred-&gt;uid.val // UID of the user of the</td>
<td width="276">process</td>
</tr>
</tbody>
</table>
1

2

3

We use the for_each_process macro to iterate through the task list to access each task_struct. The macro goes over all the task_struct in the task list one by one. The following code example calculates the number of processes in the task list using for_each_process.

<table width="624">
<tbody>
<tr>
<td width="624">#include&lt;linux/sched.h&gt;

#include &lt;linux/sched/signal.h&gt;

struct task_struct* p; size_t process_counter = 0;
</td>
</tr>
</tbody>
</table>
1

2

3

4

5

<table width="624">
<tbody>
<tr>
<td width="624">// On each iteration, p points to the next task in the list.

for_each_process(p) {

++process_counter;

}
</td>
</tr>
</tbody>
</table>
6

7

8

9

10

<h1>Task #1: Write Producer Thread Code</h1>
In your kernel module, the producer thread should search the task list for all the processes that belong to the test_cse330 user (our test scripts will automatically create this user) and add their task_struct to a shared buffer. There will be only one producer in your module, and it should exit after it has iterated through the entire task list.

<h1>Task #2: Write Consumer Thread Code</h1>
Each consumer thread should read the task_struct of the processes from the shared buffer and calculate the elapsed time for each process and the total elapsed time.

<ul>
<li>For each process, you need the pid, start_time, and boot_time to calculate elapsed time.</li>
<li>The total elapsed time is the sum of elapsed time for all processes of a user.</li>
</ul>
You will need to synchronize the access of threads from the shared buffer using a semaphore. Also, multiple consumers in the system can work in an infinite loop; remember to check end_flag so they know when to stop.

<h1>Task #3: Cleanly Exit The Kernel Module</h1>
Your kernel module will not exit cleanly if any threads are waiting for semaphores (e.g., it might hang the VM). Hence, you need to make sure that no threads are waiting for semaphores. To do so, signal all the semaphores; if you expect multiple threads waiting on a semaphore; signal it multiple times.

<h1>3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Submission Details</h1>
Please place the following in one zip file and submit on canvas.

<ul>
<li>The producer_consumer.c file. Please do not submit any binaries/.ko files.</li>
<li>Output screenshots that show your code is working for each test case.</li>
<li>A README text file clearly describing the name of the members within your group and any other details you want the TAs to know.</li>
</ul>
<h1>4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Grading Rubric (Regular)</h1>
There are 100 points available for this assignment, with 10 points of bonus. To test your assignment, you must run the test.sh script we have provided.

Here is a breakdown of how to use the script:

<table width="624">
<tbody>
<tr>
<td width="624">./test.sh &lt;Number of processes&gt; &lt;Buffer Size&gt; &lt;Number of Producers&gt; &lt;Number of

Consumers&gt; &lt;Lines from dmesg&gt;
</td>
</tr>
</tbody>
</table>
1

<ul>
<li>Number of Processes: The total number of processes that the script will create.</li>
<li><sub>Buffer Size</sub>: The size of the shared buffer which will be used by the producers and consumers.</li>
<li>Number of Producers: The number of producer threads to be used.</li>
<li>Number of Consumers: The number of consumer threads to be used.</li>
<li><sub>Lines from dmesg</sub>: The number of lines which will be printed from the dmesg to the console.</li>
</ul>
Test Case Scoring

<ul>
<li>sudo ./test.sh 10 5 1 0 25: 5 points</li>
<li>sudo ./test.sh 10 5 0 1 25: 5 points</li>
<li>sudo ./test.sh 10 50 1 1 25: 10 points</li>
<li>sudo ./test.sh 100 50 1 1 25: 15 points</li>
<li>sudo ./test.sh 1000 50 1 1 100: 15 points</li>
<li>Points Awarded for Code: 50 points</li>
</ul>
<h1>5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Grading Rubric (Bonus)</h1>
This bonus test case tests if your code is able to handle multiple consumer threads.

<ul>
<li>sudo ./test.sh 100 50 1 2 25: 10 points</li>
<li>There is no partial grading within individual test cases for the bonus part.</li>
</ul>

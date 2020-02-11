The goal of the assignment is to 1) compare and analyze sort algorithms from the perspectives of time complexity and actual execution time respectively and 2) learn of the advantage and disadvantage of empirical analysis and theoretical analysis. This is a practice of both empirical and mathematical analysis.

General Plan for Empirical Analysis of Algorithm Time Efficiency

1. Understand the experiment's purpose.

2. Decide on the efficiency metric M to be measured and the measurement unit (an operation's count vs. a time unit).

3. Decide on characteristics of the input sample (its range, size, and so on). 4. Prepare a program implementing the algorithm (or algorithms) for the experimentation.

5. Generate a sample of random inputs.

6. Run the algorithm (or algorithms) on the sample's inputs and record the data observed.

7. Analyze the data obtained.


There are several different goals one can pursue in analyzing algorithms empirically. They include checking the accuracy of a theoretical assertion about the algorithm's efficiency, comparing the efficiency of several algorithms for solving the same problem or different implementations of the same algorithm, developing a hypothesis about the algorithm's efficiency class, and ascertaining the efficiency of the program implementing the algorithm on a particular machine.

Here, in the assignment, we emphasize on empirically and theoretically comparing the efficiency of three sort algorithms: insertion sort, selection sort, and merge sort. 

Also, as for the timing clock-based empirical analysis approach, it is important to keep several facts in mind, however. First, a system's time is typically not very accurate, and you might get somewhat different results on repeated runs of the same program on the same inputs. An obvious remedy is to make several such measurements and then take their average (or the median) as the sample's observation point. Second, given the high speed of modern computers, the running time may fail to register at all and be reported as zero. The standard trick to overcome this obstacle is to run the program in an extra loop many times, measure the total running time, and then divide it by the number of the loop's repetitions. Third, on a computer running under a time-sharing system (such as UNIX), the reported time may include the time spent by the CPU on other programs, which obviously defeats the purpose of the experiment. Therefore, you should take care to ask the system for the time devoted specifically to execution of your program. (In UNIX, this time is called the "user time," and it is automatically provided by the time command.) Thus, measuring the physical running time has several disadvantages, both fundamental (dependence on a particular machine being the most important of them) and technical, not shared by counting the executions of a basic operation.

On the other hand, the physical running time provides very specific information about an algorithm's performance in a particular computing environment, which can be of more importance to the experimenter than, say, the algorithm's asymptotic efficiency class. In addition, measuring time spent on different segments of a program can pinpoint a bottleneck in the program's performance that can be missed by an abstract deliberation about the algorithm's basic operation. Getting such data-called profiling-is an important resource in the empirical analysis of an algorithm's running time; the data in question can usually be obtained from the system tools available in most computing environments. 

The principal strength of the mathematical analysis is its independence of specific inputs; its principal weakness is its limited applicability, especially for investigating the average-case efficiency. The principal strength of the empirical analysis lies in its applicability to any algorithm, but its results can depend on the particular sample of instances and the computer used in the experiment.

Tasks of Comparing time complexity of insertion sort, selection sort, and merge sort

Please perform the following two types of run time analysis and write a report. 

1) Empirical analysis

Please develop a test framework to run the implementations of these three algorithms for various input sizes (N), for example, 100,200,300,..., 10000 and measure running time T(N). In details, for example of input size k = 200, we would randomly generate k numbers, run these sort algorithms on the same random set of size k. We repeat the procedure for input size k for ten times, average the run time for each sort algorithm with input size k.

Plot executable running time T (N) vs. input size N.

For best case or worst case, we generate random set, then sort them by using any standard sort algorithm, use the ordered set as input to rerun the sort algorithms for comparison.

You can use the codes or adapt the codes that we uploaded in Canvas: InsertionSort.java, SelectionSort.java, MergeSort.java, TestSort.java

2) Asymptotic analysis (theoretical analysis)

List the order of growth function for each sort algorithm and specify the growth function in worst case, best case, and average case. It is okay to list them in a table. Also also briefly explain the growth function for each algorithm under each case. If no different among each case for a sort algorithm, please briefly explain it.


Download Link: https://assignmentchef.com/product/solved-cs342-project-1-n-child-processes
<br>
Develop a program that will create  N child processes, besides the main process, to process N input files to find out the k largest integers in those files. N input files will be processed concurrently by N processes. Each input file can contain a very large number of positive integers. The result wil be written to an output file in sorted order, from largest to smallest. k can be a number between 1 and 1000. N can be a number between 1 and 5.  Input and output files will be ascii  text files. The program will be invoked as followes:




findtopk  &lt;k&gt; &lt;N&gt; &lt;infile1&gt; …&lt;infileN&gt; &lt;outfile&gt;




Each child process will read and process one input file and write its result to an intermediate file. When all child processes finish, the main process can read and process those intermediate files.




You could read and write files using fscanf and fprintf, but in this project you will use <strong>low-level I/O</strong> routines, read() and write(), so that you can practice low level I/O. You will open a file using open() function and close the file using close() function. You can read an input file one character at a time (or  few characters). An input file will contain integers seperated by whitespace characters (space, tab, newline). The output file will contain one integer per line. You program will delete the intermediate files when it terminates.




<strong>Part 2</strong>. Do the same project this time using POSIX message queues to pass information from child process to the parent process. No intermediate files will be used. The name of the program will be findtopk_mqueue in this case.




<strong>Part 3.</strong> Do the same project using POSIX threads. For each input file a seperate thread will be created. The name of the program will be findtopk_thread in this case. Thread global variables will be used to pass information from a thread to another thread. No need to use message queues or intermediate files.




<strong>Part 4.</strong> <strong>Experimentation</strong>. Measure the running time of your programs for various k, N, and filesizes (number of integers in a file). Report your results (in tables or plots).Try to draw some conclusions.  Fix k and number of integers in a file. For example, k can be 1000, and number of integers in a file can be 1000000. Measure the running time of your programs for N = 1, 2, and 3. Report your results. Try to draw conclusions.  Write a report at the end of experiments.
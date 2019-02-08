### CI346 Sem2 Lab Session 0

1. Read [Thread javadoc](https://docs.oracle.com/javase/8/docs/api/java/lang/Thread.html) to
gain a general understanding of the class.

2. What is a daemon thread?

3. Referring back to javadoc, find a way to identify the name of the current thread.
Guess the name of the thread that runs first.
Write a small program to print the name of thread that runs first.
Does it have the name you expected?

4. Spawn (create) a new thread in the program from (3) and print the names of both running threads.
You might have to use `Thread.sleep()` on the first thread to be able to see both print statements.

5. Consider [this application](https://github.com/AlmasB/FXTutorials/blob/master/src/com/almasb/dl/DownloaderApp.java).
Can you identify what it is doing?
Find the code that creates a new thread.
Consider why we need more than 1 thread for this type of application.

6. Using the application from (5) as a basis, build a command line tool that can download multiple
files at the same time.
The tool should take URL links from the command line (OK) or an external file (better) as arguments
and download all files at those URLs to current directory.
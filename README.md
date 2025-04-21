Prime number count parallelism exercise

- This code counts the number of primes in an array without parallelism
- Your goal is to add parallelism with OpenMP!
- The project should be configured properly, but you can add OpenMP to 
  Visual Studio project by going to Project Properties-C/C++-Language.
  Set the Open MP Support option to "Yes"


  Student: Alex Belote

  I implemented two functions, so that the code would run parallel proccessing. 
- The programs now run at around 3 times thr speed, by using 8 threads. The reduction clause made the implementation simple and fast. 

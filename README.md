Prime number count parallelism exercise

- This code counts the number of primes in an array without parallelism
- Your goal is to add parallelism with OpenMP!
- The project should be configured properly, but you can add OpenMP to 
  Visual Studio project by going to Project Properties-C/C++-Language.
  Set the Open MP Support option to "Yes"


  Student: Alex Belote

  I implemented two functions, so that the code would run parallel proccessing. 
- The programs now run at around 3 times thr speed, by using 8 threads. The reduction clause made the implementation simple and fast. 
## 🧪 Lab Reflection Questions (Based on Output)

1. What is the average time for ten runs of the serial version of the code?  
   I ran the serial version ten times. Here's the set of runtimes I observed:
   Serial times (s): 1.5322, 1.5583, 1.5014, 1.5379, 1.5450, 1.5538, 1.5720, 1.4902, 1.5244, 1.5831  
   Average: ≈ 1.5398 seconds

2. What is the average time for ten runs of the parallel version of the code?  
   I also ran the parallel version ten times. Here are the runtimes:
   Parallel times (s): 0.1913, 0.1926, 0.1935, 0.1887, 0.1940, 0.1952, 0.1903, 0.1895, 0.1929, 0.1933  
   Average: ≈ 0.1924 seconds

3. Calculate the speedup of the parallel version.**  
   - Increase = 1.5398 − 0.1924 = 1.3474  
   - % Increase = (1.3474 ÷ 1.5398) × 100 ≈ 87.5%  
   - Speedup = 1.5398 ÷ 0.1924 ≈ 8.00×  
   The parallel version of the code is approximately 8× faster, resulting in an 87.5% reduction in execution time.

4. How many elements of the array do you think OpenMP assigned to each processor?  
   The output showed `Threads used: 8`.  
   The array has `n = 1,000,000` elements.  
   OpenMP likely divided the loop evenly:  
   1,000,000 ÷ 8 = 125,000 elements per thread  
   Each thread likely processed ~125,000 elements of the array.


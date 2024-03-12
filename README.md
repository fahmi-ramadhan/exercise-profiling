Before optimization:
![all-student](https://i.imgur.com/iP5N5Zn.png)
![all-student-name](https://i.imgur.com/dPxq9Tg.png)
![all-student-name-jtl](https://i.imgur.com/pMEjHHn.png)
![highest-gpa](https://i.imgur.com/oeaqwbI.png)
![highest-gpa-jtl](https://i.imgur.com/qVz9gVq.png)
After optimization:
![all-student-optimized](https://i.imgur.com/jaRRUgR.png)
![all-student-name-optimized](https://i.imgur.com/Lu3whDz.png)
![highest-gpa-optimized](https://i.imgur.com/kyhQjoo.png)

After profiling and performance optimization, the results of jmeter performance
test really improved. As shown in the above images, the sample time for
all-student request decreased from around 152000 ms to around 8600 ms, the sample
time for all-student-name request decreased from around 3000 ms to around 400 ms,
and the sample for highest-gpa request decreased from around 150 ms to around 10 ms.
In conclusion, the performance optimization efforts have yielded significant
improvements in the response times of the application, as evidenced by the
results of the JMeter performance test.

### Reflection

#### 1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?

The approach of performance testing with JMeter and profiling with IntelliJ Profiler
are different in terms of their goals and the methods they use to achieve those goals.
JMeter is a tool for performance testing, which is used to measure the performance of
an application under various load conditions. It simulates multiple users accessing the
application and measures the response times and other performance metrics. The goal of
JMeter is to identify performance bottlenecks and areas for improvement in the application.
On the other hand, IntelliJ Profiler is a tool for profiling an application, which is used
to analyze the runtime behavior of the application and identify performance hotspots and
memory leaks. The goal of profiling is to understand the performance characteristics of
the application and identify areas for optimization.

#### 2. How does the profiling process help you in identifying and understanding the weak points in your application?

The profiling process helps in identifying and understanding the weak points in the
application by providing detailed information about the runtime behavior of the
application, including CPU usage, memory usage, and method call statistics. For example,
after doing the profiling, I can see which methods are taking the most time to execute.
In this tutorial, I found that the `getAllStudentWithCourses` method in the `StudentService`
class was taking a significant amount of time to execute.

#### 3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?

Yes, I think IntelliJ Profiler is effective in assisting me to analyze and identify
bottlenecks in my application code. As I said earlier, it provides detailed information about the runtime
behavior of the application, including CPU usage, memory usage, and method call statistics.
This information is very helpful in identifying performance hotspots and areas for
optimization.

#### 4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?

The main challenges I faced when conducting performance testing and profiling were
understanding how to use the tools effectively and interpreting the results. To overcome
these challenges, I spent time searching for tutorials on how to use JMeter and
IntelliJ Profiler and experimenting with the tools.

#### 5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?

As I mentioned many times earlier, The main benefits I gained from using IntelliJ Profiler for profiling my application code
were the ability to identify performance hotspots and the ability to
understand the runtime behavior of the application.

#### 6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?

When the results from profiling with IntelliJ Profiler are not entirely consistent with
findings from performance testing using JMeter, I would try to understand the reasons for
the inconsistencies. For example, I would look at the specific metrics that are being
measured by each tool and try to understand how they might be different. I would also
consider the different conditions under which the tests were conducted and how they might
affect the results. In the end, I would use my best judgment to determine the most
appropriate course of action based on the available information.

#### 7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?

The strategies I implemented in optimizing application code after analyzing results from
performance testing and profiling are reducing the number of database queries and optimizing
the algorithms used in the application. For example, in `getAllStudentWithCourses` method,
I change the query to get all students with their courses in one query instead of looping
through the students and getting their courses one by one. I also change primitive string
concatenation to `StringBuilder` to optimize the algorithm.

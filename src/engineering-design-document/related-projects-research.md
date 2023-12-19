# Related projects research

## [progschj/ThreadPool](https://github.com/progschj/ThreadPool)

This is implemented a single-header C++11 library that uses an std::vector of std::thread internally and provides an API which allows users to enqueue lambdas as threads onto the thread pool. The enqueue function returns an std::future which holds the result of the function.

## [alugowski/task-thread-pool](https://github.com/alugowski/task-thread-pool)

This is another single-header C++11 library. It features a strong suite of stress tests and benchmarks which confirm good performance. By default, if the user doesn’t specify a number of threads, the thread pool is initialised with the same number of threads as there are physical cores. It features an enqueue similar to progschj/threadpool, but it also has a function to submit tasks to the thread pool in detached mode which means no result is returned. It also provides a function to facilitate waiting until all tasks in the thread pool have finished. Tasks submitted can have arguments given to them and the thread pool can be resized after creation. The entire thread pool can also be paused and unpaused. This also makes good use of Google benchmarks.

## [bshoshany/thread-pool](https://github.com/bshoshany/thread-pool)

This is C++17 and has great documentation.

## [DeveloperPaul123/thread-pool](https://github.com/DeveloperPaul123/thread-pool)

This is C++20.

## [ConorWilliams/Threadpool](https://github.com/ConorWilliams/Threadpool)

This is C++20 and uses a "fast, generalised implementation of the Chase-Lev lock-free work-stealing deque for C++17".

# Requirements specification

## Functional Requirements

### Feature: Managed Thread

A _managed thread_ is a thread that can be given a workload and have its execution controlled ('managed').

| Requirement     | Description                                                                                                                         | Priority     |
|:---------------:|:------------------------------------------------------------------------------------------------------------------------------------|:------------:|
| F1.1            | The library must have the ability to create a managed thread.                                                                       | MUST         |
| F1.2            | A managed thread must have the ability to be given a workload to execute.                                                           | MUST         |
| F1.3            | A managed thread must have the ability be held in an idle state.                                                                    | MUST         |
| F1.4            | A managed thread must have the ability to be 'started', i.e. moved from an idle state to a state where it's executing its workload. | MUST         |
| F1.5            | A managed thread could have the ability to be ended gracefully mid-execution.                                                       | COULD        |

### Feature: Thread Pool

A _thread pool_ is a group of pre-instantiated, idle threads which stand ready to be given work. This prevents having to incur the overhead of creating a thread a large number of times.

From Java documentation:

> Using worker threads minimizes the overhead due to thread creation. Thread objects use a significant amount of memory, and in a large-scale application, allocating and deallocating many thread objects creates a significant memory management overhead.

| Requirement     | Description                                                                                                                     | Priority     |
|:---------------:|:--------------------------------------------------------------------------------------------------------------------------------|:------------:|
| F2.1            | The library must allow users to create thread pools.                                                                            | MUST         |
| F2.2            | The library must allow users to submit workloads to a thread pool.                                                              | MUST         |
| F2.3            | During creation, a thread pool should have a configurable size, i.e. the number of threads kept in reserve for use by the pool. | SHOULD       |
| F2.4            | After creation, a thread pool could have the ability to change size.                                                            | COULD        |
| F2.5            | Thread pools could have an ability to dynamically change size themselves to a more optimal thread pool size.                    | COULD        |

## Non-Functional Requirements

| Requirement     | Description                                                                                                                                                             | Priority     |
|:---------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------:|
| NF1             | The libary must have open-source code so that other engineers can validate its correctness and propose modifications/improvements.                                      | MUST         |
| NF2             | The library must have high-quality technical documentation which is primarily information-oriented, providing theoretical knowledge for those working with the library. | MUST         |
| NF3             | The library must have support for at least C++14 users.                                                                                                                 | MUST         |
| NF4             | The library should have high-quality how-to guides which are primarily problem-oriented, providing practical knowledge for those working with the library.              | SHOULD       |
| NF5             | The library should have a high-quality tutorial which is primarily learning-oriented, providing practical knowledge for those studying the library.                     | SHOULD       |
| NF6             | The library could have an explanation which is primarily understanding-oriented, providing theoretical knowledge for those studying the library.                        | COULD        |
| NF7             | The library could have support for at least C++11 users.                                                                                                                | COULD        |
| NF8             | The library won’t have support for C++98 users.                                                                                                                         | WON'T        |

# Minervan Task Scheduler

A Python task scheduler that uses a max-heap priority queue to organize a day of tasks based on importance, urgency, duration, dependencies, and fixed-time constraints.

This project applies data structures and algorithms to a realistic scheduling problem: planning a day in the life of a Minerva student while balancing academic work, city exploration, meals, and fixed class times.

## Overview

The scheduler models daily tasks as objects with attributes such as duration, dependencies, importance level, deadlines, fixed start times, and task type. It then prioritizes available tasks using a custom priority function and a max-heap implementation.

The project includes both the Python implementation and an analysis of the scheduler’s feasibility, runtime behavior, limitations, and possible improvements.

## Features

* Custom `Task` class
* Custom `MaxHeapq` priority queue
* Task dependency handling
* Fixed-time task support
* Priority-based scheduling
* Runtime complexity analysis
* Experimental performance testing
* Real-world critique of scheduler limitations

## Priority Formula

The scheduler calculates task priority using:

```text
priority = importance_score + urgency_score - duration_penalty - dependency_penalty
```

Tasks with higher priority values are scheduled earlier when their dependencies are complete and they are available to run.

## Technologies Used

* Python
* Jupyter Notebook
* matplotlib
* numpy
* random
* time

## Project Structure

```text
minervan-task-scheduler/
├── README.md
├── minervan_task_scheduler.ipynb
├── task_scheduler_analysis_report.pdf
└── requirements.txt
```

## How to Run

Open the notebook:

```bash
jupyter notebook minervan_task_scheduler.ipynb
```

Then run the cells from top to bottom.

## Key Concepts Demonstrated

* Heaps and priority queues
* Object-oriented programming
* Scheduling algorithms
* Dependency management
* Runtime analysis
* Algorithmic critique
* Experimental performance evaluation

## Limitations

The scheduler is useful for organizing tasks by priority, but it has limitations. It does not fully adapt to real-world delays, spontaneous changes, or energy level fluctuations throughout the day. The analysis report discusses these failure modes and proposes possible improvements, such as deadline-aware scheduling and dependency graphs.

## Future Improvements

* Convert the notebook into separate Python files
* Add a command-line interface
* Add dynamic rescheduling when delays occur
* Improve deadline handling
* Use a dependency graph for faster readiness checks
* Add calendar integration
* Add visual schedule output

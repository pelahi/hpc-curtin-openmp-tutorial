---
title: "Introduction to OpenMP"
teaching: 4
exercises: 5
questions:
objectives:
- Experiment with OpenMP directives
- Discuss when you would benefit from using OpenMP
keypoints:
- OpenMP allows code to use parallelism via threads on shared memory architecture
---


### OpenMP

As we have learned in our lesson, OpenMP provides directives, runtime functions
and environment variables to enable parallelism via threads. The directives provide
a means of splitting work between threads and synchronising threads.

### Testing OpenMP

The Develop-with-OpenMP repository contains several examples highlighting OpenMP
directives. We will start with the Workbench/Preliminary example (there is a c and
and fortran version of this very simple code). This code simply prints some info
to standard out.

```c
void main (){
	int thread_id = 0;
	{
		printf("Hello World from %d \n", thread_id);
	}
}
```

We suggest you try implementing

* #pragma omp parallel
* synchronisation with **barrier**, **atomic** **critical**

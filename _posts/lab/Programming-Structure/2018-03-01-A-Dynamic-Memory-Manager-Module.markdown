---
index: 0 # labs number
num: 4 # lab number
title: A Dynamic Memory Manager Module
permalink:
  /lab/Programming-Structure/A-Dynamic-Memory-Manager-Module
  # link
category: lab # project or lab
---

#### **Purpose**

---

The purpose of this assignment is to help you understand how dynamic memory management works in C. It also will give you more opportunity to use the GNU/Unix programming tools, especially bash, emacs, gcc209, gdb, and make.

<br>

#### **Task**

---

You are given the interface of a HeapMgr (heap manager) module in a file named heapmgr.h. It declares two functions:

```
void *HeapMgr_malloc(size_t uiSize);
void HeapMgr_free(void *pv);
```

You also are given three implementations of the HeapMgr module:

- heapmgrgnu.c is an implementation that simply calls the GNU malloc and free functions provided with our lab machine development environment.

- heapmgrkr.c is the Kernighan and Ritchie implementation, with small modifications for the sake of simplicity.

- heapmgrbase.c is an implementation that you will find useful as a baseline for your implementations.

Your task is to create two additional implementations of
the HeapMgr module. Your first implementation, heapmgr1.c, should
enhance heapmgrbase.c so it is reasonably efficient. To do that it should
use a single doubly-linked list and chunks that contains headers and
footers. Unlike the K&R implementation, the baseline code uses a non-circular list, and your
code should implement a non-circular, doubly-linked list.

If designed properly, heapmgr1.c will be reasonably efficient in most cases.
However, heapmgr1.c is subject to poor worst-case behavior. Your second
implementation, heapmgr2.c, should enhance heapmgr1.c so the worst-case
behavior is not poor. To do that it should use multiple doubly-linked
lists, alias bins (as described above, in lectures, and in precepts).

Your HeapMgr implementations should not call the
standard malloc, free, calloc, or realloc functions.

Your HeapMgr implementations should thoroughly validate function
parameters by calling the standard assert macro.

Your HeapMgr implementations should check invariants by:

- Defining a thorough CheckHeapValidity function, and

- Calling assert(CheckHeapValidity()) at the leading and trailing edges
  of the HeapMgr_malloc and HeapMgr_free functions.

<br>

#### **Code**

---

[Github](https://github.com/Heejinee3/Programming-Structure/tree/master/A%20Dynamic%20Memory%20Manager%20Module){:target="\_blank"}

<br>

#### **Glossary**

---

[Heap](https://velog.io/@chunjakim/Heap){:target="\_blank"}

.. _kernel_apis:

Kernel APIs
###########

This section contains APIs for the kernel's core services,
as described in the :ref:`kernel`.

.. important::
    Unless otherwise noted these APIs can be used by threads, but not by ISRs.

.. contents::
   :depth: 1
   :local:
   :backlinks: top

Threads
*******

A thread is an independently scheduled series of instructions that implements
a portion of an application's processing. Threads are used to perform processing
that is too lengthy or too complex to be performed by an ISR.
(See :ref:`threads_v2`.)

.. doxygengroup:: thread_apis
   :project: Zephyr
   :content-only:

Workqueues
**********

A workqueue processes a series of work items by executing the associated
functions in a dedicated thread. Workqueues are typically used by an ISR
or high-priority thread to offload non-urgent processing.
(See :ref:`workqueues_v2`.)

.. doxygengroup:: workqueue_apis
   :project: Zephyr
   :content-only:

Clocks
******

Kernel clocks enable threads and ISRs to measure the passage of time
with either normal and high precision.
(See :ref:`clocks_v2`.)

.. doxygengroup:: clock_apis
   :project: Zephyr
   :content-only:

Timers
******

Timers enable threads to measure the passage of time, and to optionally execute
an action when the timer expires.
(See :ref:`timers_v2`.)

.. doxygengroup:: timer_apis
   :project: Zephyr
   :content-only:

Memory Slabs
************

Memory slabs enable the dynamic allocation and release of fixed-size
memory blocks.
(See :ref:`memory_slabs_v2`.)

.. doxygengroup:: mem_slab_apis
   :project: Zephyr
   :content-only:

Memory Pools
************

Memory pools enable the dynamic allocation and release of variable-size
memory blocks.
(See :ref:`memory_pools_v2`.)

.. doxygengroup:: mem_pool_apis
   :project: Zephyr
   :content-only:

Heap Memory Pool
****************

The heap memory pools enable the dynamic allocation and release of memory
in a :cpp:func:`malloc()`-like manner.
(See :ref:`heap_v2`.)

.. doxygengroup:: heap_apis
   :project: Zephyr
   :content-only:

Semaphores
**********

Semaphores provide traditional counting semaphore capabilities.
(See :ref:`semaphores_v2`.)

.. doxygengroup:: semaphore_apis
   :project: Zephyr
   :content-only:

Mutexes
*******

Mutexes provide traditional reentrant mutex capabilities
with basic priority inheritance.
(See :ref:`mutexes_v2`.)

.. doxygengroup:: mutex_apis
   :project: Zephyr
   :content-only:

Alerts
******

Alerts enable an application to perform asynchronous signalling,
somewhat akin to Unix-style signals.
(See :ref:`alerts_v2`.)

.. doxygengroup:: alert_apis
   :project: Zephyr
   :content-only:

Fifos
*****

Fifos provide traditional first in, first out (FIFO) queuing of data items
of any size.
(See :ref:`fifos_v2`.)

.. doxygengroup:: fifo_apis
   :project: Zephyr
   :content-only:

Lifos
*****

Lifos provide traditional last in, first out (LIFO) queuing of data items
of any size.
(See :ref:`lifos_v2`.)

.. doxygengroup:: lifo_apis
   :project: Zephyr
   :content-only:

Stacks
******

Stacks provide traditional last in, first out (LIFO) queuing of 32-bit
data items.
(See :ref:`stacks_v2`.)

.. doxygengroup:: stack_apis
   :project: Zephyr
   :content-only:

Message Queues
**************

Message queues provide a simple message queuing mechanism
for fixed-size data items.
(See :ref:`message_queues_v2`.)

.. doxygengroup:: msgq_apis
   :project: Zephyr
   :content-only:

Mailboxes
*********

Mailboxes provide an enhanced message queuing mechanism
for variable-size messages.
(See :ref:`mailboxes_v2`.)

.. doxygengroup:: mailbox_apis
   :project: Zephyr
   :content-only:

Pipes
*****

Pipes provide a traditional anonymous pipe mechanism for sending
variable-size chunks of data, in whole or in part.
(See :ref:`pipes_v2`.)

.. doxygengroup:: pipe_apis
   :project: Zephyr
   :content-only:

Interrupt Service Routines (ISRs)
*********************************

An interrupt service routine is a series of instructions that is
executed asynchronously in response to a hardware or software interrupt.
(See :ref:`interrupts_v2`.)

.. doxygengroup:: isr_apis
   :project: Zephyr
   :content-only:

Atomic Services
***************

The atomic services enable multiple threads and ISRs to read and modify
32-bit variables in an uninterruptible manner.
(See :ref:`atomic_v2`.)

.. important::
    All atomic services APIs can be used by both threads and ISRs.

.. doxygengroup:: atomic_apis
   :project: Zephyr
   :content-only:

Floating Point Services
***********************

The floating point services enable threads to use a board's floating point
registers.
(See :ref:`float_v2`.)

.. doxygengroup:: float_apis
   :project: Zephyr
   :content-only:

Ring Buffers
************

Ring buffers enable simple first in, first out (FIFO) queuing
of variable-size data items.
(See :ref:`ring_buffers_v2`.)

.. doxygengroup:: ring_buffer_apis
   :project: Zephyr
   :content-only:


Legacy APIs
***********

These APIs will be deprecated in an upcoming release so we recommend you avoid
using them in your applications.

.. doxygengroup:: legacy_apis
   :project: Zephyr
   :content-only:

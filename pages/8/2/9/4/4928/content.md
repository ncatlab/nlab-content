[[!redirects Models for concurrency]]
# Contents
* automatic table of contents goes here
{:toc}




(The ideas section here is partially adapted from papers of [[Eric Goubault]].  In particular the paper in HHA, see reference list. He was one of the first to propose some form of directed homotopy as a model for aspects of concurrency.) This entry tries to list and summarise various models for concurrency and to examine some of them for (potential) interaction with other entries in the Lab.

##Idea##

Concurrency theory in Theoretical Computer Science deals with systems in which several computational activities ( *processes* ) can be performed at the same time, in an asynchronous way.  Concurrent systems were introduced in order to have increased computational power and speed or so that some concurrent transactions can be handled more efficiently (and sometimes handled at all). Some of the models discussed here have been, perhaps, superceded as the technology has moved on, and the _flavour of the month_ changes, but they still provide useful mathematical models with potential for use elsewhere, so are certainly worth examining.

One of the main problems about concurrency is to have processes cooperating successfully for a common goal.  Cooperation seems to imply some form of synchronisation and information passing.   This can be done through *message passing* models, for instance. In that class of models, processes have their own local memory, which cannot be accessed by other processes.  The way to communicate values to other processes is by explicitly sending values to these other processes. One of the possible ways of doing this is via a *Rendezvous model* in which the action of sending results in the sender being blocked until the receiver actually receives the message and then, symmetrically the action of receiving blocks the receiver until the message is actually received. This method gives a partial synchronisation of the sender and receiver for the purpose of the passing of the message.

+--{: .query}
The source I am using to help me understand this does not quite make sense here and other sources that I have looked at, have not helped that much, so can someone de-blurr the meaning for me here.  [[Tim Porter|Tim]]
=--

There are variants to this,  which include _non-blocking send but blocking receive_ , _non-blocking send and receive_ (*asynchronous message passing*), _broadcast to groups of processes_ , instead of ''point to point'' communication, etc.

####Shared memory models
These make up another class of concurrent architectures.  Here process have a local memory where they can perform local computations, but also have a common memory space which is accessible to all.  Communication between processes is essentially asynchronous and is realised by reading and writing values in this common space. Here the problem occurs that several processes may want to write values to the same part of the memory at the same time.  To avoid the problems that this implies it is necessary to 'protect' the access to shared variables by some mechanism. A classical one is the ''semaphore'' as introduced by Dijkstra in 1968.

The challenge is to find adequate mathematical models so as better to understand the behaviour of concurrent systems.


(More needs to be put here and the above is not that great.  Not sure how to rewrite it and what to add, though!)

##Models

* [[transition systems]], labelled transition systems and [[higher dimensional transition systems]];

* [[trace monoid|trace monoids]] and [[Mazurkiewicz trace]] theory;

* [[asynchronous automata]];

* [[Petri nets]];

* [[asynchronous automata]];

* [actor models](http://en.wikipedia.org/wiki/Actor_model);

* [[higher dimensional automata]].

##References##

 *  [[Eric Goubault]], [[Some geometric perspectives in concurrency theory]], 

*   [[Eric Goubault]] and [[Samuel Mimram]], [Formal Relationships Between Geometrical and Classical Models for Concurrency](http://fr.arxiv.org/abs/1004.2818)
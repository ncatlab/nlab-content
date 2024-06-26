
#Contents#
* table of contents
{:toc}




## Idea 

> (This Idea-section is partially adapted from papers of [[Eric Goubault]], in particular [Goubault 2003](#Goubault03). He was one of the first to propose some form of [[directed homotopy theory|directed homotopy]] as a model for aspects of concurrency.) This entry tries to list and summarise various models for concurrency and to examine some of them for (potential) interaction with other entries in the Lab, especially ones related to directed topology, and to causal sets ([[causets]]). (This comparison will initially not be deep, as we will first put down a lot of definitions in the linked pages, with a view to possible interactions later on.)


Concurrency theory in Theoretical Computer Science deals with systems in which several computational activities (*processes*) can be performed at the same time, in an asynchronous way.  Concurrent systems were introduced in order to have increased computational power and speed or so that some concurrent transactions can be handled more efficiently (and sometimes handled at all). Some of the models discussed here have been, perhaps, superseded as the technology has moved on, and the _flavour of the month_ changes, but they still provide useful mathematical models with potential for use elsewhere, so are certainly worth examining.

One of the main problems about concurrency is to have processes cooperating successfully for a common goal.  Cooperation seems to imply some form of synchronisation and information passing.   This can be done through *message passing* models, for instance. In that class of models, processes have their own local memory, which cannot be accessed by other processes.  The way to communicate values to other processes is by explicitly sending values to these other processes. One of the possible ways of doing this is via a *Rendezvous model* in which the action of sending results in the sender being blocked until the receiver actually receives the message and then, symmetrically the action of receiving blocks the receiver until the message is actually received. This method gives a partial synchronisation of the sender and receiver for the purpose of the passing of the message.

+--{: .query}
The source I am using to help me understand this does not quite make sense here and other sources that I have looked at, have not helped that much, so can someone de-blurr the meaning for me here.  [[Tim Porter|Tim]]
=--

There are variants to this,  which include _non-blocking send but blocking receive_ , _non-blocking send and receive_ (*asynchronous message passing*), _broadcast to groups of processes_ , instead of "point to point" communication, etc.

+--{: .query}
[[Adam]]: "Non-blocking send with blocking receive" is the rule required by Kahn process networks; this ensures that the resulting processes form a [domain](http://en.wikipedia.org/wiki/Domain_theory).  From a semantics standpoint I'm not sure that broadcast to $n$ recipients is really any different from just sending $n$ messages, one to each recipient.
=--

### Shared memory models

These make up another class of concurrent architectures.  Here processes have a local memory where they can perform local computations, but also have a common memory space which is accessible to all.  Communication between processes is essentially asynchronous and is realised by reading and writing values in this common space. Here the problem occurs that several processes may want to write values to the same part of the memory at the same time.  To avoid the problems that this implies it is necessary to 'protect' the access to shared variables by some mechanism. A classical one is the "semaphore" as introduced by Dijkstra in 1968. One of the usual pictures of a 'toy' situation used here is the [[progress graph|Swiss flag progress graph]], where two users attempt to change records in a database.  There is a shared resource and hence a problem of conflict, even of deadlock.

The challenge is to find adequate mathematical models so as better to understand the behaviour of such concurrent systems.

(More needs to be put here and the above is not that great.  Not sure how to rewrite it and what to add, though!)

+-- {: .query}
[[Adam]]: "Shared memory" is just a friendly way of presenting message-passing systems to a programmer -- at the end of the day, everything is message passing underneath if you dig down far enough.  If you want to __really__ dig, consider that digital circuits are point-to-point communication mechanisms, and physicists are suspicious of any "[action at a distance](http://en.wikipedia.org/wiki/Nonlocality)" -- which is what you would need in order to implement shared memory without some sort of message passing mechanism somewhere underneath.  Ours is a message-passing world; shared state is just an illusion used to make centralized-and-serial programmers feel more comfortable in a distributed-and-parallel world.  One could argue that the "mathematical models" called for are nothing more than simple translations into message-passing operations, which are the primary object of study.  (Note: I use message-passing here in the broadest sense, encompassing Petri Nets, CSP, trace structures, Kahn process networks, etc -- anything without shared state)

[[Tim Porter]]:  @Adam. Why not develop this a bit on some off shoot pages?  Also why not join n-forum and then it will be easier to discuss the points you make without discussions filling up the n-Lab pages. 

I hope to get a bit more CS and TCS into the n-lab as there seem to be possibilities for interesting interactions between some topics there and the 'n-POV' as well as connections with quantum computing. 

What do you think? As I suggested please do get onto the n-forum if you have the time.   
=--


## Models

### Traditional Models 

* [[transition systems]], and [[transition systems|labelled transition systems]];

* [[trace monoid|trace monoids]] and [[Mazurkiewicz trace]] theory;

* [[asynchronous automata]];

* [[Petri nets]];

*  [[event structures]];

* [actor models](http://en.wikipedia.org/wiki/Actor_model);

### Geometrical models

* [[progress graph]];

* [[higher dimensional automaton]];

* [[higher dimensional transition system]];

* [[cubical set]].

## Related entries

* [[transition system]]

* [[bisimulation]]

## References 


* [[Mogens Nielsen]], [[Glynn Winskel]]: *Models for concurrency*, in: *Handbook of Logic in Computer Science* vol 4, Oxford Univ. Press (1994) 1-148 &lbrack;[pdf](https://www.cl.cam.ac.uk/~gw104/winskel-nielsen-models-for-concurrency.pdf), [[WinskelNielsen-Concurrency.pdf:file]], [doi:10.5555/218623.218630](https://dl.acm.org/doi/10.5555/218623.218630), [ISBN:9780198537809](https://global.oup.com/academic/product/handbook-of-logic-in-computer-science-9780198537809?lang=en&cc=at)&rbrack;


* [[Lisbeth Fajstrup]], [[Eric Goubault]], [[Emmanuel Haucourt]], [[Samuel Mimram]], [[Martin Raussen]], [[Directed Algebraic Topology and Concurrency]],Springer International Publishing 2016 (xi+167 pages)

* {#Goubault03} [[Eric Goubault]], *[[Some geometric perspectives in concurrency theory]]*, Homology Homotopy Appl. **5** 2 (2003), 95-136 &lbrack;[eudml:50689](https://eudml.org/doc/50689)&rbrack; 

* [[Eric Goubault]] and [[Samuel Mimram]], [Formal Relationships Between Geometrical and Classical Models for Concurrency](http://fr.arxiv.org/abs/1004.2818), Arxiv 1004.2818.


category: computer science

[[!redirects Models for concurrency]]


# Contents
* automatic table of contents goes here
{:toc}

##Petri nets##
###Introduction###
Petri nets are a well known model of parallel computation, generalising [[transition systems]] by using a built in notion of resource.  Their use is widespread in modelling manufacturing systems, optimising control systems and in resource critical aspects of operational research, as well as being a useful model of computation.  Because of this they exist in many variants : colored, algebraic, probabilistic, timed, \ldots, and hence there are many forms of the basic definition, each thought best of that particular application.

The initial use, here, is for their links with [[transition systems]], [[event structures]], [[asynchronous automata]] etc., leading on to their comparison with [[higher dimensional automata]] and [[higher dimensional transition systems]], so the first definition we will use is that given by Winskel and Nielsen (see references below), but first we will attempt to give some idea of what a Petri net is and what is does.

##Idea##
The idea of a simple Petri net is based on a simple manufacturing shop.  You have various 'transitions' or manufacturing 'events' that form part of the various process occurring in the 'shop'. These typically take parts (of the final object), do something to them, such as combining two or more different parts to make a more complicated one, (for instance, putting the wheels on a car).

Parts, represented by 'tokens' are stored in 'places' and the assembly process are known, as above, as 'events' or 'transitions' (depending on the source being used for the theory).  The relationships are typically represented graphically.  For instance:

(PICTURE)

represents a system with three places (labelled $A$, $B$, and $C$) and one event/ transition (labelled $e$).  Shown is a situation represented by an initial 'marking' where there are two tokens in $A$, one in $B$, and none in $C$.




##References##

* [[G. Winskel]] and M. Nielsen, Models for concurrency. vol. 3, Handbook of Logic in Computer Science, pages 100 - 200, Oxford Univ. Press, 1994. (see also [online technical report](http://www.daimi.au.dk/PB/463/PB-463.pdf)).


# Contents
* table of contents
{:toc}

##Idea##
Temporal logics, as their name suggests, are logics that involve time.  They form a very large and important class of modal logics, but here we will, to start with, only look at some simple cases. Temporal logics are very closely related to [[tense logics]].

##Basic temporal language##
First the basic temporal language is built with two binary model operators, which instead of being denoted 'box' and 'diamond', are written $F$ and $P$.  The intended interpretation of thes are:

* $F\phi$ is _$\phi$ will be true at some **future** time_;

* $P\phi$ is _$\phi$ was true at some **past** time.

The reason for the notation $F$ and $P$ should be clear.

* The dual of $F$ is $G$, so $G\phi = \neg F\neg \phi$. This means that we read $G\phi$ as 'at no future time is $\phi$ not true', i.e., $\phi$ is always **going** to be true. ($G$ for 'going'.)

* The dual of $P$ is written $H$, whence $H\phi = \neg P\neg \phi$ and $H\phi$ interprets as '$\phi$ **has** always been true'. ($H$ is for 'has' - which is a bit weak, but that is life!)


+--{: . un_example}
######Examples######
*  If for all $\phi$ we have $P\phi \to GP\phi$, then _whatever has happened will always have happened_, which seems reasonable so this might be a suitable 'general truth' we might want a temporal logic to contain.

*  If we had in our logic that $F\phi \to FF\phi$, then this would means that if $\phi$ is true at some future time, then at some future time it will be true that $\phi$ will be true at some future time, so _between any two instants there must be a third_, and the general truth of this would say something about the 'internal structure' of time as modelled by such a logic. 
=--





## References## 

Generally this entry is based on

* P. Blackburn, M. de Rijke and Y. Vedema, _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001, 

but see also:

*  A Galton, [Temporal Logic, (Stanford Encyclopedia of Philosophy)] (http://plato.stanford.edu/entries/logic-temporal/)

* Patrick Blackburn, _Tense, Temporal Reference and Tense Logic_, Journal of Semantics, 1994,11,
    pages 83--101, [on-line version](http://www.loria.fr/~blackbur/papers/tense.pdf)
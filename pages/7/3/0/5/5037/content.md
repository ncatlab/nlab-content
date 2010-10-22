
# Contents
* table of contents
{:toc}

##Idea##
Temporal logics, as their name suggests, are logics that involve time.  They form a very large and important class of modal logics, but here we will, to start with, only look at some simple cases. Temporal logics are very closely related to [[tense logics]].

##Basic temporal language, (BTL)##
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

This basic temporal language does not yet really constitute a sensible logic that could model important features of 'time'. but we can still look at models so as to see what properties of the models can be identified as corresponding to seemingly feasible formulae in the language.

## Frames and Models for BTL## 
A _frame_ for BTL will be a set, $T$, with two binary relations $R+F$ and $R_P$.  We have $R_F xy$ reads that 'at $x$, $y$ is in the future'  - but, in the ordinary common sense meaning of words, this should mean $R_P yx$ and conversely.  In other words $R_P$ should be the _converse_ or [[opposite relation]] of $R_F$. 

(In general, if $R$ is a binary relation on a set $X$, then its [[opposite relation]] is defined by 

$$(y,x) \in R^{op} \Leftrightarrow (x,y)\in R.)$$

+--{: .un_defn}
######Definition ######
A frame of the form $(T,R,R^{op})$ is called a _bidirectional frame_.
=--
If we have **any** model $\mathfrak{M} = (T,R,V)$ with a valuation, $V$, then we can interpret BTL in terms of it by specifying  the interpretation of $P$ in terms that of $R$.  explicitly we define 

*  $\mathfrak{M}, t\models F\phi$ if and only if $\exists s (R t s \wedge \mathfrak{M}, s\models \phi);$

*  $\mathfrak{M}, t\models P\phi$ if and only if $\exists s (R s t \wedge \mathfrak{M}, s\models \phi)$,

but, of course, this is still a long way from having a logic that looks as if it captures 'time-like' behaviour. We could have models with 'circular time', and 'branching time'.  Both of these correspond to various situations in computational applications so should be kept in mind, both to be able to identify their occurrence and to build them in or to avoid them in the logics.

##(4)##
One condition it would be natural to impose is transitivity of $R_F$, since if $F\phi$ is true at some future time, then clearly, $\phi$ itself must also be true at some future time, i.e., later on still!  This leads one to ask that 

$$(4) \quad\quad    FF\phi \to F\phi$$

should be in our logic,  (and similarly for $P$, but that will hold in the bidirectional models since if $R$ is transitive then so will be $R^{op}$).



## References## 

Generally this entry is based on

* P. Blackburn, M. de Rijke and Y. Vedema, _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001, 

but see also:

*  A Galton, [Temporal Logic, (Stanford Encyclopedia of Philosophy)] (http://plato.stanford.edu/entries/logic-temporal/)

* Patrick Blackburn, _Tense, Temporal Reference and Tense Logic_, Journal of Semantics, 1994,11,
    pages 83--101, [on-line version](http://www.loria.fr/~blackbur/papers/tense.pdf)
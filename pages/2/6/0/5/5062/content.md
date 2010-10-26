#Contents#
* automatic table of contents goes here
{:toc}


##Arrow frames, arrow languages and arrow logics##

These structures are intended to allow one to talk about 'all such objects 
as may be represented in a picture by arrows'(Venema).

+--{: .un_defn}
######Definition######
An **arrow frame** is a [[frame (modal logic)|frame]], $\mathfrak{F} = (W, C, R, I )$ such that $C$ is a ternary relation, (so $C\subseteq 
W \times W \times W$, $R$ is a binary relation, and $I$ a unary one, so $I\subseteq W$. 
=--
###Gloss###
The interpretation intended for these relations is similar to the structure of a [[groupoid]], but from a relational point of view.

*  For $C(a,b,c)$ think $a = b\star c$, 'the' _composite_ of $b$ and $c$, but, of course, $a$ need not be uniquely defined by this;

* For $R(a,b)$, think $b$ is a 'reverse' arrow for $a$;

* For $I(a)$ i.e. $a\in I$, think $a$ is an 'identity arrow'.

This defines a frame by a relational signature.  It does not specify any formulae to be satisfied, nor is there a [[geometric models for modal logics
  |valuation]] around  to give some 'meaning' to the structure.

##References##

A general treatment of these ideas can be found in 

* P. [[Blackburn]], M. de Rijke and Y. [[Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001,

whilst a short introduction is 

*  Y. [[Venema]], [_A crash course in Arrow Logic_](http://staff.science.uva.nl/~yde/papers/arrow.pdf), in in: M Marx, L P&#243;los and M Masuch (editors), Arrow Logic and Multi-Modal Logic,
Studies in Logic, Language and Information, CSLI Publications, Stanford (1996) 3--34.


##Idea

We consider a presentation, $\mathcal{P} = (X : R)$, of a group $G$. We thus have a 
short exact sequence,
$$1\to N \to F \to G \to 1,$$ 

where $F = F(X)$, the free group on the set $X$, $R$ is a 
subset of $F$ and $N = N(R)$ is the normal closure in $F$ of the set $R$.  The group, 
$F$, acts on $N$ by conjugation: ${}^u c = ucu^{-1}$,  $c\in N$, $u \in F$, and the elements of $N$ are words in the conjugates of the elements of $R$:

$$c = {}^{u_1}(r_1^{\varepsilon_1}){}^{u_2}(r_2^{\varepsilon_2})\ldots 
{}^{u_n}(r_n^{\varepsilon_n}),$$
often says such elements are _consequences_ of 
$R$.  Heuristically, an **identity among the relations** of $\mathcal{P}$ is such an element, $c$, which equals 1.  

The problem of what this actually _means_ is analogous to that of working with a relation, since, for example, in the presentation, $( a : a^3)$, of $C_3$, the cyclic group of order 3, if $a$ is thought of as being an element of $C_3$, then $a^3 = 1$! Doesn't that say the presentation is $( a : 1)$?
Why is this then different from the situation with the 'presentation', $( a : a = 1)$?  

To get around that mess, the 
free group on the generators, $F(X)$, was introduced and, of course, in $F(\{a\})$, $a^3$ is not 1. The relation is thus thought of as being a piece of data that is giving the instruction to rewrite that element to 1.

 An analogous free algebraic device, namely [[free crossed module]]s on the presentation can be introduced  to handle the 
identities. 


##Example (Proper powers)

Suppose $r\in R$, but it is a power of some element $s\in F$, i.e., $r = s^m$.
Of course, $ r s = s r$ and 

$${}^s r r^{-1} = 1$$

so ${}^s r. r^{-1}$ is an identity.  In fact, there will be a unique $z\in F$
with $r = z^q$, $q$ maximal with this property.  This $z$ is called the
_root of_ $r$ and if $q > 1$, $r$ is called a _proper power.

##Example (Standard presentation of $S_3$

Here we take up the example from [[Cayley graph]]:

Consider one of the standard presentations of $S_3$, 

$$ (a,b  :  a^3, b^2, (ab)^2).$$ 

Write $ r = a^3$, $s = b^2$, $t = (ab)^2$.  Here the
presentation leads to $F= F(a,b)$, free of rank 2, and  $N(R) \subset F$, so it must be
free as well, by the [[Nielsen-Schreier theorem]].  Its rank will be 7, given by the Schreier index formula or,
geometrically, it will be the fundamental group of the Cayley quiver, also called the  [[Cayley graph]], of the
presentation.  This group is free on generators corresponding to edges outside 
a maximal tree.

The set of normal generators of $N(R)$ has 3 elements; $N(R)$ is free on 7
elements (corresponding to the edges not in the tree), yet it is specified as consisting of products of conjugates of $r$, $s$ 
and $t$, and there are infinitely many of these conjugates.  Clearly there must be some
_slight_ redundancy, so there must be some identities among the relations!  

Note that the Cayley graph is [[planar graph|planar]]. 


A path around the first triangle, $1 \to a \to a^2$, corresponds to the relation $r$; each other
region corresponds to a conjugate of one of $r$, $s$ or $t$.  (It may help in what follows to think of the graph being embedded on a 2-sphere, so 'outer' and 'outside' mean 'round the back face'.) Consider a loop
around a region.  

Pick a path to a start vertex of the loop, a path starting at 1.
For instance the path that leaves 1 and goes along edges labelled $a$, $b$ and then goes
around $a a a$ before returning by $b^{-1} a^{-1}$ gives
$a b r b^{-1} a^{-1}$. Now the path around the outside can be written as 
a product of paths around the inner parts of the graph,
e.g. $(a b a b) b^{-1} a^{-1} b^{-1} (b b) (b^{-1}a^{-1} b^{-1} a^{-1}) \ldots $ and so
on, thus $r$ can be written in a non-trivial way as a product of conjugates
of $r$, $s$ and $t$. (An explicit identity constructed like this is given in the paper by Brown and Huebschmann (see below).)



##References:

* [[R. Brown]] and [[J. Huebschmann]],  _Identities among relations_, in R.Brown and T.L.Thickstun, eds., Low Dimensional Topology, London Math. Soc Lecture Notes, Cambridge University Press, (1982).

* [[M. Kapranov]] and [[M. Saito]], 1999, _Hidden Stasheff polytopes in algebraic K-theory and in the space of Morse functions_, in _Higher homotopy structure in topology and mathematical physics_ (Poughkeepsie, N.Y. 1996), volume 227 of Contemporary Mathematics, 191 – 225, AMS


*  [[J.-L. Loday]], 2000, _Homotopical Syzygies_, in _Une dégustation topologique: Homotopy theory in the Swiss Alps_, volume 265 of Contemporary Mathematics, 99 – 127, AMS.


[[!redirects identities among relations]] 

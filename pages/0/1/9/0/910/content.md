
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



#Content#
* automatic table of contents goes here
{:toc}

## Idea 

A [[topological space]] is _compactly generated_ if (in a certain sense) the continuous images in it of all [[compact Hausdorff space]]s tell you everything about its topology.

Compactly generated spaces form a [[convenient category of topological spaces]].

## Definitions 

A function $f:X\to Y$ between [[topological space]]s is __$k$-continuous__
if for all [[compact topological space|compact]] [[Hausdorff space]]s $C$ and continuous functions $t: C \to X$ the composite $f \circ t:C \to Y$ is continuous.
 
The following conditions on a space $X$ are equivalent:

1. For all spaces $Y$ and all functions $f:X \to Y$, $f$ is
continuous if and only if $f$ is $k$-continuous.
1. There is a set $S$ of compact Hausdorff spaces such that the previous condition holds for all $C \in S$.
1. $X$ is an [[identification space]] of a [[disjoint union]] of compact Hausdorff spaces.
1. A subset $U\subseteq X$ is open if and only if $t^{-1}(U)$ is open for any compact Hausdorff space $C$ and continuous $t:C\to X$.

A space $X$ is a __$k$-space__ if any (hence all) of the above conditions hold.  Some authors also say that a $k$-space is __compactly generated__, while others reserve that term for a $k$-space which is also _[[weak Hausdorff space|weak Hausdorff]]_, meaning that the image of any $t:C\to X$ is closed (when $C$ is compact Hausdorff).

## Cartesian closure 

The category $k\Top$ of topological spaces and $k$-continuous maps is [[cartesian closed category|cartesian closed]]. In fact the exponential map 
$$k\Top(X \times Y, Z) \to kTop(X,k\Top(Y,Z))$$
is a homeomorphism (not just a $k$-homeomorphism). 

+--{: .query}
[[Zoran Škoda]]: I do not understand the remark. I mean if the domain is k-space then by the characterization above continuous is the same as k-continuous. Thus if both domain and codomain are continuous then homeo is the same as k-homeo. I assume that even in noHausdorff case, the test-open topology for $X$ and $Y$ k-spaces gives a k-space and that the cartesian product has the correction for the k-spaces. 

[[Todd Trimble]]: That may be just the point: that the domain is not necessarily a $k$-space. I have to admit that I haven't worked through the details of this exposition, but one thing I tripped over is the fact that we're dealing with _all_ topological spaces $X$, $Y$, not just $k$-spaces. 

[[Mike Shulman]]: But any topological space is isomorphic in $k\Top$ to its $k$-ification, right?  So $k\Top$ might as well be defined to consist of $k$-spaces and continuous maps.
=--

The topology on $k\Top(X,Y)$ that is used here is the test-open
topology, which has the [[subbase]] of sets $M(t,U)$ for a given $t: C
\to X$ and $U$ open in $Y$ of all $k$-continuous functions $f:X \to
Y$ such that $f(t(C))\subseteq U$.

It follows that the category of $k$-spaces and continuous maps is also cartesian closed.  This remains true if we also impose the weak Hausdorff condition.

## Kaonization

Let us consider for the moment only the categories $Haus$ of Hausdorff and $kHaus$ of Hausdorff k-spaces. Then the tautological inclusion $kHaus\subset Haus$ has a right adjoint $k$ sometimes (e.g. by [[M M Postnikov]]) also called **kaonization** and sometimes (e.g. by [[Peter May]]) $k$-ification.  This functor is constructed as follows: we take $k(X)=X$ as a set, but with the topology whose closed sets are those whose intersection with compact subsets of (the original topology on) $X$ is closed (in the original topology on $X$). Then $k(X)$ has all the same closed sets and possibly more, hence all the same open sets and possibly more. In particular, the identity map $id:k(X)\to X$ is continuous.

We can identify the mapping spaces $kHaus(X,Y)=k(Top(X,Y))$, where $Top(X,Y)$ is the standard mapping space in the sense of compact-open topology. Similarly, the categorical product in $kHaus$ is the kaonification of the usual (Tyhonov) product. Then $kHaus$ is [[cartesian closed category|cartesian closed]]. See G. Whitehead's _Elements of homotopy theory_, for more details.  

## Local cartesian closure 

Unfortunately neither of the above categories is [[locally
cartesian closed category|locally
cartesian closed]]. There is still a lot of work on fibred exponential
laws and their applications. One reason for the success and
difficulties is that it is easy to give a topology on the space of
closed subsets of a space $X$ by regarding this as the space of maps
to the [[Sierpinski space]] (the set $\{0,1\}$ of [[truth value]]s in which $\{1\}$
is closed but not open). From this one can get an [[exponential law for
spaces]] over $B$ if $B$ is $T_0$, so that all fibres of spaces over
$B$ are closed in their total space.  Note that weak Hausdorff implies $T_0$.

+--{: .query}
[[Mike Shulman]]: What precisely does "get an exponential law" mean?  Do you mean that $k Top/B$ is cartesian closed if $B$ is $T_0$?

_Toby_:  Hopefully that is explained in the new article.

_Mike_: Which new article?  [[exponential law for spaces]]?  That page doesn't talk about fibered exponentials at all.
=--


## References 

Compactly generated spaces were first introduced by J. L. Kelley, see his book

* [[John Kelley]], _General topology_, D. van Nostrand, New York 1955. 

Many properties of compactly generated Hausdorff spaces are used to establish a variant of the theory of fibrations, cofibrations and deformation retracts in 

* [[Norman Steenrod]], _A convenient category of topological spaces_, Michigan Math. J. 14 (1967) 133--152, [project euclid](http://projecteuclid.org/euclid.mmj/1028999711)

Later references include

* [[Ronnie Brown]], _Topology and groupoids_, Booksurge 2006, section 5.9. 

* Booth, Peter I.; Heath, Philip R.; Piccinini, Renzo A.
Fibre preserving maps and functional spaces. Algebraic topology (Proc. Conf., Univ. British Columbia, Vancouver, B.C., 1977), pp. 158--167, Lecture Notes in Math., 673, Springer, Berlin, 1978.

* [[Peter May]], _A concise course in algebraic topology_, Chapter 5 [file, revised version](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf)


[[!redirects compactly generated spaces]]
[[!redirects k-space]]
[[!redirects k-spaces]]
[[!redirects kaonization]]
[[!redirects kaonisation]]
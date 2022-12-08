
\tableofcontents

## Idea

Hedberg's theorem in [[dependent type theory]] says that given a type $A$ with [[untruncated decidable equality]], then $A$ it is an [[h-set]]. This was first proven in ([Hedberg](#Hedberg))

## Theorem

+-- {: .num_theorem #DecidableIsSet}
###### Theorem
(**[[Hedberg's theorem]]**)

Suppose that $A$ is a [[type]] which has [[untruncated decidable equality]]. In other words, the projection
$$\array{Paths_A + (0\to A\times A)^{(Paths_A\to A\times A)}\\
\downarrow\\
A\times A}
$$

(where $Paths_A$ is the [[path object|path type]] of $A$, "+" forms the [[sum type]], and on the right we have the $A \times A$-[[dependent type|dependent]] [[function type]] into the [[empty type]]), has a section.  

Then $A$ is a h-set.

=--

+-- {: .proof}
###### Proof
Let $d$ be the given [[section]].  Thus, for any $x,y\colon A$, $d(x,y)$ is either a path from $x$ to $y$ or a function from $Paths(x,y)$ to the empty type (implying that $Paths(x,y)$ is also empty).

It suffices to exhibit an operation connecting any endo-path $p \in Paths(x,x)$ to the identity path $1_x$.  Given such a path, define $q = d(x,x)$.  If $d(x,x)$ lies in the second case, then $Paths(x,x)$ is empty, a contradiction since we know it contains $1_x$; hence we may assume $q\in Paths(x,x)$ as well.

Let $r$ be the image of $(1_x,p) \in Paths_{A\times A}((x,x),(x,x))$ under the section $d$.  This is a path in the total space $Paths_A$ lying over the path $(1_x,p)$ in $A\times A$.  Equivalently, it is a path in the fiber over $x$ from $(1_x,p)_*(d(x,x))$ to $d(x,x)$, where $(1_x,p)_*$ denotes transport in the fibration $Paths_A \to A\times A$ along the path $(1_x,p)$.  However, we have defined $d(x,x) = q$, and transport in a path-space is just composition, so $r$ may be regarded as a path from $q p$ to $q$.  Canceling $q$, we obtain a path from $p$ to $1_x$.
=--

## See also

* [[h-set]]
* [[decidable equality]]

## References

* {#Hedberg} Michael Hedberg, *A coherence theorem for Martin-L&#246;f's type theory*, J. Functional Programming, (1998) 

* Nicolai Kraus, *A direct proof of Hedberg's theorem*, [blog post](http://homotopytypetheory.org/2012/03/30/a-direct-proof-of-hedbergs-theorem/)

* [[Nicolai Kraus]], [[Martin Escardo]], [[Thierry Coquand]] , [[Thorsten Altenkirch]], _Generalizations of Hedberg's theorem_, in M. Hasegawa (Ed.): TLCA 2013, LNCS 7941, pp. 173-188. Springer, Heidelberg 2013. ([pdf](http://www.cs.bham.ac.uk/~mhe/papers/hedberg.pdf))

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

[[!redirects Hedberg's theorem]]
[[!redirects Hedberg theorem]]
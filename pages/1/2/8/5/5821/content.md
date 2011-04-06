# Crossed G-algebra
* table of contents
{: toc}

##Idea

A crossed $G$-algebra is a type of $G$-[[graded algebra]], with an inner product and a 'crossed' or 'twisted' multiplication. They arise as the analogues of [[Frobenius algebras]] for 2d-[[HQFTs]], [[equivariant TQFTs]] and in slight generality in the study of symmetries of singularities.  They were introduced by [[Turaev]] in 1998. The generalised structures have been studied by [[R. Kaufmann]].


##Nomenclature
Moore and Segal do not like the term 'crossed algebra' and suggest the alternative name 'Turaev algebra'.


##Definitions:

We will lead up to the definition of crossed $G$-algebra thorugh various stages.

Here $G$ will be a group (a discrete one for the moment). We need a particular form of [[graded algebra]] in which the summands are projective modules, so we give that form first.

A **graded $G$-algebra** or **$G$-algebra** over a field (or more generally a commutative ring), $\mathbb{k}$ is an associative algebra, $L$, over $\mathbb{k}$ with a decomposition,

$$L = \bigoplus_{g\in G} L_g,$$ 

as a direct sum of projective $\mathbb{k}$-modules of finite type such that

(i) $L_gL_h \subseteq L_{gh}$ for any $g,h \in G$ 
(so, if $\ell_1$ is graded $g$, and $\ell_2$ is graded $h$, then $\ell_1\ell_2$ is graded $gh$),

and 

(ii) $L$ has a unit $1 = 1_L\in L_1$ for 1, the identity element of $G$.


###Example:###

(i)  The [[group algebra]], $\mathbb{k}[G]$, has an obvious $G$-algebra structure in which each summand of the decomposition is free of dimension 1. 

(ii)  For any associatve $\mathbb{k}$-algebra, $A$, the algebra,   $A[G]= A\otimes_\mathbb{k}\mathbb{k}[G]$, is also $G$-algebra.  Multiplication in $A[G]$ is given by $(ag)(bh) = (ab)(gh)$ for $a,b \in A$, $g,h \in G$, in the obvious notation.

(iii) If $G$ is the trivial group, then a $G$-graded algebra is just an algebra (of finite type), of course.


[[!redirects crossed G-algebras]]
[[!redirects Turaev algebra]]
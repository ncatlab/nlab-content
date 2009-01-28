##Idea##
A _$cat^n$-group_ is a strict [[n-category]] [[internal category|internal]] to [[Grp]]. 

Regarding a [[group]] as a [[groupoid]] with a single object, this is the same as an [[n-fold category|(n+1)-fold groupoid]] in which in one direction all morphisms are endomorphisms.

As with the cases $n=1$ and 2, there is a neat purely group theoretic definition of these objects.

##Algebraic definition##
A _cat$^n$-group_  is a group $G$ together with $2n$ endomorphisms $s_i, t_i, (1 \le i \le n)$ such that 

$$s_i t_i = t_i, and  t_i s_i = s_i  for all  i, $$

$$ s_i s_j = s_j s_i,   t_i t_j = t_j t_i, s_i t_j = t_j s_i  for i\neq  j$$ 

and, for all $i$,

$$[ Ker\, s_i, Ker\, t_i] = 1.$$

Morphisms of cat$^n$-groups are the obvious things, morphisms of the groups compatible with the endomorphisms.

A cat$^{n}$-group is thus a group with $n$ independent cat$^{1}$-group structures on it.

#Special cases#

* A $cat^0$-group is a group.

* A [[cat-1-group]] is a strict [[2-group]], viewed in a slightly different way.

#Remarks#

* Even though $cat^n$-groups are examples of strict [[n-category|n-categories]], Loday has shown that the [[homotopy category]] of $cat^{n-1}$-groups is equivalent to that of spaces which are pointed connected [[homotopy n-type]]s. Hence for $cat^n$-groups (thought of as $(n+1)$-fold groupoids) the [[homotopy hypothesis]] is true in this sense. See there for more details.

+-- {.query}
[[Tim Porter|Tim]] Is the first statement above correct? $Cat^n$-groups are examples of strict (n+1)-fold categories, not strict n=categories or am I missing something?

[[Ronnie Brown|Ronnie]] I have corrected that. cat^1-groups are equivalent to crossed modules which model homotopy 2-types. 
=--

###Reference###
The original proof of Loday's result is to be found in

J.-L. Loday, _Spaces with finitely many homotopy groups_, J.Pure Appl. Alg., 24, (1982), 179 &#8211; 202.

There are one or two gaps in that proof and various patches and complete proofs were then given. The main one is in 

R. Steiner, Resolutions of spaces by $n$-cubes of fibrations. J. London Math. Soc. (2) 34 (1986), 169-176.


A proof using $cat^n$-groups and a neat detailed analysis of multisimplicial groups and related topics was given in

M. Bullejos, A. M. Cegarra. and J. Duskin, _On $cat^n$ -groups and homotopy types_, J. Pure Appl. Alg., 86, (1993), 135 &#8211; 154.

Porter gave a proof in terms of [[crossed n-cube]]s (and attempting to use as little high-powered simplicial techniques as possible) in

T. Porter, _n-types of simplicial groups and crossed n-cubes_, Topology, 32, (1993), 5 &#8211; 24.
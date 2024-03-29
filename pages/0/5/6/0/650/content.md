
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Just as [[cat-1-group]]s (i) give models for connected [[homotopy 2-type]]s, (ii) are equivalent to [[crossed modules]], or [[2-group]]s,and are an algebraic encoding of [[internal category|internal categories]] within the category [[Grp]] of groups, so it is not surprising that higher dimensional analogues encode higher order homotopy information. This gives one the abstract definition:

##Abstract definition

A _$cat^n$-group_ is a strict [[n-fold category]] [[internal category|internal]] to [[Grp]]. 


Regarding a [[group]] as a [[groupoid]] with a single object, this is the same as an [[n-fold category|(n+1)-fold groupoid]] in which in one direction all morphisms are [[endomorphism]]s and there is corresponding notion of cat$^n$-groupoid.

As with the cases $n=1$ and 2, there is a neat purely group theoretic definition of these objects.

## Algebraic definition

A _cat$^n$-group_  is a [[group]] $G$ together with $2n$ [[endomorphism]]s $s_i, t_i, (1 \le i \le n)$ such that 

$$s_i t_i = t_i, and  t_i s_i = s_i  for all  i, $$

$$ s_i s_j = s_j s_i,   t_i t_j = t_j t_i, s_i t_j = t_j s_i  for i\neq  j$$ 

and, for all $i$,

$$[ Ker\, s_i, Ker\, t_i] = 1.$$

Morphisms of cat$^n$-groups are the obvious things, morphisms of the groups compatible with the endomorphisms.

A cat$^{n}$-group is thus a group with $n$ independent cat$^{1}$-group structures on it.

## Special cases

* A $cat^0$-group is a group.

* A [[cat-1-group]] is a strict [[2-group]], viewed in a slightly different way.


## Homotopical example 

 For simplicity, we describe  $\Pi X_{*}$   in a special
case, namely  when  the $n$-cube of spaces $X_{*}$   arises from a pointed  $(n +
1)$-ad  $ (X;X_1,\ldots ,X_n)$  by the  rule:  $X_{
\langle n \rangle}  = X$  and for  $A$  properly contained in
$\langle n \rangle$,   $X_A = \bigcap _{i \not\in A} X_i$, with
maps  the inclusions.  Let  $\Phi$   be the space of maps  $I^n
\to   X$  which take  the  faces of  $I^n$  in the  $i$th
direction into  $X_i$.  Notice that  $\Phi$  has the  structure
of $n$ compositions derived from the gluing of cubes in each
direction.  Let  $\bullet  \in  \Phi$   be the constant map at the
base point.   Then  $G = \pi_1(\Phi ,\bullet )$ is certainly a
group.  Gilbert, 1988, identifies   $G$ with  Loday's  $\Pi
X_{*}$, so that Loday's results, obtained by methods of
simplicial  spaces, show that  $G$  becomes a cat$^n$-group.  It
may also be shown that  the  extra groupoid structures are
inherited from the compositions on  $\Phi$.   It  is this
cat$^n$-group which is written  $\Pi X_*$   and is called
the  _fundamental  cat$^n$-group of the  $(n + 1)$-ad_. 

See also [[crossed n-cube]] for an alternative description. 


## Remarks

* Even though $cat^n$-groups are examples of strict [[n-fold category|(n+1)-fold categories]], Loday has shown that the [[homotopy category]] of $cat^{n-1}$-groups is equivalent to that of spaces which are pointed connected [[homotopy n-type]]s. Hence for $cat^n$-groups (thought of as $(n+1)$-fold groupoids) the [[homotopy hypothesis]] is true in this sense. See there for more details.

## Related concepts

* [[crossed n-cube]]


## References

The original proof of Loday's result is to be found in

* [[J.-L. Loday]], _Spaces with finitely many nontrivial homotopy groups_, J. Pure Appl. Alg., 24, (1982), 179--202.

This paper also uses the term n-cat-group, but later use favours the term cat$^n$-group to make it clearer that these were an [[n-fold category]] [[internalization|internal]] to [[Grp]]. There are one or two gaps in that proof and various patches and complete proofs were then given. The main one is in 

* [[R. Steiner]], Resolutions of spaces by cubes of fibrations. J. London Math. Soc. (2) 34 (1986), 169--176.


A proof using $cat^n$-groups and a neat detailed analysis of multisimplicial groups and related topics was given in

* [[Manuel Bullejos]], [[Antonio M. Cegarra]], [[John W. Duskin]], *On cat$^n$ -groups and homotopy types*, J. Pure 
Appl. Alg. **86** (1993) 135-154 \[<a href="https://doi.org/10.1016/0022-4049(93)90099-F">doi:10.1016/0022-4049(93)90099-F</a>&rbrack;


A simple proof in terms of [[crossed n-cube|crossed n-cubes]]  using as little high-powered simplicial techniques as possible:

* [[Tim Porter|T. Porter]], _n-types of simplicial groups and crossed n-cubes_, Topology, 32, (1993), 5--24.

[[!redirects cat-n-groups]]


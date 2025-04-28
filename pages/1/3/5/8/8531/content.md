
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Coextension of scalars is the [[right adjoint]] to _[[restriction of scalars]]_.  It is the dual notion to _[[extension of scalars]]_.

## Definition

Let $f \colon R \to S$ be a [[homomorphism]] of [[algebra|algebraic]] objects such as [[rings]].  If $\cdot_S$ is the left [[action]] of $S$ on some [[module]] $M$, then 
$$
  r\cdot_R m \coloneqq f( r )\cdot_S m
$$ 
defines a left action of $R$ on $M$. This construction extends to a  [[functor]] called *restriction of scalars* along $f$ and denoted
$$
  f^\ast \colon SMod \longrightarrow RMod
$$
This functor has both a [[left adjoint]] and a [[right adjoint]].  The left adjoint $f_!$ is called *[[extension of scalars]]*. Its right adjoint is called *coextension of scalars* and denoted
$$
  f_* \colon
  RMod
   \longrightarrow 
  SMod
$$
Concretely, for any left $R$-module $M$, $f_*(M)$ is the [[hom set]] $RMod(S,M)$ made into a left $S$-module by
$$
    (s g)(s') \coloneqq g(s' s)
$$ 
for $g \in RMod(S,M)$ and $s,s' \in S$.  Here $S$ is made into a left $R$-module by
$$
   r \cdot s \coloneqq f(r) s 
$$

## Example

Here is one special case.

For $R$ a [[ring]], write $R$[[Mod]] for its category of [[modules]]. Write [[Ab]] = $\mathbb{Z}$[[Mod]] for the category of [[abelian groups]].

Write $U\colon R Mod \to Ab$ for the [[forgetful functor]] that forgets the $R$-module structure on a module $N$ and just remembers the underlying abelian group $U(N)$. 

+-- {: .num_lemma #CoextensionOfScalarsForRModToZMod}
###### Lemma

The [[functor]] $U\colon R Mod \to Ab$ has a [[right adjoint]] 

$$
  R_* : Ab \to R Mod
$$

given by sending an [[abelian group]] $A$ to the abelian group

$$
  U(R_*(A)) \coloneqq Ab(U(R),A)
$$

equipped with the $R$-[[module]] struture by which for $r \in R$ an element $(U(R) \stackrel{f}{\to} A) \in U(R_*(A))$ is sent to the element $r f$ given by

$$
  r f : r' \mapsto f(r' \cdot r)
  \,.
$$ 

This is called the **[[coextension of scalars]]** along the ring homomorphism $\mathbb{Z} \to R$.

The [[unit of an adjunction|unit]] of the $(U \dashv R_*)$ [[adjunction]]

$$
  \epsilon_N : N \to R_*(U(N))
$$

is the $R$-module homomorphism

$$
  \epsilon_N : N \to Hom_{Ab}(U(R), U(N))
$$

given on $n \in N$ by

$$
  j(n) : r \mapsto r n
  \,.
$$

=--


## Properties

### Relation to extension of scalars

In some cases coextension of scalars is naturally isomorphic to [[extension of scalars]], which is the *left* adjoint to restriction of scalars.  For example if $H$ is a [[subgroup]] of [[finite number|finite]] [[index of a subgroup|index]] of a group $G$, for any field $k$ there is an inclusion of [[group algebras]]
$$   
 i \colon k[H] \to k[G]
$$
and coextension of scalars along $i$ is naturally isomorphic to extension of scalars along $i$.

### Frobenius extensions

Co-Extension of scalars coincides with *[[extension of scalars]]* (to make an [[ambidextrous adjunction]] with [[restriction of scalars]]) in the case of [[Frobenius extensions]], see there for more.



## Related concepts

* [[extension of scalars]] $\dashv$ [[restriction of scalars]] $\dashv$ **coextension of scalars**



## References

* H. Fausk, P. Hu, [[Peter May]], _Isomorphisms between left and right adjoints_ ([pdf](https://www.math.uchicago.edu/~may/PAPERS/FormalFinalMarch.pdf))


[[!redirects coextensions of scalars]]

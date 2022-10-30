
> Currently this entry consists mainly of notes taken live in a talk by [[John Francis]] at [ESI Program on K-Theory and Quantum Fields](http://maths-old.anu.edu.au/esi/2012/) (2012), without as yet, any double-checking or polishing. So handle with care for the moment.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Factorization homology_  is a notion of [[homology theory]] for [[framed manifold|framed]] $n$-[[dimension|dimensional]] [[manifolds]] with coefficients in [[En-algebras]], due to ([Francis](#Francis)). It is similar in spirit to _[[factorization algebras]]_, _[[blob homology]]_ and _[[topological chiral homology]]_. In fact the definition of factorization homology turns out to be equivalent to that of topological chiral topology ([Francis b](#Francisb)).


## Definition

Write $Mfd_n^{\coprod}$ for the category of [[manifolds]] with [[embeddings]] as morphisms. This is naturally a [[topological category]], hence regard it as an [[(infinity,1)-category]].
Regard it furthermore as a [[symmetric monoidal (∞,1)-category]] with [[tensor product]] given by [[disjoint union]]. 

For $k$ a [[field]], write $Mod_k$ for the [[symmetric monoidal (∞,1)-category]] of $k$-[[chain complexes]].

Let $H(Mfd_n^{\coprod}, Mod_k)$ be the [[sub-(∞,1)-category]] of those  [[monoidal (∞,1)-functors]] $F : Mfd_n^{op} \to Mod_k$ which are "[[cosheaves]]" in that for any decomposition of a manifold $X$ into submanifolds $X'$ and $X''$ with overlap $O$, we have an [[equivalence in an (∞,1)-category|equivalence]] 

$$
  F(X) \simeq F(X') \otimes_{F(O) F(X'')}
  \,.
$$

Next, let $Disk_n \subset Mfd_n$ be the full [[sub-(∞,1)-category]] on those [[manifolds]] which are finite [[disjoint unions]] of the [[Cartesian space]] $\mathbb{R}^n$. 

Restriction along this inclusion gives an [[(∞,1)-functor]]

$$
  H(Mfd_n, Mod_k)
  \to
  Disk_n-Alg (Mod_k)
$$

This turns out to be an [[equivalence of (∞,1)-categories]].  The inverse is defined to be _factorization homology_ 

$$
  FactorizationHomology
   :
  Disk_n-Alg (Mod_k)
  \to
  H(Mfd_n, Mod_k)
  \,.
$$

This inverse sends an $n$-disk algebra

$$
  A : Disk_n \to Mod_k
$$

to the functor that sends a manifold $X$ to the 

The factorization homology is then the [[derived functor|derived]] [[coend]]

$$
  \int^X A = \mathbb{E}_X \otimes_{Disk_n} A
$$

of $A$ with

$$
  \mathbb{E}_X 
    : 
  Disk_n \stackrel{Emb(-,X)}{\to} Top \stackrel{C_\bullet(-)}{\to} Mod_k
  \,.
$$


This is equivalent to [[topological chiral homology]], to be thought of as a topological version of [[chiral algebras]]. A version with values in [[homotopy types]] instead of chain complexes was given by Salvatore and [[Graeme Segal]].

## Properties

### Relation to cobordism hypothsis

From a functor $F \in H(Mfd_n, Mod_k)$ we get an [[extended TQFT]] with values in $k$-linear $(\infty,n)$-categories

$Z_F : Bord_n \to Cat_n(k)$ which sends a $k$-manifold $X$ to $F(X \times \mathbb{R}^{n-k})$, regarded as a [[bimodule]] between the analogous boundary restriction, and hence as a [[n-morphism|k-morphism]] in $Cat_n(k)$.

From a  $Disk_n$-algebra $A$ we obtain the corresponding [[delooping]] $\mathbf{B}A \in (Cat_n(k)_{dualizable})^{O(n)}$ which is a $k$-linear [[(infinity,n)-category]] that is a [[fully dualizable object]]. The [[cobordism hypothesis]] identifies this with cobordism representations, and the claim is that this identification is compatible factorization homology.



## Examples

### Dimension 1

A $Disk_1$-algebra $A$ in $Mod_k$ is equivalently a [[differential graded algebra]].

The value of the corresponding $F_A \in H(Mfd_1, Mod_k)$ on the circle is the [[Hochschild homology]] of $A$

$$
  \int_{S^1} A \simeq \int_{\mathbb{R}^1} A \otimes_{\int_{S^0 \times \mathbb{R}}A} \int_{\mathbb{R}^1} A \simeq HH_\bullet(A)
  \,.
$$

### From $n$-fold loop spaces

Given a [[toplogical space]] $Z$ we get a $Disk_n$-algebra

$$
  Disk_n^\coprod 
  \stackrel{Maps_{compact}(-,Z)}{\to}
  Top
  \stackrel{C_\ast(-)}{\to} Mod_k
$$

Where $Maps_{compact}(\mathbb{R}^n, Z) \simeq \Omega^n Z$ is the [[n-fold loop space]] of $Z$.

**Theorem** (Salvatore and [[Jacob Lurie|Lurie]])

If $Z$ is $(n-1)$-[[n-connected object of an (infinity,1)-category]]


$$
  \int_X C_\ast(\Omega^n Z) \simeq C_\ast Maps_{compact}(X,Z)
  \,.
$$






## References

The definition appears in section 3 of 

* [[John Francis]], _The tangent complex and Hochschild cohomology of $\mathcal{E}_n$-rings_ ([arXiv:1104.0181](http://arxiv.org/abs/1104.0181))
 {#Francis}

More details are to appear in 

* [[John Francis]], _Factorization homology of topological manifolds_, in preparation
 {#Francisb}

See also

* [[Hiro Lee Tanaka]], _Manifold calculus is dual to factorization homology_, at [Talbot 2012:_ Calculus of functors](http://math.mit.edu/conferences/talbot/2012/_2012.php) ([pdf](http://math.mit.edu/conferences/talbot/2012/notes/14_Tanaka_FactorizationHomology%28hiro%29.pdf))

Application to higher [[Hochschild cohomology]] is discussed in 

* [[Grégory Ginot]], Thomas Tradler, [[Mahmoud Zeinalian]], _Higher Hochschild cohomology, Brane topology and centralizers of $E_n$-algebra maps_, ([arXiv:1205.7056](http://arxiv.org/abs/1205.7056))


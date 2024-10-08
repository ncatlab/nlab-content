
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Morava K-theory
* table of contents
{:toc}

## Idea

For each [[prime]] $p$, the Morava K-theories are a tower $\{K(n)\}_{n \in \mathbb{N}}$ of [[complex oriented cohomology theories]] whose [[coefficient]] [[ring]] is

$$
  \pi_\bullet\left(K\left(n\right)\right)
  \simeq
  \mathbb{F}_p [v_n, v_n^{-1}]
$$

where $v_n$ is in degree $2(p^n-1)$.

Hence with $p = 2$ for $n = 1$ $v_1$ is a [[Bott element]] of degree 2 and $K(1)$ is closely related to [[complex K-theory]], while for $n= 2$ $v_2$ is then a [[Bott element]] of degree 6 and $K(2)$ is closely related to [[elliptic cohomology]].

There is also [[integral Morava K-theory]] which instead has coefficient ring

$$
  \pi_\bullet\left(K\left(n\right)\right)
  \simeq
  \mathbb{Z}_{(p)} [v_n, v_n^{-1}]
  \,,
$$

where $\mathbb{Z}_{(p)}$ is the [[p-adic integers]].

Integral Morava K-theory can be obtained as a localization of a quotient $MU/I$ of [[complex cobordism cohomology theory]] $MU$ ([Buhn&#233; 11](#Buhne11)).



## Definition

We need the following standard notation throughout this entry.

+-- {: .num_defn}
###### Definition

For $p \in \mathbb{N}$ a [[prime number]], we write

* $\mathbb{F}_p = \mathbb{Z}/(p)$ for the [[field]] with $p$ elements;

* $\mathbb{Z}_{(p)}$ for the [[localization of a ring|localization ring]] of the [[integers]] at $p$;

* $\mathbb{Z}_p$ for the [[p-adic integers]].

=--

### Construction from complex cobordism

(e.g. [Lurie 10, lecture 22, def. 5](#LurieLecture))


### Axiomatic characterization

+-- {: .num_prop #AxiomaticCharacterization}
###### Proposition/Definition

For each [[prime number|prime integer]] $p$ 
the _Morava K-theories_ are the [[sequences]] 

$$
  \big\{
    K(n)
  \big\}_{n \in \mathbb{N}}
$$ 

of [[multiplicative cohomology theory|multiplicative]] [[generalized cohomology theories|generalized cohomology]]/[[generalized homology theories|homology theories]] with the following properties:

1. $K(0)_\ast(X)=H_\ast(X;\mathbb{Q})$ and $\overline{K(0)}_\ast(X)=0$ when $\overline{H}_\ast(X)$ is all [[torsion]].

1. $K(1)_\ast(X)$ is one of $p-1$ isomorphic summands of mod-$p$ complex [[topological K-theory]]. 

1. $K(0)_\ast(pt.)=\mathbb{Q}$ and for $n\neq 0$, $K(n)_\ast(pt.)=\mathbb{F}_p[v_n,v_n^{-1}]$ where $\vert v_n\vert=2p^n-2$.  

   > (This [[ring]] is a graded [[field]] in the sense that every graded [[module]] over it is [[free module|free]].  $K(n)_\ast(X)$ is a module over $K(n)_\ast(pt.)$, see [below](#AsInfinityFields))

1. There is a [[Künneth isomorphism]]: $K(n)_\ast(X\times Y)\cong K(n)_\ast(X)\otimes_{K(n)_\ast(pt.)}K(n)_\ast(Y).$

1. Let $X$ be a p-local finite [[CW-complex]]. If $\overline{K(n)}_\ast(X)$ vanishes then so does $\overline{K(n-1)}_\ast(X)$.

1. If $X$ is as above, then $\overline{K(n)}_\ast(X)=K(n)_\ast(pt.)\otimes \overline{H}_\ast(X;\mathbb{Z}/(p))$ for $n$ sufficiently large.

=--

([Ravenel 1992, Prop. 1.5.2](#Ravenel92))

\begin{remark}
Due to the third point in \ref{AxiomaticCharacterization}, one may regard $K(n)$ as a [[∞-field]] among the [[A-infinity rings]]. See [below](#AsInfinityFields).
\end{remark}


## Properties

### Universal characterization

+-- {: .num_prop}
###### Proposition

For each [[prime number]] $p$ and each $n \in \mathbb{N}$, the Morava K-theory $K(n)$ is, up to [[equivalence in an (∞,1)-category|equivalence]], the unique [[spectrum]] underlying an [[H-space|homotopy associative]] spectrum which is

1. [[complex oriented cohomology theory|complex oriented]];

1. whose [[formal group]] has [[height of a formal group|height]] exactly $n$;

1. whose [[homotopy groups]] are $\pi_\bullet \simeq \mathbb{F}_p[v_n^\pm]$. (with $v_n$ defined as at _[[height of a formal group|height]]_).

=--

For instance ([Lurie, lecture 24, prop. 11](#LurieLecture)).

### Ring structure

+-- {: .num_prop}
###### Proposition


$K(n)$ admits the structure of an [[A-∞ algebra]], in fact of an $MU_{(p)}$-[[A-∞ algebra]]. 

=--

Due to Robinson (and [[Andrew Baker]] at $p = 2$). (See e.g. [Lurie 10, lecture 22, lemma 2](#LurieLecture))

+-- {: .num_remark}
###### Remark

With the exception of the extreme case of $n=0$, the fields $K(n)$ do not admit [[E-∞-ring]] multiplicative structures. However, when $p\neq 2$, the multiplication is homotopy commutative. For $p = 2$ it is _not_ even homotopy commutative. Nevertheless, for many spaces $X$, the $K(n)$-[[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology]] at the prime $2$ of $X$ forms a commutative ring.

=--

(e.g. [Lurie 10, lecture 22, warning 6](#LurieLecture))


### As $A_\infty$-fields
 {#AsInfinityFields}

+-- {: .num_prop}
###### Proposition

If $E$ is an [[∞-field]] and $E \otimes K(n) \neq 0$, then $E$ admits the structure of a $K(n)$-[[module spectrum|module]].

=--

This appears for instance as ([Lurie, lecture 24, prop. 9, remark 13](#LurieLecture))

+-- {: .num_remark}
###### Remark

This means that the Morava $A_\infty$-rings $K(n)$ are essentially the only [[∞-fields]] in the [[stable homotopy category]].

=--

See ([Lurie, lecture 24, remark 13](#LurieLecture))


### As the primes in the $\infty$-category of spectra

The Morava K-theories label the [[prime spectrum of a symmetric monoidal stable (∞,1)-category]] of the [[(∞,1)-category of spectra]] for [[p-localization|p-local]] and [[finite spectra]] . This is the content of the _[[thick subcategory theorem]]_.


### Relation to chromatic homotopy theory

The layers in the [[chromatic homotopy theory|chromatic tower]] capture periodic phenomena in [[stable homotopy theory]], corresponding to the Morava K-theory $E_\infty$-fields.

Specifically the [[Bousfield localization of spectra]] $L_{K(n)}$ acts on [[complex oriented cohomology theories]] like completion along the locally closed substack

$$
  \mathcal{M}^n_{FG}
  \hookrightarrow
  \mathcal{M}_{FG}
$$

of the [[moduli stack of formal groups]] at those of [[height of a formal group|height]] $n$.

([Lurie 10, lecture 29](#LurieLecture))

[[!include chromatic tower examples - table]]


### Relation to Bousfield lattice

It is known that in the [[Bousfield lattice]] of the [[stable homotopy category]], the Bousfield classes of the Morava K-theories are minimal. It is conjectured by [[Mark Hovey]] and John Palmieri that the [[Boolean algebra]] contained in the Bousfield lattice is atomic and generated by the Morava K-theories and the spectra $A(n)$ which measure the failure of the [[telescope conjecture]].

### Orientation
 {#Orientation}

The [[orientation in generalized cohomology|orientation]] of [[integral Morava K-theory]] is discussed in ([Sati-Kriz 04](#SatiKriz04), [Buhn&#233; 11](#Buhne11)). It is essentially given by the vanishing of the seventh [[integral Stiefel-Whitney class]] $W_7$. 

Notice that this is in higher analogy to how [[orientation in generalized cohomology|orientation]] in [[complex K-theory]] is given by the vanishing third [[integral Stiefel-Whitney class]] $W_3$ ([[spin^c-structure]]).

### $\infty$-Group rings and twists

Write $gl_1(K(n))$ for the [[∞-group of units]] of the (a) Morava K-theory spectrum

+-- {: .num_prop}
###### Proposition

For $p = 2$ and all $n \in \mathbb{N}$, there is an [[equivalence in an (infinity,1)-category|equivalence]]

$$
  Maps(B^{n+1}U(1), B gl_1(K(n)))
  \simeq
  \mathbb{Z}_2
$$

between 

* the [[mapping space]] from the [[classifying space]] for [[circle n-bundle|circle (n+1)-bundles]] to the [[delooping]] of the [[∞-group of units]] of $K(n)$

and 

* the [[p-adic integers|2-adic integers]].

=--

([Sati-Westerland 11, theorem 1](#SatiWesterland11))

+-- {: .num_remark}
###### Remark

By the discussion at [[(∞,1)-vector bundle]] this means that for each such map there is a type of [[twisted cohomology|twist]] of Morava K-theory (at $p = 2$).

=--


## Related concepts

* [[equivariant Morava K-theory]]

* [[2-periodic Morava K-theory]]

* [[K-theory]], [[topological K-theory]], [[algebraic K-theory]]

* [[chromatic homotopy theory]]

* [[K(n)-local stable homotopy theory]]

* [[integral Morava K-theory]]

* [[Morava E-theory]]

  * [[Lubin-Tate theory]]



## References

Morava K-theory originates in unpublished preprints by [[Jack Morava]] in the early 1970s. 

A first published account appears in (see at _[[Johnson-Wilson spectrum]]_):

* [[David Copeland Johnson]], [[W. Stephen Wilson]], _BP operations and Morava's extraordinary K-theories_, Math. Z. 144 (1): 55&#8722;75,  (1975) ([pdf](http://www.math.jhu.edu/~wsw/papers2/math/08-BP-Kn-J2W-1975.pdf))

see also

* {#Ravenel92} [[Doug Ravenel]], _Nilpotence and Periodicity in Stable Homotopy Theory_, Annals of Mathematics Studies **128**, Princeton University Press (1992) &lbrack;[ISBN:9780691025728](https://press.princeton.edu/books/paperback/9780691025728/nilpotence-and-periodicity-in-stable-homotopy-theory-am-128-volume), [pdf](https://people.math.rochester.edu/faculty/doug/mybooks/nilpb.pdf), [webpage](https://people.math.rochester.edu/faculty/doug/nilp.html)&rbrack;

Textbook account:

* {#Rudyak98} [[Yuli Rudyak]], Section IX.7 in: _On Thom Spectra, Orientability, and Cobordism_, Springer 1998 ([doi:10.1007/978-3-540-77751-9](https://doi.org/10.1007/978-3-540-77751-9))


A discussion with an eye towards [[category theory|category theoretic]] general abstract properties of localized stable homotopy theory is in 

* [[Mark Hovey]], [[Neil Strickland]], _Morava K-theories and localization_, American Mathematical Soc., Jan 1, 1999 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/kn.pdf))


A survey of the theory is in 

* Urs W&#252;rgler, _Morava K-theories: a survey_, Algebraic topology Poznan 1989, Lecture Notes in Math. 1474, Berlin: Springer, pp. 111 138 (1991) ([doi:10.1007/BFb0084741](https://doi.org/10.1007/BFb0084741))


In 

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture notes, ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture22.pdf)){#LurieLecture}

  Lecture 22 _Morava E-theory and Morava K-theory_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture22.pdf))

  Lecture 23 _The Bousfield Classes of $E(n)$ and $K(n)$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture23.pdf))

  Lecture 24 _Uniqueness of Morava K-theory_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture24.pdf))

the explicit definition via [[formal group laws]] is in lecture 22 and the abstract characterization in lecture 24.

The $E_\infty$-algebra structure over $\widehat{E(n)}$ is comment on in 

* {#Baker} [[Andrew Baker]], _Brave new Hopf algebroids_ ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/brave-ha.pdf))
 

based on 

* {#Strickland99} [[Neil Strickland]], _Products on $MU$-modules_, Trans. Amer. Math. Soc. 351 (1999), 2569-2606.

Discussion in relation to the [[Arnold conjecture]] in [[symplectic topology]]:

* [[Mohammed Abouzaid]], [[Andrew J. Blumberg]], _Arnold Conjecture and Morava K-theory_, ([arXiv:2103.01507](https://arxiv.org/abs/2103.01507))
 
On the Morava K-theory of [[iterated loop spaces]] of [[n-spheres]]:

* [[Douglas Ravenel]], *What we still don't know about loop spaces of spheres*, in: [[Mark Mahowald]], [[Stewart Priddy]] (eds.), *Homotopy Theory via Algebraic Geometry and Group Representations*, Contemporary Mathematics **220**, AMS 1998  ([pdf](https://people.math.rochester.edu/faculty/doug/mypapers/loop.pdf), [[Ravenel_LoopSpacesOfSpheres.pdf:file]], [doi:10.1090/conm/220](http://dx.doi.org/10.1090/conm/220))



The [[orientation in generalized cohomology|orientation]] of [[integral Morava K-theory]] is discussed in

* {#SatiKriz04} [[Igor Kriz]], [[Hisham Sati]], _M-theory, type IIA superstrings, and elliptic cohomology_, Adv. Theor.
Math. Phys. 8 (2004), no. 2, 345&#8211;394 ([arXiv:hep-th/0404013](http://arxiv.org/abs/hep-th/0404013))
 

* {#Buhne11} [[Lukas Buhné]], _[[Properties of Integral Morava K-Theory and the Asserted Application to the Diaconescu-Moore-Witten Anomaly]]_, Diploma thesis Hamburg (2011)
 

Some [[twisted cohomology|twists]] of Morava K-theory/maps into its [[∞-group of units]] as well as the [[Atiyah-Hirzebruch spectral sequence]] for Morava $K$ and Morava $E$ are discussed in 

* {#SatiWesterland11} [[Hisham Sati]], [[Craig Westerland]], _Twisted Morava K-theory and E-theory_ ([arXiv:1109.3867](http://arxiv.org/abs/1109.3867))
 

For a review in the context of [[M-theory]] see

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_ (2010)


[[!redirects Morava K-theories]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Nullstelle_ means [[zero locus]]. Hilbert's _Nullstellensatz_ (theorem about zero loci) characterizes the joint zero loci of an [[ideal]] of functions in a [[polynomial ring]]. This is a foundational result in [[algebraic geometry]] at the heart of the [[Isbell duality|duality]] by which [[rings]] are dually interpreted as [[spaces]] ([[varieties]]).

## Classical formulation in algebraic geometry 

In classical algebraic geometry over an [[algebraically closed field]] $k$, the Nullstellensatz concerns the [[fixed points]] of a standard [[Galois connection]] between [[ideals]] $I$ of $k[x_1, \ldots, x_n]$ and [[subsets]] $V \subseteq k^n$. The Galois connection is induced by a [[relation]] $I \perp V$ iff $f(x) = 0$ for all $f \in I, x \in V$. Accordingly, letting $Idl(k[x_1, \ldots, x_n])$ be the set of ideals ordered by inclusion and $P(k^n)$ the set of subsets of $k^n$ ordered by inclusion, there are contravariant maps $Ideal: P(k^n) \to Idl(k[x_1, \ldots, x_n])$ and $Var: Idl(k[x_1, \ldots, x_n]) \to P(k^n)$ defined by 

$$Ideal(S) = \{f \in k[x_1, \ldots, x_n]: \forall_x x \in S \Rightarrow f(x) = 0\}, \qquad Var(I) = \{x \in k^n: \forall_f f \in I \Rightarrow f(x) = 0\}$$ 

which defines the Galois connection. 

The fixed points of $Var \circ Ideal: P(k^n) \to P(k^n)$ are, by definition, the closed sets of the [[Zariski topology]] on the [[affine space]] $k^n$ ("affine space" here in the sense of algebraic geometry). These are the closed subvarieties of $k^n$. 

On the other side, the fixed points of $Ideal \circ Var$ is what the classical Nullstellensatz is about: 

+-- {: .num_theorem} 
###### Theorem 
**(Strong Nullstellensatz)** The fixed points of $Ideal \circ Var$ are precisely the [[radical]] ideals $I$ of $k[x_1, \ldots, x_n]$, i.e., ideals $I$ such that for any $r \in \mathbb{N}$, the condition $f^r \in I$ implies $f \in I$. 
=-- 

Thus there is a [[Galois correspondence]] between closed subvarieties and radical ideals. 

Typically the way that the strong Nullstellensatz is proved is by reduction to the so-called "weak Nullstellensatz" by means of the "Rabinowitsch trick". (The "weak" here may be misleading, as the weak Nullstellensatz may be considered the core result and the strong Nullstellensatz a corollary.) We now turn to these. 

### A weak Nullstellensatz: Existence of points
 {#ExistenceOfPoints}

One weak version of the Nullstellensatz says the following (e.g. [theorem 3.99.1 here](http://www.math.unipd.it/~frank/ALGANT/2010/Notes/7-12.pdf)).

For $k$ an [[algebraically closed field]] and $I$ a proper [[ideal]] in the [[polynomial ring]] $k[X_1, \cdots, X_n]$, then the set $V(I)$ (of $n$-[[tuples]] $x = (x_i) \in k^n$ such that all polynomials in $I$ vanish when evaluated on these $x$) is an [[inhabited set]].

Before giving a proof, we remark (in view of more abstract formulations to come later) that an element of $V(I)$ is just a $k$-[[associative algebra|algebra]] [[homomorphism]] of the form

$$
  k \longleftarrow  k[X_1, \cdots, X_n]/I
  \,.
$$

[[Isbell duality|Dually]] this is a morphism of [[affine schemes]] ([[spectrum of a commutative ring|ring spectra]]) of the form

$$
  Spec(k) \longrightarrow Spec(k[X_1, \cdots, X_n]/I)
  \,.
$$

Moreover, since $Spec(k)$ is the [[terminal object]] in this context, such a map is the same as a "point", a [[global element]] of $Spec(k[X_1, \cdots, X_n]/I)$.

Hence in this form the Nullstellensatz simply says that (for $k$ algebraically closed) affine schemes have points. This formulation of the Nullstellensatz leads one to a [more general abstract formulation](#GeneralAbstract). 

+-- {: .num_lemma #uncountable} 
###### Lemma 
If $k$ is an *uncountable* algebraically closed field, then for any proper ideal $I \subset k[X_1, \ldots, X_n]$ there is $(a_1, \ldots, a_n) \in k^n$ such that $f(a_1, \ldots, a_n) = 0$ for all $f \in I$. 
=-- 

+-- {: .proof} 
###### Proof 
By the [[axiom of choice]], $I$ is contained in a [[maximal ideal]] $M$. So it suffices to prove it in the case where $I = M$ is maximal, where we prove there is an isomorphism $\phi: k[X_1, \ldots, X_n]/M \cong k$. Then the composite 

$$k[X_1, \ldots, X_n] \stackrel{quot}{\twoheadrightarrow} k[X_1, \ldots, X_n]/M \stackrel{\phi}{\to} k$$ 

sends each $X_i$ to a value $a_i$, so we have an inclusion of maximal ideals 

$$(X_1 - a_1, \ldots, X_n - a_n) \subseteq M$$ 

which must be an equality. In that case $(a_1, \ldots, a_n)$ is the desired point. 

Since $k$ is algebraically closed, it suffices to prove that the extension field $F = k[X_1, \ldots, X_n]/M$ over $k$ is algebraic over $k$. Clearly $F$ as a [[vector space]] over $k$ has countable [[dimension]]. If there is an element $t \in F$ which is transcendental over $k$, then as a vector space we have 

$$k(t)/k[t] \cong \bigoplus_{a \in k} k \cdot \frac1{t - a}$$ 

by partial fraction decomposition (ultimately the [[Chinese remainder theorem]]), but the right side has an uncountable basis (being parametrized by uncountably many $a \in k$), and this leads to a contradiction. 
=-- 

Now we reduce to the case where $k$ is uncountable by employing a [[model theory|model-theoretic]] argument: 

+-- {: .num_theorem} 
###### Theorem 
If $k$ is an algebraically closed field, then for any proper ideal $I \subset k[X_1, \ldots, X_n]$ there is $(a_1, \ldots, a_n) \in k^n$ such that $f(a_1, \ldots, a_n) = 0$ for all $f \in I$. 
=-- 

+-- {: .proof} 
###### Proof 
Let $U$ be a non-principal ultrafilter on $\mathbb{N}$, and let $K$ be the [[ultraproduct|ultrapower]] $k^\mathbb{N}/U$. By &#321;o&#347;'s theorem, $K$ is an algebraically closed field. Also $K$ is uncountable (proof to be inserted somewhere, sometime later). 

First $K \otimes_k I$ is a proper ideal of $K \otimes_k k[x_1, \ldots, x_n] \cong K[x_1,\ldots, x_n]$. For suppose we have $1 = \sum_{i = 1}^s f_i p_i$ for $p_1, \ldots, p_s \in I$ and $f_i \in K[x_1, \ldots, x_n]$. Writing the $f_i$ as $K$-linear combinations of monomials $x^\alpha$, there are finitely many $q_1, \ldots, q_t \in I$, each of the form $x^\alpha p_i$, so as to enable us to write $1 = \sum_{i=1}^t a_i q_i$ for $a_i = [(a_{i, m})] \in K$ and $q_i \in I$. By &#321;o&#347;'s theorem, 

$$\{m \in \mathbb{N}: 1 = \sum_{i=1}^t a_{i, m} q_i\; in\; k[x_1, \ldots, x_n]\} \in U;$$ 

this set is nonempty, and so there is at least one $m$ rendering the equation true. This contradicts $1 \notin I$. 

By Lemma \ref{uncountable}, there is a point $(a_1, \ldots, a_n) \in K^n$ that belongs to $Var(I)$. By [[noetherian ring|Hilbert's basis theorem]], $I \subset k[x_1, \ldots, x_n]$ is generated by finitely many polynomials $p_1, \ldots, p_s$, so $Var(I) \subseteq K^n$ is defined by finitely many formulas $p_1(x) = 0, \ldots, p_s(x) = 0$ and thus by &#321;o&#347;'s theorem again, 

$$\{m \in \mathbb{N}: p_i(a_{1, m}, a_{2, m}, \ldots, a_{n, m}) = 0\; for\; i = 1, \ldots, s\}$$ 

belongs to $U$, and so this set is nonempty and therefore there is a point $(a_{1, m}, \ldots, a_{n, m}) \in k^n$ that belongs to $Var(I)$. 
=-- 



## General abstract formulations 
 {#GeneralAbstract}

By the discussion above at _[Existence of points](#ExistenceOfPoints)_ it follows that phrased in terms of the [[sheaf topos]] over the [[Zariski site]], the weak Nullstellensatz says that "objects have global points". 

Motivated by this, in ([Lawvere 07, def. 2](#Lawvere07)) is a proposal for a [[general abstract]] formulation of what constitutes a _Nullstellensatz_, formalized in the context of [[cohesion]].

A [[cohesive topos]] $\mathbf{H}$ over some [[base topos]] $\mathbf{S}$ is a relative [[topos]] such that the terminal [[geometric morphism]] extended to an [[adjoint quadruple]] $(\Pi \dashv Disc \dashv \Gamma \dashv coDisc)$ with $Disc, coDisc \colon \mathbf{S}\hookrightarrow \mathbf{H}$ [[full and faithful functor|full and faithful]] and $\Pi$ preserving [[finite products]]. The top [[adjoint triple]] here induces a canonical [[natural transformation]]

$$
  ptp \;\colon\; \Gamma \longrightarrow \Pi
$$

which deserves to be called the _[points-to-pieces transformation](cohesive+topos#CanonicalComparison)_. 

Consider the condition that $ptp$ is on every object $X$ of $\mathbf{H}$ an [[epimorphism]]. In terms of the geometric interpretation of [[cohesion]] this means that "all pieces of $X$ have at least one point". (See at _[cohesive topos -- Pieces have points](cohesive+topos#PiecesHavePoints)_) 
This statement is what in [Lawvere 07, def. 2 c)](#Lawvere07) is also referred to as **Nullstellensatz**. More comments on this are in ([Lawvere 11](#Lawvere11)). (In ([Johnstone 11](#Johnstone11)) this condition is called "punctual local connectedness".)

For a detailed analysis of how this general abstract concept indeed captures the traditional meaning of _Nullstellensatz_, see ([Lawvere 15](#Lawvere15), [Menni](#Menni)), also ([Tholen](#Tholen)).

## References

### Traditional

* Wikipedia, _[Hilbert's Nullstellensatz](http://en.wikipedia.org/wiki/Hilbert's_Nullstellensatz)_

### The model theoretic perspective

* [[Marta Bunge|M. Bunge]], _On the transfer of an abstract Nullstellensatz_ , Comm. Alg. **10** (1982) pp.1891-1906.

* W. A. MacCaull, _Hilbert's Nullstellensatz revisited_ , JPAA **54** (1988) pp.289-297.

* V. Weispfenning, _Nullstellens&#228;tze - a model theoretic framework_ , Z. Math. Logik Grundl. Math. **23** (1977) pp. 539-545. 

### In terms of cohesion

Discussion of the Nullstellensatz in terms of [[cohesion]]:

* {#Lawvere07} [[William Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3 (2007) pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* {#Lawvere11} [[William Lawvere]], _[MO comment on the general abstract Nullstellensatz](http://mathoverflow.net/a/52894/381)_ (2011)

* {#Lawvere15} [[F. William Lawvere]], _Birkhoff's Theorem from a geometric
perspective: A simple example_, Categories and General Algebraic Structures with Applications, Vol. 4, No. 1 (2015) pp. 1&#8211;7. ([pdf](http://www.cgasa.ir/pdf_12425_5ddf468d82aad53ce2e8ee88dd3bf84d.html))
 
* {#Johnstone11} [[Peter Johnstone]], _Remarks on punctual local connectedness_, Theory and Applications of Categories, Vol. 25, 2011, No. 3, pp 51-63 ([TAC](http://tac.mta.ca/tac/volumes/25/3/25-03abs.html))

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004. (pp.206-224)

* {#Menni} Matias Menni, _The manifestation of Hilbert's Nullstellensatz in Lawvere's Axiomatic Cohesion_ ([pdf slides](http://www.mat.uc.pt/~workct/slides/Menni.pdf) [pdf abstract](http://www.mat.uc.pt/~workct/abstracts/Menni.pdf))

* {#Menni14a} [[Matías Menni|M. Menni]], _Sufficient Cohesion over Atomic Toposes_ , Cah.Top.G&#233;om.Diff.Cat. **LV** (2014). ([preprint](https://sites.google.com/site/matiasmenni/SufCohesion12.pdf?attredirects=0))

* {#Menni14b} [[Matías Menni|M. Menni]], _Continuous Cohesion over Sets_ , TAC **29** no.20 (2014) pp.542-568. ([pdf](http://www.tac.mta.ca/tac/volumes/29/20/29-20.pdf))

* {#Tholen} [[Walter Tholen]], _Nullstellen and Subdirect Representation_ ([pdf](http://www.math.yorku.ca/~tholen/nullstMarch2013bis.pdf))


[[!redirects Nullstellensätze]]

[[!redirects Hilbert's Nullstellensatz]]

[[!redirects nullstellensatz]]
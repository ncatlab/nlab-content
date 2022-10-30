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
If $k$ is an **uncountable** algebraically closed field, then for any proper ideal $I \subset k[X_1, \ldots, X_n]$ there is $(a_1, \ldots, a_n) \in k^n$ such that $f(a_1, \ldots, a_n) = 0$ for all $f \in I$. 
=-- 

+-- {: .proof} 
###### Proof 
By the [[axiom of choice]], $I$ is contained in a [[maximal ideal]] $M$. So it suffices to prove it in the case where $I = M$ is maximal, where we prove there is an isomorphism $\phi: k[X_1, \ldots, X_n]/M \cong k$. Then the composite 

$$k[X_1, \ldots, X_n] \stackrel{quot}{\twoheadrightarrow} k[X_1, \ldots, X_n]/M \stackrel{\phi}{\to} k$$ 

sends each $X_i$ to a value $a_i$, so we have an inclusion of maximal ideals 

$$(X_1 - a_1, \ldots, X_n - a_n) \subseteq M$$ 

which must be an equality. In that case $(a_1, \ldots, a_n)$ is the desired point. 

Since $k$ is algebraically closed, it suffices to prove that the extension field $F = k[X_1, \ldots, X_n]/M$ over $k$ is algebraic over $k$. Clearly $F$ as a [[vector space]] over $k$ has countable [[dimension]]. Supposing to the contrary there is an element $t \in F$ that is transcendental over $k$, we have a [[subquotient]] vector space of $F$, 

$$\frac{k(t)}{k[t]} \cong \bigoplus_{a \in k} \frac{k[\frac1{t - a}]}{k},$$ 

where the isomorphism is by partial fraction decomposition (ultimately by the [[Chinese remainder theorem]]), but the vector space on the right clearly has uncountable dimension because there are uncountably many $a \in k$, and this leads to a contradiction. 
=-- 

Now we reduce to the case where $k$ is uncountable by employing a [[model theory|model-theoretic]] argument: 

+-- {: .num_theorem #weak} 
###### Theorem 
**(Weak Nullstellensatz)** 
If $k$ is an algebraically closed field, then for any proper ideal $I \subset k[X_1, \ldots, X_n]$ there is $(a_1, \ldots, a_n) \in k^n$ such that $f(a_1, \ldots, a_n) = 0$ for all $f \in I$. 
=-- 

+-- {: .proof} 
###### Proof 
Let $U$ be a non-principal [[ultrafilter]] on $\mathbb{N}$, and let $K$ be the [[ultraproduct|ultrapower]] $k^\mathbb{N}/U$. By [[Łoś's ultraproduct theorem]], $K$ is an algebraically closed field. Also $K$ is uncountable (Lemma \ref{ultrapower} below). 

First we claim $K \otimes_k I$ is a proper ideal of $K \otimes_k k[X_1, \ldots, X_n] \cong K[X_1,\ldots, X_n]$. For suppose we have $1 = \sum_{i = 1}^s f_i p_i$ for $p_1, \ldots, p_s \in I$ and $f_i \in K[X_1, \ldots, X_n]$. Writing the $f_i$ as $K$-linear combinations of monomials $X^\alpha$, there are finitely many $q_1, \ldots, q_t \in I$, each of the form $X^\alpha p_i$, so as to enable us to write $1 = \sum_{i=1}^t a_i q_i$ for $a_i = [(a_{i, m})] \in K$ and $q_i \in I$. By &#321;o&#347;'s theorem, 

$$\{m \in \mathbb{N}: 1 = \sum_{i=1}^t a_{i, m} q_i\; in\; k[X_1, \ldots, X_n]\} \in U;$$ 

this set is nonempty, and so there is at least one $m$ rendering the equation true. This contradicts $1 \notin I$. 

By Lemma \ref{uncountable}, there is a point $(a_1, \ldots, a_n) \in K^n$ that belongs to $Var(I)$. By [[noetherian ring|Hilbert's basis theorem]], $I \subset k[X_1, \ldots, X_n]$ is generated by finitely many polynomials $p_1, \ldots, p_s$, so $Var(I) \subseteq K^n$ is defined by finitely many formulas $p_1(X) = 0, \ldots, p_s(X) = 0$ and thus by &#321;o&#347;'s theorem again, 

$$\{m \in \mathbb{N}: p_i(a_{1, m}, a_{2, m}, \ldots, a_{n, m}) = 0\; for\; i = 1, \ldots, s\}$$ 

belongs to $U$, and so this set is nonempty and therefore there is a point $(a_{1, m}, \ldots, a_{n, m}) \in k^n$ that belongs to $Var(I)$. 
=-- 

To prove $K$ uncountable, we use the fact that an algebraically closed field is at least infinite. Then the missing piece is supplied by the following result. 

+-- {: .num_lemma #ultrapower} 
###### Lemma 
If $X$ is infinite and $U$ is a non-principal ultrafilter on $\mathbb{N}$, then the ultrapower $X^\mathbb{N}/U$ has cardinality at least $2^{\aleph_0}$. 
=-- 

+-- {: .proof} 
###### Proof 
For $j \in \mathbb{N}$, put $[j] = \{i \in \mathbb{N}: i \lt j\}$. For a set $X$, let $X^\ast = \sum_{j \geq 0} X^{[j]}$ be the free monoid on $X$. If $X$ is infinite, then there is a mono $i: X^\ast \to X$, which restricts to an mono $i_j: X^{[j]} \to X$. For any $h: \mathbb{N} \to X$, let $h|_{[j]}$ denote the composite $[j] \hookrightarrow \mathbb{N} \stackrel{h}{\to} X$, and define $h': \mathbb{N} \to X$ by $h'(j) = i_j(h|_{[j]})$. Let $[h']_U$ denote the value of $h'$ under the quotient map $X^\mathbb{N} \to X^\mathbb{N}/U$. 

Claim: The map $X^\mathbb{N} \to X^\mathbb{N}/U$ that takes $h$ to $[h']_U$ is injective. For, if $g, h: \mathbb{N} \to X$ are distinct, then they differ at some $i \in \mathbb{N}$. Then $g|_{[j]} \neq h|_{[j]}$ whenever $i \lt j$, which in turn implies $i_j(g|_{[j]}) \neq i_j(h|_{[j]})$ i.e. $g'(j) \neq h'(j)$ for all $j$ such that $j \gt i$. (That is, "for almost all $j$", belonging to a cofinite set that belongs to $U$.) Thus $[g']_U \neq [h']_U$, which establishes the claim. The lemma follows immediately from the claim. 
=-- 


### Rabinowitsch's trick 

Rabinowitsch, who later renamed himself Rainich (see the story [here](http://mathoverflow.net/a/45195/2926)), is the originator of a clever trick that allows one to deduce the Strong Nullstellensatz from the Weak Nullstellensatz. 

Let $k$ be algebraically closed and let $I \subseteq k[x_1, \ldots, x_n]$ be an ideal. To show that $Ideal(Var(I)) = \sqrt{I}$, suppose that $f \in k[x_1, \ldots, x_n]$ vanishes at any point where all of a given set of polynomials $f_1, \ldots, f_s \in k[x_1, \ldots, x_n]$ vanish. It suffices to show that for some $r$ we have that $f^r$ belongs to the ideal generated by the $f_i$. 

Introduce a fresh variable $x_0$, and observe that there is no point $(a_0, a_1, \ldots, a_n) \in k^{n+1}$ where the polynomials $1 - x_0 f, f_1, \ldots, f_s$ simultaneously vanish. By the Weak Nullstellensatz (Theorem \ref{weak}), these polynomials must generate the unit ideal, say 

$$1 = p_0(x)(1 - x_0 f) + p_1(x) f_1 + \ldots + p_s(x) f_s$$ 

where $x = (x_0, x_1, \ldots, x_n)$. There is a $k$-algebra map $k[x_0, x_1, \ldots, x_n] \to k(x_1, \ldots, x_n)$ sending $x_0 \mapsto 1/f$ and $x_i \mapsto x_i$ for $1 \leq i \leq n$, where the above identity yields 

$$1 = \sum_{i=1}^s p_i(1/f, x_1, \ldots, x_n) f_i$$ 

which, if $r$ is the highest degree of $x_0$ appearing in a $p_i$, may be rewritten in the form $f^r = \sum_{i=1}^s g_i f_i$ in $k[x_1, \ldots, x_n]$ by clearing denominators. 

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

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--

# Finite objects
* table of contents
{: toc}

## Idea

The notion of _[[finite object]]_ in a [[category]] -- notably in a [[topos]] -- is a generalisation of the notion of [[finite set]] in [[Set|the category of sets]].

As there are already at least five distinct notions of [[finite set]] in [[constructive mathematics]], so there must be at least five distinct notions of finite object internal to a [[topos]].  Additionally, the definitions may also be interpreted in an 'external' sense, giving even further notions.  Only some are mentioned below.

Also beware that in [[category theory]] the term 'finite object' is also used in a much more general sense to mean a _[[compact object]]_. Similar finiteness meaning may also be attributed to [[dualizable objects]] in [[monoidal categories]] and to [[perfect complexes]] (of [[abelian sheaves]]) in [[geometry]].



## Definitions
 {#Definitions}

Consider an ambient [[topos]] $\mathcal{T}$. 
Assume that $\mathcal{T}$ is equipped with a [[natural numbers object]] $N$. Write $N_{\lt} \hookrightarrow N\times N$ is its strict order relation.  


### External version   
 {#ExternalDefinition}
   
A "finite set" in $\mathcal{T}$ in the strictest sense is usually called a **finite cardinal**.  This is an [[object]] $[n] \in \mathcal{C}$ which is the [[pullback]] of $N_{\lt}\to N$ along some [[global element]] $n:1\to N$.  

   We can then consider [[subobjects]], [[quotient objects]], and [[subquotient objects]] of finite cardinals to obtain external versions of subfinite, finitely indexed, and subfinitely indexed sets.


### Internal version
 {#InternalDefinition}

 The _internal_ version of a "finite set" is an object $X$ such that "$X$ is a finite cardinal" is true in the [[internal logic]].  This is equivalent to the following

+-- {: .num_defn #KFinite}
###### Definition


An object $X \in \mathcal{T}$ is _locally_ isomorphic to a finite cardinal, if there is an [[epimorphism]] $U\to 1$ and a [[generalized element]] $n:U\to N$ such that $U\times X \cong n^*(N_\lt)$ over $U$.  Equivalently, there is a $U\to 1$ such that $U\times X$ is a finite cardinal in the 
[[slice topos]] $\mathcal{T}/U$.

An  **internally finitely indexed object** is an object $X$ is which is locally a [[quotient]] of a finite cardinal, hence such that there is an [[epimorphism]] $U \to *$, a finite cardinal in the slice topos $n \in \mathcal{T}_{/U}$ and an epimorphism $n \to U \times X$.

=--

An "internally finitely indexed" object is generally called a **Kuratowski-finite object**  or **$K$-finite object** for short, and an "internally subfinitely indexed" one is called a **$\tilde{K}$-finite object**.  

There is a more general definition of K-finite objects that does not need to assume the presence of a [[natural number object]]. See ([Johnstone, theorem D5.4.13](#Johnstone)).

Since it is still provable in the [[internal logic]] that any decidable finitely indexed set is finite, the "internally finite" objects (those that are locally isomorphic to a finite cardinal, as above) can be characterized as the __decidable $K$-finite objects__.


## Properties

### Closure of finite objects

The following lists closure properties of K-finite objects, def. \ref{KFinite}.

+-- {: .num_prop}
###### Proposition

1. The [[initial object]] and the [[terminal object]] are K-finite.

1. The [[image]] of a K-finite object under an [[epimorphism]] is K-finite.

1. The [[union]] of two K-finite [[subobjects]] is K-finite.

1. A [[coproduct]] is K-finite precisely if both summands are.

1. A [[subterminal object]] is K-finite precisely if it is a [[complemented subobject]].

1. A [[product]] of two K-finite objects is K-finite.

=--

This appears in ([Johnstone](#Johnstone)) as lemma D5.4.4, corollary D5.4.5, pro. 5.4.8.


### Subcategories of finite objects

The [[full subcategory]] of finite cardinals in any [[topos]] is again a topos, and it is [[Boolean topos|Boolean]].  Its [[subobject classifier]] is $2=1\sqcup 1$, which in the ambient topos is the classifier only of [[decidable object|decidable]] subobjects.  This means that [[classical logic|classically]] valid arguments, including all of finitary combinatorics, can generally be applied easily to finite cardinals, as long as we always interpret "subset" to mean "decidable subset."

+-- {: .num_theorem}
###### Theorem

The [[full subcategory]] $\mathcal{T}_{dKf} \hookrightarrow \mathcal{T}$ of decidable $K$-finite objects in a topos $\mathcal{T}$ is a [[Boolean topos]] whose subobject classifier is $2$.

The category of $K$-finite objects is a topos if and only if every $K$-finite object is decidable, and the category of $\tilde{K}$-finite objects is a topos if (but not only if) the subobject classifier is $K$-finite.

=--

The first statement appears as ([Johnstone, theorem 5.4.18](#Johnstone)).

+-- {: .num_remark}
###### Remark


The full subcategory $\mathcal{T}_{dKf} \hookrightarrow \mathcal{T}$ can be regarded as the "[[stack]] completion" of the topos of finite cardinals.  

=--


### Relation to slice toposes

+-- {: .num_prop}
###### Proposition

An object $X \in \mathcal{T}$ is K-finite precisely if the [[étale geometric morphism]]

$$
  \mathcal{T}_{/X} \to \mathcal{T}
$$

out of the [[slice topos]] is a [[proper geometric morphism]].

=--

([Moerdijk-Vermeulen, examples III 1.4](#MoerdijkVermeulen))


## Examples

* In any [[Boolean topos]], all four internal notions coincide.  In a [[well-pointed topos]], each internal notion coincides with its external notion.  Therefore, in a well-pointed Boolean topos, including the topos [[Set]] as usually conceived, all notions of finiteness coincide.

* In a [[presheaf]] topos $[C^{op},Set]$, the finite cardinals are the finite-set-valued functors which are constant on each connected component.  In particular, if $C$ is a [[group]], then the topos of finite cardinals is equivalent to [[FinSet]].

* Likewise, in the [[Grothendieck topos]] $Sh(X)$ of [[sheaf|sheaves]] on a space $X$, the finite cardinals are the locally constant functions $X\to N$.  So if $X$ is connected, the topos of finite cardinals in $Sh(X)$ is also equivalent to $FinSet$.

* Examples of such are [[tiny object]]s and [[infinitesimal object]]s in sheaf toposes.

* By contrast, the $K$-finite objects in $[C^{op},Set]$ are the finite-set-valued functors each of whose transition functions is surjective, and the _decidable_ K-finite objects are the finite-set-valued functors each of whose transition functions is bijective.

* In particular, if $C$ is a groupoid, the topos of decidable $K$-finite objects is equivalent to $[C^{op},FinSet]$.  Since the topos of presheaves on a groupoid is Boolean, this gives an example of a Boolean topos in which the finite cardinals ("externally finite objects") and the (decidable) $K$-finite objects ("internally finite objects") fail to coincide.

* In the [[category of sheaves]] $Sh(X)$ over a [[topological space]], the decidable K-finite objects are those that are "locally finite;" i.e. there is an [[open cover]] of $X$ such that over each open in the cover, the sheaf is a [[locally constant function]] to $N$.  These are essentially the same as [[covering space|covering spaces]] of $X$ with finite fibres.

## Related concepts

* [[finite set]], [[hereditarily finite set]]

* [[finite category]], [[finite limit]]

* [[finite graph]]

* [[decidable object]], [[theory of objects]]

* [[finite type]]

* [[finite homotopy type]], [[finite CW-complex]], [[finite spectrum]]

* [[π-finite homotopy type]]

* [[finite (infinity,1)-category]], [[finite (infinity,1)-limit]]

[[!include finite objects -- table]]

## References

In

* [[Peter Johnstone]], _[[Sketches of an elephant]]_
 {#Johnstone}

finite cardinal objects are discussed in section D5.2, Kuratowski finite objects in section D5.4

See also

* O. Acu&#241;a-Ortega, [[Fred Linton]], _Finiteness and decidability: I_ , Springer Lecture Notes in Mathematics, (1979), Volume **753**, pp.80-100, (DOI: 10.1007/BFb0061813)

* [[Peter Johnstone]], [[Fred Linton]], _Finiteness and decidability: II_ , Cambridge Philosophical Society Mathematical Proceedings of the Cambridge Philosophical Society (1978).

* B. P. Chisala, M.-M. Mawanda, _Counting Measure for Kuratowski Finite Parts and Decidability_ , Cah.Top.G&#233;om.Diff.Cat. **XXXII** 4 (1991) pp.345-353. ([pdf](archive.numdam.org/article/CTGDC_1991__32_4_345_0.pdf))

* S. J. Henry, _Classifying Topoi and Preservation of Higher Order Logic by Geometric Morphisms_ , PhD University of Michigan (2013). ([arxiv](http://arxiv.org/abs/1305.3254))

* C. Kuratowski, _Sur la notion d'ensemble fini_ , Fund. Math. **1** (1920) pp.129-131. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm1/fm1117.pdf))

* [[Ieke Moerdijk]], J. Vermeulen,  _Relative compactness conditions for toposes_ ([pdf](http://igitur-archive.library.uu.nl/math/2001-0702-142944/1039.pdf)) and _Proper maps of toposes_ , American Mathematical Society (2000)
  {#MoerdijkVermeulen}

* L. N. Stout, _Dedekind finiteness in topoi_ , JPAA **49** (1987) pp.219-225.

* T. Streicher, P. Freyd, F. Linton, P.Johnstone, W. Lawvere, _catlist discussion 'finiteness in toposes'_, January 1997. ([link](http://www.mta.ca/~cat-dist/catlist/1999/finite-topos))

* [[Alfred Tarski|A. Tarski]], _Sur les ensembles finis_ , Fund. Math. **3** (1924) pp.45-95. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm6/fm619.pdf))

* H. Volger, _Ultrafilters, ultrapowers and finiteness in a topos_ , JPAA **6** (1975) pp.345-356.

[[!redirects finite object]]
[[!redirects finite objects]]
[[!redirects finite]]
[[!redirects finiteness]]
[[!redirects B-finite object]]
[[!redirects B-finite objects]]
[[!redirects B-finite]]
[[!redirects B-finiteness]]
[[!redirects F-finite object]]
[[!redirects F-finite objects]]
[[!redirects F-finite]]
[[!redirects F-finiteness]]

[[!redirects subfinite object]]
[[!redirects subfinite objects]]
[[!redirects subfinite]]
[[!redirects subfiniteness]]
[[!redirects B-tilde-finite object]]
[[!redirects B-tilde-finite objects]]
[[!redirects B-tilde-finite]]
[[!redirects B-tilde-finiteness]]
[[!redirects F-tilde-finite object]]
[[!redirects F-tilde-finite objects]]
[[!redirects F-tilde-finite]]
[[!redirects F-tilde-finiteness]]

[[!redirects finitely indexed object]]
[[!redirects finitely-indexed object]]
[[!redirects finitely indexed objects]]
[[!redirects finitely-indexed objects]]
[[!redirects finitely indexed]]
[[!redirects finitely-indexed]]
[[!redirects Kuratowski-finite object]]
[[!redirects Kuratowski finite object]]
[[!redirects Kuratowski-finite objects]]
[[!redirects Kuratowski finite objects]]
[[!redirects Kuratowski-finite]]
[[!redirects Kuratowski finite]]
[[!redirects Kuratowski finiteness]]
[[!redirects Kuratowski-finiteness]]
[[!redirects K-finite object]]
[[!redirects K-finite objects]]
[[!redirects K-finite]]
[[!redirects K-finiteness]]

[[!redirects subfinitely indexed object]]
[[!redirects subfinitely-indexed object]]
[[!redirects subfinitely indexed objects]]
[[!redirects subfinitely-indexed objects]]
[[!redirects subfinitely indexed]]
[[!redirects subfinitely-indexed]]
[[!redirects Kuratowski-subfinite object]]
[[!redirects Kuratowski subfinite object]]
[[!redirects Kuratowski-subfinite objects]]
[[!redirects Kuratowski subfinite objects]]
[[!redirects Kuratowski-subfinite]]
[[!redirects Kuratowski subfinite]]
[[!redirects Kuratowski subfiniteness]]
[[!redirects Kuratowski-subfiniteness]]
[[!redirects K-tilde-finite object]]
[[!redirects K-tilde-finite objects]]
[[!redirects K-tilde-finite]]
[[!redirects K-tilde-finiteness]]

[[!redirects Dedekind-finite object]]
[[!redirects Dedekind finite object]]
[[!redirects Dedekind-finite objects]]
[[!redirects Dedekind finite objects]]
[[!redirects Dedekind-finite]]
[[!redirects Dedekind finite]]
[[!redirects Dedekind finiteness]]
[[!redirects Dedekind-finiteness]]
[[!redirects D-finite object]]
[[!redirects D-finite objects]]
[[!redirects D-finite]]
[[!redirects D-finiteness]]

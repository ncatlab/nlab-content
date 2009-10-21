A _regular category_ is a [[finitely complete category]] which admits a good notion of [[image]] factorization. A primary _raison d'etre_ behind regular categories $C$ is to have a decently behaved _calculus of [[relation]]s_ in $C$.  Regular categories are also the natural setting for [[internal logic|regular logic]].

## Definition

A category $C$ is **regular** if 

* It is finitely complete; 

* The [[kernel pair]] $p_1, p_2: e \,\rightrightarrows\, d$ of any $f: d \to c$ admits a [[coequalizer]];  and

* The pullback of a regular epi along any map is a regular epi.

Here the "kernel pair" is the parallel pair of projection maps coming out of a pullback $e$ of the diagram 

$$d \stackrel{f}{\to} c \stackrel{f}{\leftarrow} d$$

The kernel pair is always an [[congruence]] on $d$ in $C$; informally, $\ker(f)$ is the subobject of $d \times d$ consisting of pairs of elements which have the same value under $f$ (sometimes called the 'kernel' of a function in $\Set$). The coequalizer above is supposed to be the "object of equivalence classes" of $\ker(f)$ as an internal [[equivalence relation]].

A map which is the coequalizer of a parallel pair of morphisms is called a _[[regular epimorphism]]_. In fact, in any category satisfying the first two conditions above, every coequalizer is the coequalizer of its kernel pair. (See for instance Lemma 5.6.6 in _[[Practical Foundations]]_.)

The last condition may equivalently be stated in the form "coequalizers of kernel pairs are stable under pullback". However, it is not generally true in a regular category that the pullback of a general coequalizer diagram 

$$e \stackrel{\to}{\to} d \to c$$ 

along a morphism $c' \to c$ is again a coequalizer diagram. 

To form the image factorization of a map $f: d \to c$, let $q: d \to k$ be the coequalizer of the kernel pair of $f$. Since $f$ coequalizes its kernel pair, there is a unique map $i: k \to c$ such that $f = i q$. It may be shown from the regular category axioms that $i$ is monic and in fact represents the [[image]] of $f$, i.e., the smallest subobject through which $f$ factors.  Moreover, the classes of regular epis and of (all) monomorphisms form a [[orthogonal factorization system|factorization system]].

In fact, a regular category can alternately be defined as a finitely complete category with pullback-stable [[image]] factorizations.  See [[familial regularity and exactness]] for a generalization of this approach to include [[coherent category|coherent]] categories as well.


## Examples

* [[Set]] is a regular category. In fact, any [[topos]] is regular. More generally, a locally cartesian closed category with coequalizers is regular, and so any quasitopos is regular. 

* The category of models of any finitary algebraic theory (i.e., [[Lawvere theory]]) $T$ is regular. This applies in particular to the category [[Ab]] of abelian groups. 

* Any [[abelian category]] is regular. 

* If $C$ is regular, then so is $C^D$ for any category $D$. 

Examples of categories which are _not_ regular include [[Cat]], [[Pos]], and [[Top]]. 


## Remarks

1. As exactness properties go, the ones possessed by general regular categories are fairly moderate; the main condition is of course stability of regular epis under pullback. In the first place, the focus is just on certain coequalizers; finite coproducts aren't even mentioned. Some of that imbalance is redressed by the notion of l[[extensive category]], where coproducts are also stable under pullback (and are also disjoint). 

Further desirable exactness properties can be phrased in the language of [[Galois connection]]s. For each object $d$, consider the following relation $coeq$ between the class of parallel pairs $f, g: e \stackrel{\to}{\to} d$) and maps $h: d \to c$: 

$$\langle (f, g); h \rangle \in coeq \qquad iff \qquad h f = h g$$

[to be continued...]

An application of the regularity condition is found in the paper
*Tensor envelopes of regular categories, by F. Knop.   [arXiv:math/0610552v2](http://arxiv.org/abs/math/0610552)

Knop's condition for regularity is slightly different from that presented here; he works with categories that when augmented by an absolutely initial object are regular in the terminology here.  In the paper, Knop generalizes a construction of Deligne by showing how to construct a symmetric pseudo-abelian [[tensor category]] out of a regular category through the calculus of relations.
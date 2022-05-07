
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of coring is a generalization of a $k$-[[coalgebra]]. While for
a coalgebra $k$ must be a __commutative__ ring (often a [[field]]), a coring is defined
over a general noncommutative ring $k$ or even an associative algebra $A$. 

Whereas a coalgebra structure is defined on a $k$-module (if $k$ is a field, it is a [[vector space]]) -- which may be regarded as a central $k$-[[bimodule]] -- a coring structure is defined on a general bimodule over a general [[ring]].


## Definition

An __$A$-coring__ is a [[comonoid]] in the [[monoidal category]] of central [[bimodule]]s over a fixed (typically noncommutative) unital [[ring]] $A$. 

This generalizes the notion of $A$-[[coalgebra]]s which are defined only if $A$ is commutative and where the bimodules in question are [[central bimodule|central]]. 

## Base ring extension

More generally, fix a ground commutative ring $R$. Corings will be now over $R$-algebras. So a coring will mean a pair $(A,C)$ where $A$ is an $R$-algebra and $C$ an $A$-coring.

Let $\alpha:A\to B$ be a morphism of rings and $C$ an $A$-coring. Then the $B$-$B$-bimodule $B\otimes_A C\otimes_A B$ has an induced structure of a $B$-coring
with comultiplication

$$
B\otimes_A C\otimes_A B \stackrel{B\otimes \Delta_C\otimes B}\longrightarrow
 B\otimes_A C\otimes_A C\otimes_A B
\stackrel{B\otimes C\otimes 1_B\otimes C\otimes B}\longrightarrow
B\otimes_A C\otimes_A B\otimes_A C\otimes_A B \cong
(B\otimes_A C\otimes_A B)\otimes_B (B \otimes_A C\otimes_A B)
$$
and the counit
$$
B\otimes_A C\otimes_A B \stackrel{B\otimes\epsilon_C\otimes B}\longrightarrow B\otimes_A A\otimes_A B \stackrel{B\otimes\phi\otimes B}\longrightarrow 
B\otimes_A B\otimes_A B \stackrel{mult}\longrightarrow B
$$

## Morphisms of corings over different bases

A morphism $(A,C)\to (B,D)$ is a pair $(\alpha,\gamma)$ where

* $\alpha : A\to B$ is an $R$-algebra morphism; by restriction this makes $D$ an $A$-$A$-bimodule by restriction. Denote also by $p:D\otimes_A D\to D\otimes_B D$ the canonical projection of bimodules induced by $\alpha$.
* $\gamma : C\to D$ is a map of $A$-$A$-bimodules
* $\gamma$ commutes with counit $\alpha \circ \epsilon_C = \epsilon_D\circ \gamma$
* $p\circ (\gamma\otimes_A\gamma)\circ \Delta_C = \Delta_D\circ \gamma$

The last two conditions can be said that the base ring extension coring $B\otimes_A C\otimes_A B$ of $C$ maps to $D$ (via map induced by $\gamma$) as a morphism of $B$-corings. 

## Examples

### Sweedler corings

The classical example of a coring is the [[Sweedler coring]] corresponding to an extension $R\hookrightarrow S$ of unital rings. The category of [[descent]] data for this extension is equivalent to the category of [[comodule]]s over the Sweedler coring. 

Corings are in general useful for the treatment of [[descent in noncommutative algebraic geometry]].

### Matrix corings

Another major class of examples are the so-called [[matrix coring]]s.


## References

The notion of an $A$-coring is introduced by M. Sweedler and recently lived through a renaissance in works of [[T. Brzeziński]], R. Wisbauer, [[G. Böhm]], L. Kaoutit, G&#243;mez-Torrecillas, S. Caenepeel, J. Y. Abuhlail, J. Vercruysse and others, including the creation of Galois theory for corings. Some prefer to speak about $A$-[[cocategory|cocategories]].

There is already a monograph:

* [[T. Brzeziński]], R. Wisbauer, _Corings and comodules_, London Math. Soc. Lec. Note Series __309__, Cambridge 2003.

Special topics:

* [[T. Brzeziński]], _Descent cohomology and corings_,  Comm. Algebra 36:1894-1900, 2008, [arxiv:math.RA/0601491](http://arxiv.org/abs/math.RA/0601491)

* L. El Kaoutit, J. Gomez-Torrecillas, _On the set of grouplikes of a coring_, [arxiv/0901.4291](http://arxiv.org/abs/0901.4291)

* [[T. Brzeziński]], _Flat connections and (co)modules_, [in:] New Techniques in Hopf Algebras and Graded Ring Theory, S Caenepeel and F Van Oystaeyen (eds), Universa Press, Wetteren, 2007 pp. 35-52   [arxiv:math.QA/0608170](http://arxiv.org/abs/math.QA/0608170)

* [[T. Brzeziński]], _The structure of corings. Induction functors, Maschke-type theorem, and Frobenius and Galois-type properties_, Algebras and Representation Theory __5__ (2002) 389-410, [math.QA/0002105](http://arxiv.org/abs/math.QA/0002105)

* Lars Kadison, _Depth two and Galois coring_, [math.RA/0408155](http://arxiv.org/abs/math.RA/0408155)

* [[George M. Bergman]], Adam O. Hausknecht, _Cogroups and co-rings in categories of associative rings_, A.M.S. Math. Surveys and Monographs __45__, ix+388 pp., 1996; ISBN 0-8218-0495-2. [MR 97k:16001](http://www.ams.org/mathscinet-getitem?mr=97k:16001) [errata and updates](http://math.berkeley.edu/~gbergman/papers/updates/coalg.html).

* [[T. Brzeziński]], L. Kadison, [[R. Wisbauer]], _On coseparable and biseparable corings_,  Hopf algebras in noncommutative geometry and physics,  71--87, Lecture Notes in Pure and Appl. Math., 239, Dekker, New York, 2005. 
* T. Brzeziński, L. El Kaoutit, J. Gómez-Torrecillas, _The bicategories of corings_, J. Pure & Appl. Alg. __205__:3 (2006) 510-541 [doi:10.1016/j.jpaa.2005.07.013](https://doi.org/10.1016/j.jpaa.2005.07.013) [math.RA/0408042](https://arxiv.org/abs/math/0408042)

There is a generalization of corings:

* Jawad Y. Abuhlail, _Semicorings and semicomodules_, [arxiv/1303.3924](http://arxiv.org/abs/1303.3924)

category: algebra
[[!redirects corings]]
[[!redirects semicoring]]
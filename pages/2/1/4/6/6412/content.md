
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


# $p$-adic numbers
* table of contents
{: toc}

## Idea

For $p$ any [[prime number]], the _$p$-adic numbers_ $\mathbb{Q}_p$ (or _$p$-adic rational numbers_, for emphasis) are a [[field]] that [[complete field|completes]] the field of [[rational numbers]]. As such they are analogous to [[real numbers]]. A crucial difference is that the reals form an [[archimedean field]], while the $p$-adic numbers form a [[non-archimedean field]].

$p$-Adic numbers play a role in non-archimedean [[analytic geometry]] that is analogous to the role of the [[real numbers]]/[[Cartesian spaces]] in ordinary [[differential geometry]]. 

Moreover, as such they serve as an approximation technique in [[arithmetic geometry]] over [[prime fields]] $\mathbb{F}_p$ (see e.g. [Lubicz](#Lubicz)).

There have long been speculations (see the references [below](#ReferencesApplications)) that this must mean that $p$-adic numbers also play a central role in the description of [[physics]], see _[[p-adic physics]]_.

## Definition

We first recall the definition and construction of the [[p-adic integers]]

* [Recollection of the p-adic integers](#RecollectionOfPAdicIntegers)

and then consider

* [The p-adic numbers proper](#PAdicNumbersProper)

### Recollection of the $p$-adic integers
 {#RecollectionOfPAdicIntegers}


Let $\mathbf{Z}$ be the [[ring]] of [[integers]] and for every $q\neq 0$, $q\mathbf{Z}$ its ideal consisting of all integer multiples of $q$, and $\mathbf{Z}/q\mathbf{Z}$ the corresponding [[quotient]], the ring of residues mod $q$.

Let now $p\in \mathbf{Z}_+$ be a [[prime number]]. Then for any two positive integers $n\geq m$ there is an inclusion $p^m \mathbf{Z}\subset p^n\mathbf{Z}$ which induces the canonical homomorphism of quotients $\phi_{n,m}:\mathbf{Z}/p^n\mathbf{Z}\to \mathbf{Z}/p^m\mathbf{Z}$. These homomorphism for all pairs $n\geq m$ form a family closed under composition, and in fact a category, which is in fact a poset, and moreover a directed system of (commutative unital) rings. The __ring of [[p-adic integers]]__ $\mathbf{Z}_p$ is the (inverse) [[limit]] of this directed system (inside the category of rings).

Regarding that the rings in the system are finite, it is clear that the underlying set of $\mathbf{Z}_p$ has a natural topology as a [[profinite space|profinite]] ([[Stone space|Stone]]) space and it is in particular a [[compact space|compact]] [[Hausdorff topological space|Hausdorff topological ring]]. More concretely, $\mathbf{Z}_p$ is the closed (hence compact) subspace of the cartesian product $\prod_{n} \mathbf{Z}/p^n\mathbf{Z}$ of discrete topological spaces $\mathbf{Z}/p^n\mathbf{Z}$ (which is by the [[Tihonov theorem]] compact Hausdorff) consisting of [[thread]]s, i.e. sequences of the form $x = (...,x_n,...,x_2,x_1)$ with $x_n\in p^n\mathbf{Z}$ and satisfying $\phi_{n,m}(x_n) = x_m$.

The kernel of the projection $pr_n: \mathbf{Z}_p\to\mathbf{Z}/p^n\mathbf{Z}$, $x\mapsto x_n$ to the $n$-th component (which is the corresponding projection of the limiting cone) is $p^n\mathbf{Z}_p\subset\mathbf{Z}_p$, i.e. the sequence

$$
0 \longrightarrow \mathbf{Z}_p\stackrel{p^n}\longrightarrow \mathbf{Z}_p\longrightarrow \mathbf{Z}/p^n\mathbf{Z} \longrightarrow 0
$$

is an [[exact sequence]] of [[abelian groups]], hence also $\mathbf{Z}_p/p^n\mathbf{Z}_p\cong \mathbf{Z}/p^n\mathbf{Z}$.

An element $u$ in $\mathbf{Z}_p$ is invertible (and called a $p$-adic unit) iff $u$ is not divisible by $p$. 

Let $U\subset\mathbf{Z}_p$ be the group of all invertible elements in $\mathbf{Z}_p$. Then _every element $x\in \mathbf{Z}_p$ can be uniquely written as $s= u p^n$ with $n\geq 0$ and $u\in U$_. The correspondence $x\mapsto n$ defines a [[discrete valuation]] $v_p:\mathbf{Z}_p\to \mathbf{Z}\cup\{\infty\}$ called the  [[p-adic valuation]] and $n$ is said to be the $p$-adic valuation of $x$. Of course, $v_p(0)=\infty$ as required by the axioms of valuation. The [[norm]] induced by the valuation is (up to equivalence) given by ${|x|}_p = p^{-v_p(x)}$, and this in turn induces a metric 

$$
d(x,y) = {|x-y|}_p,
$$

making the ring $\mathbf{Z}_p$ a [[complete metric space]] and in fact a completion of $\mathbf{Z}$, in that $d$ is a complete [[metric]], and $\mathbf{Z}$ is dense in it. 

Concretely, a $p$-adic integer $x$ may be written as a base-$p$ expansion 

$$x = \sum_{n \geq 0} a_n p^n$$ 

with $a_n \in \{0, 1, \ldots, p-1\}$. Addition and multiplication are performed with [[carrying]] as in ordinary base-$p$ arithmetic, carried infinitely far to the left if $x$ is written as $\ldots a_n a_{n-1} \ldots a_1 a_0$. 

#### As an endomorphism ring 

Algebraically, the ring of $p$-adic integers is isomorphic to the endomorphism ring $\hom(\mathbf{Z}(p^\infty), \mathbf{Z}(p^\infty))$ where $\mathbf{Z}(p^\infty)$ is the [[Pruefer group|Prüfer group]] $\mathbf{Z}(p^\infty) \coloneqq \mathbb{Z}[1/p]/\mathbb{Z}$. In particular, $\mathbf{Z}(p^\infty)$ is tautologically a $\mathbf{Z}_p$-module. 

Relatedly, the additive group of $p$-adic integers is [[Pontrjagin duality|Pontrjagin dual]] to $\mathbf{Z}(p^\infty)$. Observe that $\mathbf{Z}(p^\infty)$ embeds in $S^1$ as the set of all [[root of unity|roots of unity]] of order $p^n$, and that every character $\chi: \mathbf{Z}(p^\infty) \to S^1$ factors through this embedding $\mathbf{Z}(p^\infty) \hookrightarrow S^1$. 

### The $p$-adic numbers proper
 {#PAdicNumbersProper}

The __field of $p$-adic numbers__ $\mathbf{Q}_p$ is the [[field of fractions]] of the [[p-adic integers]] $\mathbf{Z}_p$. The $p$-adic valuation $v_p$ extends to a discrete valuation, also denoted $v_p$ on $\mathbf{Q}_p$. Indeed, it is still true for all $x\in \mathbf{Q}_p$ that they can be uniquely written in the form $p^n u$ where $u\in U$ (the same group $U$ as before), but now one needs to allow $n\in \mathbf{Z}$. One defines the metric on $\mathbf{Q}_p$ by the same formula as for $\mathbf{Z}_p$. It appears that $\mathbf{Q}_p$ is a [[complete field]] (in particular locally compact Hausdorff) and that $\mathbf{Z}_p$ is an *open* subring. 

The distance $d$ satisfies the "ultrametric" inequality

$$
d(x,z) \leq sup\{d(x,y),d(y,z)\}
$$ 

Concretely, a $p$-adic number $x$ may be written as $\sum_{n \geq k} a_n p^n$, with only finitely many negative powers of $p$ occurring. If $k \lt 0$, the expansion is conventionally displayed as 

$$x = \ldots a_1 a_0.a_{-1} \ldots a_k$$ 

with finitely many terms to the "right" of the "decimal" point. Again such expressions are added and multiplied with carrying as in ordinary arithmetic. 

## Properties

### As a field completion

[[Ostrowski's theorem]] implies there are precisely two kinds of [[complete field|completions]] of the [[rational numbers]]: the [[real numbers]] and the $p$-adic numbers.


+-- {: .num_theorem}
###### Theorem
**([[Ostrowski's theorem]])**

Any non-trivial [[absolute value]] on the [[rational numbers]] is equivalent either to the standard real absolute value, or to the $p$-adic absolute value.

=-- 

### Topological disconnectedness and G-topology
 {#Disconnectedness}

While the $p$-adic numbers are complete in the [[p-adic norm]], that [[topology]] is exotic: $\mathbb{Q}_p$ is a [[Stone space]], hence in particular a [[totally disconnected topological space]].

For that reason the naive idea of formulating [[p-adic geometry]] in analogy to [[complex analytic geometry]] as modeled on domains in $\mathbb{Q}_p^n$, regarded with their [[subspace topology]], fails (for instance there would be no [[analytic continuation]]), as also all these domains are totally disconnected. 

Instead there is ([Tate 71](#Tate71)) a suitable [[Grothendieck topology]] on uch [[affinoid domains]] -- the _[[G-topology]]_ -- with respect to which there is a good theory of [[non-archimedean analytic geometry]] ("[[rigid analytic geometry]]") and hence in particular of [[p-adic geometry]]. Moreover, one may sensibly assign to an $p$-adic domain a [[topological space]] which _is_ well behaved (in particular locally connected and even locally contractible), this is the _[[analytic spectrum]]_ construction. The resulting topological spacs equipped with covers by [[affinoid domain]] under the [[analytic spectrum]] are called [[Berkovich spaces]].


### Pontryagin duality 

Earlier we observed that as an additive compact Hausdorff [[topological group]], the inverse limit $\mathbf{Z}_p = \lim_{\leftarrow n} \mathbb{Z}/(p^n)$ is [[Pontryagin duality|dual]] to the discrete [[Pruefer group|Prüfer group]] $\mathbf{Z}(p^\infty) \coloneqq \mathbb{Z}[1/p]/\mathbb{Z}$ that is isomorphic to a direct limit of finite cyclic groups $\lim_{\to n} \mathbb{Z}/(p^n)$. The canonical inclusion $\mathbb{Z}[1/p] \to \mathbf{Q}_p$ induces an isomorphism $\mathbf{Z}(p^\infty) \to \mathbf{Q}_p/\mathbf{Z}_p$, in fact an isomorphism of $\mathbf{Z}_p$-modules, so there is an exact sequence 

$$0 \to \mathbf{Z}_p \stackrel{i}{\hookrightarrow} \mathbf{Q}_p \stackrel{q}{\to} \mathbf{Z}(p^\infty) \to 0.$$ 

This exact sequence is Pontrjagin self-dual in the sense that the map $\mathbf{Q}_p \to \mathbf{Q}_p^\wedge$ induced from the pairing 

$$\mathbf{Q}_p \times \mathbf{Q}_p \stackrel{mult}{\to} \mathbf{Q}_p \stackrel{q}{\to} \mathbb{Z}[1/p]/\mathbb{Z} \hookrightarrow \mathbb{R}/\mathbb{Z}$$  

fits into an isomorphism of exact sequences 

$$\array{
0 & \to & \mathbf{Z}_p & \stackrel{i}{\to} & \mathbf{Q}_p & \stackrel{q}{\to} & \mathbf{Z}(p^\infty) & \to & 0 \\ 
 & & \downarrow & & \downarrow & & \downarrow & & \\ 
0 & \to & \mathbf{Z}(p^\infty)^\wedge & \stackrel{q^\wedge}{\to} & \mathbf{Q}_p^\wedge & \stackrel{i^\wedge}{\to} & \mathbf{Z}_p^\wedge & \to & 0
}$$ 

where the commutativity of the squares can be traced to the fact that $q$ is a $\mathbf{Z}_p$-module homomorphism, and where the vertical isomorphisms on left and right come from [[Pontrjagin duality]]. The middle arrow is then an isomorphism by the [[short five lemma]] for [[topological groups]], which holds by protomodularity of topological groups. 

This self-duality figures in Tate's thesis; for more, see [[ring of adeles]].

### Function field analogy

[[!include function field analogy -- table]] 

## Related concepts

* [[ring of adeles]] 

* [[carrying]]

* [[natural number]], [[integer]], [[rational number]], [[algebraic number]], [[Gaussian number]], [[irrational number]], [[real number]]



* [[p-adic integer]], [[p-adic complex number]]

* [[p-adic geometry]]

  * [[p-adic analytic space]], [[non-commutative analytic space]]

* [[p-adic homotopy]]

* [[p-adic cohomology]]

* [[p-adic physics]]

  * [[p-adic string theory]]

## References
 {#References}

The $p$-adic numbers had been introduced in 

* [[Kurt Hensel]], _&#220;ber eine neue Begr&#252;ndung der Theorie der algebraischen Zahlen_ Jahresbericht der Deutschen Mathematiker-Vereinigung 6 (3): 83&#8211;88. (1897)

A standard reference is

* [[Jean-Pierre Serre]], _A course in arithmetic_, Grad. Texts in Math. __7__, Springer (1973)

Review in the context of [[p-localization|p-local]] [[homotopy theory]] is in

* {#Sullivan70} [[Dennis Sullivan]], pp. 9 of _Localization, Periodicity and Galois Symmetry_ (The 1970 MIT notes) edited by [[Andrew Ranicki]], K-Monographs in Mathematics, Dordrecht: Springer ([pdf](http://www.maths.ed.ac.uk/~aar/surgery/gtop.pdf)) 


Review of the use of $p$-adic numbers in [[arithmetic geometry]] includes

* {#Lubicz} [[David Lubicz]], _An introduction to the algorithmic of $p$-adic numbers_ ([pdf](http://www.hyperelliptic.org/tanja/conf/summerschool08/slides/p-adics.pdf))

A formalization in [[homotopy type theory]] and there in [[Coq]] is discussed in

* &#193;lvaro Pelayo, [[Vladimir Voevodsky]], [[Michael Warren]], _A preliminary univalent formalization of the p-adic numbers_ ([arXiv:1302.1207](http://arxiv.org/abs/1302.1207))



$p$-adic [[differential equations]] are discussed in 

* [[Kiran Kedlaya]], _$p$-adic differential equations_ ([pdf](http://math.ucsd.edu/~kedlaya/18.787/compiled.pdf), [course notes](http://math.ucsd.edu/~kedlaya/18.787/))

* [[Gilles Cristol]], _Exposants $p$-adiques et solutions dans les couronnes_ ([pdf](http://www.math.jussieu.fr/~christol/exposants.pdf))

The development of [[rigid analytic geometry]] starts with

* {#Tate71} [[John Tate]], _Rigid analytic spaces_, Invent. Math. __12__:257&#8211;289, 1971.

[[p-adic homotopy theory]] is discussed in 

* [[Jacob Lurie]], _[[Rational and p-adic Homotopy Theory]]_

[[!redirects p-adic]]

[[!redirects p-adic number]]
[[!redirects p-adic numbers]]

[[!redirects adic number]]
[[!redirects adic numbers]]

[[!redirects p-adic number field]]
[[!redirects p-adic number fields]]
[[!redirects p-adic field]]
[[!redirects p-adic fields]]

[[!redirects p-adic valuation]]
[[!redirects p-adic valuations]]

[[!redirects p-adic norm]]
[[!redirects p-adic norms]]


[[!redirects p-adic rational number]]
[[!redirects p-adic rational numbers]]
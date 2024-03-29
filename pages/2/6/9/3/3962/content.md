
> This article concerns the notion of "local field" as it is commonly used in [[algebraic number theory]]. For another notion of "local field" in [[commutative algebra]], see [[local field (commutative algebra)]]. 

--- 

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

## Definition

A **local field** is a [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] (non-[[discrete space|discrete]]) [[topological field]]. 

Basic examples are the [[p-adic numbers]] $\mathbb{Q}_p$ and the field of [[Laurent series]] $\mathbb{F}_q((t))$ over a [[finite field]] $\mathbb{F}_q$. Local fields are opposite to _[[global fields]]_ in that where (under the [[function field analogy]]) the latter may be thought of as fields of [[rational functions]] on [[arithmetic curves]], local fields are like fields of functions on [[formal disks]] inside such curves. Accordingly the [[Langlands correspondence]] for [[global fields]] has a "localization" to the [[local Langlands correspondence]] for local fields.

Note that for a [[topological field]], the [[closed subspace|topological closure]] of $\{0\}$ is an [[ideal]], which must therefore be either $\{0\}$ or the whole field. It follows that either a topological field is [[separation axioms|T]]$_1$ (and therefore Hausdorff or T$_2$; see [[uniform space]]), or has the [[discrete and codiscrete topology|codiscrete topology]]. 

## Properties

A local field $K$ carries a [[valuation]] ${\|-\|}: K \to \mathbb{R}_{\geq 0}$ defined by 

$${\|a\|} = \frac{\mu(a X)}{\mu(X)}$$ 

where $\mu$ is any [[Haar measure]] defined on the underlying locally compact Hausdorff additive group of $K$, and $X$ is any set such that $0 \lt \mu(X) \lt \infty$. 

By analyzing the possibilities for the valuation, any local field is one of the following types: 

* [[characteristic|Characteristic zero]]. In this case local fields $F$ are [[complete space|completions]] of [[number fields]] with respect to [[metrics]] induced by [[valuations]]. The valuations may be 

  * [[archimedean field|Archimedean]]. Here for every $x \in F$, there exists $n \in \mathbb{N}$ such that ${\|n x\|} \gt 1$, where ${\| \cdot \|}$ is the valuation. The local fields in this case are isomorphic as topological fields to $\mathbb{R}$ or $\mathbb{C}$. 

  * [[nonarchimedean field|Nonarchimedean]]. Such valuations are [[discrete valuations]], and are the completions of discrete valuations induced by prime ideals $v$ of the ring of [[algebraic integers]] $\mathcal{O}_k$ in a number field $k$. The valuation on the [[number field]] is defined by ${\|x\|_v} = q^{-n}$ where $q$ is the cardinality of the [[finite field]] $\mathcal{O}_k/v$, and $n$ is the least integer such that $x \in v^n$. The completion is called the **$v$-adic completion** and is denoted $k_v$. 

* [[characteristic|Characteristic]] $p \gt 1$. In this case local fields are fields of [[Laurent series]] $\mathbb{F}_q((t))$ over a finite field $\mathbb{F}_q$ of cardinality $q = p^n$; here ${\|f(t)\|} = q^{-n}$ where $f(t) = a_n t^n + a_{n+1}t^{n+1} + \ldots$. The valuation is nonarchimedean. 

Local fields are technically useful in modern [[number theory]]; for example in formulating local-to-global principles, and in formulations of [[class field theory]] following Tate's thesis. Part of the technical convenience resides in the fact that one can effectively do [[Fourier analysis]] on them; as additive [[topological abelian group|topological groups]], they are self-dual locally compact abelian groups (in the sense of [[Pontrjagin dual|Pontryagin duality]]). 
 

## Relation to local rings (warning)

It is possible to construe "local field" in at least two other ways, to wit: 

* As meaning "[[field of fractions]] of an [[integral domain]] that is a [[local ring]]". 

* As meaning "field of fractions of an integral domain that arises as the completion of a local ring with respect to its canonical valuation". 

The first meaning is not too serious (and is seldom if ever considered seriously), since usually a field $F$ will not uniquely determine a local subring giving rise to it, nor does this meaning imply any tight connection to local topological conditions such as local compactness. Under this interpretation, $\mathbb{Q}$ would be a "local field", which is virtually unheard of. 

The second meaning has more content, because the Cauchy completeness (with respect to an $\mathfrak{m}$-topology, where $\mathfrak{m}$ is the maximal ideal of some local ring) determines the local ring via the topology: the complement of $x$ such that $x^{-n}$ converges to $0$. There is nontrivial intersection with the notion of local field as defined above, since the _nonarchimedean_ local fields as defined above are conspicuous examples of this second meaning. Observe however that 

* The archimedean local fields $\mathbb{R}$, $\mathbb{C}$ do _not_ arise this way; 

* Under the $m$-[[adic topology]], the completion of a local ring $R$ with maximal ideal $m$, i.e., the [[inverse limit]] of the [[diagram]] 
$$\ldots R/m^{n+1} \stackrel{proj}{\to} R/m^n \to \ldots \to R/m$$
is typically not compact (and its field of fractions is not locally compact). It is of course compact if each $R/m^n$ is finite with the discrete topology. 

In any case, the second meaning certainly occurs in the literature, as in the famous text _Corps Loceaux_ by Serre. For more on this, see [[local field (commutative algebra)]]. 

## Related concepts

* [[local Langlands correspondence]]

* [[higher local field]]

* [[global field]]

## References


* {#Cassels86} [[J. W. S. Cassels]], *Local Fields*, Cambridge University Press, 1986 (ISBN:9781139171885, [doi:10.1017/CBO9781139171885](https://doi.org/10.1017/CBO9781139171885)) 


See also:

* Wikipedia, _[Local field](http://en.wikipedia.org/wiki/Local_field)_

[[!redirects local field]]
[[!redirects local fields]]
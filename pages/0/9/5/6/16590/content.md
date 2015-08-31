
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Topologically complete spaces
* table of contents
{: toc}

## Idea

A [[topological space]] is topologically complete if and only if it is [[complete space|completely]] [[metrizable space|metrizable]].  However, the term 'topologically complete' may be applied to other [[spaces]] as well, and in this case it means that the [[underlying topological space]] is completely metrizable.

One can vary this by considering some other kind of underlying space (besides the underlying topological one) and other kinds of completability (besides complete metrizability).


## Definitions

Suppose $\mathcal{S}$ is some category of "spaces" with a notion of "[[completion|completeness]]", together with an [[underlying topology|underlying functor]] $U: \mathcal{S} \to Top$. In fact, let us take as a running example the case where $\mathcal{S} = Met$ with the usual meaning of completeness and the usual underlying functor to $Top$. Then one may say that a metric space $X$ is __topologically complete__[^1] if the underlying [[topological space]] $U X$ is completely [[metric space|metrizable]]; that is with the [[property]] of having some complete metric on its [[underlying set]] that is compatible with the underlying topology. 

More generally, one could say that a "space" (an object $X$ of $\mathcal{S}$) is *topologically* ($\mathcal{S}$-)complete if there is an $\mathcal{S}$-complete space $Y$ for which $U(Y) = U(X)$ (or if this is considered too "[[principle of equivalence|evil]]", then we could appeal to an isomorphism $U(Y) \cong U(X)$ instead, preferably under the assumption that $U$ is an [[isofibration]]). For instance, if $\mathcal{S}$ is the category of [[uniform spaces]], we could refer to a uniform space as topologically (uniformly) complete; this would be synonymous with (topologically) "completely [[uniform space|uniformizable]]", analogous to being completely metrizable; another synonym for this, still in the uniform space context, is *Dieudonn&#233;-complete*. 

+-- {: .num_remark} 
###### Remark 
According to Wikipedia, the term 'topologically complete' is sometimes used to mean "completely metrizable", other times it refers to Dieudonn&#233;-completeness.  Obviously this makes "topologically complete" a terribly confusing name, just asking for trouble, but it is traditional, and there are many results associated with it.
=-- 

[^1]: This terminology, despite its flaws, really does appear in the literature. See for instance [Arkhangel&#8242;skii 1977](#Ark1977). 

So in other words (again appealing to the running example), the [[groupoid]] of topologically complete spaces is (up to [[equivalence of categories|equivalence]]) the groupoid of completely metrizable topological spaces, or equivalently the category whose [[objects]] are complete metric spaces and whose [[morphisms]] are [[homeomorphisms]].  

All this can be generalized further. If $\mathcal{S}$ and $\mathcal{T}$ are two notions of space, with a notion of $\mathcal{S}$-completeness and a forgetful functor $U: \mathcal{S} \to \mathcal{T}$, then analogously we can refer to an object $X$ of $\mathcal{S}$ as being "$\mathcal{T}$-ly $\mathcal{S}$-complete". For example, there is a forgetful functor $U: Met \to Unif$, and then we can make sense of an utterance that a metric space is "uniformly completely metrizable", etc.


## References

A list of classical concepts of completeness in topology (including some not listed here) is at

*  A.V. Arkhangel&#8242;skii (1977).  _Complete space_.  Matematicheskaya entsiklopediya.  [Updated English version](https://www.encyclopediaofmath.org/index.php/Complete_space). 
   {#Ark1977}


[[!redirects topologically complete space]]
[[!redirects topologically complete spaces]]

[[!redirects Dieudonne complete space]]
[[!redirects Dieudonne complete spaces]]
[[!redirects Dieudonné complete space]]
[[!redirects Dieudonné complete spaces]]
[[!redirects Dieudonne-complete space]]
[[!redirects Dieudonne-complete spaces]]
[[!redirects Dieudonné-complete space]]
[[!redirects Dieudonné-complete spaces]]

[[!redirects complete topological space]]
[[!redirects complete topological spaces]]

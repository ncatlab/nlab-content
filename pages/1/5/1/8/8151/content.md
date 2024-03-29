
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The _Leray spectral sequence_ is the special case of the [[Grothendieck spectral sequence]] for the case where the two [[functors]] being composed are a [[direct image|push-forward]] of [[sheaves of abelian groups]] along a [[continuous map]] $f : X \to Y$ between [[topological spaces]] or more generally the [[direct image]] of a [[morphism of sites]], followed by the push-forward $Y \to *$ to the [[point]] -- the [[global section]] functor. This yields a [[spectral sequence]] that computes the [[abelian sheaf cohomology]] on $X$ in terms of the abelian sheaf cohomology on $Y$.

## Properties

+-- {: .num_theorem}
###### Theorem

Let $X, Y$ be suitable [[sites]] let and $f : X \to Y$ be a [[morphism of sites]].  Let $\mathcal{C} = Ch_\bullet(Sh(X,Ab))$ and $\mathcal{D} = Ch_\bullet(Sh(Y,Ab))$ be the [[model structure on chain complexes|model categories of complexes of sheaves of abelian groups]]. The [[direct image]] $f_*$ and [[global section]] functor $\Gamma_Y$ compose to $\Gamma_X$:

$$
  \Gamma_X : \mathcal{C} \stackrel{f_*}{\to} \mathcal{D} \stackrel{\Gamma_Y}{\to} Ch_\bullet(Ab)
  \,.
$$

Then for $A \in Sh(X,Ab)$ a sheaf of abelian groups on $X$ there is a cohomology spectral sequence

$$
  E_2^{p,q} := H^p(Y, R^q f_* A)
$$

that converges as

$$
  E_2^{p,q} \Rightarrow H^{p+q}(X, A)
$$

and hence computes the [[abelian sheaf cohomology]] of $X$ with coefficients in $A$ in terms of the cohomology of $Y$ with coefficients in the derived [[direct image]] of $A$.

=--

## Related concepts

* [[Leray-Serre spectral sequence]]

## References

Lecture notes include

* Dan Petersen, _Leray spectral sequence_, November 2010  ([pdf](http://staff.science.uva.nl/~heinloth/StacksSeminar/DanLeray.pdf))

* [[Greg Friedman]], _Some extremely brief notes on the Leray spectral sequence_ ([pdf](http://faculty.tcu.edu/richardson/Seminars/Gregspecseq.pdf))



Textbook accounts with an eye specifically towards [[étale cohomology]] 


* [[Günter Tamme]], section I 3.7 of _[[Introduction to Étale Cohomology]]_

* [[James Milne]], section 11 of _[[Lectures on Étale Cohomology]]_

&#8206;


[[!redirects Leray spectral sequences]]
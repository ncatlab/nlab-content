
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Complete small categories
* toc
{: toc}

## Definition

A **complete small category** (or **small complete category**) is a [[category]] which is both [[small category|small]] (has only a [[set]] of [[objects]] and [[morphisms]]) and [[complete category|complete]] (has a [[limit]] of every small [[diagram]]).

(Note that the phrase "[[small-complete category]]" is sometimes used to mean merely a complete category, i.e. one which is "complete relative to small diagrams".  Therefore, "complete small category" is a safer term for our concept.)


## In classical logic

In the presence of [[classical logic]], complete small categories reduce to [[complete lattices]] by the following theorem of Freyd.

+-- {: .un_theorem}
###### Theorem

If (in some [[universe]] $U$) a small [[category]] $D$ has [[product]]s of families of objects whose size is at least that of its set of morphisms, then $D$ is a [[preorder]].  In particular, any complete small category is a [[preorder]].  

=--

+-- {: .proof}
######Proof

Let $x$, $y$ be any two objects, and suppose (contrary to $D$ being a preorder) that there are at least two different morphisms $x \,\underoverset{s}{r}{\rightrightarrows}\, y$. Then the set of morphisms 

$$x \to \prod_{f \in Mor(D)} y$$ 

has [[cardinality]] at least $2^{|Mor(D)|} \gt {|Mor(D)|}$, which is a contradiction. 

=--


## In Grothendieck toposes

The [[internal logic]] of a [[topos]] is not, in general, classical, so the above proof does not apply when considering [[internal categories]] in a topos.  However, in a [[Grothendieck topos]], one can show that the conclusion still holds by essentially reducing the question to the analogous one in $Set$.  A brief description of the argument can be found in the answer to [this question](http://mathoverflow.net/questions/43433/small-complete-categories-in-a-grothendieck-topos).


## In more general toposes and constructive mathematics

However, it is possible to have non-preorder complete small categories in non-Grothendieck topoi.  In particular, the [[effective topos]], along with most other [[realizability topos|realizability toposes]], does contain such internal categories, arising for example from the [[modest sets]] or [[partial equivalence relations]].  See [Hyland88](#Hyland88) and [HRR90](#HRR90) for details.

It follows that, in [[constructive mathematics]], it is impossible to prove even that every complete small category in $Set$ or in a Grothendieck topos must be a preorder.

There is a subtlety, however, because in the absence of the [[axiom of choice]], there is a difference between a category being "strongly complete" in the sense of being equipped with limit-assigning [[functors]], and being "weakly complete" in the sense that there merely *exists* a limit for every diagram.  The complete small categories in realizability toposes are only weakly complete, which categorically means that only the [[stack]] completions of their corresponding [[indexed categories]] are complete in the relevant indexed-category sense.

It seems to be unknown whether there exists a (necessarily non-Grothendieck) topos containing a *strongly* complete small category.  However, one of the complete small categories in the effective topos does become strongly complete when the ambient context is restricted to the subcategory of [[assemblies]] rather than the entire effective topos.


## Modelling impredicative type theory

Complete small categories have applications to the modeling of impredicative [[polymorphism]].  Suppose that there is a full subcategory $\mathbf C$ of $\mathbf{Set}$ that is small and complete.  Then we can interpret an impredicatively-quantified type as
\[\llbracket \forall X.T \rrbracket = \prod_{A\in \mathbf{C}} \llbracket T\rrbracket_{A/X}\]
although there are more elaborate formulations that use a subset of this product.

At least at first glance, this requires $\mathbf{C}$ to be *strongly* complete.  Hence it works in the category of assemblies, but not the entire realizability topos.

An alternative approach is to suppose that there is a full [[replete subcategory]] $\mathcal{C}$ of $\mathbf{Set}$ which is complete in the sense of being closed under set-indexed products and equalizers, yet [[essentially small]], i.e. with a small skeleton $\mathbf C$. (Being replete, $\mathcal{C}$ will not itself be small.)  Such a category can be obtained as the repletion of any *weakly* complete *actually* small subcategory, such as exist in realizability toposes.  See [MS09](#MS09).  For discussion about whether this works, see the nForum thread for this page.


## References

* {#Hyland88} A small complete category, [[Martin Hyland]], Annals of Pure and Applied Logic 40 (1988), [pdf](https://webdpmms.maths.cam.ac.uk/~martin/Research/Oldpapers/smallcomplete88.pdf)

There was much activity around that time, by [[Peter Freyd]], [[Eugenio Moggi]], [[Andrew Pitts]], [[John Reynolds]], Guiseppe Rosolini, and others.  One important reference, which discusses the strong/weak completeness issue and the relation to stacks in more detail, is:

* {#HRR90} Hyland, J. M., Robinson, E. P. and Rosolini, G. (1990), The Discrete Objects in the Effective Topos. Proceedings of the London Mathematical Society, s3-60: 1-36. [doi:10.1112/plms/s3-60.1.1](https://doi.org/10.1112/plms/s3-60.1.1)

The idea of using a replete complete subcategory which is essentially small in [[constructive set theory|IZF]] is discussed in
 
* {#MS09} Relational parametricity for computational effects, Rasmus Møgelberg and [[Alex Simpson]], Logical Methods in Computer Science, Vol 5 (3:7), 2009. [arxiv](https://arxiv.org/abs/0906.5488).



[[!redirects complete small category]]
[[!redirects complete small categories]]
[[!redirects small complete category]]
[[!redirects small complete categories]]

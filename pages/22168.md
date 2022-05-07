[[!redirects condensed cohesion]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

The typical [[gros topos|gros]] -[[toposes]] and -[[(∞,1)-toposes|$\infty$-toposes]] considered in [[arithmetic geometry|arithmetic]]/[[algebraic geometry]] are far from being [[cohesive toposes|cohesive]] over [[Set]] and even farther from being [[cohesive (infinity,1)-topos|$\infty$-cohesive]] over [[Infinity-Grpd|$Grpd_\infty$]], respectively: The extra [[left adjoint]] to their [[terminal geometric morphism]] would mean that [[varieties]]/[[schemes]] were [[locally connected topos|locally connected]] or even [[locally infinity-connected (infinity,1)-topos|locally $\infty$-connected]], which they are not. 

(This is in contrast to the situation in [[differential geometry]], where  [[smooth manifolds]], [[formal smooth manifolds]], and [[supermanifolds]], etc.,  generate the [[cohesive (infinity,1)-topos|cohesive $\infty$-toposes]] over [[Infinity-Grpd|$Grpd_\infty$]] of [[smooth infinity-groupoids|smooth $\infty$-groupoids]], [[formal smooth infinity-groupoids|formal smooth $\infty$-groupoids]] and [[super formal smooth infinity-groupoid|super formal smooth $\infty$-groupoids]], etc.)

But [[cohesion]] may usefully be considered over non-trivial [[base toposes]] or [[base (infinity,1)-topos|base $\infty$-toposes]]. For example, the [[slice (infinity,1)-topos|slice $\infty$-topos]] of [[global equivariant homotopy theory]] over the archetypical $G$-[[orbi-singularity]] is cohesive over proper $G$-[[equivariant homotopy theory]] (see at *[[cohesion of global- over G-equivariant homotopy theory]]*).

{#AlmostCohesionInIntroduction} Analogously, the [[gros topos]] of [[pro-étale topos|pro-étale]] [[arithmetic geometry|arithmetic]]/[[algebraic geometry]], while not cohesive over [[sets]], has at least an extra left adjoint over some base topos related to condensed or pyknotic sets.
This and the analogous statement for the respective [[hypercomplete (infinity,1)-topos|hypercomplete $\infty$-toposes]] is claimed in [Scholze 2020](#Scholze2020), see also [Scholze a](#Scholzea). 

In view of the terminology of "[[condensed mathematics]]" one might call this local contractibility of pro-étale arithmetic geometry relative to something like pyknotic sets: _condensed local contractibility_. 


## Structures in condensed local contractibility
 {#StructuredInCondensedCohesion}

The point of axiomatic [[cohesion]] is that it formally implies the presence of structures of the form of key phenomena known in traditional [[differential topology]], but now [[internalization|internal]] into any given [[cohesive topos]]/[[cohesive (infinity,1)-topos|$\infty$-topos]]. Hence to the extent that [[pro-étale topos|pro-étale]] [[arithmetic geometry]] is cohesive over the [[pro-étale topos|pro-étale]] [[base topos]] it inherits these structures.

There would be much to be discussed here. The following lists some first observations with links to further commentary.


## Possible construction

### Differential cohomology diagram

Every [[spectrum object]] in a [[locally infinity-connected (infinity,1)-topos|locally $\infty$-connected $\infty$-topos]] sits in the center of a *[[differential cohomology diagram]]*, which may be understood as decomposing the object  into its various [[modality|modal]] aspects, such that, at least for [[smooth infinity-groupoids|smooth $\infty$-groupoids]], it exhibits each object as representing a [[Whitehead-generalized cohomology theory|Whitehead-generalized]] [[differential cohomology theory]].

Since the construction of the differential cohomology hexagon does not require the extra left adjoint to [[preserved limit|preserve]] [[finite products]], it should exist in [[pro-étale topos|pro-étale]] [[arithmetic geometry]]. Commentary in this direction is in [Scholze b](#Scholzeb).




## References

The idea of the possibility of pro-étale local contractibility is voiced in discussion here: 

* [[Marc Hoyois]], [[Urs Schreiber]], *étale ∞-site* (around [nForum comment 43431](https://nforum.ncatlab.org/discussion/5473/etale-site/?Focus=43431#Comment_43431)), November 2013

The claim of cohesion-except-for-product-preservation of gros [[pro-étale toposes]] over the corresponding pro-étale base topos appears in:

* {#Scholze2020} [[Peter Scholze]], *[Re: Pyknoticity versus Cohesiveness](https://golem.ph.utexas.edu/category/2020/03/pyknoticity_versus_cohesivenes.html#c057631)*, March 2020

Related remarks and discussion:

* {#Scholzea} [[Peter Scholze]], _Answer to 'What is the precise relationship between pyknoticity and cohesiveness?'_, April 2020 ([MO:https://mathoverflow.net/a/356836](https://mathoverflow.net/a/356836/447)).

* {#Scholzeb} [[Peter Scholze]], _Answer to 'Cohesion relative to a pyknotic/condensed base'_, Feb 2021 ([MO:a/384900](https://mathoverflow.net/a/384900/381)).

* {#Scholzec} [[Peter Scholze]], _Answer to 'Condensed / pyknotic approach to orbifolds?'_, Feb 2021 ([MO:a/384898](https://mathoverflow.net/a/384898/381))

[[!redirects condensed cohesion]]

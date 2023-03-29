

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


This is a subentry of [[(∞,1)-Grothendieck construction]].


#Contents#
* table of contents
{:toc}

## Idea

When [[(∞,1)-categories]] are modeled as [[quasi-categories]], the [[(∞,1)-Grothendieck construction]] takes the form of a [[Quillen equivalence]] 
between
a [[model structure on sSet-enriched presheaves]]
and a [[slice model structure]] of [[simplicial sets]] which has been introduced under the name *straightening and unstraightening* in [Lurie 2009, Sec. 3.2](#Lurie09):

Concretely, in the notation recalled at *[[relation between quasi-categories and simplicial categories]]*:

For a [[simplicial set]] $S$, [[simplicially enriched category]] $C$, and [[sSet]]-[[enriched functor]] $\mathfrak{C}[S] \to C$, there is a [[pair]] of [[adjoint functors]]
$$
  (St_\phi\dashv Un_\phi) 
  \;\colon\; 
  sSet/S \xrightarrow{\;\; St \;\;} [C^{op}, sSet]
$$
which (under an assumption on the parameter $\phi$) can be shown to be a [[Quillen equivalence]] between 

1. the [[slice category]] of [[sSet]] equipped with the [[model structure for right fibrations]] (also called contravariant model structure in [[Higher Topos Theory|HTT]]) 

1. the category of [[simplicial presheaves]] equipped with [[model structure on simplicial presheaves|global projective model structure]].

There is also a [[Quillen equivalence]]
$$
  (St_\phi \dashv Un_\phi) 
  \;\colon\; 
  sSet^+/S \stackrel{St}{\;\; \longrightarrow \;\;} [C^{op}, sSet^+]
$$
between 

1. the [[model structure for Cartesian fibrations]] 

1. the global projective [[model structure on functors]] with values in the [[model structure on marked simplicial sets]].

In both cases, 

* $St_\phi$ is called the *straightening functor* 

* $Un_\phi$ is called the *unstraightening functor*. 

These names have been chosen due to the fact that objects in the left hand category are defined by existential assertions and choices where on the right side these properties become [[coherence laws]] being part of the structure.

## Related concepts

* [[cartesian fibration]]

* [[Grothendieck fibration]]

* [[(∞,1)-Grothendieck construction ]]

* [[cleavage]]

## References

The original result is due to:

* {#Lurie09} [[Jacob Lurie]], Sec. 3.2 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))


Further discussion:

* {#Stevenson15} [[Danny Stevenson]], *Covariant Model Structures and Simplicial Localization*, North-West. Eur. J. Math. **3** (2017) 141-202 &lbrack;[arXiv:1512.04815](http://arxiv.org/abs/1512.04815)&rbrack;

* [[Gijs Heuts]], [[Ieke Moerdijk]], *Left fibrations and homotopy colimits II* &lbrack;[arXiv:1602.01274](https://arxiv.org/abs/1602.01274)&rbrack;

* [[Alexander Campbell]], *A modular proof of the straightening theorem*, talk at Macquarie University (2020) &lbrack;[pdf](https://acmbl.github.io/straight_slides.pdf), [[Campbell-ModularProofofStraightening.pdf:file]]&rbrack;

* [[Fabian Hebestreit]], [[Gijs Heuts]], [[Jaco Ruit]], _A short proof of the straightening theorem_ ([arXiv:2111.00069](https://arxiv.org/abs/2111.00069)).

Discussion [[category internal to an (infinity,1)-topos|internal to]] any [[(∞,1)-topos]]:

* [[Louis Martini]], *Cocartesian fibrations and straightening internal to an ∞-topos* &lbrack;[arXiv:2204.00295](https://arxiv.org/abs/2204.00295)&rbrack;


Discussion of straightening and unstraightening entirely within the context of [[quasi-categories]]:

* [[Denis-Charles Cisinski]], [[Hoang Kim Nguyen]], *The universal coCartesian fibration* &lbrack;[arXiv:2210.08945](https://arxiv.org/abs/2210.08945)&rbrack;

which (along the lines of the discussion of the universal left fibration from [Cisinski 2019](universal+coCartesian+fibration#Cisinski19)) allows to understand the [[universal coCartesian fibration]] as [[categorical semantics]] for the [[univalence axiom|univalent]] [[type universe]] in [[directed homotopy type theory]]:

* {#CisinskiEtAl23} [[Denis-Charles Cisinski]], [[Hoang Kim Nguyen]], Tashi Walde: *Univalent Directed Type Theory*, lecture series in the *[CMU Homotopy Type Theory Seminar](https://www.cmu.edu/dietrich/philosophy/hott/seminars/index.html)* (13, 20, 27 Mar 2023) &lbrack;[web](https://www.cmu.edu/dietrich/philosophy/hott/seminars/index.html#230313), video 1:[YT](https://www.youtube.com/watch?v=5YOltuTcBK8), 2:[YT](https://www.youtube.com/watch?v=xWmELBvHMPo), 3:[YT](https://www.youtube.com/watch?v=P0Cfb4eUJo4); slides 0:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-intro_talk1.pdf), 1:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk1.pdf), 2:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk2.pdf), 3:[pdf](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk3.pdf)&rbrack;

(see [video 3 at 1:16:58](https://youtu.be/P0Cfb4eUJo4?t=4618) and [slide 3.33](https://www.cmu.edu/dietrich/philosophy/hott/seminars/slides/cisinski-nguyen-walde-talk3.pdf#page=33)).



[[!redirects straightening and unstraightening]]

[[!redirects straightening theorem]]



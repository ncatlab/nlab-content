
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

In the simplest case, _tensorial strength_ is a property of an [[endofunctor]] $T \colon V \to V$ on a [[monoidal category]] which characterizes it as a  $V$-[[enriched functor]] when $V$ is canonically regarded as an [[enriched category]] over itself. 

More generally, tensorial strength on a functor
$$
  F \,\colon\, \mathbf{C}_0 \to \mathbf{C}_1
$$

between categories that are [[tensoring|tensored]] ([[copowering|copowered]]) over $V$

$$
  \textstyle{\otimes} 
    \,\colon\, 
  V \times C_i \longrightarrow C_i
$$

is a [[natural transformation]] 

$$
  v \otimes F(c) \to F(v \otimes c)
$$

exhibiting compatibility of $F$ with that [[tensoring]].

In the case that $V$ is also [[closed monoidal category|closed monoidal]], there is a close relation between strong functors and [[enriched functors]] (see [below](#RelationToEnrichedFunctors)).

{#WarningOnTerminology} In fact, beware that [Kock 1972](#Kock72) originally said *tensorial strength* in constrast to the *strength* of *strong functors* by which he referred to $V$-[[enriched functors]]. Beware that today "strong functor" (certainly as in "[[strong monad]]") is usually understood in the sense of tensorial strength, not in the sense of "enriched functor"  (to the extent that the two notions differ at all, see again [below](#RelationToEnrichedFunctors)). Hence historically it would be more accurate to say "tensorially strong functors" for the notion discussed here, but this term is not commonly used at all.



## Definition 

### Standard definition

Given a [[monoidal category]] $(V, \otimes, I)$ with [[tensor product]] $\otimes$, a **tensorial left-strength** for a functor 

$$F \colon V \to V$$

is usually defined as a [[natural transformation]] 

$$
  \beta_{v, w}
  \;\colon\; 
  v \otimes F(w) 
    \longrightarrow
  F(v \otimes w)
$$

making the following [[commuting diagram|diagrams commute]]: 

$$
\array{
  (u \otimes v) \otimes F(w) & & \overset{\beta_{u\otimes v,w}}{\to} & & F((u\otimes v)\otimes w)\\
  ^\mathllap{\alpha_{u,v,F(w)}}\downarrow & & & & \downarrow^{\mathrlap{F(\alpha_{u,v,w})}}\\
  u\otimes (v\otimes F(w)) & \underset{1_u\otimes\beta_{v,w}}{\to} & u\otimes F(v\otimes w) & \underset{\beta_{u,v\otimes w}}{\to} & F(u\otimes (v\otimes w))
}
$$
and
$$
\array{
I\otimes F(v) & \overset{\beta_{I,v}}{\to} & F(I\otimes v) \\
& _\mathllap{\lambda_{F(v)}}\searrow & \downarrow^\mathrlap{F(\lambda_v)}\\
& & F(v)
}
$$
where $\alpha$ is the [[associator]] and $\lambda$ is the [[unitor]] of the [[monoidal category]] $V$.

A **tensorial right-strength** (not to be confused with a [[tensorial costrength]]) is defined symmetrically, as a natural transformation
$$\gamma_{v, w}: F(w) \otimes v \to F(w \otimes v)$$

When $V$ is [[symmetric monoidal category|symmetric]], tensorial left strengths are equivalently tensorial right strengths, and in this setting, one usually drops "left-" or "right-" and simply talks about **tensorial strengths**.

A functor equipped with a tensorial strength is called a **strong functor** (not to be confused with a *strong 2-functor*, which is another name for a [[pseudofunctor]], i.e. a [[lax 2-functor]] whose coherence cells are invertible).

More generally, the notion makes sense not just for endofunctors of $V$, but for functors between any categories that are "tensored over $V$."
 

### Tentative reformulation

+-- {: .standout}

_Tentative_ -- The following reformulation &lbrack;[Baez 2009](&Baez09)&rbrack; of the standard definition is tentative.

=--

It seems we may phrase this definition more conceptually as follows. There is a bicategory $V-Act$ where:

* the objects are categories $C$ equipped with a lax left $V$-action, i.e. a [[lax monoidal functor]] $\alpha : V \to End(C)$,
* the morphisms are functors laxly preserving this action, and 
* the 2-morphisms are natural transformations compatible with this action.  

$V$ has a canonical left action on itself, which allows us to think of it as an object of $V-Act$.  So, given a functor $F: V \to V$, a **tensorial strength** for $F$ is defined to be a way of equipping it with the structure of a morphism in $V-Act$.

A bit more precisely: 

$$V-Act = Lax(B V, Cat)$$

Here $B V$ is $V$ regarded as a 1-object weak 2-category, $Cat$ is regarded as a 2-category, and $Lax$ is the bicategory of 

* weak 2-categories
* [[lax functor|lax functors]]
* [[lax natural transformation|lax natural transformations]]

There is a forgetful 2-functor

$$V-Act \to Cat $$

and a **tensorial strength** for a functor $F: V \to V$ is a way of lifting it to a morphism $\tilde{F}: \tilde{V} \to \tilde{V}$ in $V-Act$, where $\tilde{V}$ is $V$ equipped with its canonical left action on itself.


## Properties

### Relation to enriched functors
 {#RelationToEnrichedFunctors}

> (For more references see also at *[enriched monad -- relation to Strong monads](enriched+monad#RelationToStrongMonads)*)


One possible reason why it may be hard to grasp the notion of strength is because in the case $V = Set$, they're sort of invisible. Every functor $T: Set \to Set$ has one, in fact a canonical one! This will make more sense in a moment. 

Strengths are easier to understand by considering the case where $V$ is [[closed monoidal category|closed monoidal]]. Here $V$ is [[enriched category|enriched]] in itself, and one of the most important aspects of strengths is this: 

* A functor $T: V \to V$ with a strength is the same thing as a $V$-enrichment on $T$. 

Here's how that works. An enrichment on $T$ in $V$-[[enriched category theory]] consists of a natural family of morphisms in $V$, 

$$hom(a, b) \to hom(T(a), T(b)),$$ 

satisfying some suitable axioms. Here $hom$ denotes the enrichment of $V$ in itself -- the [[internal hom]]. Starting from a strength on $T$, you can cook up an enrichment on $T$, roughly as follows: the map above is equivalent by hom-tensor [[adjunction]] to a map 

$$hom(a, b) \otimes T(a) \to T(b)$$ 

and now the strength allows you to slide $hom(a, b)$ inside $T$, and from there you just apply $T$ to the evaluation: 

$$T(hom(a, b) \otimes a) \overset{T(eval_{a, b})}{\to} T(b)$$ 

and presto, you're done. The strength axioms ensure that this enrichment structure on $T$ satisfies the axioms you need for a functor to be enriched. 

(And going back the other way, from an enrichment to a strength, is also easy -- there you have to dualize. That is, instead of using the evaluation which is the counit of the hom-tensor adjunction, you use the coevaluation which is the unit. ) 

After some work, one can convince oneself that the notions of strength and enrichment for endofunctors on closed monoidal categories really are equivalent notions. 


And now we can understand why strengths in the case $V = Set$ are so "invisible" -- every functor $T: Set \to Set$ is $Set$-enriched; that's what we mean by an ordinary functor!  

## Examples

(Plenty of examples of [[strong monads]] are of interest, particularly in the context of [[monads in computer science]]. See there for more.)

\begin{example}
\label{ForHeytingAlgebras}
Suppose the theory of [[Boolean algebras]] -- say we're studying the structure of a free Boolean algebra on a set of generators, $B[X]$. Then again we can think of this, or of any [[Heyting algebra]], as enriched in itself. Further, we have definable unary operators 

$$T \colon B[X] \to B[X]$$ 

in the theory, such as $T = p \wedge (-)$, or $T = p \Rightarrow (-)$, etc. The great discovery of [[Charles S. Peirce]] is that any definable unary operator in the theory of Boolean algebras carries a strength, or if you prefer is enriched. That may be taken to be the essence of Peirce's iteration rule for Alpha, and it [[vertical categorification|categorifies]] right over to a similar statement for the theory of [[closed monoidal category|closed categories]], [[star-autonomous category|star-autonomous categories]], what have you: all definable unary covariant functors in such theories carry canonical strengths. 

(Peirce went a little further, and incorporated notions of contravariant strength as well.) 
\end{example}

## Related concepts

* [[strong natural transformation]]

* [[cartesian closed functor]]

* [[strong monad]]

* [[tensorial costrength]]

* [[commutative monad]]


## References 

The notion of tensorial strength originates in

* {#Kock72} [[Anders Kock]], below Thm. 1.3 of: *Strong functors and monoidal monads*, Arch. Math **23** (1972) 113–120 &lbrack;[doi:10.1007/BF01304852](https://doi.org/10.1007/BF01304852), [pdf](http://home.imf.au.dk/kock/SFMM.pdf)&rbrack;

Comprehensive review:

* {#Ratkovic12} [[Kruna S. Ratkovic]], *Tensorial Strength*, Section 3 of: *Morita theory in enriched context* (2012) &lbrack;[arXiv:1302.2774](https://arxiv.org/abs/1302.2774), [hal:tel-00785301](https://theses.hal.science/tel-00785301/document)&rbrack;
 
Review in the context of [[monads in computer science]]:

* [[Tarmo Uustalu]], *Strong functors, Strong monads*, in: *[Containers for effects and contexts](https://www.ioc.ee/~tarmo/ssgep15/)*, Lecture notes (2015) &lbrack;[pdf](https://www.ioc.ee/~tarmo/ssgep15/ssgep-1a.pdf), [[Uustalu-StrongFunctors.pdf:file]]&rbrack;

* {#McDermottUustalu22} [[Dylan McDermott]], [[Tarmo Uustalu]], Section 3 of: *What Makes a Strong Monad?*, EPTCS **360** (2022) 113-133 &lbrack;[arXiv:2207.00851](https://arxiv.org/abs/2207.00851), [doi:10.4204/EPTCS.360.6](https://doi.org/10.4204/EPTCS.360.6)&rbrack;


The tentative 'more conceptual' definition of tensorial strength, as well as the 'description' above, arose in this discussion:

* {#Baez09} [[John Baez]], _The Monads Hurt My Head -- But Not Anymore_ ([blog](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025476))



[[!redirects tensorial strengths]]
[[!redirects strong functor]]
[[!redirects strong functors]]
[[!redirects strength]]

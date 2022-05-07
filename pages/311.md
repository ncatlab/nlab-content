
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea 

For a [[locally small category]] $C$, a [[presheaf]] on $C$ or equivalently a [[functor]] 

$$F: C^{op} \to Set$$ 

on the [[opposite category]] of $C$ with values in [[Set]] is **representable** if it is [[natural isomorphism|naturally isomorphic]] to a [[hom-functor]] $h_X := \hom_C(-, X): C^{op} \to Set$, which sends an object $U \in C$ to the [[hom-set]] $Hom_C(U,X)$ in $C$

<img src="http://ncatlab.org/ericforgy/files/hx2.jpg" width = "200"/>

and which sends a [[morphism]] $\alpha : U' \to U$ in $C$ to the [[function]] which sends each morphism $U \to X$ to the composite $U' \stackrel{\alpha}{\to} U \to X$

<img src="http://ncatlab.org/ericforgy/files/hxalpha3.jpg" width = "400"/> 

If we picture $Hom_C(U,X)$ as strands of morphisms as above, then the morphism $\alpha:U'\to U$ serves to "comb" the strands back from $Hom_C(U,X)$ to $Hom_C(U',X)$, i.e.

$$h_X\alpha: Hom_C(U,X)\to Hom_C(U',X).$$

The object $X$ is determined uniquely up to [[isomorphism]] in $C$, and is called a **representing object** for $F$. 

Representability is one of the most fundamental concepts of [[category theory]], with close ties to the notion of [[adjoint functor]] and to the [[Yoneda lemma]]. It is the crucial concept underlying the idea of [[universal property]]; thus for example crucial concepts such as "[[limit]]", "[[colimit]]", "[[exponential object]]", "[[Kan extension]]" and so on are naturally expressed in terms of representing objects. The concept permeates much of algebraic geometry and algebraic topology. 

## Definition 

### In ordinary category theory

For a functor $F: C^{op} \to Set$ (also called a [[presheaf]] on $C$), a **representation** of $F$ is a specified [[natural isomorphism]] 

$$\theta: \hom_C(-, c) \stackrel{\sim}{\to} F$$ 

By the [[Yoneda lemma]], any such transformation $\theta$ (isomorphism or not) is uniquely determined by an element $\xi \in F(c)$. As above, the object $c$ is called a **representing object** (or often, **universal object**) for $F$, and the element $\xi$ is called a **[[universal element]]** for $F$. Again, it follows from the [[Yoneda lemma]] that the pair $(c, \xi)$ is determined uniquely up to unique isomorphism. 

Following the proof of the Yoneda lemma, representability means precisely this: given any object $x$ of $C$ and any element $\alpha \in F(x)$, there exists a unique morphism $f: x \to c$ such that the function $F(f)$ carries the universal element $\xi \in F(c)$ to $\alpha \in F(x)$. Such a dry formulation fails to convey the remarkable power of this concept, which can really only be appreciated through the myriad examples which illustrate it. 

### In enriched category theory 

The above definition generalizes straightforwardly
to [[enriched category theory]].

Let $V$ be a [[closed monoidal category]] and $C$ a $V$-[[enriched category]].

Then for every object $c \in C$ there is a 
$V$-[[enriched functor]]

$$
  C(c,-) : C \to V
$$

from $C$ to $V$ regarded canonically as a $V$-[[enriched category]].

This is defined

* on objects by $C(c,-) : d \mapsto C(c,d) \in V$

* on morphisms between $d$ and $d'$ by 

$$
  C(c,-)_{d,d'} : C(d,d') \to [C(c,d), C(c,d')]
  \,,
$$ 

being the [[adjunct]] of the composition morphism 

$$
  \circ_{c,d,d'} : C(d,d') \otimes C(c,d) \to C(c,d')
  \,.
$$ 

A $V$-enriched functor $F : C \to V$ is **representable** if there is $c \in C$ and a $V$-[[enriched natural transformation]] $\eta : F \to C(c,-)$.

If $V$ is [[symmetric monoidal category|symmetric monoidal]] one can form the [[opposite category]] $C^{op}$ and have the analogous definition for representable functors $F : C^{op} \to V$.

### In higher category theory

The notion of representable functors has its straightforward analogs also in [[higher category theory]]. 

* For [[2-category theory]] see ... .

* For [[(∞,1)-category theory]] theory see [[(∞,1)-presheaf]]


## Examples 

The central point about examples of representable functors is:

_Representable functors are ubiquitous_ . 

To a fair extent, [[category theory]] is all about representable functors and the other [[universal constructions]]: [[Kan extensions]], [[adjoint functors]], [[limits]], which are all special cases of representable functors -- and representable functors are special cases of these.

Listing examples of representable functors in [[category theory]] is much like listing examples of [[integral]]s in [[analysis]]: one can and does fill books with these. (In fact, that analogy has more to it than meets the casual eye: see [[coend]] for more).


Keeping that in mind, we do list some special cases and special classes of examples that are useful to know. But any list is necessarily wildly incomplete.


### Limits 
  {#ExampleLimits}

If $F:J\to C$ is a [[diagram]] in $C$, we can construct a diagram $\hom_C(-,F):J\to Set^{C^{op}}$ in the [[functor category]] $Set^{C^{op}}$ as the composite of $F$ with the curried [[hom-functor]] $C\to\Set^{C^{op}}$ (the [[Yoneda embedding]]).  The object-wise [[limit]] of this diagram in [[Set]], that is, the functor $C^{op}\to\Set$ sending an object $x$ to the set which is the limit of the diagram $\hom_C(x,F):J\to\Set$, is representable iff the diagram $F$ has a limit in $C$; in fact, a representing object for that limit functor is exactly $\lim F$, and we obtain a natural isomorphism

$$\lim \hom_C(-,F)\cong\hom_C(-,\lim F).$$

#### Products 

For an example in the case of the [[product]], let $c, d$ be objects of $C$, and consider the presheaf given by a product of [[hom-functor|hom-functors]]

$$\hom_C(-, c) \times \hom_C(-, d): C^{op} \to Set;$$ 

that is, the functor which takes an object $x$ of $C$ to the set $\hom_C(x, c) \times \hom_C(x, d)$. A product $c \times d$ is precisely a representing or universal object for this presheaf, where the universal element is precisely the pair of projection maps 

$$(\pi_c, \pi_d) \in \hom(c \times d, c) \times \hom(c \times d, d)$$ 

We leave it to the reader to check that the representability here means precisely that given a pair 
of maps 

$$(f, g) \in \hom(x, c) \times \hom(x, d)$$ 

there exists a unique element in $\hom(x, c \times d)$, denoted $\langle f, g \rangle$, such that 

$$\pi_c \langle f, g \rangle = f \qquad \pi_d \langle f, g \rangle = g.$$

#### Weighted limits 

The above example has an important straightforward generalization.

Noticing that the limit over the functor $H : J \to Set$ is just the collection of [[cone]]s over $H$ whose tip is the point
$$
  lim H = [J,Set](\Delta pt, H)
$$ 
the above expression
$\lim\hom_C(-,F)$ can be rewritten equivalently as 
$[J,Set](\Delta pt, C(-,F(-)))$. Replacing in this expression the constant terminal functor $\Delta pt : J \to Set$ by any other functor leads to the notion of [[weighted limit]], as described there.

### Exponential objects

Suppose $C$ is a category which admits finite products; given objects $c, d$, consider the presheaf 

$$\hom_C(- \times c, d): C^{op} \to Set.$$ 

A representing or universal object for this presheaf is an [[exponential object]] $d^c$; the universal element 

$$e \in \hom_C(d^c \times c, d)$$ 

is a morphism called the **evaluation** map $eval: d^c \times c \to d$. 

### Classifying bundles

Consider a category $Top$ of 'nice' spaces (just to fix the discussion, let's say paracompact spaces, although this is a technical point), and a topological group $G$ therein, i.e., a group internal to $Top$. There is a presheaf 

$$G\Bund: Top^{op} \to Set$$ 

which assigns to each space $X$ the set of isomorphism classes of $G$-bundles over $X$, and assigns to each continuous map $f: X \to Y$ the function 

$$G\Bund(f): G\Bund(Y) \to G\Bund(X)$$ 

which carries a (class of a) $G$-bundle $E \to Y$ to the (class of the) pullback bundle $f^*E \to X$. It is well-known that the pullback construction is invariant with respect to homotopic deformations; that is, this presheaf descends to a functor on the [[homotopy category]], 

$$G\Bund: Ho_{Top}^{op} \to Set.$$ 

A **[[classifying space]]** $\mathcal{B}G$ is precisely a representing object for this functor; the universal element is the (isomorphism class of the) classifying $G$-bundle $[\pi: \mathcal{E}G \to \mathcal{B}G]$.

These general considerations are quite commonplace in algebraic topology, where they crop up for example in the connection between generalized cohomology theories and spectra; cf. Brown's representability theorem. 


## Related concepts

* [[representable functor theorem]]

* [[Yoneda lemma]], [[Yoneda embedding]]

* [[classifying space]], [[classifying stack]], [[moduli space]], [[moduli stack]], [[derived moduli space]]

* [[classifying morphism]]

* [[representable morphism of stacks]]

* [[Artin representability theorem]], [[Artin-Lurie representability theorem]]

## References

Early accounts:

* [[Alexander Grothendieck]], Section A.1 of: *Technique de descente et théorèmes d'existence en géométrie algébriques. II. Le théorème d'existence en théorie formelle des modules*, Séminaire Bourbaki : années 1958/59 - 1959/60, exposés 169-204, Séminaire Bourbaki, no. 5 (1960), Exposé no. 195, 22 p.  ([numdam:SB_1958-1960__5__369_0](http://www.numdam.org/item/?id=SB_1958-1960__5__369_0))

A discussion of representable functors in the context of [[enriched category theory]] is in section 1.6 and section 1.10 of

* [[Max Kelly]], _Basic concepts of enriched category theory_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))

A query discussion on differences between representable functor and representation of a functor is archived [here](https://nforum.ncatlab.org/discussion/4497/representable-functor/).


[[!redirects representable functor]]
[[!redirects representable functors]]
[[!redirects represented functor]]
[[!redirects represented functors]]
[[!redirects representable]]
[[!redirects representables]]
[[!redirects representable presheaf]]
[[!redirects representable presheaves]]
[[!redirects representing object]]
[[!redirects representing objects]]

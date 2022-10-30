
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

The **Yoneda lemma** says that the [[set]] of [[morphisms]] from a [[representable presheaf]] $h_c$ into an arbitrary [[presheaf]] $F$ is in [[natural bijection]] with the set $F(c)$ assigned by $F$ to the representing [[object]] $c$.

The Yoneda lemma is an elementary but deep and central result in [[category theory]] and in particular in [[sheaf and topos theory]]. It is essential background behind the central concepts of [[representable functor]], [[universal construction]], and [[universal element]]. 

## Preliminaries

Recall that for $C$ a [[locally small category]] and $[C^{op}, Set] (= Set^{C^{op}} = Hom(C^{op},Set))$ the [[category of presheaves]] on $C$, there naturally is a functor 

$$
  Y : C \to [C^op,Set]
$$

-- called the [[Yoneda embedding]] for reasons explained below -- which sends $C$ to the category of presheaves over it: this is just the image of the Hom-functor

$$
  C(-,-) : C^op \times C \to Set
$$

under the Hom-adjunction 

$$
  Hom(C^{op} \times C, Set) \stackrel{\simeq}{\to}
  Hom(C, [C^{op}, Set])
$$

in the [[closed monoidal category|closed]] [[monoidal category|symmetric monoidal category]] of categories.

Hence $Y$ sends any object $c \in C$ to the presheaf which assigns to any other object $d$ of $C$ the set of morphisms from $d$ into $c$:

$$
  Y(c) : C^{op} \stackrel{C(-,c)}{\to} Set
  \,.
$$

### Remarks

One way to appreciate the meaning of this and of what the Yoneda lemma has to say about it is to regard this in the context of [[space and quantity]]: thinking of the objects of $C$ as test spaces, presheaves on $C$ are generalized spaces modeled on $C$ which are characterized by the way one can map objects of $C$ into them. 

The Yoneda lemma states that the functor $Y$ has good properties which make this interpretation consistent.

## The Yoneda Lemma {#StatementOfYonedaLemma}

Let $C$ be a [[locally small category]], $[C^{op}, Set]$ the category of [[presheaf|presheaves]] on $C$. Let $c \in C$ be an [[object]].

The Yoneda lemma asserts that the set of morphisms from the [[presheaf]] [[representable presheaf|represented by]] $c$ into any other presheaf $X$ is in natural bijection with the set $X(c)$ that this presheaf assigns to $c$.

Formally:

+-- {: .un_prop} 
###### Proposition

There is a canonical [[isomorphism]]

$$
  [C^op,Set](C(-,c),X) \simeq X(c)
$$

natural in $c$.

=--

Here $[C^{op}, Set]$ denotes the [[functor category]], also denoted $Set^{C^{op}}$ and $C(-,c)$ the [[representable presheaf]]. This is the standard notation used mostly in pure [[category theory]] and [[enriched category theory]]. In other parts of the literature it is customary to denote the presheaf represented by $c$ as $h_c$. In that case the above is often written

$$
  Hom(h_c, X) \simeq X(c)
$$

or

$$
  Nat(h_c, X) \simeq X(c)
$$

to emphasize that the morphisms of presheaves are [[natural transformation]]s of the corresponding functors.



+-- {: .proof} 
###### Proof 
The proof is by chasing the element $Id_c \in C(c, c)$ around both legs of a naturality square for a transformation $\eta: C(-, c) \to X$: 

$$\array{
C(c, c) & \stackrel{\eta_c}{\to} & X(c) & & & & Id_c & \mapsto & \eta_c(Id_c) & \stackrel{def}{=} & \xi \\ 
 _\mathllap{C(f, c)} \downarrow & & \downarrow _\mathrlap{X(f)} & & & & \downarrow & & \downarrow _\mathrlap{X(f)} & & \\ 
C(b, c) & \underset{\eta_b}{\to} & X(b) & & & & f & \mapsto & \eta_b(f) & & 
}$$ 

What this diagram shows is that the entire transformation $\eta: C(-, c) \to X$ is completely determined from the single value $\xi \coloneqq \eta_c(Id_c) \in X(c)$, because for each object $b$ of $C$, the component $\eta_b: C(b, c) \to X(b)$ must take an element $f \in C(b, c)$ (i.e., a morphism $f: b \to c$) to $X(f)(\xi)$, according to the commutativity of this diagram. 

The crucial point is that the naturality condition on any [[natural transformation]] $\eta : C(-,c) \Rightarrow X$ is sufficient to ensure that $\eta$ is already entirely fixed by the value $\eta_c(Id_c) \in X(c)$ of its component $\eta_c : C(c,c) \to X(c)$ on the [[identity morphism]] $Id_c$.
And every such value extends to a natural transformation $\eta$.


More in detail, the bijection is established by the map

$$
  [C^{op}, Set](C(-,c),X)
  \stackrel{|_{c}}{\to}
  Set(C(c,c), X(c))
  \stackrel{ev_{Id_c}}{\to}
  X(c)
$$

where the first step is taking the component of a [[natural transformation]] at $c \in C$ and the second step is evaluation at $Id_c \in C(c,c)$. 

The inverse of this map takes $f \in X(c)$ to the natural transformation $\eta^f$ with components
$$
  \eta^f_d := X(-)(f) : C(d,c) \to X(d)
  \,.
$$

=-- 


### Remarks

In the light of the interpretation in terms of [[space and quantity]] mentioned above this says that for $X$ a generalized space modeled on $C$, and for $c$ a test space, morphisms from $c$ to $X$ with $c$ regarded as a generalized space are just the morphisms from $c$ into $X$.

## Corollaries

The Yoneda lemma has the following direct consequences. As the Yoneda lemma itself, these are as easily established as they are useful and important.

### corollary I: Yoneda embedding

The Yoneda lemma implies that the [[Yoneda embedding]] functor $Y : C \to [C^op,Set]$ really is an _embedding_ in that it is a [[full and faithful functor]], because for $c,d \in C$ it naturally induces the isomorphism of Hom-sets.

$$
  [C^{op},Set](C(-,c),C(-,d)) \simeq (C(-,d))(c) = C(c,d)
$$


### corollary II: uniqueness of representing objects 

Since the [[Yoneda embedding]] is a [[full and faithful functor]], an [[isomorphism]] of [[representable functor|representable presheaves]] $Y(c) \simeq Y(d)$ must come from an [[isomorphism]] of the representing objects $c \simeq d$:

$$
  Y(c) \simeq Y(d) \;\; \Leftrightarrow \;\;
  c \simeq d
$$

### corollary III: universality of representing objects

A [[nLab:presheaf|presheaf]] $X : C^{op} \to Set$ is [[nLab:representable functor|representable]] precisely if the [[nLab:comma category|comma category]] $(Y,const_X)$ has a [[nLab:terminal object|terminal object]]. If a [[nLab:terminal object|terminal object]] is $(d, f : Y(d) \to X) \simeq (d, f \in X(d))$ then $X \simeq Y(d)$.

This follows from unwrapping the definition of morphisms in the [[nLab:comma category|comma category]] $(Y,const_X)$ and applying the Yoneda lemma to find

$$
  (Y,const_X)((c,f \in X(c)), (d, g \in X(d)))
  \simeq
  \{
    u \in C(c,d) : X(u)(g) = f
  \}
  \,.
$$

Hence $(Y,const_X)((c,f \in X(c), (d, g \in X(d))) \simeq pt$ says precisely that $X(-)(f) : C(c,d) \to X(c)$ is a bijection.

### Interpretation

For emphasis, here is the interpretation of these three corollaries in words:

* **corollary I** says that the interpretation of presheaves on $C$ as generalized objects probeable by objects $c$ of $C$ is consistent: the probes of $X$ by $c$ are indeed the maps of generalized objects from $c$ into $X$;

* **corollary II** says that probes by objects of $C$ are sufficient to distinguish objects of $C$: two objects of $C$ are the same if they have the same probes by other objects of $C$.

* **corollary III** characterizes [[representable functor]]s by a [[universal property]] and is hence the bridge between the notion of [[representable functor]] and [[universal construction]]s.


## Generalizations

The Yoneda lemma tends to carry over to all important generalizations of the context of [[locally small category|categories]]:

* There is an analog of the Yoneda lemma in [[enriched category theory]]. See [[enriched Yoneda lemma]].

* In the context of [[module]]s (see also [[Day convolution]]) the Yoneda lemma becomes the important statement of [[Yoneda reduction]], which identifies the bimodule $\hom_C(-, -)$ as a unit bimodule.

* There is a [[Yoneda lemma for bicategories]].

* There is a [[Yoneda lemma for (∞,1)-categories]].

* In [[functional programming]], the Yoneda embedding is related to the [[continuation passing style]] transform.

* Formulation of the lemma in [[dependent type theory]]: [A type theoretical Yoneda lemma](http://homotopytypetheory.org/2012/05/02/a-type-theoretical-yoneda-lemma/) at [homotopytypetheory.org](http://homotopytypetheory.org)

## Related constructions

* [[Yoneda reduction]]

* [[co-Yoneda lemma]]

* [[Brown representability theorem]]

## Applications

* The Yoneda lemma is the or a central ingredient in various [[reconstruction theorem]]s, such as those of [[Tannaka duality]]. See there for a detailed account.

* In its incarnations as [[Yoneda reduction]] the Yoneda lemma governs the algebra of [[end]]s and [[coend]]s and hence that of [[bimodule]]s and [[profunctor]]s.

* The Yoneda lemma is effectively the reason that [[Isbell conjugation]] exists. This is a fundamental duality that relates [[geometry]] and [[algebra]] in large part of mathematics.

## References

The term _Yoneda lemma_ originated in an interview of [[Nobuo Yoneda]] by [[Saunders Mac Lane]] at Paris Gare du Nord:

* Yoshiki Kinoshita, [posting to catlist in 1996](http://www.mta.ca/~cat-dist/catlist/1999/yoneda).

In _[[Categories for the Working Mathematician]]_ MacLane writes that this happened in 1954.

<img src="http://ncatlab.org/nlab/files/YonedaObituary.jpg">


Reviews and expositions include

* [[Saunders MacLane]], _The Yoneda Lemma_, Mathematica Japonicae 47: 156 (1998)

* [[Tom Leinster]], _[[LeinsterYoneda.ps:file]]_

A discussion of the Yoneda lemma from the point of view of [[universal algebra]] is in

* [[Vaughan Pratt]], _The Yoneda lemma without category theory: algebra and applications_ ([pdf](http://boole.stanford.edu/pub/yon.pdf)).


[[!redirects yoneda lemma]]
[[!redirects Yoneda Lemma]]
[[!redirects Yoneda embedding lemma]]
[[!redirects Yoneda imbedding lemma]]
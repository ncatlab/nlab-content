
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

The **Yoneda lemma** says that the [[set]] of [[morphisms]] from a [[representable presheaf]] $y(c)$ into an arbitrary [[presheaf]] $X$ is in [[natural bijection]] with the set $X(c)$ assigned by $X$ to the representing [[object]] $c$.

The Yoneda lemma is an elementary but deep and central result in [[category theory]] and in particular in [[sheaf and topos theory]]. It is essential background behind the central concepts of _[[representable functors]]_, _[[universal constructions]]_, and _[[universal elements]]_. 


## Statement and proof
  {#StatementOfYonedaLemma}

+-- {: .num_defn #FunctorUnderlyingTheYonedaEmbedding}
###### Definition
**([[functor]] underlying the [[Yoneda embedding]])

For $\mathcal{C}$ a [[locally small category]] we write

$$
  [C^{op}, Set] \coloneqq Func(C^{op}, Set)
$$

for the [[functor category]] out of the [[opposite category]] of $\mathcal{C}$ into [[Set]].  

This is also called the _[[category of presheaves]]_ on $\mathcal{C}$.
Other notation used for it includes $Set^{C^{op}}$ or $Hom(C^{op},Set))$.

There is a [[functor]]

$$
  \array{
    C &\overset{y}{\longrightarrow}& [C^op,Set]
    \\
    c &\mapsto& Hom_{\mathcal{C}}(-,c)
  }
$$

(called the _[[Yoneda embedding]]_ for reasons explained below) from $\mathcal{C}$ to its [[category of presheaves]], which sends each [[object]] to the [[hom-functor]] into that object, also called the [[representable presheaf|presheaf represented]] by $c$.

=--

+-- {: .num_remark}
###### Remark
**([[Yoneda embedding]] is [[adjunct]] of [[hom-functor]])**

The Yoneda embedding functor $y \;\colon\; \mathcal{C} \to [\mathcal{C}^{op}, Set]$ from Def. \ref{FunctorUnderlyingTheYonedaEmbedding} is equivalently the [[adjunct]] of the [[hom-functor]]

$$
  Hom_{\mathcal{C}}
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
  \longrightarrow
  Set
$$

under the [[product category]]/[[functor category]] [[adjoint functor|adjunction]] 

$$
  Hom(C^{op} \times C, Set) 
    \stackrel{\simeq}{\to}
  Hom(C, [C^{op}, Set])
$$

in the [[closed monoidal category|closed]] [[monoidal category|symmetric monoidal category]] of categories.

=--



+-- {: .num_prop #YonedaLemma} 
###### Proposition
**([[Yoneda lemma]])**

Let $\mathcal{C}$ be a [[locally small category]], with [[category of presheaves]] denoted $[\mathcal{C}^{op},Set]$, according to Def. \ref{FunctorUnderlyingTheYonedaEmbedding}. 

For $X \in [\mathcal{C}^{op}, Set]$ any [[presheaf]], there is a canonical [[isomorphism]]

$$
  Hom_{[C^op,Set]}(y(c),X) \;\simeq\; X(c)
$$

between the [[hom-set]] of [[presheaf]] [[homomorphisms]] from the [[representable presheaf]] $y(c)$ to $X$, and the value of $X$ at $c$.



=--

This is the standard notation used mostly in pure [[category theory]] and [[enriched category theory]]. In other parts of the literature it is customary to denote the presheaf represented by $c$ as $h_c$. In that case the above is often written

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


The proof is by chasing the element $Id_c \in C(c, c)$ around both legs of a [[naturality square]] for a [[natural transformation]] $\eta: C(-, c) \to X$ (hence a homomorphism of presheaves): 

$$
  \array{
     C(c, c) 
       & \stackrel{\eta_c}{\to} & 
     X(c) & & & & Id_c & \mapsto & \eta_c(Id_c) & \stackrel{def}{=} & \xi \\ 
 _\mathllap{C(f, c)} \downarrow & & \downarrow _\mathrlap{X(f)} & & & & \downarrow & & \downarrow _\mathrlap{X(f)} & & \\ 
C(b, c) & \underset{\eta_b}{\to} & X(b) & & & & f & \mapsto & \eta_b(f) & & 
}
$$ 

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

where the first step is taking the component of a [[natural transformation]] at $c \in C$ and the second step is [[evaluation]] at $Id_c \in C(c,c)$. 

The inverse of this map takes $f \in X(c)$ to the natural transformation $\eta^f$ with components
$$
  \eta^f_d := X(-)(f) : C(d,c) \to X(d)
  \,.
$$

=-- 



## Corollaries

The Yoneda lemma has the following direct consequences. As the Yoneda lemma itself, these are as easily established as they are useful and important.

### corollary I: Yoneda embedding

The Yoneda lemma implies that the [[Yoneda embedding]] functor $y \colon C \to [C^op,Set]$ really is an _embedding_ in that it is a [[full and faithful functor]], because for $c,d \in C$ it naturally induces the isomorphism of Hom-sets.

$$
  [C^{op},Set](C(-,c),C(-,d)) \simeq (C(-,d))(c) = C(c,d)
$$


### corollary II: uniqueness of representing objects 

Since the [[Yoneda embedding]] is a [[full and faithful functor]], an [[isomorphism]] of [[representable functor|representable presheaves]] $y(c) \simeq y(d)$ must come from an [[isomorphism]] of the representing objects $c \simeq d$:

$$
  y(c) \simeq y(d) \;\; \Leftrightarrow \;\;
  c \simeq d
$$

### corollary III: universality of representing objects

A [[presheaf|presheaf]] $X \colon C^{op} \to Set$ is [[representable functor|representable]] precisely if the [[comma category|comma category]] $(y,const_X)$ has a [[terminal object]]. If a [[terminal object]] is $(d, g : y(d) \to X) \simeq (d, g \in X(d))$ then $X \simeq y(d)$.

This follows from unwrapping the definition of [[morphisms]] in the [[comma category]] $(y,const_X)$ and applying the Yoneda lemma to find

$$
  (y,const_X)((c,f \in X(c)), (d, g \in X(d)))
  \simeq
  \{
    u \in C(c,d) : X(u)(g) = f
  \}
  \,.
$$

Hence $(y,const_X)((c,f \in X(c), (d, g \in X(d))) \simeq pt$ says precisely that $X(-)(f) \colon C(c,d) \to X(c)$ is a bijection.

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

* There is a [[Yoneda lemma for tricategories]].

* There is a [[Yoneda lemma for (∞,1)-categories]].

* In [[functional programming]], the Yoneda embedding is related to the [[continuation passing style]] transform.

* Formulation of the lemma in [[dependent type theory]]: [A type theoretical Yoneda lemma](http://homotopytypetheory.org/2012/05/02/a-type-theoretical-yoneda-lemma/) at [homotopytypetheory.org](http://homotopytypetheory.org)

## Necessity of naturality

The assumption of naturality is necessary for the Yoneda lemma to hold. A simple counter-example is given by a category with two objects $A$ and $B$, in which $Hom(A,A) = Hom(A,B) = Hom(B,B) = \mathbb{Z}_{\geq 0}$, the set of integers greater than or equal to $0$, in which $Hom(B,A) = \mathbb{Z}_{\geq 1}$, the set of integers greater than or equal to $1$, and in which composition is addition. Here it is certainly the case that $Hom(A,-)$ is isomorphic to $Hom(B,-)$ for any choice of $-$, but $A$ and $B$ are not isomorphic (composition with any arrow $B \rightarrow A$ is greater than or equal to $1$, so cannot have an inverse, since $0$ is the identity on $A$ and $B$).

A finite counter-example is given by the category with two objects $A$ and $B$, in which $Hom(A,A) = Hom(A,B) = Hom(B,B) = \{0, 1\}$, in which $Hom(B,A) = \{0, 2\}$, and composition is multiplication modulo 2. Here, again, it is certainly the case that $Hom(A,-)$ is isomorphic to $Hom(B,-)$ for any choice of $-$, but $A$ and $B$ are not isomorphic (composition with any arrow $B \rightarrow A$ is $0$, so cannot have an inverse, since $1$ is the identity on $A$ and $B$).

## The Yoneda lemma in semicategories

An interesting phenomenon arises in the case of [[semicategory|semicategories]] i.e. "categories" (possibly) lacking [[identity morphisms]]: 

the Yoneda lemma fails in general, since its validity in a semicategory $\mathcal{G}$ implies that $\mathcal{G}$ is in fact already a category because the Yoneda lemma permits to embed $\mathcal{G}$ into $PrSh(\mathcal{G})$ and the latter is always a category, the embedding then implying that $\mathcal{G}$ is itself a category!

But for [[regular semicategories]] $\mathcal{R}$ there is a [[unity of opposites]] in the category of all [[semipresheaves]] on $\mathcal{R}$ between the so called regular presheaves that are [[colimits]] of [[representable presheaf|representables]] and presheaves satisfying the Yoneda lemma, whence _the Yoneda lemma holds dialectically for regular presheaves!_ 

For some of the details see at _[[regular semicategory]]_ and the references therein.

## Applications

* The Yoneda lemma is the or a central ingredient in various [[reconstruction theorem]]s, such as those of [[Tannaka duality]]. See there for a detailed account.

* In its incarnations as [[Yoneda reduction]] the Yoneda lemma governs the algebra of [[end]]s and [[coend]]s and hence that of [[bimodule]]s and [[profunctor]]s.

* The Yoneda lemma is effectively the reason that [[Isbell conjugation]] exists. This is a fundamental duality that relates [[geometry]] and [[algebra]] in large part of mathematics.

## Related entries

* [[Yoneda reduction]]

* [[co-Yoneda lemma]]

* [[Yoneda structure]]

* [[Brown representability theorem]]

* [[continuation-passing style]]

* [[regular semicategory]]

* [[Yoneda lemma for (∞,1)-categories]]

\linebreak

## References
 {#References}

For general references see any text on [[category theory]], as listed in the references [there](category+theory#References).

The term _Yoneda lemma_ originated in an interview of [[Nobuo Yoneda]] by [[Saunders Mac Lane]] at Paris Gare du Nord:

* Yoshiki Kinoshita, [posting to catlist in 1996](http://www.mta.ca/~cat-dist/catlist/1999/yoneda).

In _[[Categories for the Working Mathematician]]_ MacLane writes that this happened in 1954.

<img src="http://ncatlab.org/nlab/files/YonedaObituary.jpg">


Reviews and expositions include

* [[Saunders MacLane]], _The Yoneda Lemma_, Mathematica Japonicae 47: 156 (1998)

* [[Tom Leinster]], _[[LeinsterYoneda.ps:file]]_ 

* [[Emily Riehl]], _Category Theory in Context. Chapter 2. Universal Properties, Representability, and the Yoneda Lemma_ [pdf](http://www.math.jhu.edu/~eriehl/context.pdf)

* {#RRZ2004} Marie La Palme Reyes, Gonzalo E. Reyes, and Houman Zolfaghari, _Generic figures and their glueings: A constructive approach to functor categories_, Polimetrica sas, 2004 ([author page](https://reyes-reyes.com/2004/06/01/generic-figures-and-their-glueings-a-constructive-approach-to-functor-categories/),[pdf](https://marieetgonzalo.files.wordpress.com/2004/06/generic-figures.pdf)).

* [[Paolo Perrone]], _Notes on Category Theory with examples from basic mathematics_, Chapter 2. ([arXiv](http://arxiv.org/abs/1912.10642))

A discussion of the Yoneda lemma from the point of view of [[universal algebra]] is in

* [[Vaughan Pratt]], _The Yoneda lemma without category theory: algebra and applications_ ([pdf](http://boole.stanford.edu/pub/yon.pdf)).

A treatment of the Yoneda lemma for [[internal category in an (infinity,1)-category|categories internal to an (∞,1)-topos]] is in 

* Louis Martini, _Yoneda's lemma for internal higher categories_, ([arXiv:2103.17141](https://arxiv.org/abs/2103.17141))


[[!redirects yoneda lemma]]
[[!redirects Yoneda Lemma]]
[[!redirects Yoneda embedding lemma]]
[[!redirects Yoneda imbedding lemma]]
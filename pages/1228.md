
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is sometimes called the _co-Yoneda lemma_ is a basic fact about [[presheaves]] (a basic fact of [[topos theory]]): it says that every [[presheaf]] is a [[colimit]] of [[representable functor|representables]] and more precisely that it is the "colimit over itself of all the representables contained in it".

One might think of this as related by [[duality]] to the [[Yoneda lemma]], hence the name.

## Every presheaf is a colimit of representables
 {#EveryPresheafIsAColimitOfRepresentables}

Throughout, let 

* $V$ be a [[closed monoidal category|closed]] [[symmetric monoidal category]] (for instance $V = $ [[Set]] with its [[Cartesian product]]);

* $\mathcal{C}$ a [[small category|small]] $V$-[[enriched category]].

For $c,d \in Obj(\mathcal{V})$ two objects, we write $\mathcal{C}(c,d) \in V$ for the [[hom-object]].

+-- {: .num_remark}
###### Remark
**([[Yoneda reduction]])**

Recall that the ([[enriched Yoneda lemma|enriched]]) [[Yoneda lemma]] says that for $F \colon \mathcal{C}^{op} \to V$ a $V$-[[enriched functor]] out of the [[opposite category]] of $\mathcal{C}$, hence a $V$-valued [[presheaf]] on $\mathcal{C}$ and $c \in \mathcal{C}$ an [[object]] of $\mathcal{C}$, there is a [[natural isomorphism]] in $V$

$$
  [\mathcal{C}^{op},V](\mathcal{C}(-,c), F) \simeq F(c)
  \,,
$$

where on the left we have the [[hom-object]] in the [[enriched functor category]] between the [[representable functor|functor represented]] by $c$ and the given functor $F$.

Using the expression of these hom-objects on the left as _[[ends]]_, this reads

$$
  \int_{c' \in \mathcal{C}} V(\mathcal{C}(c',c), F(c')) \simeq F(c)
  \,.
$$

In this form the Yoneda lemma is also referred to as _[[Yoneda reduction]]_.

=--

Under [[duality|abstract duality]] an [[end]] turns into a [[coend]], so a co-Yoneda lemma ought to be a similarly fundamental expression for $F(c)$ in terms of a [[coend]].

The natural candidate is the statement that:


+-- {: .num_prop #coYonedaLemma}
###### Proposition

Every [[presheaf]] $F$ is a [[colimit]] of [[representable functor|representables]], in that

$$
  F(c) \simeq \int^{c' \in C} \mathcal{C}(c,c')\otimes F(c')
$$

hence

$$
  F(-) \simeq \int^{c' \in \mathcal{C}} Y(c')\otimes F(c')
  \,,
$$

where $Y$ denotes the [[Yoneda embedding]]. In [[module]]-language, using the [[tensor product of functors]], this reads

$$
  F(c) \simeq \mathcal{C}(c,-)\otimes_{\mathcal{C}} F
  \,.
$$

Yet another way to state this is as a [[colimit]] over the [[comma category]] $(Y,F)$, for $Y$ the [[Yoneda embedding]]:

$$
  F \simeq colim_{(U \to F) \in (Y,F)} Y(U)
  \,.
$$


=--

This statement we call the **co-Yoneda lemma**.



+-- {: .proof}
######Proof

To show that a presheaf $F \colon \mathcal{C}^{op} \to V$ is canonically presented as a colimit of representables, we exhibit a natural isomorphism 

$$
  \int^{c} F(c) \otimes \mathcal{C}(-, c) 
   \;\cong\; 
  F
$$

By the definition of the [[coend]], maps 

$$
  \int^c F(c) \times \mathcal{C}(-, c) \to G(-)
$$ 

are in [[natural bijection]] with families of maps 

$$
  F(c) \otimes \mathcal{C}(d, c) \to G(d)
$$ 

[[extranatural transformation|extranatural]] in $c$ and [[natural transformation|natural]] in $d$. Those are in natural bijection with families of maps 

$$
  F(c) \to V(\mathcal{C}(d, c), G(d))
$$ 

natural in $c$ and extranatural in $d$. These are in natural bijection with families of maps 

$$
  F(c) \to Nat(\mathcal{C}(-, c), G) \cong G(c)
$$ 

(natural in $c$), where the isomorphism is by the Yoneda lemma. Thus we have exhibited a natural isomorphism 

$$
  Nat(\int^c F(c) \times \mathcal{C}(-, c), G) \cong Nat(F, G)
$$ 

(natural in $G$). By Yoneda again, this gives 

$$
  \int^c F(c) \times \mathcal{C}(-, c) \cong F
  \,.
$$
 
=--

+-- {: .num_remark}
###### Remark

The statement of the [[co-Yoneda lemma]] in prop. \ref{coYonedaLemma} is a kind of [[categorification]] of the following statement in [[analysis]] (whence the notation with the integral signs):

For $X$ a [[topological space]], $f \colon X \to\mathbb{R}$ a [[continuous function]] and $\delta(-,x_0)$ denoting the [[Dirac distribution]], then

$$
  \int_{x \in X} \delta(x,x_0) f(x)
  = 
  f(x_0)
  \,.
$$

=--



+-- {: .num_remark}
###### Remark

If one follows the Yoneda-lemma argument at the end of the proof of prop. \ref{coYonedaLemma}, one arrives at the explicit isomorphism 

$$
  \int^c F(c) \times \mathcal{C}(-, c) \to F
  \,.
$$ 

Namely, it corresponds to the family of maps 

$$
  F(c) \times \mathcal{C}(d, c) \to F(d)
$$ 

(extranatural in $c$ and natural in $d$) which in turn corresponds to the natural family 

$$
  \mathcal{C}(d, c) \to \hom(F(c), F(d))
$$ 

associated with the structure of the functor $F \colon \mathcal{C}^{op} \to V$. 

=--

+-- {: .num_example #CoYonedaInSetViaCoequalizer}
###### Example

Let $V = $ [[Set]], and recall the definition of the [[coend]] as a [[coequalizer]]

$$
  \underset{c,d \in \mathcal{C})}{\coprod} 
   \mathcal{C}(c,d) \times \mathcal{C}(c_0,c) \times F(d)
   \underoverset
     {\underset{\underset{c,d}{\sqcup} \rho_{(d,c)}(c) }{\longrightarrow}}
     {\overset{\underset{c,d}{\sqcup} \rho_{(c,d)}(d) }{\longrightarrow}}
     {\phantom{AAAAAAAA}}
  \underset{c \in \mathcal{C}}{\coprod} \mathcal{C}(c_0,c) \times F(c)
   \overset{coeq}{\longrightarrow}
  \overset{c\in \mathcal{C}}{\int} \mathcal{C}(c_0,c) \times F(c)
  \,.
$$

This says that the coend is the set of [[equivalence classes]] of [[pairs]]

$$
  ( c_0 \overset{}{\to} c,\; x \in F(c) )
  \,,
$$

where two such pairs

$$
  ( c_0 \overset{f}{\to} c,\; x \in F(c) )
  \,,\;\;\;\;
  ( c_0 \overset{g}{\to} d,\; y \in F(d) )  
$$

are regarded as equivalent if there exists

$$
  c \overset{\phi}{\to} d
$$

such that 

$$
  g = \phi \circ f
  \,,
  \;\;\;\;\;and\;\;\;\;\;
  x = \phi^\ast(y)
  \,.
$$

(Because then the two pairs are the two images of the pair $(f,y)$ under the two morphisms being coequalized.)

But now considering the case that $c = c_0$ and $f = id_{c_0}$, so that $g= \phi$ shows that any pair

$$
  ( c_0 \overset{\phi}{\to} d, \; y \in F(d))
$$

is identified, in the coequalizer, with the pair

$$
  (id_{c_0},\; \phi^\ast(y) \in F(c_0))
  \,,
$$ 

hence with $\phi^\ast(y)\in F(c_0)$, and that this coequalizing operation is the action

$$
  Hom(c_0,d)\times F(d)\longrightarrow F(c_0)
$$

of morphisms on elements of the presheaf by pullback.


=--


## MacLane's co-Yoneda lemma
 {#MacLanesCoYonedaLemma}

In a brief uncommented exercise on [MacLane, p. 62](#MacLane)  
the following statement, which is attributed to Kan, is called the **co-Yoneda lemma**.


For $D$ a [[category]], [[Set]] the [[category]] of [[set]]s, $K : D \to Set$ a [[functor]], let $(* \darr K)$ be the [[comma category]] of elements $x \in K d$, let $\Pi: (* \darr K) \to D$ be the projection $(x \in K d) \mapsto d$ and let for each $a \in D$  the functor $\Delta_a: (* \darr K) \to D$ be the diagonal functor sending everything to the constant value $a$. 

The **co-Yoneda lemma in the sense of Kan/MacLane** is the statement that there is a [[natural isomorphism]] of [[functor category|functor categories]]

$$
[D,Set](K, D(a, -)) \cong [(*\darr K), D](\Delta_a, \Pi).
$$

Here is an outline of an explicit proof:

+-- {: .proof}
######Proof

A natural transformation $\phi: K \to D(a, -)$ assigns to each element $x \in K c$ an element $\phi_c(x) \in D(a, c)$, i.e., an arrow $\phi_c(x): a \to c$. We define a corresponding transformation $\psi: \Delta_a \to \Pi$ which assigns to each object $(c, x \in K c)$ in $(*\darr K)$ the morphism $\phi_c(x): a \to c = \Pi(c, x)$. It is easy to check that the naturality condition on $\phi$ corresponds to the naturality condition on $\psi$, and that the correspondence is bijective.   

=--

Here is a more conceptual proof in terms of [[comma categories]]:

+-- {: .proof}
######Proof

[[Set]] classifies discrete fibrations, in the sense that a functor $G : D \to Set$ classifies the discrete [[fibration]]

$$
  Q : \Pi_G : El(G) \to D
$$

and natural transformations $\alpha : G \to F$ correspond to maps of fibrations 

$$
  El(G) \to El(f)
$$

i.e. functor which commute on the nose with the projections $\Pi_G$, $\Pi_F$ to the base category $D$).


This applies in particular to $F = hom(a,-)$. Notice the [[category of elements]] $El(hom(a,-))$ is the co-slice $(a \downarrow D)$, with its usual projection $\Pi$ to $D$.

However, the [[comma category]] $(a \downarrow D)$ is the "lax pullback" (really, the [[comma object]], the discussion at [[2-limit]]) appearing in

$$
  \array{
    (a \downarrow D) &\stackrel{\Pi}{\to}& D
    \\
    \downarrow &\Uparrow& \downarrow^{Id}
    \\
    * &\stackrel{a}{\to}& D
  }  
$$

and so a fibration map $El(G) \to (a \downarrow D)$ corresponds exactly to a lax square

$$
  \array{
    El(G) &\stackrel{\Pi_G}{\to}& D
    \\
    \downarrow &\Uparrow& \downarrow^{Id}
    \\
    * &\stackrel{a}{\to}& D
  }    
   \,.
$$


This yields the co-Yoneda lemma in the sense of MacLane's exercise.

=--

## References

For enrichment over $V = Top^{\ast/}_{cg}$  ([[pointed topological spaces|pointd]] [[compactly generated topological spaces]]) the co-Yoneda lemma in the sense of [every presheaf is a colimit of representables](#EveryPresheafIsAColimitOfRepresentables) appears for instance as

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], lemma 1.6 of _[[Model categories of diagram spectra]]_, Proceedings London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))

The [co-Yoneda lemma in the sense of MacLane](#MacLanesCoYonedaLemma) appears as a brief uncommented exercise on p. 63 of 

* {#MacLane} [[Saunders MacLane]], _[[Categories Work|Categories for the Working Mathematician]]_,
 
where it is attributed to [[Daniel Kan]].


[[!redirects Coyoneda lemma]]
[[!redirects coYoneda lemma]]
[[!redirects co-yoneda lemma]]
[[!redirects coyoneda lemma]]
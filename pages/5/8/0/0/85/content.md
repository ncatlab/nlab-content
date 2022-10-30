+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Just as we can convolve [[function|functions]] $f : M \to \mathbb{C}$ where $M$ is a [[group]], or more generally a [[monoid]], we can convolve [[functor|functors]] $f: M \to Set$ where $M$ is a [[monoidal category]].  So, for any monoidal category $M$, the [[functor category]] $Set^M$ becomes a monoidal category in its own right.  The tensor product in $Set^M$ is called **Day convolution** ([Day 70](#Day70)).

This may be generalized by replacing [[Set]] with a more general [[cocomplete category|cocomplete]] [[symmetric monoidal category]] $V$. The technical condition is that the tensor product $u \otimes v$ must preserve colimits in the separate arguments $u$ and $v$; that is, that the functors $u \otimes -$ and $- \otimes v$ must preserve colimits. This occurs when for instance $V$ is symmetric monoidal closed (so that these functors are left adjoints). 

## Definition

### For monoidal categories

For $(C, \otimes)$ a [[monoidal category]] and $F, G : C^{op} \to Set$ two [[presheaf|presheaves]] on $C$, their _Day convolution product_ $F \star G$ is the presheaf given by the [[coend]]

$$
  F \star G
  \coloneqq
  \int^{c,d \in C}
  F(c) \times G(d) \times Hom_C(-, c \otimes d)
  \,.
$$


### For promonoidal categories

In the original article ([Day 70](#Day70)), a stronger form of the convolution is discussed, in which $A$ is assumed only to be a [[promonoidal category]].

Let $V$ be a [[Benabou cosmos]], and $A$ a small $V$-[[enriched category]].


+-- {: .num_prop}
###### Proposition
There is an equivalence of categories between the category of [[pro-monoidal structures]] on $A$ with strong pro-monoidal functors between them and the category of biclosed monoidal structures on $V^{A^{op}}$ with strong monoidal functors between them.  
=--

+-- {: .proof}
###### Proof

...

=--



## Properties 
  {#Properties}

Let $j : C \to PSh(C)$ be the [[Yoneda embedding]]. 

+-- {: .num_lemma}
###### Lemma

With $I \in C$ the tensor unit of $C$, the presheaf $j(I)$ is a unit for the Day convolution product.

=--

+-- {: .proof}
###### Proof

Using the [[co-Yoneda lemma]] on the two [[coend]]s we have

$$
  \begin{aligned}
  F \star j(I)
  &  \simeq
  \int^{c,d \in C}
  F(c) \times Hom_C(d,I)
  \times
  Hom_C(-, c\otimes d)
  \\
  & \simeq
  \int^{c \in C}
  F(c) \times Hom_C(-, c \otimes I)
  \\
  & \simeq
  \int^{c \in C}
  F(c) \times Hom_C(-, c)
  \\
  & \simeq
  F(-)
  \end{aligned}
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

For $C$ a small [[monoidal category]], regard the [[category of presheaves]] $(PSh(C), \star, j(I))$ as a [[monoidal category]] with tensor product the Day convolution product and unit the unit of $C$ under the [[Yoneda embedding]] $j : C \hookrightarrow PSh(C)$. 

Then

1. $(PSh(C), \star, j(I))$ is a [[closed monoidal category]];

1. the [[Yoneda embedding]] constitutes a strong [[monoidal functor]] $(C,\otimes, I) \hookrightarrow (PSh(C), \star, j(I))$.

=--

+-- {: .proof}
###### Proof

In analogy to the cartesian [[closed monoidal structure on presheaves]]
we see that if the [[internal hom]] in $PSh(C)$ exists at all, 
(with $[F,-]$ [[right adjoint]] to $(-) \star F$) then by the [[Yoneda lemma]] it has to be given by

$$
  \begin{aligned}
    [F,G](c) & \simeq Hom_C(j(c), [F,G])
    \\
    &\simeq Hom_C(j(c)\star F, G)
  \end{aligned}
  \,.
$$

...

=--



## Examples

+-- {: .num_example}
###### Example

Let $C$ be a [[discrete category]] over a set, which is hence a [[monoid]] (for instance a [[group]]) with product $\cdot$. 


Then the Day convolution product is

$$
  F \star G : e \mapsto \oplus_{c \cdot d = e} F(c) \times G(d)
  \,.
$$

Notice that if we regard the presheaves $F$ and $G$ here, assuming they take values in finite sets, as [[vertical categorification|categorifications]] of $\mathbb{N}$-valued functions $|F|, |G| : C \to \mathbb{N}$, where $|\cdot| : Set \to \mathbb{N}$ is the cardinality operation on finite sets, then this reproduces precisely the ordinary convolution product of these $\mathbb{N}$-valued functions

$$
  \begin{aligned}
    |F \star G| : e &\mapsto 
       \sum_{c,d \in C}
        |F(c)| \times |G(d)| \times \delta(e, c \otimes d)       
       & =
       \sum_{c \cdot d = e} |F(c)| \cdot |F(d)|
  \end{aligned}
$$

This uses in particular that for every object $c \in C$ the functor

$$
  Hom_C(c,-) = \delta_c
$$

is in this sense the Kronecker delta-function on the set $C$ supported at $c \in C$. Precisely because by assumption $C$ has only identity morphisms.

$$
 Hom_C(c,d) = \left\{ \array{
   * & if c = d
   \\
   \emptyset & if c \neq d
 } \right.
$$


=--

Further examples:

* There is an obvious monoidal structure on the [[cube category]]. By Day convolution this induces a monoidal structure on [[cubical set|cubical sets]]. This in turn induces a monoidal structure on [[strict omega-category|strict omega-categories]].

* There is a monoidal structure on the [[augmented simplex category]] which by Day convolution induces a monoidal structure on the category of [[augmented simplicial sets]], which by restriction induces the [[join of simplicial sets|join operation]] on [[simplicial sets]].

* If $C$ is a [[large category]] in one [[universe]], then its [[universe enlargement]] to a bigger universe can be given a closed monoidal structure via Day convolution.

* The [[semantics]] of [[linear logic]] obtained from Girard's "phase spaces", or more generally from [[ternary frames]], is essentially Day convolution for [[posets]].


+-- {: .num_example #SymmetricSmashProductOfSpectra}
###### Example

The [[symmetric smash product of spectra]] on, in particular,  [[symmetric spectra]] and  [[orthogonal spectra]] is the Day convolution product for [[Top]]-[[enriched functors]] on monoidal categories of [[symmetric groups]] of [[orthogonal groups]], respectively ([MMSS 00, theorem 1.7 and section 21.](#MMSS00)).

Similarly the [[symmetric smash product of spectra]] on the [[model structure for excisive functors]] is Day convolution for [[sSet]]-[[enriched functors]] on the plain [[smash product]] of finite pointed [[simplicial sets]] ([Lydakis 98](#Lydakis98)).

See also at _[[functor with smash products]]_.

=--

## Related concepts

* [[monoidal topos]]

## References
 {#References}

The concept originates in

* {#Day70} [[Brian Day]], _On closed categories of functors_, Reports of the Midwest Category Seminar IV, Lecture Notes in Mathematics Vol. 137. Springer-Verlag, 1970, pp 1-38

General discussion includes

* [[Todd Trimble]] on Day convolution [here](http://golem.ph.utexas.edu/category/2008/01/the_concept_of_a_space_of_stat.html#c014365)

The application of Day convolution to the construction of [[symmetric smash products of spectra]] for [[highly structured spectra]] is due to

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _Model Categories of Diagram Spectra_, Proceedings London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))

and for [[excisive functors]] due to

* {#Lydakis98} Lydakis, _Simplicial functors and stable homotopy theory_ Preprint, available via Hopf archive, 1998 ([pdf](http://hopf.math.purdue.edu/Lydakis/s_functors.pdf))



(see also at [[functors with smash product]]).


Day convolution for [[(∞,1)-categories]] is discussed in

* Saul Glasman, _Day convolution for infinity-categories_ ([arXiv:1308.4940](http://arxiv.org/abs/1308.4940))


[[!redirects Day convolutions]]

[[!redirects day convolution]]


[[!redirects Day tensor product]]
[[!redirects Day tensor products]]

[[!redirects Day convolution product]]
[[!redirects Day convolution products]]


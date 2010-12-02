
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
* automatic table of contents goes here
{:toc}

## Idea

Just as we can convolve [[function|functions]] $f : M \to \mathbb{C}$ where $M$ is a [[group]], or more generally a [[monoid]], we can convolve [[functor|functors]] $f: M \to Set$ where $M$ is a [[monoidal category]].  So, for any monoidal category $M$, the [[functor category]] $Set^M$ becomes a monoidal category in its own right.  The tensor product in $Set^M$ is called **Day convolution**, named after [[Brian Day]].

We can generalize this idea by replacing [[Set]] with a more general [[cocomplete category|cocomplete]] [[symmetric monoidal category]] $V$. The technical condition is that the tensor product $u \otimes v$ must preserve colimits in the separate arguments $u$ and $v$; that is, that the functors $u \otimes -$ and $- \otimes v$ must preserve colimits. This occurs when for instance $V$ is symmetric monoidal closed (so that these functors are left adjoints). 

## Definition

For $(C, \otimes)$ a [[monoidal category]] and $F, G : C^{op} \to Set$ two [[presheaf|presheaves]] on $C$, their _Day convolution product_ $F \star G$ is the presheaf given by the [[end|coend]]

$$
  F \star G
  :=
  \int^{c,d \in C}
  F(c) \times G(d) \times Hom_C(-, c \otimes d)
  \,.
$$


## Properties {#Properties}

Let $j : C \to PSh(C)$ be the [[Yoneda embedding]]. 

+-- {: .un_lemma}
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


+-- {: .un_prop}
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

* Let $C$ be a [[discrete category]] over a set, which is hence a [[monoid]] (for instance a [[group]]) with product $\cdot$. 


Then the above convolution product is

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


* There is an obvious monoidal structure on the [[cube category]]. By Day convolution this induces a monoidal structure on [[cubical set|cubical sets]]. This in turn induces a monoidal structure on [[strict omega-category|strict omega-categories]].

* If $C$ is a [[large category]] in one [[universe]], then its [[universe enlargement]] to a bigger universe can be given a closed monoidal structure via Day convolution.

## Blog resources

* [[Todd Trimble]] on Day convolution [here](http://golem.ph.utexas.edu/category/2008/01/the_concept_of_a_space_of_stat.html#c014365)

## Discussion

_[[Eric Forgy|Eric]] says_: When I see "convolution", I think "Fourier transform". Is Day convolution somehow related to a categorified version of Fourier transforms?

_[[Todd Trimble|Todd]] says_: Yes, something like that. I talk a little about this in the article on [[operad|operads]], in the detailed theoretical section. 

The usual Fourier transform (for periodic functions) passes between Fourier coefficients $a_n$ and functions $\sum_n a_n z^n$ on $S^1$. One way of categorifying this is to pass from the category of functors $a: \mathbb{N} \to Set$ (considered as a monoidal category with respect to Day convolution) to their so-called "analytic functors" $\hat{a}: Set \to Set$, mapping a set $x$ to $\hat{a}(x) = \sum_n a_n \cdot x^n$. The "categorified Fourier transform" $a \mapsto \hat{a}$ takes Day convolution products to (pointwise) cartesian products. 

If the "Fourier transform" is properly formulated (using enriched tensor products), then the same holds for any monoidal category in place of the discrete monoidal category $\mathbb{N}$. 

_[[AnonymousCoward]] says_: The passage to analytic functors seems more like a z-transform or Laplace transform. In the particular case of species, it is the Laplace transform formula that applies to the analytic functor of a derivative of a species, not the Fourier transform one involving multiplication by the imaginary unit.

The use of hom above is reminiscent of the Dirac delta. Is there a connection?

_[[John Baez]] says_: It's true that the passage from a sequence $a_n$ to a power series $\sum_n a_n z^n$ is precisely the $z$-transform.  If we set $z = exp(i \theta)$, we get the Fourier transform --- but as you note this makes use of the imaginary unit $i$, which plays no evident role in Day convolution.  So, the analogies Todd is discussing become most precise if we work with the $z$-transform.  But the Fourier transform is closely related.

On the other hand, I've discovered that many 'pure mathematicians' don't know about the $z$-transform --- at least, not under that name.  I think it's 'engineers' who talk most about the $z$-transform.  So, if you're trying to explain Day convolution to pure mathematicians, it's pedagogically best to start talking about the Fourier transform, and then later mention the $z$-transform.

In general $hom$ is a categorified version of an inner product.  I'm too lazy to figure out how this is related to the Dirac delta, but I would not be surprised if there were a connection.

[[Urs Schreiber|Urs]]: maybe all that "anonymous coward" is looking for is this statement: 

if $C$ is a discrete category (i.e. just a set regarded as a category with only identity morphisms) then a functor $C \o Set$ is like a $\mathb{Z}$-valued function on the set $C$ and then for every object $c$ in $C$ the functor $Hom_C(c,-) = \delta_c$ is the Kronecker delta on $C$ at $c$, in that 

$$
 Hom_C(c,d) = \left\{ 
  \array{
   * & if c = d
   \\
   \emptyset & if c \neq d
 } \right.
$$

I have added this remark now explicitly to the entry above.


[[!redirects day convolution]]
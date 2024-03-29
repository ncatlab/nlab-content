
> This entry discusses line objects, their multiplicative groups and additive groups in generality. For the traditional notions see at _[[affine line]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents 
{:toc}

## In linear algebra

In [[linear algebra]] over a [[field]] $k$, the __line__ is the field $k$ regarded as a [[vector space]] over itself. More generally, _a line_ is a vector space [[isomorphic]] to this, i.e. any 1-dimensional $k$-vector space.

The [[real line]] $\mathbb{R}$ models the naive intuition of the geometric line in [[Euclidean geometry]]. See also at _[[complex line]]_.

In many contexts of modern mathematics, however, _line_ implicitly refers to the complex line $\mathbb{C}$ (which as a real vector space is the [[complex plane]]!). For instance this is the line usually meant when speaking of [[line bundle]]s.

## Over an algebraic theory

We discuss here how in the context of [[space]]s modeled on duals of [[algebra over a Lawvere theory|algebras over]] an [[algebraic theory]] $T$, there is a canonical space $\mathbb{A}_T$ which generalizes the [[real line]] $\mathbb{R}$. 

### Definition

For $T$ (the [[syntactic category]] of) any [[Lawvere theory]] we have that [[Isbell conjugation]] 

$$
  (\mathcal{O} \dashv Spec)\colon 
   T Alg^{op} \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
   Sh(C)
$$

relates $T$-algebras to the [[sheaf topos]] over duals $T \hookrightarrow C \subset T Alg^{op}$ of $T$-algebras, for $C$ a [[small category|small]] [[full subcategory]] with [[subcanonical coverage]].

By the [free T-algebra adjunction](http://ncatlab.org/nlab/show/Lawvere+theory#FreeAlgebras)

$$
  (F_T \dashv U_T)\colon T Alg \stackrel{\overset{F_T}{\leftarrow}}{\underset{U_T}
{\to}}
  Set
$$

we have the free $T$-algebra $F_T(*) \in TAlg$ on a single generator.

+-- {: .num_defn}
###### Definition

The **$T$-line object** is 

$$
  \mathbb{A}_T \coloneqq Spec F_T(*) \in Sh(C)
  \,.
$$

=--


### The additive group object
 {#AdditiveGroupObject}

For $\mathcal{Ab}$ the [[Lawvere theory]] of [[abelian group]]s, say that a morphism $ab\colon \mathcal{Ab} \to T$ of Lawvere theories is an **abelian Lawvere theory**. Algebras over abelian Lawvere theories have underlying abelian groups

$$
  (ab_* \dashv ab^*)\colon
  T Alg \stackrel{\overset{ab_*}{\leftarrow}}{\underset{ab^*}{\to}}
  Ab
  \,.
$$

+-- {: .num_defn}
###### Definition

For $T$ an abelian Lawvere theory, by its underlying abelian group we have that $\mathbb{A}_T$ inherits the structure of an abelian [[group object]] in $Sh(C)$. Write

$$
  \mathbb{G}_T \in Ab(Sh(C))
$$

for this group object on $\mathbb{A}_T$.

=--

### The multiplicative group object
 {#MultiplicativeGroup}


+-- {: .num_defn}
###### Definition

For $\mathbb{A}_T$ a line object, write

$$
  (\mathbb{A}_T^\times \hookrightarrow \mathbb{A}_T)
  \in Sh(C)
$$

be the maximal [[subobject]] of the line on those [[generalized element|elements]] that have [[inverses]] under the multiplication $\mathbb{A}_T \times \mathbb{A}_T \to \mathbb{A}_T$.

This is called the **multiplicative group** of the line object, often denoted $\mathbb{G}_m$.

=--

### The group of roots of unity

See at _[[roots of unity]]_.

### Examples

* For $T$ the theory of ordinary commutative [[associative algebras]] over a [[ring]] $R$, we have that 

  * $\mathbb{A}_T = \mathbb{A}_R$ is what is the _[[affine line]]_ over $R$;

  * $\mathbb{G}_m$ is the standard [algebraic multiplicative group](affine+line#MultiplicativeGroup);

  * $\mathbb{G}_a$ is the standard [algebraic additive group](affine+line#AdditiveGroup).

* For $T \coloneqq Smooth \coloneqq$ [[CartSp]] the theory of [[smooth algebra]]s, we have that $\mathbb{A}_{Smooth} = \mathbb{R}$ is the [[real line]] regarded as a [[diffeological space]].

  The additive group in this case the the additive [[Lie group]] of [[real numbers]]. The multiplicative group is the Lie group $\mathbb{R}^\times = \mathbb{R} - \{0\}$ of non-zero real numbers under multiplication.

See also _[[analytic affine line]]_.

#### Properties

##### Cohomology

For $R$ a [[ring]] and $H^n_{et}(-,-)$ the [[etale cohomology]], $\mathbb{G}_m$ the [[multiplicative group]] of the [[affine line]]; then

* $H^0_{et}(R, \mathbb{G}_m) = R^\times$ ([[group of units]])

* $H^1_{et}(R, \mathbb{G}_m) = Pic(R)$ ([[Picard group]]: iso classes of invertible $R$-modules)

* $H^2_{et}(R, \mathbb{G}_m) = Br(R)$ ([[Brauer group]] Morita classes of Azumaya $R$-algebras)

### Related concepts

* [[function algebra]]

* [[formal multiplicative group]]

* [[exponential exact sequence]]

* [[affine modality]]

* [[Picard scheme]], [[Picard modality]]

### References

The notion of a line object over general abelian Lawvere theories has been considered in

* [[nLab:Herman Stel]], _[[schreiber:master thesis Stel|∞-Stacks and their Function Algebras -- with Applications to ∞-Lie Theory]]_ (2010)
{#Stel}

in the context of [[function algebras on ∞-stacks]].


## In a monoidal category

Given a [[monoidal category]] $C$, one may define a _line object in $C$_ to be an object $L$ such that the tensoring [[functor]]  $- \otimes L : C \to C$ has an [[inverse]].

## Related concepts

* [[2-line]]

[[!include moduli of higher lines -- table]]

[[!redirects line object]]
[[!redirects line objects]]

[[!redirects line]]
[[!redirects lines]]

[[!redirects multiplicative group]]
[[!redirects additive group]]
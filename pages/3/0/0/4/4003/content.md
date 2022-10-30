
> This entry is about a notion in [[category theory]]. For a different notion of the same name in ([[stable homotopy theory|stable]]) [[homotopy theory]] see at _[[Goodwillie calculus]]_. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Polynomial functors
* table of contents
{: toc}

## Idea

The concept of _polynomial functor_ is a [[categorification]] of that of _[[polynomial]]_. 

Polynomial endo-functors are used to encode a class of [[inductive types]] called _[[W-types]]_.

## Definition

Let $C$ be a [[locally cartesian closed category]].  A **polynomial functor** is specified by the data
$$ W \overset{f}{\leftarrow} X \overset{g}{\to} Y \overset{h}{\to} Z $$
in $C$.  The resulting functor is the composite

$$ 
  C/W 
   \overset{f^*}{\to} 
  C/X 
   \overset{\Pi_g}{\to} 
  C/Y 
   \overset{\Sigma_h}{\to} 
  C/Z
  \,, 
$$

where $\Pi_g$ and $\Sigma_h$ are the [[dependent product]] and [[dependent sum]] operations, right and left adjoint respectively to [[pullback]] functors $g^*$ and $h^*$.

When $W=Z$, this is a **polynomial endofunctor**.

Sometimes this general notion is called a **dependent polynomial functor**, with "polynomial (endo)functor" reserved for the "one-variable" case, when $W=Z=1$ is the [[terminal object]].

The data $f$, $g$, and $h$ which specify a polynomial functor is sometimes referred to as a **container** (or an **indexed container**, with *container* reserved for the case $W=Z=1$).  Other times *container* is used as a synonym for "polynomial functor".

If $g$ is an identity, the functor is sometimes called a **linear functor** or a **linear polynomial functor**.  Note that this notion makes sense even if $C$ is not locally cartesian closed; all it needs are [[pullbacks]].  More generally, we can make sense of polynomial functors in any category with pullbacks if we restrict $g$ to be an [[exponentiable morphism]].


## Example

### On sets
 {#ExamplesOnSets}

For $C$ = [[Set]] the polynomial functor induced from a 
[[function]] $g$

$$
  \ast \stackrel{}{\leftarrow} X \stackrel{g}{\longrightarrow} Y
  \stackrel{}{\longrightarrow} \ast
$$ 

is given by

$$
  S \mapsto P_f(S) = \coprod_{y \in Y} S^{X_y}
  \,,
$$

where $X_y$ is the [[fiber]] of $g$ over $y \in Y$, and where the [[exponential object]] $S^{X_y}$ is the [[function set]] of [[functions]] from the fiber to $S$. The [[cardinality]] of the set on the right is

$$
  {\vert P_g(S)\vert}
   = 
  \sum_{y \in Y} {\vert S\vert}^{\vert X_y\vert}
$$

and it is in this sense that the concept of polynomial functor is a kind of [[categorification]] of that of [[polynomial]].

On the other hand the dependent polynomial functor associated to

$$
  A \stackrel{p_1}{\leftarrow} X \stackrel{id}{\longrightarrow} X
  \stackrel{p_2}{\longrightarrow} B
$$ 

acts by

$$
  (S_a)_{a \in A}
  \mapsto
  \left(\coprod_{a \in A} S_a \times X_{a b} \right)_{b \in B}
  \,.
$$

Under [[cardinality]] this becomes [[matrix multiplication]] acting on [[vectors]] (with entries in the [[natural numbers]]). So in this case the dependent polynomial functor is a linear functor of several variables, an [[integral transform]].

## The 2-category of polynomial functors

Any polynomial functor, as defined above, is automatically equipped with a [[tensorial strength]], when the slice categories of $C$ are regarded as tensored over $C$ in the canonical way.  The following theorem is proven in [Gambino--Kock](#GK):

+--{: .num_theorem}
###### Theorem
There is a [[bicategory]] whose objects are the objects of $C$, whose morphisms from $W$ to $Z$ are diagrams of the form
$$ W \overset{f}{\leftarrow} X \overset{g}{\to} Y \overset{h}{\to} Z, $$
and whose 2-morphisms are diagrams of the form
$$
\array{ & & X & \to & Y \\
  & \swarrow & \uparrow & & \mathllap{id}\uparrow & \searrow\\
  W && X' \times_{Y'} Y & \to & Y && Z\\
  &\nwarrow & \downarrow & & \downarrow & \nearrow \\
  && X' & \to & Y'. }
$$
This bicategory is equivalent to the 2-category whose objects are slice categories of $C$, whose morphisms are polynomial functors regarded as strong functors, and whose 2-morphisms are strength-respecting natural transformations.
=--

Note that the above bicategory contains, as a locally full sub-bicategory, the usual bicategory of [[spans]].  Thus, as a special case, the bicategory of spans is equivalent to the 2-category of "linear" polynomial functors.  Both of these are instances of [[Lack's coherence theorem]].


## Related topics

* Polynomial endofunctors are important in the definition of [[W-types]] in categories.

* Polynomial functors are a special case of [[parametric right adjoint|parametric right adjoints]].

* Polynomial functors can be defined using [[exponentiable morphisms]] in a category that may not be locally cartesian closed.  See also [[distributivity pullback]].

* Kripke frames $(R,S)$ (with a transition relation $R$ of arity $2$) as studied in [[modal logic]] are [[coalgebra]]s for the power-set functor $P$. Kripke frames for a more general *modal similarity type* $t$ are a coalgebras of a functor of the form $X\mapsto \product_{d\in t} P(S^{arity(d)})$. Kripke models are coalgebras of functor $K:X\mapsto P(Prop)\times P(X)$ where $Prop$ is the set of propositional variables of the logic in consideration. In particular all the functors appearing here are polynomial functors. So, at least in some aspects, the study of modal logics reduces to the study of (certain) polynomial functors

## Examples

* [[symmetric polynomial]], [[elementary symmetric polynomial]]

## Related entries

* [[polynomial monad]]

* [[integral transform]]


## References

The relation of plain polynomial functors to [[trees]] is discussed in

* [[Joachim Kock]], _Polynomial functors and trees_, (2009)  ([arXiv:0807.2874](http://arxiv.org/abs/0807.2874))
 {#Kock}

Dependent (multivariate) polynomial functors are considered in 

* [[Nicola Gambino]] and [[Joachim Kock]], _Polynomial functors and polynomial monads_, (2009) ([arXiv:0906.4931](http://arxiv.org/abs/0906.4931)).
{#GK}

Generalization to [[homotopy theory]] is discussed in 

* [[Joachim Kock]], _Data types with symmetries and polynomial functors over groupoids_,  28th Conference on the Mathematical Foundations of Programming Semantics (Bath, June 2012); in Electronic Notes in Theoretical Computer Science.  ([arXiv:1210.0828](http://arxiv.org/abs/1210.0828))

* [[Benno van den Berg]], [[Ieke Moerdijk]], _W-types in Homotopy Type Theory_ ([arXiv:1307.2765](http://arxiv.org/abs/1307.2765))
 {#vdBergMoerdijk13}

See also

* [[Joachim Kock]], [[André Joyal]], [[Michael Batanin]], [[Jean-François Mascari]], _Polynomial functors and opetopes_, Advances in Mathematics, vol 224, pages 2690--2737, (2010) ([arXiv:0706.1033](http://arxiv.org/abs/0706.1033))
{#KJBM}

* [[Yde Venema]], _Algebras and Coalgebras_, &#167;6 (p.332-426) in Blackburn, van Benthem, Wolter, _Handbook of modal logic_, Elsevier, 2007.


[[!redirects polynomial functor]]
[[!redirects polynomial functors]]
[[!redirects polynomial endofunctor]]
[[!redirects polynomial endofunctors]]

[[!redirects dependent polynomial functor]]
[[!redirects dependent polynomial functors]]
[[!redirects dependent polynomial endofunctor]]
[[!redirects dependent polynomial endofunctors]]

[[!redirects linear polynomial functor]]
[[!redirects linear polynomial functors]]
[[!redirects linear polynomial endofunctor]]
[[!redirects linear polynomial endofunctors]]

[[!redirects linear dependent polynomial functor]]
[[!redirects linear dependent polynomial functors]]
[[!redirects linear dependent polynomial endofunctor]]
[[!redirects linear dependent polynomial endofunctors]]

[[!redirects dependent linear polynomial functor]]
[[!redirects dependent linear polynomial functors]]
[[!redirects dependent linear polynomial endofunctor]]
[[!redirects dependent linear polynomial endofunctors]]


[[!redirects container]]
[[!redirects containers]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

The **slice category** or **over category** $\mathbf{C}/c$ of a [[category]] $\mathbf{C}$ over an object $c \in \mathbf{C}$ has 

* objects that are all arrows $f \in \mathbf{C}$ such that $cod(f) = c$, and

* morphisms $g: X \to X' \in \mathbf{C}$ from $f:X \to c$ to $f': X' \to c$ such that $f' \circ g = f$.

$$
  C/c
  =
  \left\lbrace
    \array{
       X &&\stackrel{g}{\to}&& X'
       \\
       & {}_f \searrow && \swarrow_{f'}
       \\   
       && c
    }
  \right\rbrace
$$


The slice category is a special case of a [[comma category]]. Specifically, if $F_c: \mathbf{*} \to \mathbf{C}$ is a constant functor to $c$, then $\mathbf{C}/c := (Id_{\mathbf{C}} \downarrow F_c)$.

The slice constructor $\mathbf{C}/(\cdot): \mathbf{C} \to Cat$ is functorial. A morphism $f: c \to d$ in $\mathbf{C}$ induces a functor between over-categories $F: \mathbf{C}/c \to \mathbf{C}/d$ by "composing" an object of $\mathbf{C}/c$ with $f$. Below is a commutative diagram illustrating the functoriality of $F$:
\begin{tikzcd}
	\bullet && \bullet \\
	& {\bullet{c}} \\
	& {\bullet{d}}
	\arrow["{\phi = F(\phi)}"{description}, from=1-1, to=1-3]
	\arrow["\alpha", from=1-1, to=2-2]
	\arrow["{F(\alpha)}", from=1-1, to=3-2]
	\arrow["\beta", from=1-3, to=2-2]
	\arrow["{F(\beta)}", from=1-3, to=3-2]
	\arrow["f", from=2-2, to=3-2]
\end{tikzcd}
The properties of the slice functor are explored further [below](#SliceFunctor).

There is a [[forgetful functor]] $U_c: \mathbf{C}/c \to \mathbf{C}$ which maps an object $f:X \to c$ to its domain $X$ and a morphism $g: X \to X' \in \mathbf{C}/c$ (from $f:X \to c$ to $f': X' \to c$ such that $f' \circ g = f$) to the morphism $g: X \to X'$.

The [[duality|dual]] notion is an [[under category]].


## Examples 

* If $\mathbf{C} = \mathbf{P}$ is a [[partial order|poset]] and $p \in \mathbf{P}$, then the slice category $\mathbf{P}/p$ is the [[down set]] $\downarrow (p)$ of elements $q \in \mathbf{P}$ with $q \leq p$. 

* If $1$ is a [[terminal object]] in $\mathbf{C}$, then $\mathbf{C}/1$ is isomorphic to $\mathbf{C}$.

* For $X$ a [[topological space]] then the [[category of covering spaces]] over $X$ is a [[full subcategory]] of the slice category $Top_{/X}$ of the [[category of topological spaces]].

* The [[fundamental theorem of topos theory]] states that the slice category over any object in a topos is itself a topos.

* For a [[monoidal category]] the slice category over any [[monoid object]] is monoidal.

  {#MonoidalTopos} For instance, the [[slice topos]] of a given [[topos]] over any [[monoid object]] is canonically a *[[monoidal topos]]* (see the Example [there](monoidal+topos#SliceToposOverAMonoidObject)).

## Properties

### Comonadicity

If $C$ admits binary coproducts with the fixed object $c$, then the forgetful functor $C/c \to C$ is [[comonadic]]. See [[coreader comonad]] for more details.

### Relation to codomain fibration
{#SliceFunctor}

The assignment of overcategories $C/c$ to objects $c \in C$ extends to a [[functor]]

$$
  C/(-) : C \to Cat
$$

Under the [[Grothendieck construction]] this functor corresponds to the [[codomain fibration]]

$$
  cod : [I,C] \to C
$$

from the [[arrow category]] of $C$.  (Note that unless $C$ has [[pullbacks]], this functor is not actually a [[Grothendieck fibration|fibration]], though it is always an opfibration.)

### Base change 

(Main article: [[base change]])
This is another important induced functor between over-categories. If $\mathbf{C}/c$ has finite products, then a morphism $f: d \to c$ in $\mathbf{C}$ induces the base change functor $f^*: \mathbf{C}/c \to \mathbf{C}/d$, which takes an object $\alpha: z \to c$ in $\mathbf{C}/c$ to the projection from the fibered product $y \times_{f,\alpha} d \to_{\pi_1} d$ as an object of $\mathbf{C}/d$. 
The [[right adjoint]] to this functor is (by definition) the [[dependent product]].


[[!include sliced adjoint functors -- section]]






### Presheaves on over-categories and over-categories of presheaves {#RelWithPresheaves}

See [[slice of presheaves is presheaves on slice]].

Let $C$ be a [[category]], $c$ an [[object]] of $C$ and let $C/c$ be the [[over category]] of $C$ over $c$. Write
$PSh(C/c) = [(C/c)^{op}, Set]$ for the [[category of presheaves]] on $C/c$ and write
$PSh(C)/Y(c)$ for the [[over category]] of [[presheaf|presheaves]] on $C$ over the presheaf $Y(c)$, where $Y : C \to PSh(c)$ is the [[Yoneda embedding]]. 

+-- {: .num_prop}
###### Proposition


There is an [[equivalence]] of categories

$$
  e : PSh(C/c) \stackrel{\simeq}{\to} PSh(C)/Y(c)
  \,.
$$

=--


+-- {: .proof}
###### Proof

The functor $e$ takes $F \in PSh(C/c)$ to the presheaf
$F' : d \mapsto \sqcup_{f \in C(d,c)} F(f)$ which is equipped with the natural transformation $\eta : F' \to Y(c)$ with component map $\eta_d: \sqcup_{f \in C(d,c)} F(f) \to C(d,c)$.

A weak inverse of $e$ is given by the functor 
$$
  \bar e : PSh(C)/Y(c) \to PSh(C/c)
$$
which sends
$
  \eta : F' \to Y(C))
$ to $F \in PSh(C/c)$ given by
$$
  F : (f : d \to c) \mapsto F'(d)|_c
  \,,
$$
where $F'(d)|_c$ is the [[pullback]]
$$
  \array{
     F'(d)|_c &\to& F'(d)
     \\
     \downarrow && \downarrow^{\eta_d}
     \\
     pt &\stackrel{f}{\to}& C(d,c)
  }
  \,.
$$ 

=--


+-- {: .num_example}
###### Example

Suppose the presheaf $F \in PSh(C/c)$ does not actually depend on the morphisms to $C$, i.e. suppose that it factors through the forgetful functor from the [[over category]] to $C$:
$$
  F : (C/c)^{op} \to C^{op} \to Set
  \,.
$$

Then
$
  F'(d) = \sqcup_{f \in C(d,c)} F(f)
  = \sqcup_{f \in C(d,c)} F(d)
  \simeq
  C(d,c) \times F(d) 
$
and hence $F' = Y(c) \times F$ with respect to the [[closed monoidal structure on presheaves]].

=--

See also [[functors and comma categories]].

For the analogous statement in [[(∞,1)-category theory]]  see at *[(∞,1)-category of (∞,1)-presheaves -- Interaction with overcategories](infinity1-category+of+infinity1-presheaves#WithOvercategories)*.




### Limits and colimits
 {#LimitsAndColimits}

+-- {: .num_prop #ColimitInSliceAreReflectedByColimitsInPlainCategory}
###### Proposition

A  [[colimit]] in an [[over category]] is computed as a colimit in the underlying category.

Precisely: let $\mathcal{C}$ be a [[category]], $t \in \mathcal{C}$ an [[object]], and $\mathcal{C}/t$ the corresponding [[overcategory]], and $p \colon \mathcal{C}/t \to \mathcal{C}$ the obvious projection.

Let $F \colon D \to \mathcal{C}/t$ be any [[functor]]. Then, if it exists, the [[colimit]] of $p \circ F$ in $\mathcal{C}$ is the image under $p$ of the colimit over $F$:

$$
  p
  \big(
    \underset{\longrightarrow}{\lim}
    F
  \big)  
  \;\simeq\; 
  \underset{\longrightarrow}{\lim} (p \circ F)
$$

and $\underset{\longrightarrow}{\lim} F$ is uniquely characterized by $\underset{\longrightarrow}{\lim} (p \circ F)$ this way.

=--

This statement, and its proof, is the [[formal dual]] to the corresponding statement for [[undercategories]], see [there](under+category#LimitsAndColimits).


+-- {: .num_prop #LimitsInSliceViaLimitsOfCoconedDiagram}
###### Proposition

For $\mathcal{C}$ a [[category]], $X \;\colon\; \mathcal{D} \longrightarrow \mathcal{C}$ a [[diagram]], $\mathcal{C}_{/X}$ the [[comma category]] (the over-category if $\mathcal{D}$ is the point) and $F \;\colon\; K \to \mathcal{C}_{/X}$ a [[diagram]] in the [[comma category]], then the [[limit]] $\underset{\leftarrow}{\lim} F$ in $\mathcal{C}_{/X}$ coincides with the limit $\underset{\leftarrow}{\lim} F/X$ in $\mathcal{C}$. 
 
=--

For proof

* with formalization in [Cubical Agda](Agda#CubicalAgda): see  [[1lab]], *[arbitrary-limits-in-slices](https://1lab.dev/Cat.Instances.Slice.Limit.html#arbitrary-limits-in-slices)*,

* in the generality of [[(∞,1)-category theory]]: see [at [[(∞,1)-limit]]  _[here](limit+in+a+quasi-category#InOvercategories)_.




### Initial and terminal objects
 {#InitialAndTerminalObjects}

As a special case of the above discussion of limits and colimits in a 
slice $\mathcal{C}_{/X}$ we obtain the following statement, which of 
course is also immediately checked explicitly.

+-- {: .num_cor }
###### Corollary

* If $\mathcal{C}$ has an initial object $\emptyset$, then $\mathcal{C}_{/X}$ has an [[initial object]], given by $\langle \emptyset \to X\rangle$.

* The [[terminal object]] of $\mathcal{C}_{/X}$ is $\mathrm{id}_X$.

=--




## Related concepts

* **over-category** 

  * [[enriched over category]]

  * [[under category]]

  * [[over topos]]

* [[slice 2-category]]

* [[over (∞,1)-category]],

  * [[model structure on an over category]] 

  * [[over-(∞,1)-topos]]

## References

Textbook accounts:

* [[Francis Borceux]]. Ex. 1.2.7 in: *[[Handbook of Categorical Algebra]]*, Vol **1**: *Basic Category Theory*, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;

* {#Riehl17} [[Emily Riehl]], Ex. 1.1.3 in: *[[Category Theory in Context]]*, Dover Publications (2017) &lbrack;[ISBN:9780486809038](https://store.doverpublications.com/products/9780486809038), [pdf](https://emilyriehl.github.io/files/context.pdf), [webpage](https://math.jhu.edu/~eriehl/context/)&rbrack;

Formalization in [[cubical Agda]]:

* [[1lab]]: *[Slice categories](https://1lab.dev/Cat.Instances.Slice.html)*

[[!redirects overcategory]]
[[!redirects over categories]]
[[!redirects over-category]]
[[!redirects over-categories]]
[[!redirects overcategories]]
[[!redirects slice category]]
[[!redirects slice categories]]

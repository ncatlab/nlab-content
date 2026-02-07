+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea
A ([[small category|small]]) _cocategory_ is a [[category]] [[internal category|internal to]] $Set^{op}$, the [[opposite category]] of [[Set]].

More generally, if $C$ is [[finitely complete category|finitely cocomplete]], there is a notion of cocategory internal to $C$, namely a [[comonad]] in the [[bicategory]] of [[span|cospans]] in $C$. 

If $c_0 \to c_1 \leftarrow c_0$ is a cocategory object in $C$, then by homming out of $c_\bullet$, one obtains a limit-preserving functor $C \to Cat$. Under reasonable conditions, the [[adjoint functor theorem]] conversely implies that all limit-preserving functors $C \to Cat$ are obtained in this way.

## Definitions

### Cocategory

Let $A$ be a [[category]] with [[pullbacks]]. A __cocategory__ $C$ is a category object [[internal category|internal to]] category $A^{op}$, consisting of:

* an [[object]] _of [[objects]]_ $C_0 \in A$;

* an [[object]] _of [[morphisms]] $C_1 \in A$;

* structure morphisms:
   *  cosource and cotarget morphisms $s,t: C_0 \to C_1$;

   *  counit $\varepsilon : C_1 \to C_0$;

   *  cocomposition (comultiplication) morphism $\Delta : C_1 \to C_1 \sqcup_{C_0} C_1$;

*  such that the following properties are satisfied, expressing the usual category laws: 
   *  coassociativity law: $(\Delta \sqcup \mathrm{id}) \circ \Delta \;=\;
 (\mathrm{id} \sqcup \Delta) \circ \Delta \;:\; C_1 \longrightarrow C_1 \sqcup_{C_0} C_1 \sqcup_{C_0} C_1$,
where the two iterated [[pushouts]] are identified via the canonical [[associativity]] isomorphism;
   *  counitality law: $(\varepsilon \sqcup \mathrm{id}) \circ \Delta = \mathrm{id}_{C_1} = (\mathrm{id} \sqcup \varepsilon) \circ \Delta.$


### Cocomposition

#### In a plain cocategory

__Cocomposition__ (or _comultiplication_) is the operation that takes a [[morphism]] $f\colon  x \to z$ ​ in a cocategory $C$ and produces a pair of composable morphisms $(f_1,  f_2)$ with

$$
  f_{1} \colon  x \to y  \quad \text{and}  \quad f_{2} \colon  y \to z
$$

represented collectively as a morphism $\Delta(f) \in C_1 \sqcup_{C_0} C_1$ called the __cocomposite__ of $f$.

Intuitively, a single arrow is "split" into two arrows, [[duality|dually]] to the [[composition]] morphism $c: C_1 \times_{C_0} C_1 \to C_1$ that "merges" two arrows into one.

#### In an enriched cocategory

In [[enriched category theory]], for $V$ a [[monoidal category]] the cocomposition operation on a $V$-[[enriched category|enriched cocategory]] $C$ is, for each 3-tuple $(x,y,z)$ of [[objects]] of $C$, a [[morphism]]

$$
  \Delta_{x,y,z} : C(x,z) \to C(x,y) \otimes C(y,z)
$$


in $V$.

This reduces to the above definition in the case that $V =$ [[Set]]. The cocomposition morphism $\Delta_{x,y,z}$ sends any morphism to a pair of composable morphisms

$$
  \Delta_{x,y,z} : (x \stackrel{f}{\to} z) \;\; \mapsto \;\; \bigl( (x \stackrel{f_1}{\to} y), (y \stackrel{f_2}{\to} z) \bigr).
$$


## Cocategorical semantics

In the context of [[formal logic]], particularly in [[linear logic]] and [[type theories]] with costructural rules, cocomposition is the [[categorical semantics|cocategorical semantics]] for the [[contraction rule]], realized categorically as [[monoidal category with diagonals|diagonal (comultiplicative) maps]] on objects or morphisms.

## Examples

 - Many [[interval object|interval objects]] are cocategory objects. For example, the arrow category is a cocategory object in $Cat$.

 - Any [[coalgebra]] object is a cocategory object. This includes [[coring|corings]], [[Hopf algebroid|Hopf algebroids]], [[cogroupoid|cogroupoids]], etc.

 - In $Set$, every cocategory object is a coproduct of copies of the trivial cocategory object $1 \to 1 \leftarrow 1$ and the cocategory object $1 \to 2 \leftarrow 1$ where the two points are distinct. These represent the [[discrete category]] functor and the [[codiscrete category]] functors $Set \to Cat$, respectively.

## Related concepts

* [[comonoid]]
* [[Trimble n-category]]
* [[span]], [[cospan]]
* [[composition]]

## References

* [[Peter LeFanu Lumsdaine]], _A Small Observation on Co-categories_ &lbrack;[arXiv:0902.4743](https://arxiv.org/abs/0902.4743)&rbrack;

* Vasileios Aravantinos-Sotiropoulos, and [[Christina Vasilakopoulou]], _Sweedler theory for double categories_ &lbrack;[arXiv:2408.03180](https://arxiv.org/abs/2408.03180)&rbrack;

Presentation slides on $V$-cocategories and cocomposition:

* [[Christina Vasilakopoulou]], _Enriched duality in double categories_ &lbrack;[link](http://www.math.ntua.gr/~cvasilak/documents/EnrichedDualityDoubleCatsPlain.pdf)&rbrack;


[[!redirects cocomposition]]
[[!redirects co-composition]]

[[!redirects cocategories]]
[[!redirects co-category]]
[[!redirects co-categories]]

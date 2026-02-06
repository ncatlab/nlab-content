> [[Kourouklides]]

### Personal sandbox - please ignore

===

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

In [[enriched category theory]], for $V$ a [[monoidal category]] the cocomposition operation on a $V$-[[enriched category]] $C$ is, for each 3-tuple $(x,y,z)$ of [[objects]] of $C$, a [[morphism]]

$$
  \Delta_{x,y,z} : C(x,z) \to C(x,y) \otimes C(y,z)
$$


in $V$.

This reduces to the above definition in the case that $V =$ [[Set]]. The cocomposition morphism $\Delta_{x,y,z}$ sends any morphism to a pair of composable morphisms

$$
  \Delta_{x,y,z} : (x \stackrel{f}{\to} z) \;\; \mapsto \;\; \bigl( (x \stackrel{f_1}{\to} y), (y \stackrel{f_2}{\to} z) \bigr).
$$


### Categorical semantics

In the context of [[formal logic]], particularly in [[linear logic]] and [[type theories]] with costructural rules, cocomposition is the [[categorical semantics]] for the [[contraction rule]], realized categorically as [[monoidal category with diagonals|diagonal (comultiplicative) maps]] on objects or morphisms.

===


===




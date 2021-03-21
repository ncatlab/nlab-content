+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Two-valued object
* table of contents
{: toc}

## Idea

Recall that a [[topos]] is a [[category]] that behaves likes the category [[Set]] of [[sets]].

An two-valued object internal to a topos is an object that behaves in that topos like the set $\mathbf{2}$ with exactly two elements does in Set.

## Definition

### In a topos or cartesian closed category

An **two-valued object** in a [[topos]] (or any [[cartesian closed category]]) $E$ with [[terminal object]] $1$ is 

* an [[object]] $\mathbf{2}$ in $E$ 

* equipped with 
  
  * a [[morphism]] $zero:1 \rightarrow \mathbf{2}$ from the [[terminal object]] $1$;

  * a [[morphism]] $one:1 \rightarrow \mathbf{2}$ from the [[terminal object]] $1$;

* such that for every other tuple $(A, t, f)$ there is a morphism $u : \mathbf{2} \to A$ such that

\begin{center}
  \begin{tikzcd}
    \mathbf{2} \ar[d, "u"] &
    1 \ar[l, "zero"] \ar[ld, "f"] \ar[r, "one"] \ar[rd, "t"]        &
    \mathbf{2} \ar[d, "u"] \\
    A & & A
  \end{tikzcd}
\end{center}

By the [[universal property]], the two-valued object is unique up to [[isomorphism]].

## Properties

### Coproducts

The two-valued object $\mathbf{2}$ is the [[disjoint coproduct]] of the terminal object $1$ with itself. 

... (One should be able to define binary [[coproduct]]s using the [[dependent sum]] functor and the two-valued object, as dependent sums exist in topoi and cartesian closed categories.)

### Products

... (Same thing as above but with binary [[products]] and [[dependent product]]s.)

### Subobject classifier

A topos with a [[subobject classifier]] that is also a two-valued object is a [[two-valued topos]]. The [[internal logic]] of such a topos is [[two-valued logic]]. 

### Type theory

Two-valued objects are the [[categorical semantics]] of the [[two-valued type]] in type theory. The [[inductive type|inductive property]] of the two-valued type, case analysis or if/else expressions, corresponds to the [[initial object|initiality]] of the two-valued object in the subcategory of objects with more than one global element, similar to how the principle of [[induction]] over [[natural numbers]] corresponds to the initiality of the [[natural numbers object]] in the subcategory of triples $(A, q:1\rightarrow A, f:A\rightarrow A)$ representing infinite sequences. 

## Examples

* The [[subobject classifier]] $\Omega$ and the [[Sierpinski space]] $\mathbb{S}$ in the category of [[axiom of choice|choice sets]] are two-valued objects. 

* Any [[interval object]] is a two-valued object with a [[2-morphism]] connecting the global elements $zero$ and $one$. 

## See also

* [[natural numbers object]]

* [[integers object]]

* [[subobject classifier]]

* [[two-valued type]], [[two-valued topos]], [[two-valued logic]]
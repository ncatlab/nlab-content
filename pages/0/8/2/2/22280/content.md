+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Boolean domain object
* table of contents
{: toc}

## Idea

Recall that a [[topos]] is a [[category]] that behaves likes the category [[Set]] of [[sets]].

A boolean domain object internal to a topos is an object that behaves in that topos like the [[boolean domain]] $\mathrm{Bool}$ does in Set.

## Definition

### In a topos or cartesian closed category

A **boolean domain object** in a [[topos]] (or any [[cartesian closed category]]) $E$ with [[terminal object]] $1$ is 

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

By the [[universal property]], the boolean domain object is unique up to [[isomorphism]].

## Properties

### As an initial object

The boolean domain object $\mathbf{2}$ is an [[initial object]] in the category of [[bi-pointed object]]s.

### Coproducts

The boolean domain object $\mathbf{2}$ is the [[disjoint coproduct]] of the terminal object $1$ with itself. 

... (One should be able to define binary [[coproduct]]s using the [[dependent sum]] functor and the boolean domain object, as dependent sums exist in topoi and cartesian closed categories.)

### Products

... (Same thing as above but with binary [[products]] and [[dependent product]]s.)

### Subobject classifier

A topos with a [[subobject classifier]] that is also a boolean domain object is a [[two-valued topos]]. The [[internal logic]] of such a topos is [[two-valued logic]]. 

### Type theory

Boolean domain objects are the [[categorical semantics]] of the [[boolean domain]] in type theory. The [[inductive type|inductive property]] of the boolean domain type, case analysis or if/else expressions, corresponds to the [[initial object|initiality]] of the boolean domain object in the subcategory of triples $(A, t:1\rightarrow A, f:1\rightarrow A)$ representing [[bi-pointed object]]s, similar to how the principle of [[induction]] over [[natural numbers]] corresponds to the initiality of the [[natural numbers object]] in the subcategory of triples $(A, q:1\rightarrow A, f:A\rightarrow A)$ representing infinite sequences. 

## See also

* [[natural numbers object]]

* [[bi-pointed object]]

* [[subobject classifier]]

* [[boolean domain]]

* [[two-valued topos]], [[two-valued logic]]

[[!redirects two-valued object]]

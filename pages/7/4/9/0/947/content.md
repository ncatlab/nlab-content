
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

### In sets

The __complement__ $X \setminus S$ of a [[subset]] $S \subset X$ of a [[set]] $X$ is the set of ell [[elements]] of $X$ not contained in $S$: 


$$
  X \setminus S 
  \;\coloneqq\; 
  \big\{ 
    x \in X \;|\; 
    x \notin S  
  \big\}
  \,.
$$


(Besides $X \setminus S$, there are many other notations, such as $X - S$, $\bar{S}$, $S^c$, $\neg{S}$, and so forth.)

Notice that $S \cap (X \setminus S) = \empty$, while $S \cup (X \setminus S) = X$ by the principle of [[excluded middle]].  

### In lattices

A __complement__ of an element $S$ of a [[lattice]] is an element $T$ such that $S \wedge T = \bot$ and $S \vee T = \top$. Note that in general, complements need not be unique; for example, in the lattice of vector subspaces of a 2-dimensional [[vector space]] over a [[field]] $k$, a 1-dimensional subspace will have as many complements as there are elements of $k$. However, in some cases complements will be unique, for example in a [[distributive lattice]], in which case it is denoted $\tilde{S}$ (or $\neg S$, etc.). 

If every element has a complement, one speaks of a [[complemented lattice]]. Examples are [[Boolean algebras]], and in fact complemented distributive lattices are the same thing as Boolean algebras (in the sense that the [[category]] of Boolean algebras is [[equivalence|equivalent]] to the category of complemented distributive lattices). 

More generally, the __pseudocomplement__ of an element $S$ of a [[Heyting algebra]] is given by $\tilde{S} = S \Rightarrow \bot$.  This satisfies $S \wedge \tilde{S} = \bot$ but not $S \vee \tilde{S} = \top$ in general.  This case includes the complement of a subset even in [[constructive mathematics]].

### In any category

In another direction, the __complement__ of a [[complemented subobject]] $S$ of an [[object]] $X$ in a [[coherent category]] is the unique subobject $\tilde{S}$ such that $S \cap \tilde{S}$ is the [[initial object]] and $S \cup \tilde{S} = X$.

### In truth values

The complement of a [[truth value]] (seen as a subset of the [[point]]) is called its _[[negation]]_.


## Related concepts

* [[orthocomplemented lattice]]

* [[open subset]], [[closed subset]] 

* [[complemented subobject]] 

* [[decidable subset]] 

* [[decidable object]] 

* [[pushout complement]]

[[!redirects complement]]
[[!redirects complements]]
[[!redirects complementation]]

[[!redirects pseudocomplement]]
[[!redirects pseudocomplements]]

[[!redirects complemented]]

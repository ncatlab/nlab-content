

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Opposite magmas
* table of contents
{: toc}


## Idea

The _opposite_ of a magma -- hence of a set with a binary operation $(x,y) \mapsto x y$ --  has the same underlying set of elements, but binary operation changed by _reversing the order_ of the factors: $(x,y) \mapsto y x$.

This is often considered for the case that $A$ a [[monoid]], [[group]], [[ring]], or algebra ([[nonassociative algebra|nonassociative]] or [[associative algebra|associative]]), in which case one speaks of the _opposite group_, _opposite ring_, etc.


## Definitions

### In $Set$

Let $A$ be a [[magma]], that is a [[set]] ${|A|}$ equipped with a [[binary operation]] 

$$
  \array{
    {\left\vert A \right\vert} \times 
    {\left\vert A \right\vert} 
    &\longrightarrow& 
    {\left\vert A \right\vert}
    \\
    (x,y)
    &\mapsto&
    x \cdot y 
    \mathrlap{
      \coloneqq 
    {\color{blue}x} {\color{red}y}  
    }
  }
$$ 

written as multiplication or juxtaposition.  

Then the _opposite magna_ $A^{op}$ (also denoted $A^*$ or $A^\perp$) has the same underlying set

$$
  \left\vert A^{op} \right\vert
  \;\coloneqq\;
  \left\vert A \right\vert
$$

but [[binary operation]] that of $A$ but with the [[ordering]] in the [[pair]] of arguments reversed:


\[
  \label{elementDefinition}
  \array{
    {\left\vert A^{op} \right\vert} 
      \times 
    {\left\vert A^{op} \right\vert} 
    &\longrightarrow& 
    {\left\vert A^{op} \right\vert}
    \\
    (x,y)
    &\mapsto&
    x * y 
    \mathrlap{
      \coloneqq  
    {\color{red}y}{\color{blue}x}
    }
    \,.
  }
\]

If $A$ is a [[monoid]] or a [[group]] (or [[semigroup]], [[quasigroup]], [[quasigroup|loop]], etc), the same definition applies, and we see that $A^op$ is again a monoid or a group (etc).

If $A$ is a [[ring]] or a $K$-[[nonassociative algebra|algebra]], the same definition applies, and we see that $A^op$ is again a ring or a $K$-algebra (including such special cases of algebra as an [[associative algebra]], [[Lie algebra]], etc).  However, one can also interpret this situation as internal to [[Ab]] or $K\,$[[Mod]]; see below.


### In other categories

The notion of magma makes sense [[internalisation|in]] any [[monoidal category]] $C$.  The notion of opposite does not make sense in this general context, because we must switch the order of the variables $x$ and $y$ in (eq:elementDefinition).  It does make sense in a [[braided monoidal category]], although now there are two ways to write it, depending on whether we use the [[braiding]] or its [[inverse morphism|inverse]] to switch the variables.  In a [[symmetric monoidal category]], the definition not only makes sense but gives the same result either way.

In particular, a magma object in $K\,$[[Mod]] is a [[nonassociative algebra]] over $K$, a monoid object in $K Mod$ is an [[associative algebra]] over $K$, and a monoid object in [[Ab]] is a [[ring]].  So all of these have opposites.


## Commutative magmas

If $A$ is [[commutativity|commutative]], then $A^op \cong A$.  In fact, this [[isomorphism]] lives [[over category|over]] $Set$ (or over the underlying monoidal category $C$), so we may write $A^op = A$ to denote this.


## Categorifications

The concept of monoid may be [[horizontal categorification|oidified]] to that of [[category]]; the concept of opposite monoid is then oidified to that of [[opposite category]].

The concept of monoid may also be [[vertical categorification|categorified]] to that of [[monoidal category]]; the concept of opposite monoid is then categorified to that of [[opposite monoidal category]].

In particular, a monoidal category $A$ has *two* kinds of opposites: one as a mere category (an oidified monoid) and one as a monoidal object (a categorified monoid).  We denote the first as $A^op$ and the second as $A^co$.

If we categorify *and* oidify, then we get the concept of [[2-category]].  Again, a $2$-category $A$ has $2$ kinds of opposites, again denoted $A^op$ and $A^co$.  So $A^op$ reverses the [[1-morphisms]] while $A^co$ reverses the [[2-morphisms]].  See [[opposite 2-category]].

An $n$-[[n-category|category]] has $n$ kinds of opposites.  See (or write) [[opposite n-category]].  A [[monoidal n-category]] has $n + 1$ kinds of opposites.

## Related concepts

* under [[delooping]] a [[monoid]] to a pointed one-object [[category]], passing to the opposite monoid corresponds to passing to the [[opposite category]].

* [[antihomomorphism]]

[[!redirects opposite magma]]
[[!redirects opposite magmas]]

[[!redirects opposite monoid]]
[[!redirects opposite monoids]]

[[!redirects opposite group]]
[[!redirects opposite groups]]

[[!redirects opposite ring]]
[[!redirects opposite rings]]

[[!redirects opposite algebra]]
[[!redirects opposite algebras]]

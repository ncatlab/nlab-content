
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

> This entry is about extension of morphisms, [[formal dual|dual]] to [[lift]]. For extensions in the sense of "added structure" see at _[[group extension]]_, _[[Lie algebra extension]]_, _[[infinitesimal extension]]_ etc. In [[foundations]] and [[formal logic]]  there is also [[extension (semantics)]] and [[context extension]].

#Contents#
* table of contents
{:toc}

## Idea

### Extension of morphisms

The __extension of a morphism__ $f: A\to Y$ along a monomorphism $i: A\hookrightarrow X$ is a morphism $\tilde{f}:X\to Y$ such that $\tilde{f}\circ i = f$. One sometimes, extends along more general morphisms than monomorphisms. 

The dual problem is the problem of [[lifting]] a morphism $f: Y\to B$ through an epimorphism (or more general map) $p:X\to B$, giving a morphism $\tilde{f}: Y\to X$ such that $f = p\circ\tilde{f}$.

### Extension of an object by another object 

In a [[category]] $C$ with a notion of [[short exact sequence]] (e.g. any [[semiabelian category]], [[Quillen exact category]] etc.) an **extension** of an object $Q$ by an object $K$ is any object $X$ fitting in a short exact sequence

$$ 
K \stackrel{i}\to X \stackrel{p}\to Q
$$


Classification of extensions in many categories is obtained using a [[forgetful functor]] $C\to D$ to a simpler category $D$, which preserves short exact sequences. For example, if all extensions in $D$ are isomorphic to $K\coprod Q$, then one looks for an additional structure in $C$ needed to equip the coproduct $K \coprod Q$ with a structure of an object in $C$ such that the $i$ and $p$ are morphisms in
$C$ making above a short exact sequence in $C$.

### Other notions of extension

* [[extension (semantics)]]

* [[context extension]]

* [[absolute extensor]]

* [[extension of distributions]]

## Examples 

### Extension of functions


The [[Tietze extension theorem]] is about *extensions of continuous maps* from a subspace to a normal toplogical space. 


### Group extensions

For example, in the category [[Grp]] of (possibly nonabelian) groups one has a short exact sequence usually denoted $1\to X\to Z\to Y\to 1$ corresponding to a [[group extension]].

## Related concepts

* [[homotopy extension property]]

[[!redirects extensions]]
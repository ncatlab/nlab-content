
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A **G-structure** on an $n$-[[manifold]] $M$, for a given structure group $G$, is a $G$-subbundle of the [[frame bundle]] (of the [[tangent bundle]]) of $M$. 

Equivalently, this means that a $G$-structure is a choice of [[reduction of structure groups|reduction]] of the canonical structure group $GL(n)$ of the [[principal bundle]] to which the [[tangent bundle]] is [[associated bundle|associated]] along the given inclusion $G \hookrightarrow GL(n)$.

More generally, one can consider the case $G$ is not a [[subgroup]] but equipped with any group homomorphism $G \to GL(n)$. If this is instead an [[epimorphism]] one speaks of a [[lift of structure groups]].

Both cases, in turn, can naturally be understood as special cases of [[twisted differential c-structures]], which is a notion that applies more generally to [[principal infinity-bundles]].

## Definition

### Traditional

(...)

### In terms of higher geometry

We give an equivalent definition of $G$-structures in terms of [[higher geometry]] ("from the [[nPOV]]"). This serves to clarify the slightly subtle but important difference between existence and choice of $G$-structure, and seamlessly embeds the notion into the more general context of [[twisted differential c-structures]].

+-- {: .num_defn}
###### Definition

Let $G \to K$ be a [[homomorphism]] of [[Lie groups]]. Write 

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}K
$$

for the morphism of [[delooping]] [[Lie groupoids]] ( the [[smooth infinity-groupoid|smooth]] [[moduli stacks]] of smooth $K$- and $G$-[[principal bundles]], respectively).

For $X$ a [[smooth manifold]] (or generally an [[orbifold]] or [[Lie groupoid]], etc.) Let $P \to X$ be a $K$-[[principal bundle]] and let $g : X \to \mathbf{B}K$ be any choice of morphism representing it.

Write $\mathbf{H}(X, \mathbf{B}G)$ etc. for the [[derived hom space|hom-groupoid]] of [[smooth infinity-groupoid|smooth groupoids]] / smooth stacks . This is equivalently the groupoid of $G$-principal bundles over $X$ and smooth [[gauge transformations]] between them.

Then the **groupoid of $G$-structure on $P$** (with respect to the given morphism $G \to K$) is the [[homotopy pullback]]

$$
  \array{
    \mathbf{c}Struc_{[P]}(X)
    &\to&
    *
    \\
    \downarrow & \swArrow& \downarrow^{g}
    \\
    \mathbf{H}(X, \mathbf{B}G)
     &\stackrel{\mathbf{H}(X, \mathbf{c})}{\to}&
    \mathbf{H}(X, \mathbf{B}K)
  }
$$

(the groupoid of _[[twisted differential c-structure|twisted c-structures]]_).

Specifically, when $X$ is a [[smooth manifold]] of [[dimension]] $n$, the [[tangent bundle]] $T X$ canonically comes from a morphism $T X : X \to \mathbf{B} GL(n)$ into the [[moduli stack]] for the [[general linear group]] $K := GL(n)$. Then for any group homomorphism $G \to GL(n)$, a **$G$-structure** on $X$ is a $G$-structure on $T X$, as above.

=--

## Examples

* For the [[subgroup]] of $GL(n, \mathbb{R})$ of matrices of positive determinant, a $GL(n, \mathbb{R})^+$-structure defines an [[orientation]].

* For the [[orthogonal group]], an $O(n)$-structure defines a [[Riemannian metric]]. (See the discussion at [[vielbein]] and at

* For the [[special linear group]], an $SL(n,R)$-structure defines a [[volume form]]. 

* For the trivial group, an $\{e\}$-structure consists of an [[absolute parallelism]] of the manifold.

* For $n = 2 m$ even, a $GL(m, \mathbb{C})$-structure defines an [[almost complex structure]] on the manifold. It must satisfy an integrability condition to be a [[complex structure]].

An example for a lift of structure groups is

* for the [[spin group]]  $spin(n)$, a $G$-structure is a [[spin structure]].

This continues with lifts to the 

* [[string group]] giving [[string structure]];

* [[fivebrane group]] giving [[fivebrane structure]].

## Further issues

Need to talk about integrability conditions, and those of higher degree. Also need to discuss [[pseudo-group|pseudo-groups]], and relation of all this with [[Cartan geometry]].

## Related concepts

* [[special holonomy]]

## References

### Traditional

* [Wikipedia](http://en.wikipedia.org/wiki/G-structure)

* S.S. Chern 1966, _[The geometry of G-structures](http://www.ams.org/journals/bull/1966-72-02/S0002-9904-1966-11473-8/S0002-9904-1966-11473-8.pdf)_, Bull. Amer. Math. Soc. 72(2): 167&#8211;219.

* Shoshichi Kobayashi, Katsumi Nomizu, _Foundations of differential geometry_

* Shlomo Sternberg, _Lectures on differential geometry_

### In higher geometry

Some discussion is in section 4.4.2 of

* _[[schreiber:differential cohomology in a cohesive topos]]_

[[!redirects G-structures]]
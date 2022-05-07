
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

The **diagonal** of an [[object]] $X$ in a [[category]] with [[Cartesian product]] is the canonical [[morphism]]

$$
  \Delta 
    \;\colon\; 
  X 
    \stackrel{(Id,Id)}{\longrightarrow} 
  X \times X
$$

which is induced, via the [[universal property]] of the [[Cartesian product]], by the [[span]] whose two legs each are both the [[identity morphism]] on $X$:

$$
  \array{
    && X
    \\
    & 
      {}^{\mathllap{Id}}\swarrow 
    & 
      \downarrow 
      {}^{\mathrlap{\Delta}}
    & 
      \searrow^{\mathrlap{Id}}
    \\
    X 
      &\underset{pr_1}{\longleftarrow}&
    X \times X
      &\underset{pr_2}{\longrightarrow}&
    X
  }
$$

The dual concept is _[[codiagonal]]_ . 

In the absence of [[Cartesian products]], or when intentionally disregarding them, diagonal morphisms may still be considered in a generalized sense in [[monoidal categories with diagonals]].

## Details

Recall that the [[diagonal subset|diagonal]] of a [[set]] is a [[subset]] of its [[cartesian product|cartesian square]] $X^2$.  If $X$ is now an object in some [[cartesian monoidal category]] $C$, then the diagonal of $X$ is now a [[subobject]] of its [[product|categorial square]] $X^2$.  (Actually, $C$ need not be cartesian monoidal, as long as the product $X \times X$ exists.)

Specifically, the __diagonal morphism__ of $X$ is [[generalized the|the]] morphism $\Delta_X: X \to X^2$ to the [[cartesian product ]] of $X$ with itself given (using the [[universal property]] of the [[cartesian product]]) by the [[identity morphism]] from $X$ to itself, taken twice.  That is, $\Delta_X$ is the universal solution to
$$ \array {
                            &          & X \\
                            & \swarrow & \downarrow _ { \Delta _ X } & \searrow \\
   X                        &          & X ^ 2                       &          & X \\
   \downarrow _ { \id _ X } & \swarrow &                             & \searrow & \downarrow _ { \id _ X } \\
   X                        &          &                             &          & X
} $$
If $C$ is $Set$ (the [[category of sets]]), then this diagonal morphism is precisely the [[diagonal function]] of $X$.

## Properties

The diagonal morphism is always a [[regular monomorphism]], since it is the [[equaliser]] of the two projection maps $X^2 \to X$.  (In fact, it is a [[split monomorphism]], since it is also a [[section]] of either projection map.)  Thus, it makes $X$ into a regular [[subobject]] of $X^2$, the __diagonal subobject__.  When $C$ is the $Set$, this recovers the original notion of the [[diagonal subset]] of $X^2$.

In any category with binary [[pullbacks]], the [[kernel pair]] of the [[identity morphism]] $id$ on an object $X$ is the diagonal morphism $(id,id)$ of $X$, and has a [[coequalizer]] [[isomorphic]] to $X$ itself. 

## Examples

In the category [[Set]] the diagonal $\Delta_X$ is the [[function]] $a \mapsto (a,a)$ for all $a \in X$. See [[diagonal subset]].

In the category [[Top]] of [[topological spaces]], an object $X$ is a [[Hausdorff space]] if and only if its diagonal subobject is a [[closed subspace]] of $X^2$; this fact can be generalised to other notions of [[space]].

In [[Cat]] the diagonal morphisms are [[diagonal functors]].

## Related concepts

* [[fat diagonal]]

* [[monoidal category with diagonals]]

* [[formal neighbourhood of the diagonal]]


[[!redirects diagonal]]
[[!redirects diagonals]]

[[!redirects diagonal subobject]]
[[!redirects diagonal morphisms]]

[[!redirects diagonal map]]
[[!redirects diagonal maps]]

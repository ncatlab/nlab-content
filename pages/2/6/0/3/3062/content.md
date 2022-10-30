
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


# Lie $2$-algebras
* table of contents
{: toc}


## Idea

A Lie 2-algebra is to a [[Lie 2-group]] as a [[Lie algebra]] is to a [[Lie group]].  Thus, it is a [[vertical categorification]] of a [[Lie algebra]].


## Definition

### Semistrict case

A ("semistrict") Lie 2-algebra $\mathfrak{g}$ is an [[L-∞-algebra]] with generators concentrated in the lowest two degrees.

This means that it is

* a pair of [[vector space]]s $\mathfrak{g}_0, \mathfrak{g}_1$

* equipped with [[linear function]]s

  $$
    \delta : \mathfrak{g}_1 \to \mathfrak{g}_0
  $$

  (the _[[differential]]_ )

  $$
    [-,-] : \mathfrak{g}_0 \vee \mathfrak{g}_0 \to \mathfrak{g}_0
  $$

  (the _bracket_)

  $$
    \alpha(-,-) : \mathfrak{g}_0 \otimes \mathfrak{g}_1 \to 
     \mathfrak{g}_1
  $$

  (the weak [[action]])
  
  $$
    [-,-,-] : \mathfrak{g}_0 \vee \mathfrak{g}_0 \vee \mathfrak{g}_0 \to \mathfrak{g}_1
  $$

  (the _Jacobiator_)

* such that

  * $[-,-]$ and $[-,-,-]$ are skew-symmetric in their arguments, as indicated;

  * the [[differential]] respects the brackets: for all $x \in \mathfrak{g}_0$ and $h \in \mathfrak{g}_1$ we have

    $$
      \delta [x,h] = [x, \delta h]
    $$
    

  * the [[Jacobi identity]] of $[-,-]$ holds up to the image under $\delta$ of the _Jacobiator_ $[-,-,-]$: for all $x,y,z \in \mathfrak{g}_0$ we have

    $$
      [x,[y,z]] + [y,[z,x]] + [z,[x,y]] 
      =
      \delta [x,y,z]
    $$

  * as does the [[action]] property:

    $$
      \alpha(x,[y,h]) - \alpha(y,[x,h])
      =
      \alpha([x,y],h)
      +
      [x,y,\delta h]
    $$

  * the Jacobiator is [[coherence law|coherent]]:

    $$
      [[w,x,y], z] + [[w,y,z],x] + [[w,y],x,z]
      +
      [[x,z],w,y]
      =
      [[w,x,z], y] + [[x,y,z], w]
      +
      [[w,x],y,z]
      + 
      [[w,z], x,y]
      + 
      [[x,y], w,z]
      +
      [[y,z],w,x]
      \,.
    $$

### Strict

If the trinary bracket $[-,-,-]$ in a Lie 2-algebra is trivial, one speaks of a [[strict Lie 2-algebra]]. Strict Lie 2-algebras arise from [[differential crossed module]]s.


## Examples

* [[derivation Lie 2-algebra]]

* [[string Lie 2-algebra]]

## Related concepts

* [[Lie algebra]], [[Lie group]]

* **Lie 2-algebra**, [[Lie 2-group]]

* [[L-∞ algebra]], [[smooth ∞-group]]

* [[Lie algebroid]], [[Lie groupoid]]

* [[L-∞ algebroid]], [[smooth ∞-groupoid]]

## References

* [[John Baez]], [[Alissa Crans]], _Higher-Dimensional Algebra VI: Lie 2-Algebras_ Theory and Applications of Categories, Vol. 12, (2004) No. 15, pp 492-528. ([TAC](http://www.tac.mta.ca/tac/volumes/12/15/12-15abs.html)) 

[[!redirects Lie 2-algebras]]
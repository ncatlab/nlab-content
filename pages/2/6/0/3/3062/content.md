
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

* equipped with [[linear functions]] as follows:

  a unary bracket $[-]$ encoding a _[[differential]]_ 

  $$
    \delta : \mathfrak{g}_1 \to \mathfrak{g}_0
    \,
  $$

  and a binary bracket $[-,-]$, whose component on elements in degree 0
  is a [[Lie bracket]]

  $$
    [-,-] : \mathfrak{g}_0 \vee \mathfrak{g}_0 \to \mathfrak{g}_0
  $$

  and whose component on elements in degree 0 and degree 1 is a _weak [[action]]_

  $$
    \alpha(-,-) : \mathfrak{g}_0 \otimes \mathfrak{g}_1 \to 
     \mathfrak{g}_1
     \,;
  $$
  
  and a trinary bracket

  $$
    [-,-,-] : \mathfrak{g}_0 \vee \mathfrak{g}_0 \vee \mathfrak{g}_0 \to \mathfrak{g}_1
  $$

  called the _Jacobiator_;


* such that

  * $[-,-]$ and $[-,-,-]$ are skew-symmetric in their arguments, as indicated;

  * the [[differential]] respects the brackets: for all $x \in \mathfrak{g}_0$ and $h \in \mathfrak{g}_1$ we have

    $$
      \delta [x,h] = [x, \delta h]
    $$

    hence

    $$
      \delta \alpha(x,h) = [x, \delta h]
      \,;
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

The Jacobiator identity equivalently expresses the [[commuting diagram|commutativity]] of the following [[diagram]] in the given [[2-vector space]] (analogous to the [[pentagon identity]])

<img src="https://ncatlab.org/nlab/files/JacobiatorIdentity.jpg" width="560">

> (graphics grabbed from [Baez-Crans 04, p. 19](#BaezCrans04))

### Strict case

If the trinary bracket $[-,-,-]$ in a Lie 2-algebra is trivial, one speaks of a [[strict Lie 2-algebra]]. Strict Lie 2-algebras are equivalently [[differential crossed module]]s (see there for details).


## Examples

* [[derivation Lie 2-algebra]]

* [[string Lie 2-algebra]]

* [[4d supergravity Lie 2-algebra]]

## Related concepts

* [[Lie algebra]], [[Lie group]]

* **Lie 2-algebra**, [[Lie 2-group]]

  * [[membrane matrix model]]

* [[Lie 3-algebra]], [[Lie 3-group]]

* [[L-∞ algebra]], [[smooth ∞-group]]

* [[Lie algebroid]], [[Lie groupoid]]

* [[L-∞ algebroid]], [[smooth ∞-groupoid]]

## References

* {#BaezCrans04} [[John Baez]], [[Alissa Crans]], _Higher-Dimensional Algebra VI: Lie 2-Algebras_ Theory and Applications of Categories, Vol. 12, (2004) No. 15, pp 492-528. ([TAC:12-15](http://www.tac.mta.ca/tac/volumes/12/15/12-15abs.html)) 

* [[Daniel Berwick-Evans]], [[Eugene Lerman]], _Lie 2-algebras of vector fields_, [arxiv/1609.03944](http://arxiv.org/abs/1609.03944)

On [[weak Lie 2-algebras]]:

* {#Roytenberg07} [[Dmitry Roytenberg]], _On weak Lie 2-algebras_, AIP Conference Proceedings 956, 180 (2007) ([arXiv:0712.3461](http://arxiv.org/abs/0712.3461), [doi:10.1063/1.2820967]( https://doi.org/10.1063/1.2820967))



[[!redirects Lie 2-algebras]]
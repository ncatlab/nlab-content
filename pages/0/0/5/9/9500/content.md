
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A double Lie algebroid is the [[Lie algebroid]]-analog of a [[Lie groupoid]]-[[double groupoid]]; essentially a Lie algebroid object [[internalization|internal]] to the category of Lie algebroids. 

## Examples

+-- {: .num_example}
###### Example

For $(A \stackrel{\rho}{\to} X, [-,-] : \wedge^2\Gamma(A) \to \Gamma)$ a [[Lie algebroid]], its **tangent double Lie algebroid** $T A$ is the degreewise [[tangent Lie algebroid]] of the base space $X$ and of the total space $A$, respectively

$$
  \array{
    T A &\stackrel{d \rho}{\to}& T X
    \\
    \downarrow && \downarrow
    \\
    A &\stackrel{\rho}{\to}& X
  }
  \,.
$$

=--

+-- {: .num_example}
###### Example

For 

$$
  \array{
    \mathcal{Mor}_1 &\stackrel{\to}{\to}& \mathcal{Mor}_0
    \\
    \downarrow && \downarrow
    \\
    \mathcal{Obj}_1 &\stackrel{\to}{\to}& \mathcal{Obj}_0
  }
$$

a [[double Lie groupoid]], applying [[Lie differentiation]] degreewise yields a double Lie algebroid

$$
  \array{
    Lie(\mathcal{Mor})
    \\
    \downarrow
    \\
    Lie(\mathcal{Obj})
  }
  \,.
$$

=--


## Related concepts

* [[double Lie algebroid]], [[Lie algebroid-groupoid]], [[double Lie groupoid]]


* [[foliation of a Lie algebroid]]

## References

The notion originates somewhere around

* [[Kirill Mackenzie]], _Double Lie algebroids and the double of a Lie bialgebroid_ ([arXiv:math/9808081](http://arxiv.org/abs/math/9808081))

Further discussion is in 

* [[Kirill Mackenzie]], _Double Lie algebroids and second-order geometry. I_. Adv. Math. 94 (1992), no. 2, 180&#8211;239

  _Double Lie algebroids and second-order geometry. II_. Adv.Math. 154 (2000), no. 1, 46&#8211;75. [dg-ga/9712013]([arXiv:dg-ga/9712013](http://arxiv.org/abs/dg-ga/9712013)).

A textbook account is in 

* [[Kirill Mackenzie]], _General theory of Lie groupoids and Lie algebroids_ Cambridge Univ. Press, Cambridge, 2005.MR2157566.

[[!redirects double Lie algebroids]]


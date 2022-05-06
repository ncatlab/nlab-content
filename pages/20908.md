
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The [[Lie algebra]] $\mathfrak{su}(2)$ is the special case of [[special unitary Lie algebras]] $\mathfrak{su}(n)$ for $n = 2$, underlying the [[Lie group]] [[SU(2)]] (the [[special unitary group]] $SU(n)$ for $n =2$).

## Idea

The Lie algebra $\mathfrak{su}(2)$ is equivalently given as follows:

1. the Lie algebra on 3 [[generators]] $\{\sigma_1, \sigma_2,\sigma_3\}$ subject to the following [[relations]] on their [[Lie bracket]]:

   $$
     [e_i, e_j] = \underset{k}{\sum} \epsilon_{i j k} e_k
   $$

1. the Lie algebra spanned by ($i$ times) the three [[Pauli matrices]] with [[Lie bracket]] their [[commutator]] in their [[matrix algebra]].

## Properties

### Pauli matrix presentation

+-- {: .num_prop}
###### Proposition

The [[Lie algebra]] $\mathfrak{su}(2)$ as a [[complex numbers|complex]] [[matrix Lie algebra]] is the sub Lie algebra on those matrices of the form

$$
  \left(
    \array{
      i z & x + i y
      \\
      - x + i y & - i z
    }
  \right)
  \;\;\;  
  with
  \;\;
  x,y,z \in \mathbb{R}
  \,.
$$

=--

(

+-- {: .num_defn}
###### Definition

The standard [[basis]] elements of $\mathfrak{su}(2)$ given by the above presentation are 

$$
  \sigma_1 
   \coloneqq
  \frac{1}{\sqrt{2}}
  \left(
   \array{
     0 & 1
     \\
     -1 & 0
   }
  \right)
$$

$$
  \sigma_2 
   \coloneqq
  \frac{1}{\sqrt{2}}
  \left(
   \array{
     0 & i
     \\
     i & 0
   }
  \right)
$$

$$
  \sigma_3
   \coloneqq
  \frac{1}{\sqrt{2}}
  \left(
   \array{
     i & 0
     \\
     0 & -i
   }
  \right)
  \,.
$$

These are called the _[[Pauli matrices]]_.

=--

+-- {: .num_prop}
###### Proposition

The [[Pauli matrices]] satisfy the [[commutator]] [[relations]]

$$
  [\sigma_1, \sigma_2] = \sigma_3
$$

$$
  [\sigma_2, \sigma_3] = \sigma_1
$$

$$
  [\sigma_3, \sigma_1] = \sigma_2
  \,.
$$


=--


### Complexification
 {#Complexification}

The [[complexification]] of $\mathfrak{su}(2)$ is the [[special linear Lie algebra]] $\mathfrak{sl}(2, \mathbb{C})$ (see at [[sl(2)]]) (...)

## Related concepts

* [[fuzzy 2-sphere]]

  [[fuzzy funnel]], [[Dp-D(p+2)-brane bound state]]

* [[SU(2)]]

## References

Textbook accounts:

* {#Pfeifer} Walter Pfeifer, _The Lie algebra $\mathfrak{su}(2)$_, In: _The Lie Algebras $\mathfrak{su}(N)$, Birkhäuser, Basel (2003) ([doi:10.1007/978-3-0348-8097-8_3](https://doi.org/10.1007/978-3-0348-8097-8_3), [pdf](https://link.springer.com/content/pdf/10.1007/978-3-0348-8097-8_3.pdf))

See also

* [[Qiaochu Yuan]], _[The representation theory of SU(2)](https://qchu.wordpress.com/2011/06/26/the-representation-theory-of-su2/)_

* Wikipedia, _<a href="https://en.m.wikipedia.org/wiki/Representation_theory_of_SU(2)">Representation theory of SU(2)</a>_


[[!redirects su2]]

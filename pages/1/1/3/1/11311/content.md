
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Jacobi forms are [[power series]] of two variables which in one variable behave like a [[modular form]] and in the other have an "elliptic" nature. They arise naturally as the characteristic series of the [[elliptic genus]]/[[Witten genus]] ([Zagier 86, pages 8-9](#Zagier86)).

## Definition

For $k, n \in \mathbb{Z}$, a _Jacobi form_ of _weight_ $k$ and _index_ $n$ is a [[function]] of the form

$$
  \phi \;\colon\; H \times \mathbb{C} \longrightarrow \mathbb{C}
$$

hence from the [[product]] of the [[upper half plane]] with the full [[complex plane]] which transforms under

$$
  \left(
    \array{
       a & b
       \\
       c & d
    }
  \right)
  \in 
  SL_2(\mathbb{Z})
$$

as

$$
  \phi
  \left(
     \frac{a \tau + b}{c \tau + d},
     \frac{z}{c \tau + d}
  \right)
   =
  (c \tau+ d)^k
  \exp(2 \pi i n c z^2 / (c \tau + d))
  \phi(\tau, z)
  \,.
$$

## Examples

### Jacobi theta-functions
 {#JacobiThetaFunctions}

The most important examples are the  [[Jacobi theta-functions]].
The four Jacobi $\theta$-functions are (with $q = e^{2\pi i \tau}$)

$$
  \theta(z,\tau) 
    \coloneqq
  2 q^{1/8} sin(\pi z)
  \prod_{j = 1}^{\infty}
  \left(   
    \left(
      1 - q^{j}
    \right)
    \left(
      1 - e^{2\pi i z} q^{j}
    \right)
    \left(
      1 - e^{-2 \pi i z} q^{j}
    \right)
  \right)
$$

$$
  \theta_1(z,\tau) 
    \coloneqq
  2 q^{1/8} cos(\pi z)
  \prod_{j = 1}^{\infty}
  \left(   
    \left(
      1 - q^{j}
    \right)
    \left(
      1 + e^{2\pi i z} q^{j}
    \right)
    \left(
      1 + e^{-2 \pi i z} q^{j}
    \right)
  \right)
$$

$$
  \theta_2(z,\tau) 
    \coloneqq
   \;\;\;\;\;\;\;\;\;
  \prod_{j = 1}^{\infty}
  \left(   
    \left(
      1 - q^{j}
    \right)
    \left(
      1 - e^{2\pi i z} q^{j - 1/2}
    \right)
    \left(
      1 - e^{-2 \pi i z} q^{j - 1/2}
    \right)
  \right)
$$

$$
  \theta_3(z,\tau) 
    \coloneqq
   \;\;\;\;\;\;\;\;\;
  \prod_{j = 1}^{\infty}
  \left(   
    \left(
      1 - q^{j}
    \right)
    \left(
      1 + e^{2\pi i z} q^{j - 1/2}
    \right)
    \left(
      1 + e^{-2 \pi i z} q^{j - 1/2}
    \right)
  \right)
$$

See for instance ([KL 95, section 2.4](#KL95), [Chen-Han-Zhang 10, section 2](#ChenHanZhang10)) for a review in the context of [[elliptic genera]].

As part of this, the [[Kac-Weyl character]] of an integral highest-weight [[loop group representation]] is a Jacobi form ([KL 95, section 2.2](#KL95)).


The **Jacobi identity** (see at _[[Jacobi triple product]]_) asserts that these are related by


$$
  \theta'(0,\tau) \coloneqq \frac{\partial}{\partial z}\theta(0,\tau)
  =
  \pi \theta_1(0,\tau) \theta_2(0,\tau) \theta_3(0,\tau)
  \,.
$$

### Weierstrass function

(...)

## References

The original canonical account is

* Martin Eichler, [[Don Zagier]], _The theory of Jacobi forms_, Progress in Mathematics 55, Boston, MA: Birkh&#228;user Boston (1985), ISBN 978-0-8176-3180-2, MR 781735 

Discussion of Jacobi forms as coefficients of the [[elliptic genus]]/[[Witten genus]] includes

* {#Zagier86} [[Don Zagier]], pages 8,9 of _Note on the Landweber-Stong elliptic genus_ 1986 ([pdf](http://people.mpim-bonn.mpg.de/zagier/files/doi/10.1007/BFb0078047/fulltext.pdf))

* {#KL95} [[Kefeng Liu]], _On modular invariance and rigidity theorems_, J. Differential Geom. Volume 41, Number 2 (1995), 247-514 ([EUCLID](http://projecteuclid.org/euclid.jdg/1214456221), [pdf](http://www.math.ucla.edu/~liu/Research/loja.pdf))

* {#AndoFrenchGanter08} [[Matthew Ando]], Christopher French, [[Nora Ganter]], _The Jacobi orientation and the two-variable elliptic genus_, Algebraic and Geometric Topology 8 (2008) p. 493-539 ([pdf](https://msp.org/agt/2008/8-1/agt-v8-n1-p16-s.pdf))

* {#ChenHanZhang10} Qingtao Chen, [[Fei Han]], [[Weiping Zhang]], _Generalized Witten Genus and Vanishing Theorems_, Journal of Differential Geometry 88.1 (2011): 1-39. ([arXiv:1003.2325](http://arxiv.org/abs/1003.2325))

See also

* Wikipedia, _[Jacobi form](http://en.wikipedia.org/wiki/Jacobi_form)_

[[!redirects Jacobi forms]]

[[!redirects Jacobi theta-function]]

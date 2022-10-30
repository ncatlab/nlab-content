

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _tensor product of distributions_ is the generalization to [[distributions]] of the [[tensor product]] of [[smooth functions]], hence it defines for two distributions $u \in \mathcal{D}'(X)$ and $v \in \mathcal{D}'(Y)$ a new distribution $u \otimes v \in \mathcal{D}'(X \times Y)$ on the [[Cartesian product]] space which, as a [[generalized function]] behaves like $(u \otimes v)(x,y) = u(x) \cdot v(y)$.

## Definition

+-- {: .num_defn #TensorProductOfSmoothFunctions}
###### Definition
**(tensor product of smooth functions)**

For $X_1, X_2$ two [[open subsets]] of some [[Cartesian space]], there is an [[injective function|injection]] from the [[tensor product of modules|tensor product]] of the [[real vector spaces]] of [[smooth functions]] on the separate spaces to that on the [[Cartesian product]] space:

$$
  \array{
    C^\infty(X_1) \otimes_{\mathbb{R}} C^\infty(X_2)
      &\overset{}{\hookrightarrow}&
    C^\infty(X_1 \times X_2)
    \\
    (f_1, f_2)
    &\mapsto&
    f_1 \otimes f_2
  }
$$

with 

$$
  (f_1 \otimes f_2)(x_1, x_2) \coloneqq f_1(x_1) \cdot f_2(x_2)
  \,.
$$


=--

+-- {: .num_prop #TensorProductOfDistributions}
###### Proposition
**(tensor product of distributions)**

Let $u_1 \in \mathcal{D}'(X_1)$ and $u_2 \in \mathcal{D}'(X_2)$ be [[distributions]]. Then there is a unique distribution $u_1 \otimes u_2 \in \mathcal{D}'(X_1 \times X_2)$ such that for all pairs of [[bump functions]] $b_1 \in C_c^\infty(x)$ and $b_2 \in C^\infty(X_2)$ its value on their tensor product according to def. \ref{TensorProductOfSmoothFunctions} is

$$
  u(b_1 \otimes b_2)
  =
  u_1(b_1) \cdot u_2(b_2)
  \,.
$$

This $u_1 \otimes u_2$ is called the _tensor product_ of $u_1$ with $u_2$

=--

([H&#246;rmander 90, theorem 5.1.1](#Hoermander90))

## Properties


+-- {: .num_example #WaveFrontOfTensorProductDistribution}
###### Example
**([[wave front set]] of tensor product distribution)**

Let $u \in \mathcal{D}'(X)$ and $v \in \mathcal{D}'(Y)$ be two distributions. then the [[wave front set]] of their tensor product distribution $u \otimes v \in \mathcal{D}'(X \times Y)$ (def. \ref{TensorProductOfDistributions}) satisfies

$$
  WF(u \otimes v)
  \;\subset\;
  \left(
     WF(u) \times WF(v)
  \right)
    \cup
  \left(
    \left( supp(u) \times \{0\} \right)
    \times WF(v)
  \right)
    \cup
   \left(
     WF(u)
     \times
     \left(
       supp(v) \times \{0\}
     \right)
   \right)
  \,,
$$

where $supp(-)$ denotes the [[support of a distribution]].

=--

([H&#246;rmander 90, theorem 8.2.9](#Hoermander90))


## Related concepts

* [[Schwartz kernel theorem]]

## References

* {#Hoermander90} [[Lars Hörmander]], section 5.1 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990 ([pdf](http://www.ctr.maths.lu.se/media/MATP11/2014vt2014/distho.pdf))


[[!redirects tensor products of distributions]]

[[!redirects tensor product distribution]]
[[!redirects tensor product distributions]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Harmonic analysis
+-- {: .hide}
[[!include harmonic analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The Paley-Wiener-Schwartz theorem characterizes [[compact support|compactly supported]] [[smooth functions]] ([[bump functions]]) and more generally [[compactly supported distributions]] in terms of the decay property of their [[Fourier-Laplace transform]] ([[Fourier transform of distributions|of distributions]]).

Conversely this means that for a general distribution those [[covectors]] along which its [[Fourier transform of distributions|Fourier transform]] does not suitably decay detect the singular nature of the distribution (its failure to be represented by a smooth function) in a refined form which records not only the [[singular support of a distribution|singular support]] (the point at which that covector is based), but also the "direction of [[propagation of singularities theorem|propagation of singularities]]". The collection of these covectors is called the _[[wave front set]]_ of the distribution. The study of [[functional analysis]] with attention to the [[wave front sets]] is called _[[microlocal analysis]]_. This plays a central role in the definition of various operations on distributions, such as the [[pullback of distributions]] and the [[product of distributions]].


## Statement


+-- {: .num_theorem}
###### Theorem
**(Paley-Wiener-Schwartz theorem)**

For $n \in \mathbb{N}$ the vector space $C^\infty_c(\mathbb{R}^n)$ of [[compact support|compactly supported]] [[smooth functions]] ([[bump functions]]) on [[Euclidean space]] $\mathbb{R}^n$ is (algebraically and topologically) [[isomorphism|isomorphic]], via the [[Fourier transform]], to the space of [[entire functions]] $F$ on $\mathbb{C}^n$ which satisfy the following estimate: there is a [[positive number|positive]] [[real number]] $B$ such that for every [[integer]] $N \gt 0$ there is a real number $C_N$ such that:

$$ 
  \underset{\xi \in \mathbb{C}^n}{\forall} 
  \left(
    {\vert  F(\xi) \vert}
    \le C_N (1 + {\vert \xi\vert })^{-N} \exp{ (B \; |Im(\xi)|)}
  \right)
  \,.
$$ 

More generally, the space of [[compactly supported distributions]] on $\mathbb{R}^n$ of [[order of a distribution|order]] $N$ is isomorphic via [[Fourier transform of distributions]] to those [[entire functions]] on $\mathbb{C}^n$ for which there exists positive [[real numbers]] $C$ and $B$ such that

$$ 
  \underset{\xi \in \mathbb{C}^n}{\forall} 
  \left(
    {\vert F(\xi)  \vert}
      \le 
    C_N (1 + {\vert \xi\vert })^{N} \exp{ (B \; |Im(\xi)|)}
  \right)
  \,.
$$ 

(Notice that the [[Fourier-Laplace transform]] [[Fourier transform of a distribution|of a]] [[compactly supported distribution]] is guaranteed to be an [[entire holomorphic function]], by [this prop.](Fourier+transform+of+distributions#FourierTransformOfCompactlySupportedDistributions).)

=--

(e.g. [Hoermander 90, theorem 7.3.1](#Hoermander90))

In fact

+-- {: .num_prop #DecayPropertyOfFourierTransformOfCompactlySupportedFunctions}
###### Proposition
**(decay of [[Fourier transform of distributions|Fourier transform]] of [[compactly supported functions]])**

A [[compactly supported distribution]] $u \in \mathcal{E}'(\mathbb{R}^n)$ is non-[[singular support of a distribution|singular]], hence given by a [[compactly supported function]] $b \in C^\infty_{cp}(\mathbb{R}^n)$ via $u(f) = \int b(x) f(x) dvol(x)$, precisely if its [[Fourier transform of a distribution|Fourier transform]] $\hat u$ ([this def.](compactly+supported+distribution#FourierTransformOfCompactlySupportedDistribution)) satisfies the following decay property:

For all $N \in \mathbb{N}$ there exists $C_N \in \mathbb{R}_+$ such that for all $\xi \in \mathbb{R}^n$ we have that the [[absolute value]] ${\vert \hat v(\xi)\vert}$ of the Fourier transform at that point is bounded by

$$
  {\vert \hat v(\xi)\vert}
  \;\leq\;
  C_N \left( 1 + {\vert \xi\vert} \right)^{-N}
  \,.
$$

=--

(e.g. [Hoermander 90, around (8.1.1)](#Hoermander90))

## Related entries

* [[Fourier transform of distributions]]

## References

* {#Hoermander90} [[Lars Hörmander]], section 7.3 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

See also

* Wikipedia, _[Paley-Wiener theorem](https://en.wikipedia.org/wiki/Paley%E2%80%93Wiener_theorem)_

[[!redirects Paley-Wiener theorem]]

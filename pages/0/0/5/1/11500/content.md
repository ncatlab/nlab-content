

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Statement

For $U \subset \mathbb{C}$ an [[open subset]] of the [[complex plane]] $\mathbb{C}$ and for $C$ a [[Jordan curve]] in $U$, a [[holomorphic function]] $f$ of $U$ sends a point $\zeta$ enclosed by $C$ to the [[contour integral]]

$$ 
  f(\zeta) =  \frac{1}{2\pi\mathrm{i}}\oint_C \frac{f(z)}{z - \zeta} \,\mathrm{d}z.
$$

Hence the [[contour integral]] picks out the enclosed _[[residues]]_.

More generally, this implies, by [[Taylor series]] expansion of $f$, that for $n \in \mathbb{N}$ the $n$th complex [[derivative]] $f^{(n)}$ is

$$
  f^{(n)}(\zeta)
    =
  \frac{n!}{2\pi i}  \oint_C \frac{f(z)}{(z - \zeta )^{n+1}} d z
  \,.
$$

This is also known as _Cauchy's differentiation formula_.

## Proof in synthetic differential geometry

Here is a proof written in terms of [[synthetic mathematics|synthetic]] [[infinitesimals]] as in [[synthetic differential geometry]]: 

Let $\epsilon$ be a nilpotent. Let $S_\epsilon$ denote the [[circle]] of [[radius]] $\epsilon$ centered at $\zeta$. By the holomorphicity of $f$, the [[differential 1-form]] $f(z)/(z-\zeta) \,\mathrm{d}z$ is [[closed differential form|closed]] in the region bounded by $C$ and $S_\epsilon$. By the [[Stokes theorem]],  
$$\frac{1}{2\pi\mathrm{i}}\oint_C \frac{f(z)}{z - \zeta} \,\mathrm{d}z = \frac{1}{2\pi\mathrm{i}}\oint_{S_\epsilon} \frac{f(z)}{z - \zeta} \,\mathrm{d}z.$$
Parametrize $S_\epsilon$ by 
$(t\mapsto \zeta + \epsilon \,\exp(2\pi\mathrm{i}t))$ 
to transform the above integral to
$$\frac{1}{2\pi\mathrm{i}}\int_0^1 \frac{f(\zeta + \epsilon\, \exp(2\pi\mathrm{i}t))}{\epsilon \,\exp(2\pi\mathrm{i}t))} \,\mathrm{d}(\zeta + \epsilon\, \exp(2\pi\mathrm{i}t)) = \int_0^1 f(\zeta + \epsilon\, \exp(2\pi\mathrm{i}t)) \, \mathrm{d}t$$
By the infinitesimal [[Taylor series|Taylor formula]] and the [[holomorphic function|holomorphicity]] of $f$, 
$$f(\zeta + \epsilon\exp(2\pi\mathrm{i}t)) = f(\zeta) + \epsilon\,\exp(2\pi\mathrm{i}t) \frac{\partial f(\zeta)}{\partial z}.$$
Hence the above integral is equal to
$$\int_0^1 \left[f(\zeta) + \epsilon\,\exp(2\pi\mathrm{i}t) \frac{\partial f(\zeta)}{\partial z}\right] \, \mathrm{d}t = \left[f(\zeta) + \epsilon\frac{\partial f(\zeta)}{\partial z} \int_0^1 \exp(2\pi\mathrm{i}t)  \, \mathrm{d}t\right] = f(\zeta).$$

## Related concepts

* [[Cauchy's integral theorem]]

* [[Cauchy's theorems]]

* [[Goursat theorem]]


## References

* Wikipedia, _[Cauchy's integral formula](https://en.wikipedia.org/wiki/Cauchy's_integral_formula)_

[[!redirects Cauchy integral formula]]

[[!redirects Cauchy differentiation formula]]
[[!redirects Cauchy's differentiation formula]]


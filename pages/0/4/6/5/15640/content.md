
#Contents#
* table of contents
{:toc}

## Idea

The archetypical exmaple of a [[zeta function]]:

$$
   \zeta \colon s \mapsto \underset{n = 1}{\sum}^\infty \frac{1}{n^s}
  \,.
$$


## Properties

### Relation to the Jacobi theta function
 {#RelationToThetaFunctions}

The _completed_ Riemann zeta function is 

$$
  \hat \zeta(s) \coloneqq \pi^{-s/2}\Gamma(s/2)\zeta(s)
 \,.
$$

This has an [[integral]]-representation in terms of the [[Jacobi theta function]]

$$
  \theta(x)\coloneqq \underset{n \in \mathbb{Z}}{\sum} \exp(- \pi n ^2 x)
$$

in the form

$$
  \hat \zeta(s)
  = 
   \int_0^\infty (\theta(x^2)-1) x^s  \frac{d x}{x}
 \,.
$$

e.g. ([Fesenko 08, section 0.1](#Fesenko08))

## References


Discussion in the more general context of [[higher arithmetic geometry]] is in 

* {#Fesenko08} [[Ivan Fesenko]], _Adelic approch to the zeta function of arithmetic schemes in dimension two_, Moscow Math. J. 8 (2008), 273&#8211;317 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/ada.pdf))

[[!redirects Riemann zeta-function]]

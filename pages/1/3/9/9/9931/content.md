
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[moduli stack of formal groups]] $\mathcal{M}_{FG}$ admits a natural [[stratification]] whose open [[strata]] are labeled by a [[natural number]] called the _height_ of formal groups.

The [[complex oriented cohomology theories]] associated to these [[formal groups]] by the [[Landweber exact functor theorem]] accordingly also inherit such an integer label, called _[[chromatic filtration]]_. Studying this is the topic of [[chromatic homotopy theory]].

## Definition

Let $R$ be a [[commutative ring]] and fix 

$$
  f(x,y) \in R [ [ x,y ] ]
$$ 

a [[formal group law]] over $R$. 



+-- {: .num_defn}
###### Definition

For every $n \in \mathbb{N}$ the **$n$-series** of $f$ 

$$
  [n](t) \in R[ [ t ] ] 
$$

is defined [[recursion|recursively]] by

1. if $n = 0$ then $[n](t) = 0$;

1. if $n \gt 0$ then $[n](t) = f([n-1](t),t)$.

=--


Now fix $p \in \mathbb{N}$ a [[prime number]], 

+-- {: .num_defn}
###### Definition

Write $v_n$ for the [[coefficient]] of $t^{p^n}$ in the $p$-series $[p]$ of $f$.

=--

+-- {: .num_defn}
###### Definition

Say that $f$

* has **height** $\geq n$ if $v_i = 0$ for $i \lt n$;

* has **height exactly** $n$ if it has height $\geq n$ and $v_n \in R$ is invertible.

=--

For instance ([Lurie 10, lecture 12, def. 13](#Lurie10)).

## Examples

+-- {: .num_example}
###### Example

For $f(x,y) = x + y + x y$ the [[formal multiplicative group]] the $n$-series is 

$$
  [n](t) = (1+t)^n - 1
  \,.
$$

If $p = 0$ in $R$ then 

$$
  [p](t) = (1+t)^p - 1 = t^p
$$ 

and thus $f$ has height exactly 1.

=--

For instance ([Lurie 10, lecture 12, example 16](#Lurie10)).

+-- {: .num_example}
###### Example

An [[elliptic curve]] over a [[field]] of [[positive number|positive]] [[characteristic]] whose [[formal group law]] has [[height of a formal group|height]] equal to 2 is called a _[[supersingular elliptic curve]]_. Otherwise the height equals 1 and the elliptic curve is called _ordinary_.

=--

## Properties

### Chromatic height filtation

The height of formal groups induces the [[height filtration]] on the [[moduli stack of formal groups]].

[[!include Lurie spectral sequences -- table]]



## Related pages

* [[moduli stack of formal groups]]

* [[chromatic homotopy theory]]

* [[Morava K-theory]]

## References

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series (2010) ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html)), Lecture 12 _Heights and formal groups_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture12.pdf))
 


[[!redirects height of a formal group law]]

[[!redirects height of formal groups]]

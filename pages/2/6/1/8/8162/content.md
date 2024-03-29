
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For 

$$
  \cdots
  \hookrightarrow
   X_{(n)} 
  \hookrightarrow X_{(n+1)} \hookrightarrow \cdots \hookrightarrow X  
$$ 

a [[filtered object]] in an [[abelian category]] $\mathcal{C}$, the _associated graded object_ $Gr(X)$ is the [[graded object]] which in degree $n$ is the [[cokernel]] of the $n$th inclusion, fitting into a [[short exact sequence]]

$$
  0 \to X_{(n-1)} \to X_{(n)} \to Gr_n(X) \to 0
  \,,
$$

hence the [[quotient]] of the $n$th layer of $X$ by the next lower one:

$$
  Gr_n(X) := X_{(n)}/X_{(n-1)}
  \,,
$$

## Examples

* For $\mathcal{A}$ an [[abelian category]] and $C_{\bullet, \bullet}$ a [[double complex]] in $\mathcal{A}$, let $X = Tot(C)$ be the corresponding [[total complex]]. This is naturally filtered by either row-degree or by column-degree. The corresponding associated graded complex is what the terms in the _[[spectral sequence of a filtered complex]]_ compute.

* [[associated graded vector space]]

## Related concepts

[[!include filtered objects -- contents]]


## References

Discussion of the universal property of the associated graded construction on [mathoverflow](http://mathoverflow.net/questions/263/what-is-the-universal-property-of-associated-graded)


[[!redirects associated graded]]
[[!redirects associated graded objects]]

[[!redirects associated graded space]]
[[!redirects associated graded spaces]]



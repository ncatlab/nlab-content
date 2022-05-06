
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Rational parametrized homotopy theory is _[[parametrized homotopy theory]]_ in the approximation of [[rational homotopy theory]].

## Properties


+-- {: .num_prop #} 
###### Proposition

Let

$$
  \array{
    F &\overset{fib(p)}{\longrightarrow}& A
    \\
    && \big\downarrow{}^{\mathrlap{p}}
    \\
    && B    
  }
$$

be a [[Serre fibration]] of [[connected topological space|connected]] [[topological spaces]], with [[fiber]] $F$ (over any base point) also connected.

If in addition

1. the [[fundamental group]] $\pi_1(B)$ [[nilpotent module|acts nilpotently]] on the [[homology groups]] $H_\bullet(F,k)$ 

   (e.g. if $B$ is [[simply connected topological space|simply connected]]);

1. at least one of $A$, $F$ has rational [[finite type]] 

then the [[cofiber]] of any [[relative Sullivan model]] for $p$ is a [[Sullivan model]] for $F$.

=-- 

([Félix-Halperin-Thomas 00, Theorem 15.3](#FelixHalperinThomas00), following [Halperin 83, Section 16](#Halperin83))


Moreover, if $CE(\mathfrak{l}B)$ is a [[minimal Sullivan model]] for $B$, then the cofiber of the corresponding minimal [[relative Sullivan model]] for $p$ is the [[minimal Sullivan model]] $CE(\mathfrak{l}F)$ for $F$:

$$
  \array{
    CE(\mathfrak{l}F)
    &\overset{
      cofib
      \big(
        CE(\mathfrak{l}p)
      \big)
    }{\longleftarrow}&
    CE(\mathfrak{l}_{{}_B}A)
    \\
    && \big\downarrow{}^{\mathrlap{ CE(\mathfrak{l}p) }}
    \\
    && CE(\mathfrak{l}B)
  }
$$

([Félix-Halperin-Thomas 00, Corollary on p. 199](#FelixHalperinThomas00)) 

## Related concepts

* [[parametrized homotopy theory]]

* [[rational parametrized stable homotopy theory]]

## References

* {#Halperin83} [[Steve Halperin]], Section 16-20 of: _Lectures on minimal models_, Mem. Soc. Math. Franc. no 9/10 (1983) ([doi:10.24033/msmf.294](https://doi.org/10.24033/msmf.294))


* {#Silveira84} [[Flavio da Silveira]], _Rational homotopy theory of fibrations_, Pacific Journal of Mathematics, Vol. 113, No. 1 (1984) ([pdf](http://msp.org/pjm/1984/113-1/pjm-v113-n1-p01-s.pdf))



* {#FelixHalperinThomas00} [[Yves Félix]], [[Stephen Halperin]], [[Jean-Claude Thomas]], Sections 14 and 15 of: _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000 ([doi:10.1007/978-1-4613-0105-9](https://link.springer.com/book/10.1007/978-1-4613-0105-9))

[[!redirects parametrized rational homotopy theory]]
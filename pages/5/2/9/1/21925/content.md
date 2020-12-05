

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Let $X \overset{f}{\longrightarrow} Y$ be a [[morphism]] in the [[stable homotopy category]] and let $E$ be a [[Whitehead-generalized cohomology theory]] (usually assumed to be at least [[multiplicative cohomology theory|multiplicative]]).

Then the _$d$-invariant of $f$_ with respect to $E$ is just the class of the corresponding [[pullback in cohomology|pullback]] morphism, regarded as an element of the 0th [[Ext-group]] (i.e. the plain [[hom-object]]) between the $E$-cohomologies of $X$ and $Y$:

$$
  d(f)
  \;\in\;
  Ext^0
  \big(
    E^\bullet(Y);
    \,
    E^\bullet(X);    
  \big)
  \,.
$$

The fancy name is justified by the fact that this is beginning of a hierarchy of more interesting invariants of stable maps seen in $E$-cohomology, each of which defined when the previous one vanishes: The next is the _[[e-invariant]]_, then comes the _[[f-invariant]]_ (e.g. [BL 09, Section 2](#BL09)), all this being part of the structure seen on the second page of the $E$-[[Adams spectral sequence]] for $[X,Y]_\bullet$.


## Related concepts

* [[e-invariant]]

* [[f-invariant]]

[[!include notions of pullback -- contents]]

## References

* {#Adams66} [[John Adams]], Section 7 of: _On the groups $J(X)$ IV_, Topology 5: 21 (1966)   ([pdf](http://math.unice.fr/~cazanave/Gdt/ImJ/J-IV.pdf), <a href="https://doi.org/10.1016/0040-9383(66)90004-8">doi:10.1016/0040-9383(66)90004-8</a>)

See also

* {#BL09} Mark Behrens, Gerd Laures, _$\beta$-Family congruences and the $f$-invariant_, Geometry & Topology Monographs 16 (2009) 9–29 ([arXiv:0809.1125](https://arxiv.org/abs/0809.1125), [doi: 10.2140/gtm.2009.16.9](https://msp.org/gtm/2009/16/p002.xhtml))

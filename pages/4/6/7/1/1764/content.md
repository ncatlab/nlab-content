+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The model structure on [[presheaves]] of (Dwyer-Kan) [[simplicial groupoids]] ([[sSet]]-[[enriched groupoids]]) is one of the [[models for ∞-stack (∞,1)-toposes]]. It is a slight variant on the [[model structure on simplicial presheaves]]. (At that link more general information is collected).


For various applications it is useful to 

* use [[simplicial groupoids]] instead of [[Kan complexes]] or [[simplicial sets]];

* use a model structure on (pre)sheaves with values in [[simplicial groupoids]] instead of the [[model structure on simplicial presheaves]] (see there for motivation on why to consider these models in the first place).

An example is the discussion of [[principal infinity-bundles]] in section 3 of ([Jardine & Luo](#JardineLuo))



## Definition/Properties


+-- {: .num_prop}
###### Proposition

Write $(G \dashv \bar W) \colon Grpd^\Delta \leftrightarrow sSet$ for the [[Quillen adjunction]] discussed at *[[model structure on simplicial groupoids]]*. This directly prolongs to an [[adjunction]] on [[presheaves]]

$$
  (G \dashv \bar W)
  \colon
  [C^{op}, Grpd^\Delta]
   \stackrel{\overset{G}{\leftarrow}}{\underset{\bar W}{\to}}
  [C^{op}, sSet]_{inj}
  \,.
$$

The [[transferred model structure]] along $\bar W$ on $[C^{op}, Grpd^\Delta]$ of the  global injective [[model structure on simplicial presheaves]] exists on $[C^{op}, sSet, Grpd^\Delta]$: fibrations and weak equivalences are those that become global injective fibrations and weak equivalences, respectively, under $\bar W$.

=--

This appears as ([LBK, theorem 3.10](#LBK)).

## Related concepts

* [[model structure on simplicial sets]]

  * [[model structure on simplicial presheaves]]

* [[model structure on simplicial groupoids]]


## References

A model structure on [[sheaves]] with values in simplicial groupoids is due to

* [[Andre Joyal]] and [[Myles Tierney]], _Strong stacks and classifying spaces_, in: _Category theory_
(Como, 1990), volume 1488 of Lecture Notes in Math., pages 213&#8211;236. Springer, Berlin (1991) ([web](http://journals.cambridge.org/action/displayAbstract?fromPage=online&aid=2105376))

* [[Andre Joyal]] and [[Myles Tierney]], *On the homotopy theory of sheaves of simplicial groupoids*, Math. Proc. Cambridge Philos. Soc. **120** 2 (1996) 263-290

A model structure on [[presheaves]] with values in simplicial groupoids:

* {#LBK} Zhi-Ming Luo, Peter Bubenik, Peter Kim, _Closed model categories for presheaves of simplicial groupoids and presheaves of 2-groupoids_ ([arXiv](http://arxiv.org/abs/math.AT/0301045))
 

A model structure on simplicial sheaves of groupoids is discussed in

* [[Sjoerd Crans]], _Quillen closed model structure for sheaves_,  J. Pure Appl. Algebra  101 (1995), 35-57 ([web](http://home.tiscali.nl/secrans/papers/thcms.html))

* {#JardineLuo} [[John F. Jardine]], Luo, _Higher order principal bundles_ ([web](http://www.math.uiuc.edu/K-theory/0681/))

* {#Jardine15} [[John F. Jardine]], §9.4 in: *[[Local homotopy theory]]*, Springer Monographs in Mathematics (2015) &lbrack;[doi:10.1007/978-1-4939-2300-7](https://doi.org/10.1007/978-1-4939-2300-7)&rbrack;


[[!redirects model structures on presheaves of simplicial groupoids]]
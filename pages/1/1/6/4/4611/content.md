
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A [[category]] $D$ is called __sifted__ if [[colimits]] of [[diagrams]] of shape $D$ (called [[sifted colimits]]) commute with finite [[products]] in [[Set]].

Of course, $D$ is called **cosifted** if $D^{op}$ is sifted.

## Properties

Gabriel and Ulmer proved that an [[inhabited set|inhabited]] category is sifted if and only if the [[diagonal functor|diagonal]] $D \to D\times D$ is a [[final functor]].  More explicitly, this means that for every pair of objects $d_1,d_2\in D$, the category $Cospan_D(d_1,d_2)$ of [[cospans]] from $d_1$ to $d_2$ is [[connected category|connected]].

Note that this condition holds in particular if $D$ has finite [[coproducts]], since then it is nonempty (it has an [[initial object]]) and each category of cospans has an initial object (the coproduct).


## Related concepts

* **sifted category**

* [[sifted (∞,1)-category]]

## References

*  P. Gabriel and F. Ulmer, _Lokal pr&#228;sentierbare Kategorien_ , Springer LNM
221, Springer-Verlag 1971
*  J. Adamek, J. Rosicky, E.M. Vitale, _What are sifted colimits?_, TAC __23__ (2010) pp. 251--260.  [link](http://www.tac.mta.ca/tac/volumes/23/13/23-13abs.html)


[[!redirects sifted categories]]
[[!redirects cosifted category]]
[[!redirects cosifted categories]]

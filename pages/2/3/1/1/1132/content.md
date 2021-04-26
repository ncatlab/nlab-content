
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##  Idea

$\infinity$-Stackification is another term for [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-sheafification]]. It is the direct [[(infinity,1)-category|(∞,1)-categorical]] analog of the following 1-categorical situation.

Recall that for $S$ a [[site]], [[sheafification]] is the [[functor]]
$$
  \bar{(-)} : PSh(S) \to Sh(S) \hookrightarrow PSh(S)
$$
which sends every [[presheaf]] $F$ on $S$ to another [[presheaf]] $\bar F$ which is weakly equivalent to $F$ with respect to the [[homotopical category]] structure on $PSh(S)$ induced from the [[Grothendieck topology]] on $X$. The presheaf $\bar F$ respects weak equivalences and satisfies [[descent]] in that the [[hom-functor]] $Hom_{PSh(S)}(-,\bar F)$ sends weak equivalences (the [[local isomorphism]]s) to weak equivalences.

Essentially by definition (according to [[Higher Topos Theory]]) the situation for $\infty$-stacks is entirely analogous, as described at [[(∞,1)-category of (∞,1)-sheaves]].

(Noticing that "$\infty$-stack" is synonymous to "[[(∞,1)-sheaf]]", "$\infty$-stackification" to "$(\infty,1)$-sheafification", and so on.

## Examples

* A concrete model for such $\infty$-stacks is the Brown-Joyal-Jardine-To&#235;n model using a [[model structure on simplicial presheaves]]. With respect to this [[model category]] structure on [[simplicial presheaf|simplicial presheaves]] the _fibrant objects_
are the globally [[Kan complex]]-valued (i.e. [[∞-groupoid]]-valued) presheaves that satisfy [[descent for simplicial presheaves]]. Therefore here $\infty$-stackification is given by _[[fibrant resolution|fibrant replacement]]_ in the model category.


## Related concepts

* [[sheafification]], [[plus-construction on presheaves]]

* [[(∞,1)-sheafification]] / **∞-stackification** 

## References

For instance section 6.5.3 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects ∞-stackification]]


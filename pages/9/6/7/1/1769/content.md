
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


# Complete spaces
* table of contents
{: toc}

## Idea

A [[space]] (with "space" taken in a sense relevant to the field of [[topology]]) is _complete_ (or _Cauchy-complete_) if every [[sequence]], [[net]], or [[filter]] that should converge really does [[convergence|converge]].  We identify the sequences, nets, or filters that "should" converge as the _[[Cauchy sequence|Cauchy]]_ ones.

A space that is not complete has "gaps" that may be filled to form its _completion_; it is rather natural to make the space (or equivalently its underlying topological space) [[Hausdorff space|Hausdorff]] at the same time.  Forming the completion of a Hausdorff space is an important example of [[completion]] in the general abstract sense. 


## Definitions

A space (which may be a [[metric space]], a [[Cauchy space]], or anything in between) is __Cauchy-complete__, or simply __complete__, if every [[Cauchy filter]] converges, equivalently if every [[Cauchy net]] converges.  A space is __sequentially complete__ if every [[Cauchy sequence]] converges.  Note that a sequentially complete metric space must be complete (in [[classical mathematics]]), but this does not hold for more general spaces (nor even for metric spaces in [[constructive mathematics]]).

A space is __topologically complete__ if its [[underlying topological space]] is completely [[metrizable space|metrizable]].  There are various other notions related to this.  See [[topologically complete space]].


## Completion

The set $\mathcal{C}X$ of Cauchy filters on a space $X$ may generally be given the same sort of structure as $X$ itself has, and this space will be complete.  Exactly how to do this depends on what structure $X$ is supposed to have, of course, and one can make the general statement false by requiring something artificial as the structure in question, most extremely the structure of being a specific non-complete space.  But it works for most natural categories of spaces.

The general idea is this: every point in $X$ generates a principal [[ultrafilter]] (consisting of those sets to which the point belongs), so there is a natural map from $X$ to $\mathcal{C}X$.  Furthermore, this map is a morphism of the appropriate structure, which in particular makes it [[Cauchy-continuous map|Cauchy-continuous]] (preserving Cauchy filters) and continuous (preserving limits).  So all of the limits in $X$ still exist in $\mathcal{C}X$, but now each Cauchy filter in $X$ (having become both a Cauchy filter in $\mathcal{C}$ and a point in $\mathcal{C}$) has a limit as well.  The additional Cauchy filters based on the additional points in $\mathcal{C}X$ will also have a limit in $\mathcal{C}X$, essentially because $\mathcal{C}$ is a [[monad]] (so a Cauchy filter of Cauchy filters folds into a single Cauchy filter).

There is a problem that $\mathcal{C}X$ is rather larger than necessary; for example, all of the filters that converge to a given point in $X$ (not just the free ultrafilter at that point) exist in $\mathcal{C}X$ and converge to one another.  But you can take a [[quotient space|quotient]] of $\mathcal{C}X$ to make it Hausdorff, obtaining the __Hausdorff completion__ of $X$.  In case $X$ was not Hausdorff to begin with, one can sometimes also force the quotient to leave in just as much redundancy as $X$ has but no more, obtain a straight __completion__ of $X$.  But really, it\'s most natural to make the space Hausdorff at the same time.

+-- {: .standout}
Details to come, if I get around to it.
=--

We have a picture like this, where $X$ is the original space, $\mathcal{H}$ gives a Hausdorff quotient, and an overline indicates completion:
$$ \array {
  &                 & \overline{X} \\
  & \hookrightarrow &              & &#8608; \\
X &                 &              &                 & \mathcal{H}\overline{X} \cong \overline{\mathcal{H}X} \\
  & &#8608;        &              & \hookrightarrow \\
  &                 & \mathcal{H}X
} $$
(Here the arrows are drawn horizontally to put styles on them; they should all be diagonal in the only possible way.)

At least if $X$ is a [[metric space]], then we can also construct its completion as a [[locale]], the [[localic completion]], whose spatial part is the above space, but which in [[constructive mathematics]] may not be spatial.  This is useful to have even if $X$ is already complete.


## Properties

### Relation to compact spaces

A [[compact space]] is necessarily complete.  A space is called __precompact__ if its completion is compact.  For metric spaces (or even [[uniform spaces]]), there is a natural notion of a [[totally bounded space]]; in [[classical mathematics]], we have the theorem that a space is totally bounded if and only if it is precompact.  Similarly, a space is compact if and only if it is both complete and totally bounded (or in [[constructive mathematics]], both complete and precompact).  Thus the purely topological property of compactness is the conjunction of the nontopological properties of completeness and total boundedness.

In some [[constructive analysis|constructive approaches to analysis]] (including most of Brouwer\'s school and some of Bishop\'s school), 'complete and totally bounded' is taken as the *definition* of 'compact', because it holds of examples such as the [[unit interval]] that fail to be compact (in the usual sense) without the [[fan theorem]].  However, in this case, compactness is no longer a [[topological property]]; see [[Bishop-compact space]] for more information.  This is reconciled somewhat with the theory of [[localic completion]], in which a uniform space is totally bounded if and only if its localic completion is compact (in the usual sense).


### Relation to Baire spaces

Every complete metric space is a [[Baire space]].  Since being a Baire space is a [[topological property]], it follows that every [[topologically complete space]] is a Baire space.

+-- {: .query}
Are there (necessarily nonmetrizable) complete uniform spaces that are not Baire spaces?
=--

There is also a topological property of [[Cech-complete space|Čech-completeness]] that is related  to this; in particular, a metric space is &#268;ech-complete if and only if it is complete, and every &#268;ech-complete space is a Baire space.  In general, we have these proper implications: topologically complete &#8594; &#268;ech-complete &#8594; Baire.


## Generalization

When [[Bill Lawvere]] interpreted (in [Lawvere 1973](#Lawvere1973)) [[metric spaces]] as certain [[enriched categories]], he found that a metric space was complete if and only if every [[adjunction]] of [[bimodules]] over the enriched category is induced by an [[enriched functor]].  Accordingly, this becomes the notion of [[Cauchy-complete category]].  (Note that one *must* say 'Cauchy' here, since this is *weaker* than being a [[complete category]], which is based on an incompatible analogy.)

## Related concepts

* a complete [[normed vector space]] is a _[[Banach space]]_

* [[completion of a space]]

## References

*  {#Ark1977} A.V. Arkhangel&#8242;skii (1977).  _Complete space_.  Matematicheskaya entsiklopediya.  [Updated English version](https://www.encyclopediaofmath.org/index.php/Complete_space). 
   

*  {#Lawvere1973} [[Bill Lawvere]] (1973).  _Metric spaces, generalized logic and closed categories_.  Reprinted in [[TAC]], 1986.  [Web](http://www.tac.mta.ca/tac/reprints/articles/1/tr1abs.html).
   


[[!redirects complete space]]
[[!redirects complete spaces]]

[[!redirects Cauchy complete space]]
[[!redirects Cauchy complete spaces]]
[[!redirects Cauchy-complete space]]
[[!redirects Cauchy-complete spaces]]


[[!redirects Cauchy completion]]
[[!redirects Cauchy completions]]
[[!redirects Cauchy-completion]]
[[!redirects Cauchy-completions]]

[[!redirects complete metric space]]
[[!redirects complete metric spaces]]
[[!redirects Cauchy complete metric space]]
[[!redirects Cauchy complete metric spaces]]
[[!redirects Cauchy-complete metric space]]
[[!redirects Cauchy-complete metric spaces]]
[[!redirects completion of a metric space]]
[[!redirects completion of metric spaces]]
[[!redirects completions of metric spaces]]
[[!redirects Cauchy completion of a metric space]]
[[!redirects Cauchy completion of metric spaces]]
[[!redirects Cauchy completions of metric spaces]]
[[!redirects Cauchy-completion of a metric space]]
[[!redirects Cauchy-completion of metric spaces]]
[[!redirects Cauchy-completions of metric spaces]]
[[!redirects complete metric]]
[[!redirects complete metrics]]
[[!redirects Cauchy complete metric]]
[[!redirects Cauchy complete metrics]]
[[!redirects Cauchy-complete metric]]
[[!redirects Cauchy-complete metrics]]
[[!redirects completion of a metric]]
[[!redirects completion of metrics]]
[[!redirects completions of metrics]]
[[!redirects Cauchy completion of a metric]]
[[!redirects Cauchy completion of metrics]]
[[!redirects Cauchy completions of metrics]]
[[!redirects Cauchy-completion of a metric]]
[[!redirects Cauchy-completion of metrics]]
[[!redirects Cauchy-completions of metrics]]
[[!redirects metric completion]]
[[!redirects metric completions]]

[[!redirects complete uniform space]]
[[!redirects complete uniform spaces]]
[[!redirects Cauchy complete uniform space]]
[[!redirects Cauchy complete uniform spaces]]
[[!redirects Cauchy-complete uniform space]]
[[!redirects Cauchy-complete uniform spaces]]
[[!redirects completion of a uniform space]]
[[!redirects completion of uniform spaces]]
[[!redirects completions of uniform spaces]]
[[!redirects Cauchy completion of a uniform space]]
[[!redirects Cauchy completion of uniform spaces]]
[[!redirects Cauchy completions of uniform spaces]]
[[!redirects Cauchy-completion of a uniform space]]
[[!redirects Cauchy-completion of uniform spaces]]
[[!redirects Cauchy-completions of uniform spaces]]
[[!redirects uniform completion]]
[[!redirects uniform completions]]

[[!redirects complete Cauchy space]]
[[!redirects complete Cauchy spaces]]
[[!redirects Cauchy complete Cauchy space]]
[[!redirects Cauchy complete Cauchy spaces]]
[[!redirects Cauchy-complete Cauchy space]]
[[!redirects Cauchy-complete Cauchy spaces]]
[[!redirects completion of a Cauchy space]]
[[!redirects completion of Cauchy spaces]]
[[!redirects completions of Cauchy spaces]]
[[!redirects Cauchy completion of a Cauchy space]]
[[!redirects Cauchy completion of Cauchy spaces]]
[[!redirects Cauchy completions of Cauchy spaces]]
[[!redirects Cauchy-completion of a Cauchy space]]
[[!redirects Cauchy-completion of Cauchy spaces]]
[[!redirects Cauchy-completions of Cauchy spaces]]

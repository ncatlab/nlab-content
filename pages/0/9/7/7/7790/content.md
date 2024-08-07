
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[group]] corresponding to a [[Kac-Moody algebra]] is a Kac-Moody group. 

This subsumes the case of [[affine Lie algebras]] in which case the corresponding Kac-Moody group is a centrally extended [[loop group]] (see there for more) and often the words "Kac-Moody group" are used synonomously with "centrally extended loop group". 


## Properties

### Classifying spaces

For $G$ a [[topological group]], write $B G$ for its [[delooping]], the [[classifying space]] for topological $G$-[[principal bundles]].

+-- {: .num_theorem}
###### Theorem

The classifying space $B G$ of every Kac-Moody group is a [[homotopy colimit]] over classifying spaces $B G_i$, $i \in I$ of [[compact topological space|compact]] [[connected topological space|connected]] [[Lie groups]] $G_i$:

$$
  B G \simeq hocolim_i B G_i
$$

in [[Top]] $\simeq$ [[∞Grpd]].

Moreover, the [[diagram]] $I$ may be taken to be a [[sieve]] in the [[poset of subobjects]] of the $n$-element set, for some $n \in \mathbb{B}$.

=--

This is due to [[Nitu Kitchloo]], 1998, see for instance [Kitchloo's survey, p. 9](#KitchlooSurvey).

+-- {: .num_remark}
###### Remark

This means that the classifying space of every Kac-Moody group has a smooth refinement to a [[smooth infinity-groupoid|smooth]] [[moduli stack]] given by forming 

$$
  \mathbf{B}G \coloneqq hocolim_i \mathbf{B}G_i
$$

in [[Smooth∞Grpd]].

=--


## Related entries

* [[Kac-Moody algebra]], [[loop group]]

* [[G₂]], [[F₄]],

  [[E₆]], [[E₇]], [[E₈]], [[E₉]], [[E₁₀]], [[E₁₁]], $\cdots$

Kay moody groups appear as [[U-duality]] groups in [[11-dimensional supergravity]] [[Kaluza-Klein mechanism|compactified]] to low dimensions.

## References

A standard textbook is

* Shrawan Kumar, _Kac-Moody groups, their flag varieties and representation theory_, Progress in Mathematics, 204. Birkhauser Boston, Inc., Boston, MA, (2002)

A survey is 

* Nitu Kitchloo, _Kac-Moody groups over the last decade_ ([pdf](http://www.math.ucsd.edu/~nkitchlo/papers/MPI%20Bonn.pdf))
 {#KitchlooSurvey}


Original articles include

* Nitu Kitchloo, _On the Topology of Kac-Moody groups_ ([arXiv](http://arxiv.org/abs/0810.0851)), ([Phd thesis](http://www.math.jhu.edu/~nitu/papers/Thesis.pdf))

* Carles Broto, Nitu Kitchloo, _Classifying spaces of Kac-Moody groups_, Math. Z. 240,621&#8211;649 (2002) ([pdf](http://www.math.jhu.edu/~nitu/papers/fulltext-2.pdf))

* Udo Baumgartner, Jacqueline Ramagge, Bertrand Remy, _Contraction groups in complete Kac-Moody groups_ (2008) ([pdf](http://ro.uow.edu.au/cgi/viewcontent.cgi?article=2260&context=infopapers))

* Andreas Mars, _On the topology and geometry of Kac-Moody groups_, PhD thesis (2011) ([web](http://tuprints.ulb.tu-darmstadt.de/2496/))


* Christof Geiss, Bernard Leclerc, Jan Schr&#246;er, _Kac-Moody groups and cluster algebras_ ([arXiv:1001.3545](http://arxiv.org/abs/1001.3545))

[[!redirects Kac-Moody groups]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A *skeletal groupoid* is a (usually: [[small category|small]]) [[strict category]] (i.e. equipped with a definite [[set]] of [[objects]]) which is both a [[groupoid]] and [[skeletal category]].

In other words, this means that a skeletal groupoid is a ([[strict groupoid|strict]]) [[groupoid]] for which, equivalently:

* for every [[morphism]] $\phi$ its [[source]] [[equality|equals]] its [[target]]: $s(\phi) = t(\phi)$,

* all morphisms are [[automorphisms]] of some object,

* all [[connected components]] are [[delooping groupoids]] $\mathbf{B} G$, namely of the [[automorphism group]] $G$ on the unique object in that connected components,

and so skeletal groupoids $\mathcal{X}$ are exactly (namely: up to [[isomorphism]]) the [[disjoint unions]] of [[delooping groupoids]]:

$$
  \mathcal{X} \,\in\, Grpd_{strct}
  \;\;\;\;\;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;\;\;\;\;
  \mathcal{X} \;\text{skeletal}
    \;\;\;\;\;\;\;\;
    \Leftrightarrow
    \;\;\;\;\;\;\;\;\;
  \mathcal{X}
  \;\;\underset{\color{red}iso}{\simeq}\;\;
  \underset{ x \in Obj(\mathcal{X}) }{\coprod}
  \mathbf{B} Aut_{\mathcal{X}}(x)
  \,.
$$

As discussed at *[[skeletal category]]* (and in much detail [here](Introduction+to+Topology+--+2#EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings) at *[[Introduction to Topology -- 2]]*), if the [[axiom of choice]] holds in the underlying category of [[Sets]] then every groupoid is [[equivalence of categories|equivalent as a category]] --- hence [[homotopy equivalence|homotopy equivalent]] as a [[homotopy 1-type]] --- to a skeletal groupoid, and to an essentially unique one, up to [[isomorphism]] of strict groupoids:  

$$
  \mathcal{X} \,\in\, Grpd_{strct}
  \;\;\;\;\;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;\;\;\;\;
  \mathcal{X}
  \;\;\;\;
    \underset{\color{red}equiv}{\simeq}
  \;\;\;\;
  \underset{ x \in \pi_0(\mathcal{X}) }{\coprod}
  \mathbf{B} \pi_1(\mathcal{X}, x)
  \,.
$$

As indicated on the right, this skeletalization of $\mathcal{X}$ extracts its [[homotopy groups]]: The set of objects of the skeleton is the set $\pi_0(\mathcal{X})$ of [[connected components]], and the [[automorphism group]] at a given object is the [[fundamental group]] $\pi_1(\mathcal{X},x)$ at that basepoint. 

## Properties

### Relation to groups

The [[1-category]] of skeletal groupoids is (see [there](free+coproduct+completion#SkeletalGroupoids)) [[equivalence of categories|equivalently]] the [[free coproduct completion]] of the category [[Grp]] of [[groups]].

## Related entries

* [[skeleton]]

* [[delooping groupoid]]



## References

Discussion of [[colimits]] over certain [[diagrams]] of the shape of skeletal groupoids and regarded as generalized [[coproducts]]:

* [[Hongde Hu]], [[Walter Tholen]], *Quasi-coproducts and accessible categories with wide pullbacks*, Appl Categor Struct **4** (1996) 387–402 &lbrack;[doi:10.1007/BF00122686](https://doi.org/10.1007/BF00122686)&rbrack;

    
Characterization of skeletal groupoids as the "trivial objects" with respect to a [[pretorsion theory]] on [[Cat]]:

* [[Francis Borceux]], [[Federico Campanini]], [[Marino Gran]], [[Walter Tholen]], *Groupoids and skeletal categories form a pretorsion theory in $Cat$* &lbrack;[arXiv:2207.08487](https://arxiv.org/abs/2207.08487)&rbrack;




[[!redirects skeletal groupoids]]




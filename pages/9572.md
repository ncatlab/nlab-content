
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The notion of _center of a monoidal category_ or _Drinfeld center_ is the [[categorification]] of the notion of [[center]] of a [[monoid]]([[associative algebra]], [[group]], etc.) from monoids to [[monoidal categories]].

Where the [[center]] of a monoid is just a sub-monoid with the [[property]] that it commutes with everything else, under categorification this becomes a [[stuff, structure, property]], since we have to specify _how_ the objects in the Drinfeld center commute ([[braided monoidal category|braid]]) with everything else.

## Definition

We first give the general-abstract definition

* [Abstract definition](#AbstractDefinition)

of Drinfeld centers. Then we spell out what this means in components in 

* [Definition in components](#DefinitionInComponents).


### Abstractly
 {#AbstractDefinition}


+-- {: .num_defn}
###### Definition

For $(\mathcal{C}, \otimes)$ a [[monoidal category]], write $\mathbf{B}_\otimes \mathcal{C}$ for its [[delooping]], the pointed [[2-category]] with a single [[object]] $*$ such that $Hom_{\mathbf{B}_\otimes \mathcal{C}}(*, *) \simeq \mathcal{C}$.

The **Drinfeld center** $Z(\mathcal{C}, \otimes)$ of $(\mathcal{C}, \otimes)$ is the [[monoidal category]] of [[endofunctor|endo]]-[[pseudonatural transformations]] of the [[identity]]-[[2-functor]] on $\mathbf{B}_\otimes \mathcal{C}$:

$$
  Z(\mathcal{C}, \otimes)
  \coloneqq
  End_{\mathbf{B}_\otimes \mathcal{C}}(id_{\mathbf{B}_\otimes \mathcal{C}})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Unwinding the definitions, we find that an [[object]] of $Z(\mathcal{C}, \otimes)$, $\Phi \colon id_{\mathbf{B}_\otimes \mathcal{C}} \to id_{\mathbf{B}_\otimes \mathcal{C}}$, has for components  pseudonaturality squares

$$
  \array{
    \ast &\stackrel{X \coloneqq \Phi(\ast)}{\to}& \ast
    \\
    {}^{\mathllap{Y}}\downarrow &\swArrow_{\Phi_Y}& \downarrow^{\mathrlap{Y}}
    \\
    \ast
    &\underset{X = \Phi(\ast)}{\to}&
    \ast
  }
$$

for each $Y \in Obj(\mathcal{C})$. As shown, these consist of a choice of an object $X \in \mathcal{C}$ together with a [[natural isomorphism]]

$$
  \Phi_{(-)} \colon X \otimes (-) \to (-) \otimes X
$$

in $\mathcal{C}$.

The [[transfor]]-property of $\Phi$ says that 

$$
  \array{
    \ast &\stackrel{X \coloneqq \Phi(\ast)}{\to}& \ast
    \\
    {}^{\mathllap{Y}}\downarrow &\swArrow_{\Phi_Y}& \downarrow^{\mathrlap{Y}}
    \\
    \ast
    &\underset{X = \Phi(\ast)}{\to}&
    \ast
    \\
    {}^{\mathllap{Z}}\downarrow &\swArrow_{\Phi_Z}& \downarrow^{\mathrlap{Z}}
    \\
    \ast
    &\underset{X = \Phi(\ast)}{\to}&
    \ast
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \array{
    \ast &\stackrel{X \coloneqq \Phi(\ast)}{\to}& \ast
    \\
    {}^{\mathllap{Y \otimes Z}}\downarrow &\swArrow_{\Phi_{Y \otimes Z}}& \downarrow^{\mathrlap{Y \otimes Z}}
    \\
    \ast
    &\underset{X = \Phi(\ast)}{\to}&
    \ast
  }
  \,.
$$

And so forth. Writing this out in terms of $(\mathcal{C}, \otimes)$ yields the following component characterization of Drinfeld centers, def. \ref{CompDef}.

=--



### In components
 {#DefinitionInComponents}

+-- {: .num_defn #CompDef}
###### Definition

Let $(\mathcal{C}, \otimes)$ be a [[monoidal category]]. Its **Drinfeld center** is a [[monoidal category]] $Z(\mathcal{C})$ whose

* [[objects]] are pairs $(X, \Phi)$ of an object $X \in \mathcal{C}$ and a [[natural isomorphism]] (braiding morphism)

  $$
    \Phi \colon X \otimes (-) \to (-) \otimes X
  $$

  such that for all $Y \in \mathcal{C}$ we have 

  $$
    \Phi_{Y \otimes Z}
    =
    (id \otimes \Phi_Z) \circ (\Phi_Y \otimes id) 
  $$

* [[morphisms]] are given by

  $$
    Hom((X, \Phi), (Y,\Psi))
    =
   \left\{
     f \in Hom_{\mathcal{C}}(X,Y)
     \;|\;
     (id \otimes f) \circ \Phi_Z
     = 
     \Psi_Z \circ (f \otimes id), \; \forall Z \in \mathcal{C}
   \right\}
   \,.
  $$

* the [[tensor product]] is given by 
 
  $$
    (X, \Phi) \otimes (Y, \Psi) = (X \otimes Y, (\Phi \otimes id) \circ (id \otimes \Psi))
    \,.
  $$

=--

## Properties

### Extra structure on the Drinfeld center

+-- {: .num_prop}
###### Proposition

The Drinfeld center $Z(\mathcal{C})$ is naturally a [[braided monoidal category]]. 

=--


\begin{proposition}
\label{DrinfeldCenterOfFusionCategory}
If $\mathcal{C}$ is a [[fusion category]] 
over an [[algebraically closed field]] of [[characteristic zero]],
then the Drinfeld center $Z(\mathcal{C})$ is also naturally a fusion category.
\end{proposition}

([Etingof, Nikshych & Ostrik 2005, Thm. 2.15](#EtingofNikshychOstrik05), review in [Davydov, Mueger, Nikshych & Ostrik 2003, Sec. 2.3](#DavydovMuegerNikshychOstrik03))

See also [Drinfeld, Gelaki, Nikshych & Ostrik 2010, Cor. 3.9](#DrinfeldGelakiNikshychOstrik10),  [Mueger 2003](#Mueger03).


### Relation to Drinfeld double under Tannaka duality

Under [[Tannaka duality]], forming the Drinfeld center of a [[category of modules]] of some [[Hopf algebra]] corresponds to forming the category of modules over the corresponding [[Drinfeld double]] algebra. See there for more.

[[!include structure on algebras and their module categories - table]]


## Related concepts

* [[Drinfeld double]]


## References

Original articles:

* {#Mueger03} [[Michael Mueger]], *From Subfactors to Categories and Topology II. The quantum double of tensor categories and subfactors*, J. Pure Appl. Alg. 180, 159-219 (2003) ([arXiv:math/0111205](https://arxiv.org/abs/math/0111205))

* {#EtingofNikshychOstrik05} [[Pavel Etingof]], [[Dmitri Nikshych]], [[Victor Ostrik]], *On fusion categories*, Annals of Mathematics Second Series, Vol. 162, No. 2 (Sep., 2005), pp. 581-642 ([arXiv:math/0203060](http://arxiv.org/abs/math/0203060), [jstor:20159926](https://www.jstor.org/stable/20159926))

* {#DrinfeldGelakiNikshychOstrik10} [[Vladimir Drinfeld]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], *On braided fusion categories I*, Selecta Mathematica. New Series 16 (2010), no. 1, 1–119 ([doi:10.1007/s00029-010-0017-z](https://doi.org/10.1007/s00029-010-0017-z))

Review:

* {#DavydovMuegerNikshychOstrik03} [[Alexei Davydov]], [[Michael Mueger]], [[Dmitri Nikshych]], [[Victor Ostrik]], Sec. 2.3 of: *The Witt group of non-degenerate braided fusion categories*, Journal fuer reine und angewandte Mathematik, **677** (2013. 135-177), de Gruyter 2003  ([arXiv:1009.2117](https://arxiv.org/abs/1009.2117), [doi:10.1515/crelle.2012.014](https://doi.org/10.1515/crelle.2012.014))


Textbook accounts:

* [[Shahn Majid]], _Foundations of quantum group theory_, Cambridge Univ. Press

* [[Christian Kassel]], _Quantum groups_, Graduate Texts in Mathematics __155__, Springer 1995 ([doi:10.1007/978-1-4612-0783-2](https://link.springer.com/book/10.1007/978-1-4612-0783-2), [webpage](http://www-irma.u-strasbg.fr/~kassel/QGbk.html), [errata pdf](http://www-irma.u-strasbg.fr/~kassel/QGerrata030399.pdf))

A general discussion of centers of [[monoid objects]] in [[braided monoidal 2-categories]] (which reduces to the above for the 2-category [[Cat]] with its [[cartesian product]]) is in 

* [[Ross Street]], _The monoidal center as a limit_, [pdf](http://maths.mq.edu.au/~street/centre.pdf)

An application to character sheaves is in 

* [[George Lusztig]], _Non-unipotent character sheaves as a categorical centre_, [arxiv/1506.04598](http://arxiv.org/abs/1506.04598)

In relation to [[spectra of tensor triangulated categories]]:

* Kent B. Vashaw, _Balmer spectra and Drinfeld centers_ ([arXiv:2010.11287](https://arxiv.org/abs/2010.11287))



[[!redirects Drinfeld centers]]

[[!redirects Drinfel'd center]]
[[!redirects Drinfel'd centers]]
  
[[!redirects center of a monoidal category]]


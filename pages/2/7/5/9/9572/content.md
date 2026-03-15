
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


\tableofcontents


## Idea

The notion of the _center of a monoidal category_ or the _Drinfeld center_ is a [[categorification]] of the notion of the [[center]] of a [[monoid]]([[associative algebra]], [[group]], etc.) from monoids to [[monoidal categories]].

Where the [[center]] of a monoid is just a sub-monoid with the [[property]] that it commutes with everything else, under categorification this becomes a [[stuff, structure, property|structure]], since we have to specify _how_ the objects in the Drinfeld center commute ([[braided monoidal category|braid]]) with everything else.

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

* [[objects]] are pairs $(X, \Phi)$ of an object $X \in \mathcal{C}$ and a [[natural isomorphism]] (the *half-braiding*)

  $$
    \Phi_{(-)}
      \;\colon\; 
    X \otimes (-) \longrightarrow (-) \otimes X
  $$

  such that for all $Y \in \mathcal{C}$ we have 

  $$
    \Phi_{Y \otimes Z}
    =
    \big(id_Y \otimes \Phi_Z\big) 
      \circ   
    \big(\Phi_Y \otimes id_Z \big) 
  $$

* [[morphisms]] are given by

  $$
    Hom\big((X, \Phi), (Y,\Psi)\big)
    =
   \Big\{
     f \in Hom_{\mathcal{C}}(X,Y)
     \;\big|\;
     (id \otimes f) \circ \Phi_Z
     = 
     \Psi_Z \circ (f \otimes id), \; \forall Z \in \mathcal{C}
   \Big\}
   \,.
  $$

* the [[tensor product]] is given by 
 
  $$
    (X, \Phi) \otimes (Y, \Psi) 
      \;=\; 
    \big(
       X \otimes Y, 
      (\Phi \otimes id_Y) \circ (id_X \otimes \Psi)
    \big)
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


## Examples
 {#Examples}

The archetypical example of Drinfeld centers is the following Drinfeld center of the category of [[finite-dimensional vector space|finite-dimensional]] $G$-[[graded vector spaces]] (cf. [EGNO 2015 Example 8.5.4. in](#EGNO15)), also known as the representation category of the *[[Drinfeld double]]* of $G$:

\begin{example}
\label{DrinfeldCenterOfGGradedVectorSpaces}
**(Drinfeld center of $G$-[[graded vector spaces]])**
\linebreak

By $\mathrm{Vec} \coloneqq \big({\mathrm{FD}\mathbb{C}\mathrm{Vec}, \otimes, \mathbb{C}}\big)$ we denote the [[monoidal category]] of [[finite-dimensional vector space|finite-dimensional]] [[complex vector spaces]] with the usual [[tensor product of vector spaces]]. For $G$ a [[group]], the monoidal category $\mathrm{Vec}_G$ of *$G$-[[graded vector spaces]]* has:

1. as [[objects]] [[vector spaces]] $V \in \mathrm{Vec}$ equipped with $G$-[[indexed set|indexed]] [[direct sum]] decomposition

   $$  
     V
     \equiv
     \bigoplus_{g \in G}
     V_g
     \mathrlap{\,,}
   $$

1. as [[morphisms]] [[linear maps]] that respect the $G$-grading,

1.  as [[monoidal category|monoidal]] [[structure]] the [[tensor product of vector spaces|ordinary tensor product]] equipped with the [[convolution]] grading:
   $$
     (V \otimes W)_g
     \coloneqq
     \bigoplus_{k \in G}
     \big({
       V_{k} \otimes W_{k^{-1} g}
     }\big)
     \mathrlap{\,.}
   $$

For example, with $X \in \mathrm{Vec}$ an ungraded vector space and $g_0 \in G$ a group element, we write
\[
  \label{GradedVectorSpaceConcentratedInSingleDegree}
  X \delta_{g_0}
  \in 
  \mathrm{Vec}_G
  \,,
  \;\;\;
  ({X \delta_{g_0}})_g
  \coloneqq
  \left\{
  \begin{array}{ll}
    X & \text{if}\;g = g_0
    \\
    0 & \text{otherwise}
  \end{array}
  \right.
\]
for the $G$-graded vector space which is concentrated on $X$ in degree $g_0$.

Now, the *Drinfeld center* $\mathcal{Z}({\mathrm{Vec}_G})$ is, by its general definition (Def. \ref{CompDef}, but we now change the conventuion for the handedness of the half-braiding in order to end up with *left* group actions), the [[monoidal category]] which has:

1. as [[objects]] [[pairs]], $(V,\beta)$, consisting of a $V \in \mathrm{Vec}_G$ and a [[natural isomorphism]] (the \emph{half-braiding})

   \[
     \label{TheHalfBraiding}
     \beta_{(-)}
     :
     (-) \otimes V
     \xrightarrow{ \sim }
     V \otimes (-)
     \mathrlap{\,,}
   \]

   satisfying for all $W, W' \in \mathrm{Vec}_G$ the relation
   \[
     \label{CoherenceOfHalfBraiding}
     \beta_{W \otimes W'}
     =
     \big({
       \beta_{W} \otimes \mathrm{id}_{W'}
     }\big)
       \circ
     \big({
       \mathrm{id}_{W} \otimes \beta_{W'}
     }\big)
     \mathrlap{\,,}
   \]

1. as [[morphisms]] $(V,\beta) \to (V',\beta')$ [[linear maps]] $f \colon V \to V'$ such that for all $W \in \mathrm{Vec}_G$ we have
  \[
    \label{ConditionOnMorphismsInDrinfeldCenter}
    \beta'_W
    \circ
    \big(
      id_W \otimes f
    \big)
    =
    \big(
      f \otimes id_{W}
    \big)
    \circ
    \beta_W
    \mathrlap{\,,}
  \]

1. as [[tensor product]] the operation
   \[
     (V,\beta)
     \otimes
     (V',\beta')
     =
     \big({
       V \otimes V',
       (\mathrm{id}_{V} \otimes \beta')
       \circ
       (\beta \otimes \mathrm{id}_{V'})
     }\big)
     \mathrlap{\,.}
   \]

But this general definition of Drinfeld center may be simplified in the present case: 

Since every [[vector space]] is [[isomorphism|isomorphic]] to a [[direct sum]] of copies of [[complex numbers|$\mathbb{C}$]], the linear maps $\beta_{(-)}$ (eq:TheHalfBraiding) are determined already by their values on $\mathbb{C} \delta_{g_0}$ (eq:GradedVectorSpaceConcentratedInSingleDegree); and if we understand that $\mathbb{C} \otimes V = V$, then, by degree reasons, their $g_0 g$-components must be [[linear isomorphisms]] $g_0 \cdot (-)$ of this form:

\begin{tikzcd}
    \big({
      \mathbb{C} \delta_{g_0}
        \otimes 
      V 
    }\big)_{g_0 g}
    \ar[
      r,
      "{ 
        ({
          \beta_{\mathbb{C}\delta_{g_0}} 
        })_{g_0 g}
      }"
    ]
    \ar[d, equals]
    &
    \big({
      V
        \otimes 
      \mathbb{C}\delta_{g_0} 
    }\big)_{g_0 g}
    \ar[d, equals]
    \\
    V_{g} 
    \ar[r, "{ g_0\cdot(-) }"]
      &
    V_{g_0 g g_0^{-1}}
    \mathrlap{\,.}
\end{tikzcd}

For these, the coherence condition (eq:CoherenceOfHalfBraiding) reduces to the *[action property](action#ActionPropertyOfGroupActions)*
\[
  g_2 \cdot ({g_1 \cdot (-)})
  =
  (g_2 g_1) \cdot (-)
  \mathrlap{\,.}
\]
This way, the objects of $\mathcal{Z}({\mathrm{Vec}_G})$ are [[bijection|bijectively]] identified with (complex, finite-dimensional) *[[groupoid representations]]* of the [[action groupoid]]
$$
  \Lambda G
  \colomneqq
  G\sslash_{\!\mathrm{Ad}} G
$$
of the [[adjoint action]] of $G$ (its *[[inertia groupoid]]*):

\begin{tikzcd}[sep=0pt]
    \Lambda G
    \ar[
      rr
    ]
    &&
    \mathrm{Vec}
    \\
    g
    \ar[
      d,
      "{ g_1 }"
    ]
    &\mapsto&
    V_g
    \ar[
      d,
      "{ g_1 \cdot }"
    ]
    \\[20pt]
    g_1
    g 
    g_1^{-1}
    &\mapsto&
    V_{g_1 g g_1^{-1}}
    \mathrlap{\,.}
\end{tikzcd}

In this representation-theoretic description, the morphisms (eq:ConditionOnMorphismsInDrinfeldCenter) of $\mathcal{Z}(\mathrm{Vec}_G)$ are equivalently the [[homomorphisms]] of [[groupoid representations]] (the *[[intertwiners]]*). This shows that:

For $G$ a [[group]], the [[Drinfeld center]] of [[graded vector spaces|$\mathrm{Vec}_G$]] is [[equivalence of categories|equivalently]] the [[representation category]] of the [[inertia groupoid]] of $G$:
  \[
    \label{DrinfeldCenterAsAdjointActionGroupoidRepresentations}
    \mathcal{Z}({\mathrm{Vec}_G})
    \simeq
    \mathrm{Rep}({
      \Lambda G
    })
    \mathrlap{\,.}
  \]

The [[equivalence of categories|equivalence]] (eq:DrinfeldCenterAsAdjointActionGroupoidRepresentations) implies at once that *[[simple objects]]* in $\mathcal{Z}({\mathrm{Vec}_G})$ (those admitting no nontrivial [[direct sum]] decomposition) are [[support|supported]] on [[conjugacy classes]] of group elements
\[
  [g]
  \coloneqq
  \big\{
    k^{-1} g k
  \big\vert
    k \in G
  \big\}
  \mathrlap{\,,}
\]
where they form a [[groupoid representation]] of the [[connected component]] $[g] \sslash_{\!\mathrm{Ad}} G \subset G\sslash_{\!\mathrm{Ad}} G$. Since these connected groupoids are equivalent to the [[delooping groupoid|delooping]] of their [[isotropy group]], $[g] \sslash_{\!\mathrm{Ad}} G \simeq \mathbf{B}Z_G(g)$ (cf. [this prop.](groupoid#EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings)), these [[groupoid representations]] are [[equivalence of categories|equivalently]] [[linear representations]] of the [[centralizer group]] $Z_G(g)$:
\[
  \Big\{
    \text{simple objects}
  \Big\}
  \simeq
  \Big\{
      [g] \sslash_{\!\mathrm{Ad}}G
      \to
      \mathrm{Vec}
   \Big\vert
      [g] \in \mathrm{Conj}(G)
  \Big\}
  \simeq
  \Big\{
      \mathbf{B}Z_G(g)
      \to
      \mathrm{Vec}
  \Big\vert
      [g] \in \mathrm{Conj}(G)
  \Big\}
  \mathrlap{\,.}
\]

\end{example}



## Related concepts

* [[center of a category]], [[center of an additive category]]

* [[Drinfeld double]]


## References

Original articles:

* {#Mueger03} [[Michael Mueger]], *From Subfactors to Categories and Topology II. The quantum double of tensor categories and subfactors*, J. Pure Appl. Alg. 180, 159-219 (2003) ([arXiv:math/0111205](https://arxiv.org/abs/math/0111205))

* {#EtingofNikshychOstrik05} [[Pavel Etingof]], [[Dmitri Nikshych]], [[Victor Ostrik]], *On fusion categories*, Annals of Mathematics Second Series, Vol. 162, No. 2 (Sep., 2005), pp. 581-642 ([arXiv:math/0203060](http://arxiv.org/abs/math/0203060), [jstor:20159926](https://www.jstor.org/stable/20159926))

* {#DrinfeldGelakiNikshychOstrik10} [[Vladimir Drinfeld]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], *On braided fusion categories I*, Selecta Mathematica. New Series 16 (2010), no. 1, 1–119 ([doi:10.1007/s00029-010-0017-z](https://doi.org/10.1007/s00029-010-0017-z))

Review:

* {#DavydovMuegerNikshychOstrik03} [[Alexei Davydov]], [[Michael Mueger]], [[Dmitri Nikshych]], [[Victor Ostrik]], Sec. 2.3 of: *The Witt group of non-degenerate braided fusion categories*, Journal fuer reine und angewandte Mathematik, **677** (2013. 135-177), de Gruyter 2003  ([arXiv:1009.2117](https://arxiv.org/abs/1009.2117), [doi:10.1515/crelle.2012.014](https://doi.org/10.1515/crelle.2012.014))


Textbook accounts:

* [[Shahn Majid]]: *Foundations of quantum group theory*, Cambridge University Press (1995, 2000) &lbrack;[doi:10.1017/CBO9780511613104](https://doi.org/10.1017/CBO9780511613104)&rbrack;

* [[Christian Kassel]]: _Quantum groups_, Graduate Texts in Mathematics __155__, Springer (1995) &lbrack;[doi:10.1007/978-1-4612-0783-2](https://link.springer.com/book/10.1007/978-1-4612-0783-2), [webpage](http://www-irma.u-strasbg.fr/~kassel/QGbk.html), [errata pdf](http://www-irma.u-strasbg.fr/~kassel/QGerrata030399.pdf)&rbrack;

* {#BakalovKirillov2001} [[Bojko Bakalov]], [[Alexandre Kirillov]]; section 3.2 in: *Lectures on tensor categories and modular functors*, University Lecture Series **21**, Amer. Math. Soc. (2001) &lbrack;[webpage](http://www.math.stonybrook.edu/~kirillov/tensor/tensor.html), [ams:ulect/21](https://bookstore.ams.org/view?ProductCode=ULECT/21), [[BakalovKirillov2000.pdf:file]]&rbrack;

* {#EGNO15} [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]]: *Tensor Categories*, Mathematical Surveys and Monographs **205**, AMS (2015) &lbrack;[ISBN:978-1-4704-3441-0](https://bookstore.ams.org/surv-205), [pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf)&rbrack;

A general discussion of centers of [[monoid objects]] in [[braided monoidal 2-categories]] (which reduces to the above for the 2-category [[Cat]] with its [[cartesian product]]) is in 

* [[Ross Street]], _The monoidal center as a limit_, [pdf](http://maths.mq.edu.au/~street/centre.pdf)

An application to character sheaves is in 

* [[George Lusztig]], _Non-unipotent character sheaves as a categorical centre_, [arxiv/1506.04598](http://arxiv.org/abs/1506.04598)

In relation to [[spectra of tensor triangulated categories]]:

* Kent B. Vashaw, _Balmer spectra and Drinfeld centers_ ([arXiv:2010.11287](https://arxiv.org/abs/2010.11287))

Relation to [[Frobenius monoidal functors]]:

* Johannes Flake, Robert Laugwitz, Sebastian Posur: *Frobenius monoidal functors from ambiadjunctions and their lifts to Drinfeld centers* &lbrack;[arXiv:2410.08702](https://arxiv.org/abs/2410.08702)&rbrack;



[[!redirects Drinfeld centers]]

[[!redirects Drinfel'd center]]
[[!redirects Drinfel'd centers]]
  
[[!redirects center of a monoidal category]]


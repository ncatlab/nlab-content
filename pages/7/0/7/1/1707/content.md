
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

* **group cohomology**

  * [[nonabelian group cohomology]], [[groupoid cohomology]]

* [[group extension]]

* [[Lie group cohomology]] 

  * [[∞-Lie groupoid cohomology]]

***

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

As described at [[cohomology]], a notion of [[cohomology]] exists for every [[(infinity,1)-topos]] $\mathbf{H}$: for $X$ and $A$ two objects of $\mathbf{H}$, 

* an $A$-valued [[cocycle]] on $X$ is an object in the [[∞-groupoid]] $\mathbf{H}(X,A)$;

* a coboundary between two such cocycles is a morphism in $\mathbf{H}(X,A)$

* the cohomology classes are the equivalence classes of $\mathbf{H}(X,A)$, so that the cohomology set of $A$-valued cohomology on $X$ is
  $$
    H(X,A) := \Pi_0 \mathbf{H}(X,A) = Ho_{\mathbf{H}}(X,A)
    \,,
  $$
  where $\mathbf{H}$ is the [[homotopy category of an (infinity,1)-category|homotopy category]] of the [[(∞,1)-category]] $\mathbf{H}$.

Now, ordinary **groupoid [[nonabelian cohomology]]** is the cohomology obtained for $\mathbf{H} = $ [[∞Grpd]] $\simeq$ [[Top]]: cohomology on [[∞-groupoid]]s (or [[topological space]]s) with coefficients in $\infty$-groupoids.

The various notions of **group cohomology** are special cases of this:

* **Group cohomology with coefficients in a trivial module** is the cohomology in $\mathbf{H} = $ [[∞Grpd]] for the case that

  * the domain $X = \mathbf{B} G$ is a one-object [[groupoid]] being the [[delooping]] of a [[group]] $G$;

  * the coefficient object is $A = \mathbf{B}^n K$, the [[strict ∞-groupoid]] coming from the [[crossed complex]] that is concentrated in degree $n$, where it is the abelian group $K$ (see [[Eilenberg-MacLane space|Eilenberg-MacLane object]] for more details).

  For $n \in \mathbb{N}$ One writes
  $$
    H_{Grp}^n(G,K) := H(\mathbf{B}G, \mathbf{B}^n K)
    = Ho_{\infty Grpd}(\mathbf{B}G , \mathbf{B}^n K)
  $$

  for the **degree-$n$ group cohomology of $G$ with values in $K$.

* **Nonabelian group cohomology** is obtained from this by allowing the coefficient object to be of the form 

  * $A =\mathbf{B} K_{(n)}$, for $K_{(n)}$ an arbitrary [[n-group]] 

  For instance for $K = AUT(H)$ the [[automorphism 2-group]] of a possibly nonabelian group $H$, nonabelian group cohomology classified $H$-extensions of $G$ (see also [[gerbe (general idea)]]).

  Details on this case are at [[nonabelian group cohomology]]

* **Group cohomology with coefficients in a nontrivial module** is in turn [[twisted cohomology]] version of [[nonabelian group cohomology]]:

  * let $A := \mathbf{B}^n_\rho K$ be a [[strict ∞-groupoid]] coming from a [[crossed complex]] of the form 

    $$
      [\mathbf{B}^n_\rho K] := (  \cdots \to {*} \to {*} \to K \to \cdots \to {*} \to {}* \to G \stackrel{\to}{\to}{*})
    $$

    with the abelian group $K$ in degree $n$ and for 

    $$
      \rho : G \to Aut(K)
    $$ 

    the [[action]] of $G$ on $K$ required by the structure of a [[crossed complex]];

  The $n$th group cohomology of $G$ with coefficients in the module $(K, \rho)$ is the connected components of the $\infty$-groupoid of [[section]]s $\sigma$

  $$
    \array{
      && \mathbf{B}^n_\rho K 
      \\
      & {}^{\sigma}\nearrow & \downarrow
      \\
      \mathbf{B}G
      &\to&
      \mathbf{B}G
    }
    \,.
  $$

  This is an example of [[twisted cohomology]], as explained there.

## Examples

We spell out in detail how the above reproduces the ordinary definition of group cohomology.

For the case of ordinary abelian group cohomology, the context of [[strict omega-groupoid]]s is in principle fully sufficient, since the domain object $\mathbf{B}G$ in that case is a 1-[[groupoid]], clearly a strict [[infinity-groupoid]], as are the abelian coefficient $n$-groupoids $\mathbf{B}^n K$, manifestly so as images of [[crossed complex]]es under the equivalence of crossed complexes with [[strict omega-groupoid]]s.

So one possibility is to model $Ho_{\infty Grpd}$ in this case as the [[homotopy category]] induced by the 
[[model structure on strict omega-groupoids]].

This is, more or less implicitly, the route taken in chapter 12 of

* [[Ronnie Brown]], [[Phil Higgins]], R. Sivera, _Nonabelian algebraic topology_ ([pdf](http://www.bangor.ac.uk/%7Emas010/pdffiles/rbrsbookb-e040609.pdf), [web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html))

Since every $\infty$-groupoid is fibrant, this model category category of strict $\infty$-groupoids is in fact a [[category of fibrant objects]] and hence the [[hom-set]]s in its [[homotopy category]] may be computed as [[colimit]]s over $\infty$-[[anafunctor]]s, namely 

$$
  H(\mathbf{B}G, \mathbf{B}^n K)
  =
  colim_{Y \stackrel{\sim}{\twoheadrightarrow} \mathbf{B}G} Hom(Y,\mathbf{B}^n K)
$$

where the colimit is over all strict $\omega$-groupoids $Y$ with $Y  \stackrel{\sim}{\twoheadrightarrow} \mathbf{B}G$ an acyclic fibration, which here is a [[k-surjective functor]] for all $k$.

On the other hand, since also the full model structure is around, this colimit localizes on the cofibrant replacement $Y = F(N(\mathbf{B}G))$ of $\mathbf{B}G$. But this is nothing but the free strict $\omega$-groupoid on the [[nerve]] of $\mathbf{B}G$, which is the usual bar resolution of $G$ (see the discusson at [[nerve]]):

$$
  N (\mathbf{B}G) = 
  \left(
    \cdots \to G \times G \times G
    \stackrel{\to}{\stackrel{\to}{\to}}
    G  \times G
    \stackrel{\to}{\to}
    G
    \to 
    {*}
  \right)
$$

This is of course nothing but the incarnation of $\mathbf{B}G$ as an object in the category of _weak_ [[infinity-groupoid]]s modeled as [[Kan complex]]es.

For instance the 2-cells in $N(\mathbf{B}G)$ are of the form

$$
  N(\mathbf{B}G)_2 
  =
  \left\{
  \left.
  \array{
    && {*}
    \\
    & {}^{g_1}\nearrow && \searrow^{g_2}
    \\
    {*}
    &&\stackrel{g_1 g_2}{\to}&& {*}
  }
  \right|
  g_1, g_2 \in G
  \right\}
  \,,
$$

where the diagram indicates what the face maps on $N (\mathbf{B}G) = G \times G$ are.

Accordingly, the 3-cells look like

$$
  N(\mathbf{B}G)_3
  =
  \left\{
  \left.
  \array{
    {*} &&\stackrel{g_2}{\to}&& {*}
    \\
    \uparrow^{g_1} &&{}^{g_1 g_2}\nearrow&& \downarrow^{g_3}
    \\
    {*}
    &&\stackrel{g_1 g_2 g_3}{\to}&&
    {*}
  }
  \;\;\;\;
  \Rightarrow
  \;\;\;\;   
  \array{
    {*} &&\stackrel{g_2}{\to}&& {*}
    \\
    \uparrow^{g_1} &&\searrow^{g_2 g_3}&& \downarrow^{g_3}
    \\
    {*}
    &&\stackrel{g_1 g_2 g_3}{\to}&&
    {*}
  }
  \right|
  g_1, g_2, g_3 \in G
  \right\}
  \,.
$$

The free strict $\omega$-groupoid on $N(\mathbf{B}G)$ has as $n$-morphisms the free $n$-groupoids generated from one $n$-[[oriental]] per such $n$-simplex in $N(\mathbf{B}G)$. 

In chapter 12 of Brown-Higgins-Sivera group cocycles are computed as morphisms out of this cofibrant replacement $F(N(\mathbf{B}G))$ of the ordinary 1-groupoid $\mathbf{B}G$ in the category of [[strict omega-groupoid]]s. (Or rather, there the equivalent [[crossed complex]]es) are used.

Alternatively, we can pass along the inclusion 
$$
  Str \omega Grpd \hookrightarrow \infty Grpd \hookrightarrow SSet
$$
of strict $\infty$-groupoids into all $\infty$-groupoids modeled as [[Kan complex]]es and compute the homotopy classes of morphisms there. Every [[Kan complex]] is already cofibrant (while of course still also being fibrant), so once the situation is interpreted in [[SSet]] we can compute group cohomology in terms of ordinary morphisms $N(\mathbf{B}G) \to N(\mathbf{B}^n K)$ without having to resolve further, without having to resort to [[anafunctor]]s etc. Of course it is the [[nerve]] operation involved both in forming the cofibrant replacement in $Str \infty Grpd$ as well as in passing to $SSet$ that accomplishes the required resolutions in either case.

The upshot of all this is just that the following illustrative pictures may be interpreted either in $Strct \infty Grpod$ or in $SSet$:

### degree-$1$ group cohomology 

A degree-one group cocycle $c$, $[c] \in H^1_{Grp}(G,K)$
is just a [[functor]] $c : \mathbf{B}G \to \mathbf{B}K$. This is a group homomorphism $G \to K$.

### Degree-$2$ group cohomology 

A degree-2 group cocycle $c$, $[c] \in H^2_{Grp}(G,K)$
is on 2-cells a map


$$
  c_2
  \;\;
  :
  \;\; 
  \left(
  \array{
    && {*}
    \\
    & {}^{g_1}\nearrow && \searrow^{g_2}
    \\
    {*}
    &&\stackrel{g_2 g_1}{\to}&& {*}
  }
  \right)
  \;\;\;
  \mapsto
  \;\;\;
  \left(
  \array{
    && {*}
    \\
    & {}^{{*}}\nearrow &\Downarrow^{c(g_1,g_2)}& \searrow^{{*}}
    \\
    {*}
    &&\stackrel{{*}}{\to}&& {*}
  }
  \right)
$$


i.e. a map $c : G \times G \to K$ such that it extends to a morphism on 3-cells:

$$
  \begin{aligned}
  c_3
  \;\;\;
  &:
  \;\;\;
  \left(
  \array{
    {*} &&\stackrel{g_2}{\to}&& {*}
    \\
    \uparrow^{g_1} &&{}^{g_2 g_1}\nearrow&& \downarrow^{g_3}
    \\
    {*}
    &&\stackrel{g_3 g_2 g_1}{\to}&&{*}
  }
  \;\;\;\;
  \Rightarrow
  \;\;\;\;   
  \array{
    {*} &&\stackrel{g_2}{\to}&& {*}
    \\
    \uparrow^{g_1} &&\searrow^{g_3 g_2}&& \downarrow^{g_3}
    \\
    {*}
    &&\stackrel{g_3 g_2 g_1}{\to}&&{*}
  }
  \right)
  \\
  & \mapsto
  \left(
  \array{
    {*} &&\stackrel{{*}}{\to}&& {*}
    \\
    \uparrow^{{*}} &\Downarrow^{c(g_1,g_2)}
    &{}^{{*}}\nearrow&\Downarrow^{c(g_2,g_3)}& 
    \downarrow^{{*}}
    \\
    {*}
    &&\stackrel{{*}}{\to}&&{*}
  }
  \;\;\;\;
  \stackrel{Id}{\Rightarrow}
  \;\;\;\;   
  \array{
    {*} &&\stackrel{{*}}{\to}&& {*}
    \\
    \uparrow^{{*}} &\Downarrow^{c(g_1,g_2 g_3)}
    &\searrow^{{*}}&\Downarrow^{c(g_2, g_3)}& \downarrow^{{*}}
    \\
    {*}
    &&\stackrel{{*}}{\to}&&{*}
  }
  \right)
  \end{aligned}  
  \,.
$$

Since there are no non-identity 3-morphisms in $\mathbf{B}^2 K$ (non-degenerate 3-cells in $N(\mathbf{B}^2 K)$) the 3-cell on the right is required to be the identity. Since the composition of the 2-cells on the right is their addition (group multiplication in the abelian group $K$) this says that the assignment $c_2 : G \times G \to G$ has to be such that

$$
  c(g_1, g_2)
  -
  c(g_1, g_2 \cdot g_3)
  +
  c(g_1 \cdot g_2, g_3)
  - 
  c(g_2, g_3)
  = 
  0
$$

This expresses the commutativity of the above tetrahedra. And it is indeed the ordinary formula for a cocycle in degree-2 [[group cohomology]].


### Degree-$3$ group cohomology 

similarly...




## Structured group cohomology {#StructuredCohomology}

If the groups in question are not plain groups ([[group object]]s internal to [[Set]]) but groups with extra structure, such as [[topological group]]s or [[Lie group]]s, then their cohomology has to be understood in the corresponding natural context.

In parts of the literature cohomology of structured groups $G$ is defined in direct generalization of the formulas above as homotopy classes of morphisms from the simplicial object

$$
  \left(
    \cdots G \times G\stackrel{\to}{\stackrel{\to}{\to}}G \stackrel{\to}{\to} *
  \right)
$$

to a simplicial object $N (\mathbf{B}^n A)$.

This is what is described above. But this does **not** in general give the right answer for structured groups:

namely [[cohomology]] is really about homotopy classes of maps in the suitable ambient [[(∞,1)-topos]]. For plain groups as in the above entry, we are working in the $(\infty,1)$-topos [[∞Grpd]]. That may be modeled by the standard [[model structure on simplicial sets]]. In that model structure, all objects a cofibrant and [[Kan complex]]es are fibrant. That means all objects we are dealing with here are both cofibrant and fibrant, and hence the simplicial set of maps between them is the cofrrect [[derived hom-space]] between these objects.

But this changes as we consider groups with extra structure. For a [[Lie group]] $G$, the object

$$
  \left(
    \cdots G \times G\stackrel{\to}{\stackrel{\to}{\to}}G \stackrel{\to}{\to} *
  \right)
$$

has to be considered as an [[Lie ∞-groupoid]]: an object in the [[model structure on simplicial presheaves]] over a [[site]] such as [[Diff]] or [[CartSp]]. As such it is in general **not** both cofibrant and fibrant. To that extent plain morphisms out of this object do **not** compute the correct [[derived hom-space]]s. Instead, the right definition of structured group cohomology uses the correct fibrant and cofibrant replacements.

### Topological group cohomology

In

* [[Jim Stasheff]], _Continuous cohomology of groups and classifying spaces_  Bull. Amer. Math. Soc. Volume 84, Number 4 (1978), 513-530 ([web](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183540920))

$n$-cocycles on a topological group $G$ with valzues in a topological abelian group $A$ are considered as continuous maps $G^{\times n}\to A$ (p. 3 ).

A definition in terms of [[derived functor|Ext-functor]]s and comparison with the naive definition is in 

* David Wigner, _Algebraic cohomology of topological groups_ Transactions of the American Mathematical Society, volume 178 (1973)([pdf](http://egg.epfl.ch/~nmonod/bonn/Wigner_1973.pdf))

A classical reference that considers the cohomology of Lie groups as topological spaces is

* [[Armand Borel]], _Homology and cohomology of compact connected Lie groups_ ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC1063923/pdf/pnas01596-0040.pdf))

A corrected definition of topological group cohomology has been given by Segal

* [[Graeme Segal]], _Cohomology of topological groups_ In Symposia Mathematica, Vol. IV (INDAM, Rome, 1968/69), pages 377{387. Academic Press, London, (1970).

* [[Graeme Segal]], _A classifying space of a topological group in the sense of Gel'fand-Fuks. Funkcional. Anal. i Prilozen.,
9(2):48{50, (1975).


### Lie group cohomology {#LieGroupcohomology}

The content of this subsection is at [[Lie group cohomology]].

## Nonabelian group cohomology

If the coefficient group $K$ is nonabelian, its higher [[delooping]]s $\mathbf{B}^n K$ to not exist. But [[n-groupoid]]s approximating this non-existant delooping do exists. Cohomology of $\mathbf{B}G$ with coefficients in these is called [[nonabelian group cohomology]] or [[Schreier theory]]. See there for more details.

## References 

Aspects of this general point of view on group cohomology is described for instance in chaper 12 of

* R. Brown, P. Higgins, R. Sivera, _Nonabelian algebraic topology_ ([pdf](http://www.bangor.ac.uk/%7Emas010/pdffiles/rbrsbookb-e040609.pdf), [web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html))

Much of what is called "nonabelian cohomology" in the existing literature concerns the case of nonabelian group cohomology with coefficients in the [[automorphism 2-group]] $AUT(H)$ of some possibly nonabelian group $H$.

This is the topic of [[Schreier theory]].

A random example for this use of terminology would be

* Roggenkamp, Scott, _Automorphisms and nonabelian cohomology_ ([pdf](http://www.math.virginia.edu/~lls2l/automorphisms_and_nonabelian.pdf))

For a conceptual discussion of nonabelian group cohomology see

* [[John Baez]], [[Mike Shulman]], _[[Lectures on n-Categories and Cohomology]]_ ([arXiv](http://arxiv.org/abs/math/0608420))

Group cocycles classify [[group extension]]s. This is often discussed only for 2-cocycles and extensions by ordinary groups. Higher cocycles classify extensions by [[2-group]]s and further by [[infinity-group]]s. In the context of [[crossed complex]]es, which are models for _strict_ $\infty$-groups, this is discussed for instance in

* [[Johannes Huebschmann]], _Crossed $n$-fold extensions and group cohomology_ ([web](http://dx.doi.org/10.1007/BF02566688))

Some standard references on group cohomology:

* Adem, Milgram, _Cohomology of finite groups_ 

...
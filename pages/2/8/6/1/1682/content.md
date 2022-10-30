
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[generalized (Eilenberg-Steenrod) cohomology]] theory called __$\mathop{tmf}$__ is the one represented by the [[spectrum]] that is obtained as the [[homotopy limit]] of the spectra of all [[elliptic cohomology]] theories.

The abbreviation "$\mathop{tmf}$" stands for the [[ring]] of [[topological modular forms]] as this is the [[cohomology ring]] that $\mathop{tmf}$ assigns, essentially, to the [[point]].

One of the greatest recent achievements in [[algebraic topology]] is the construction of the $\mathop{tmf}$ [[spectrum]] as the global [[section]] of a certain [[(infinity,1)-sheaf]] of [[higher algebra|commutative ring]] [[spectrum|spectra]] over the moduli [[stack]] of elliptic curves. 

From this sheaf, one can recover the Adams-type spectral sequence associated to $\mathop{tmf}$. According to [[A Survey of Elliptic Cohomology|SEC]], this sheaf is actually the [[structured generalized space|structure sheaf]] of the moduli stack classifying "oriented elliptic curves" over commutative ring spectra, or, to be in the correct variance, over [[derived stack|derived affine schemes]]. 

## Properties

### Inclusion of circle 2-bundles 
 {#InclusionOfCircle2Bundles}


Write $B^2 U(1) \simeq K(\mathbb{Z},3)$ for the [[abelian ∞-group]] whose underlying [[homotopy type]] is the [[classifying space]] for [[circle 2-bundle]]. Write $\mathbb{S}[B^2 U(1)]$ for its [[∞-group ∞-ring]]. 


+-- {: .num_prop}
###### Proposition

There is a canonical homomorphism of [[E-∞ rings]]

$$
  \mathbb{S}[B^2 U(1)] \to tmf
  \,.
$$

=--

See ([Ando-Blumberg-Gepner 10, section 8](#ABG10)).

+-- {: .num_remark}
###### Remark

This means that every [[circle 2-bundle]] ($U(1)$-[[bundle gerbe]]) given by a modulating map $\chi \colon X \to B^2 U(1)$ determines a class represented by

$$
  X \stackrel{\chi}{\to} B^2 U(1) \to \mathbb{S}[B^2 U(1)] \to tmf
$$

in the $tmf$-[[generalized cohomology]] of its base space $X$.

=--

### Witten genus and string orientation

The $tmf$-[[spectrum]] is the codomain of the [[Witten genus]], or rather of its refinements to the [[string orientation of tmf]]

$$ 
   \sigma : M String \to tmf
  \,.
$$

### Chromatic filtration

[[!include chromatic tower examples - table]]

### Anderson self-duality

The [[spectrum]] $tmf$ is self-dual under [[Anderson duality]], more precisley $tmf[1/2]$ is Anderson-dual to $\Sigma^{21} tmf[1/2]$ ([Stojanoska 11, theorem 13.1](#Stojanoska11))



## Construction as the global sections of a derived structure sheaf {#Construction as global sections}

There is a way to "construct" the tmf-spectrum as the [[E-∞ ring]] of [[global section]]s of a [[structured (∞,1)-topos]] whose underlying space is essentially the [[moduli stack]] of [[elliptic curve]]s. We sketch some main ideas of this construction.

### The context -- derived geometry over formal duals of $E_\infty$-rings

The discussion happens in the context of [[derived geometry]] in the [[(∞,1)-topos]] $\mathbf{H}$ over a [[small (∞,1)-category|small]] version of the [[(∞,1)-site]] of formal duals of [[E-∞ ring]]s ([[ring spectra]]). This is equipped with some [[subcanonical coverage]]. For $R \in E_\infty Ring$ we write $Spec R$ for its image under the [[(∞,1)-Yoneda embedding]] $(E_\infty Ring)^{op} \hookrightarrow \mathbf{H}$.

+-- {: .un_lemma}
###### Observation

The [[terminal object in an (∞,1)-category|terminal object]] in $\mathbf{H}$ is the formal dual of the [[sphere spectrum]]

$$
  * \simeq Spec \mathbb{S}
  \,.
$$

=--

Because the sphere spectrum is the [[initial object]] in $E_\infty Ring$.

### Coverings by the Thom spectrum

The crucial input for the entire construction is the following statement.


+-- {: .un_fact}
###### Fact

The formal dual of the [[Thom spectrum]] $M U$ is a [[well-supported object]] in $\mathbf{H}$, in that the morphism 

$$
  Spec M U \to *
$$

to the [[terminal object]] in $\mathbf{H}$ is an [[effective epimorphism]].

=--


This means that $Spec M U$ plays the role of a [[cover]] of the point. This allows to do some computations with ring spectra _locally on the cover $Spec M U$_ . Since $M U^*$ is the [[Lazard ring]], this explains why [[formal group law]]s show up all over the place.

To see this, first notice that the problem of realizing $R = tmf$ or any other ring spectrum as the ring of global sections on something has a _tautological solution_ : almost by definition (see [[generalized scheme]]) there is an $E_\infty$-ring valued [[structure sheaf]] $\mathcal{O}Spec(R)$ on $Spec R$ and its global sections is $R$. So we have in particular

$$
  tmf \simeq \mathcal{O}Spec tmf
  \,.
$$ 

In order to get a less tautological and more insightful characterization, the strategy is now to pass on the right to the $Spec M U$-cover by forming the [[(∞,1)-pullback]]

$$
  \array{
    Spec tmf \times Spec M U &\to& Spec tmf
    \\
    \downarrow && \downarrow
    \\
    Spec M U &\to& * \simeq Spec \mathbb{S}
  }
  \,.
$$

The resulting [[Cech nerve]] is a [[groupoid object in an (∞,1)-category]] given by

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spec tmf \times Spec M U \times Spec M U \stackrel{\to}{\to} Spec tmf \times Spec M U
$$

which by formal duality is

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spec (tmf \wedge M U \wedge M U) \stackrel{\to}{\to} Spec ( tmf \wedge M U)
$$

where the [[smash product]] $\wedge$ of ring spectral over the [[sphere spectrum]] $\mathbb{S}$ is the [[tensor product]] operation on function algebras formally dual to forming products of spaces.


As a [[groupoid object in an (∞,1)-category|groupoid object]] this is still equivalent to just $Spec tmf$.

### Decategorification: the ordinary moduli stack of elliptic curves

To simplify this we take a drastic step and apply a lot of [[decategorification]]: by applying the [[homotopy group]] [[(∞,1)-functor]] to all the $E_\infty$-rings involved these are sent to graded ordinary [[ring]]s $\pi_*(tmf)$, $\pi_*(M U)$ etc. The result is an ordinary [[simplicial object|simplicial]] [[scheme]]

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spec (\pi_*(tmf \wedge M U \wedge  M U)) \stackrel{\to}{\to} Spec ( \pi_*(tmf \wedge M U))
  \,,
$$

which remembers the fact that its structure rings are graded by being equipped with an [[action]] of the multiplicative group $\mathbb{G} = \mathbb{A}^\times$ (see [[line object]]).

This general Ansatz is discussed in ([Hopkins](#Hopkins)).

This simplicial scheme, which is degreewise the formal dual of a graded ring of [[generalized (Eilenberg-Steenrod) cohomology|generalized homology]]-groups one can show is in fact a [[groupoid]], hence a [[stack]]: effectively the [[moduli stack of elliptic curves]]. $\mathcal{M}_{ell}$. See ([Henriques](#HenriquesModuli)).


In fact if in this construction one replaced $Spec tmf$ by the point, one obtains the simplicial scheme

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spec (\pi_*(M U \wedge M U)) \stackrel{\to}{\to} Spec ( \pi_*(M U))
$$

which one finds is the moduli stack $\mathcal{M}_{fg}$ of [[formal group law]]s.



### Explicit computation of homotopy groups by a spectral sequence

Now, a priori these underived stacks remember little about the original [[derived scheme]]s $Spec tmf$ etc. They may not even carry any $E_\infty$-ring valued structure sheaf anymore (though some of them do). 

If they do carry an $E_\infty$-ring valued structure sheaf $\mathcal{O}$, one can compute the homotopy groups of its global sections by a [[spectral sequence]]

$$
  H^p(\mathcal{M}_{ell}, \pi_q(\mathcal{O}))
  \Rightarrow
  \pi_{p+q} \mathcal{O}(\mathcal{M}_{ell})
  \,.
$$

But it turns out that even if the derived structure sheaf does not exist, this spectral sequence may still converge and may still compute the homotopy groups of the ring spectrum that one started with. This gives one way to compute the homotopy groups of $tmf$. 

For the case of $tmf$ one finds that the homotopy sheaves $\pi_q(\mathcal{O}(\mathcal{M}_{ell}))$ are simple: they vanish in odd degree and are [[tensor power]]s $\omega^{\otimes k}$ of the canonical line bundle $\omega$ in even degree $2 k$, where the fiber of $\omega$ over an [[elliptic curve]] is the [[tangent space]] of that curve at its identity element. A [[section]] of $\omega^{\otimes k}$ is a [[modular form]] of weight $k$. So the whole problem of computing the homotopy groups of $tmf$ boils down to computing the [[abelian sheaf cohomology]] of the moduli stack of elliptic curves with coefficients in these abelian groups of modular forms --- and then examining the resulting spectral sequence.

This can be done quite explicitly in terms of a long but fairly elementary computation  in ordinary algebra. A detailed discussion of this computation is in ([Henriques](#Henriques))


## Related concepts

* [[taf]]

## References ##

The idea of a [[generalized cohomology theory]] with [[coefficients]] the ring of [[topological modular forms]] providing a home for the refined [[Witten genus]] and produced as a [[homotopy limit]] of [[elliptic cohomology]] theories over the [[moduli stack of elliptic curves]] was originally announced, as joint work with [[Mark Mahowald]] and [[Haynes Miller]], in 

* {#Hopkins94} [[Michael Hopkins]], section 9 of _Topological modular forms, the Witten Genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematics, Z&#252;rich 1994 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

(There the spectrum was still called "$eo_2$" instead of "$tmf$".) The details of the definition then appeared in

* {#Hopkins02} [[Michael Hopkins]], section 4 of _Algebraic topology and modular forms_, Proceedings of the ICM, Beijing 2002, vol. 1, 283--309 ([arXiv:math/0212397](http://arxiv.org/abs/math/0212397))


Expositions include

* {#MazelGee13} [[Aaron Mazel-Gee]], _You could've invented $tmf$_, April 2013 ([pdf slides](http://math.berkeley.edu/~aaron/writing/ustars-tmf-beamer.pdf))

* [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology]]_

See also

* [[Chris Douglas]], [[André Henriques]], _Topological modular forms and conformal nets_ , in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, Proceedings of Symposia in Pure Mathematics, AMS (2011)

More details are in  

* [[Mark Behrens]], _Notes on the construction of $tmf$_ ([pdf](http://math.mit.edu/~mbehrens/papers/buildTMF.pdf))

A complete account of the computation of the homotopy groups of $tmf$ (following previous unpublished computations) is in 

* [[Tilman Bauer]], _Computation of the homotopy groups of the spectrum $tmf$_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/eo2ss.pdf))

A survey of how this works is in

* [[Akhil Mathew]], _The homotopy groups of $TMF$_ ([pdf](http://math.mit.edu/~sglasman/tmfhomotopy.pdf))

and course notes that go through the construction of tmf and the computation of its homotopy groups are here:

*  _Talbot workshop on TMF_ ([web](http://math.mit.edu/conferences/talbot/2007/tmfproc/))

   * {#Hopkins} [[Mike Hopkins]] (talk notes by Michael Hill), _Stacks and complex oriented cohomology theories_ ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter08/MikesTalk1.pdf))
    

   * {#Henriques} [[André Henriques]], _The homotopy groups of tmf_ ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter16/TmfHomotopy.pdf))
     

   * {#HenriquesModuli} [[André Henriques]], _The moduli stack of elliptic curves_   ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter04/henriques.pdf))     



The refinement of the [[Witten genus]] to a morphism of [[E-∞ rings]] to $tmf$, hence the [[string orientation of tmf]] is due to 

* [[Michael Hopkins]], _Topological modular forms, the Witten Genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematics, Z&#252;rich 1994 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

* [[Michael Hopkins]], _Algebraic topology and modular forms_, Proceedings of the ICM, Beijing 2002, vol. 1, 283--309 ([arXiv:math/0212397](http://arxiv.org/abs/math/0212397))

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Michael Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))


see also remark 1.4 of

* [[Paul Goerss]], _Topological modular forms (after Hopkins, Miller and Lurie)_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0910/0910.5130v1.pdf)).

and for more on the [[sigma-orientation]] see

* [[Matthew Ando]], _The sigma orientation for analytic circle-equivariant elliptic cohomology_, Geom. Topol. 7 (2003) 91-153 ([arXiv:math/0201092](http://arxiv.org/abs/math/0201092))



Discussion of [[twisted cohomology]]  with [[coefficients]] in $tmf$
is in section 8 of

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 {#ABG10}

The self-[[Anderson duality]] of $tmf$ is discussed in

* {#Stojanoska11} [[Vesna Stojanoska]], Duality for Topological Modular Forms ([arXiv:1105.3968](http://arxiv.org/abs/1105.3968))


[[!redirects TMF]]

[[!redirects tmf spectrum]]
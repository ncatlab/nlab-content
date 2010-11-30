
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The [[generalized (Eilenberg-Steenrod) cohomology]] theory called __$\mathop{tmf}$__ is the one represented by the [[spectrum]] that is obtained as the [[homotopy limit]] of the spectra of all [[elliptic cohomology]] theories.

The abbreviation "$\mathop{tmf}$" stands for the [[ring]] of [[topological modular forms]] as this is the [[cohomology ring]] that $\mathop{tmf}$ assigns, essentially, to the [[point]].

One of the greatest recent achievements in [[algebraic topology]] is the construction of the $\mathop{tmf}$ [[spectrum]] as the global [[section]] of a certain [[(infinity,1)-sheaf]] of [[higher algebra|commutative ring]] [[spectrum|spectra]] over the moduli [[stack]] of elliptic curves. 

From this sheaf, one can recover the Adams-type spectral sequence associated to $\mathop{tmf}$. According to [[A Survey of Elliptic Cohomology|SEC]], this sheaf is actually the [[structured generalized space|structure sheaf]] of the moduli stack classifying "oriented elliptic curves" over commutative ring spectra, or, to be in the correct variance, over [[derived stack|derived affine schemes]]. 

## Properties

### Witten genus

The $tmf$-[[spectrum]] is the codomain of the [[Witten genus]]

$$ 
  Bord_{(\infty,\infty)}^{String} \to tmf
  \,.
$$

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
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spect tmf \times Spec M U \times Spec M U \stackrel{\to}{\to} Spec tmf \times Spec M U
$$

which by formal duality is

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spect (tmf \wedge M U \wedge M U) \stackrel{\to}{\to} Spec ( tmf \wedge M U)
$$

where the [[smash product]] $\wedge$ of ring spectral over the [[sphere spectrum]] $\mathbb{S}$ is the [[tensor product]] operation on function algebras formally dual to forming products of spaces.


As a [[groupoid object in an (infinity,1)-category|groupoid object]] this is still equivalent to just $Spec tmf$.

### Decategorification: the ordinary moduli stack of elliptic curves

To simplifyx this we takea drastic step and apply a lot of [[decategorification]]: by applying the [[homotopy group]] [[(∞,1)-functor]] to all the $E_\infty$-rings involved these are sent to graded ordinary [[ring]]s $\pi_*(tmf)$, $\pi_*(M U)$ etc. The result is an ordinary [[simplicial object|simplicial]] [[scheme]]

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spect (\pi_*(tmf \wedge M U \wedge  M U)) \stackrel{\to}{\to} Spec ( \pi_*(tmf \wedge M U))
  \,,
$$

which remembers the fact that its structure rings are graded by being equipped with an [[action]] of the multiplicative group $\mathbb{G} = \mathbb{A}^\times$ (see [[line object]]).

This general Ansatz is discussed in ([Hopkins](#Hopkins)).

This simplicial scheme, which is degreewise the formal dual of a graded ring of [[generalized (Eilenberg-Steenrod) cohomology|generalized homology]]-groups one can show is in fact a [[groupoid]], hence a [[stack]]: effectively the [[moduli stack of elliptic curves]]. $\mathcal{M}_{ell}$. See ([Henriques](#HenriquesModuli)).


In fact if in this construction one replaced $Spec tmf$ by the point, one obatins the simplicial scheme

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spect (\pi_*(M U \wedge M U)) \stackrel{\to}{\to} Spec ( \pi_*(M U))
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

For the case of $tmf$ one finds that the homotopy sheaves $\pi_q(\mathcal{O}(\mathcal{M}_{ell}))$ are simple: they vanish in odd degree and are [[tensor power]]s $\omega^{\otimes k}$ of the canoical line bundle $\omega$ in even degree $2 k$, where the fiber of $\omega$ over an [[elliptic curve]] is the [[tangent space]] of that curve at its identity element. A [[section]] of $\omega^{\otimes k}$ is a [[modular form]] of weight $k$. So the whole problem of computing the homotopy groups of $tmf$ boils down to computing the [[abelian sheaf cohomology]] of the moduli stack of elliptic curves with coefficvients in these abelian groups of modular forms --- and then examining the resulting spectral sequence.

This can be done quite explicitly in terms of a long but fairly elementary computation  in ordinary algebra. A detailed discussion of this computation is in ([Henriques](#Henriques))



## References ##

A course that goes through the construction of tmf and the computation of its homotopy groups is

*  _Talbot workshop on TMF_ ([web](http://math.mit.edu/conferences/talbot/2007/tmfproc/))

   * [[Mike Hopkins]] (talk notes by Michael Hill), _Stacks and complex oriented cohomology theories_ ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter08/MikesTalk1.pdf))
    {#Hopkins}

   * [[André Henriques]], _The homotopy groups of tmf_ ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter17/TmfHomotopy.pdf))
     {#Henriques}

   * [[André Henriques]], _The moduli stack of elliptic cirves_   ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter04/henriques.pdf))     {#HenriquesModuli}

More details are at 

* [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology]]_

and in the series of lectrue notes linked to there.


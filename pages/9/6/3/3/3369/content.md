

This entry is about the article

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ ([arXiv](http://arxiv.org/abs/0905.0731))

on a central topic in [[higher category theory and physics]]: the [[higher category theory|abstract higher categoretic]] conception of [[quantization]] of classical [[action functional]]s to [[FQFT|extended quantum field theories]].


#Contents#
* automatic table of contents goes here
{:toc}


## Preliminaries

The non-toy example application that gives the paper its title is to [[Chern-Simons theory]].


The notion of quantization discussed builds on the notion of $(\infty,n)$-categories of _families of $\infty$-groupoids_ that appears in some of the later sections of

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ .

Together with a notion of $n$-vector spaces (the [[vertical categorification]] of [[vector space]] and [[2-vector space]]) the article sketches a general abstract formalsim making precise the notion of [[path integral]] [[quantization]] for "finite" theories such as [[Dijkgraaf-Witten theory]]. 

The development, sketching a rather grand picture, remains somewhat sketchy, though, possibly due to the fact that this is a conference proceedings. Also some of the ideas claimed to now be fully generalized have appeared elsewhere before. Notably the notion of the quantization map $Fam_n(C) \to C$ (see below) is effectively what [[John Baez]], [[Jim Dolan]] call in their program on [[groupoidification]] call _degroupoidification_ . The general idea underlying this, that spaces of states are computed as colimits of sections, has been made clear previously by [[Simon Willerton]] _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv:math/0503266](http://arxiv.org/abs/math.QA/0503266))



## The general abstract notion of quantization for discrete theories

> Here is a summary of the general quantization aspect of the article, together with some additional remarks on how to think of all this by [[Urs Schreiber|an nLab author]].

The following is the formalization of the notion of [[quantization]] for discrete theories (such as [[Dijkgraaf-Witten theory]]) as presented in the article.

Fix some $n \in \mathbb{N}$, the dimension of the [[quantum field theory]] to be described.

In 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ .

are described the following two [[(∞,n)-category|(∞,n)-categories]]

* the [[(∞,n)-category of cobordisms]] $Bord_n$: its [[k-morphism]]s are roughly $k$-dimensional [[manifold]]s with boundaries and corners;

* for $C$ any [[(∞,n)-category]] the [[(∞,n)-category]] $Fam_n(C)$
  whose 

  * [[object]]s are [[∞-groupoid]]s $P$ equipped with functors $F_P : \to C$ 

  * [[morphism]]s are [[span]]s of [[∞-groupoid]]s with [[natural transformation]]s between the corresponding functors ([[bi-brane]]s)

    $$
      \array{
         && P
         \\
         & \swarrow && \searrow
         \\
         P_{in} &&\swArrow&& P_{out}
         \\
         & {}_{\mathllap{\exp(S(-))_{in}}}\searrow
         && \swarrow_{\mathrlap{\exp(S(-))_{out}}}
         \\
         && C
      }
    $$

  * "and so on".

For the application to [[quantization]] of [[sigma-model]] theories we want to be thinking of the data encoded by these $(\infty,n)$-categories as follows:

* An [[k-morphism]] $\Sigma$ in $Bord_n$ is a piece of $k$-dimensional "worldvolume" of some extended object, whose quantum dynamics we want to describe; we may roughly think of this as a [[cospan]]

  $$
    \array{
      && \Sigma
      \\
      & \nearrow && \nwarrow
      \\
      \Sigma_{in} &&&& \Sigma_{out}
     }
  $$

  where $\Sigma_{in}$ and $\Sigma_{out}$ are pieces of the boundary of $\Sigma$. We think of $\Sigma_{in}$ as the "incoming" piece of the object that we want to describe, which then experiences a self-interaction as described by the topology of $\Sigma$ and comes out in the shape of $\Sigma_{out}$ (for instace $\Sigma$ might be the three-holed sphere, $\Sigma_{in}$ the disjoint unions of two of its bounding circles and $\Sigma_{out}$ the remaining one, modelling the interaction where two strings merge to a single one).

* An [[morphism]] in $Fam_n(C)$ is to be thought of as

  * two **configuration spaces of fields** $P_{in}, P_{ou}$ 
    of some field theory;

  * together with an [[action functional]] on it in the form of an
    higher vector bundle ("[[gerbe]]") $\exp(S_P()) : P \to [I,C]$;
    being the component of the [[natural transformation]]
    that assigns to each _path_ $P$ between field
    configuration a _phase_ ;    

In these terms the **kinematics of a classical field theory** is a choice of $(\infty,n)$-functor

$$
  kin : Bord_n \to Fam_n(*)
$$

whereas the **dynamics of a classical field theory** -- the specificaton of an [[action functional]]** on the given configuration spaces,  is a lift of that to $Fam_n(C)$

$$
  \array{
    && Fam_n(C)
    \\
    & {}^{\exp(S(-))}\nearrow & \downarrow
    \\
    Bord_n &\stackrel{kin}{\to}&
    Fam_n(*)
  }
$$

To illustrate this: specifically, if we consider a [[sigma-model]] [[quantum field theory]] that is induced from a **target space** geometry $X$, such that a field configuration on $\Sigma$ is a morphism $\phi : \Sigma \to X$, and with a [[gauge field|background field]] $\nabla : X \to C$, then we think of the corresponding functor

$$
  conf_X : Bord_n \to Fam_n(C)
$$

as given by homming a [[cobordism]] [[cospan]] of the form

$$
  \array{
    && \Sigma_{in} \times I
    \\
    & \nearrow && \nwarrow
    \\
    \Sigma_{in} &&&& \Sigma_{out}
   }
$$
 

into $X$ to produce a [[span]] of path and configuration spaces

$$
  \array{
    && [\Sigma_{in} \times I,X]
    \\
    & \swarrow && \searrow
    \\
    [\Sigma_{in},X] &&&& [\Sigma_{out},X]
   }
$$

equipped with the **transgressed background field** as the corresponding action functional

$$
  \array{
    && [\Sigma_{in} \times I,X]
    \\
    & \swarrow && \searrow
    \\
    [\Sigma_{in},X] &&&& [\Sigma_{out},X]
    \\
    & {}_{\mathllap{[\Sigma_{in},\nabla]}}\searrow && \swarrow
    \\
    && [\Sigma_{in}, C]
   }
   \,.
$$

With that in hand, the **[[quantization]]** of the given classical field theory $\exp(S(-)) : Bord_n \to Fam_n(C)$ is its "pushforward to the point", given by postcomopon with a functor

$$
  \int : Fam_n(C) \to C
$$

that over objects $\exp(S(-)) : P_{in} \to C$ is given by taking $n$-categorical [[colimit]]

$$
  (\exp(S(-)) : P_{in} \to C) \mapsto (\lim_\to \exp(S(-)))
$$

which in terms of [[coend]]-notation is indeed nicely suggestively written as

$$
  (\exp(S(-)) : P_{in} \to C) \mapsto (\int \exp(S(-)))
  \,.
$$

Taking such a colimit may be thought of as forming the space of [[section]]s of the action functional $n$-vector bundle $\exp(S(-)) : P \to C$. That this is the right general idea was maybe first amplified in

* [[Dan Freed]], _Higher Algebraic Structures and Quantization_ ([arXiv:hep-th/9212115](http://arxiv.org/abs/hep-th/9212115)

a first more categorical formulation of this is in

* [[Simon Willerton]] _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv:math/0503266](http://arxiv.org/abs/math.QA/0503266))

What exactly the functor $\int : Fam_n(C) \to C$ does to [[k-morphism]]s is apparently left as an exercise for the inclined reader. it requires that in $C$ limits and colimits coincide. This is the case notably for $C = Vect$.

The authors indicate in section 8 a general recursive procedure for defining higher categories of higher vector spaces, by izterating the bimodule-style definition of [[2-vector space]]s, as described there. This yields a notion $C = n Vect$, which should be the right codomain for $n$-dimensional QFTs. So we end up with a diagram

$$
  \array{
    && Fam_n(C) &\stackrel{\int}{\to}& C
    \\
    & {}^{\exp(S(-))}\nearrow & \downarrow
    \\
    Bord_n &\stackrel{kin}{\to}&
    Fam_n(*)
  }
$$

whose left bit is the kinematical and dynamical input given by a classical field theory, and whose composition to to the right is supposed to give the corresponding quantum field theory, which by the logic motivating the [[cobordism hypothesis]] is a functor $Z : Bord_n \to n Vact$:

$$
  Z_S  = \int \exp(S(-)) : Bord_n \stackrel{\exp(S(-))}{\to}
   Fam_n(n Vect) \stackrel{\int}{\to} n Vect
   \,.
$$

+-- {: .query}

> [[Urs Schreiber]]: here is a question from me about this.

I am thinking about this kind of stuff from the premise that the right
notion of talking about the [[gauge field|background field]] data on the target space $X$ is in terms of [[schreiber:differential nonabelian cohomology]]. Of course this requires me to think of the above setup not in the discrete, but in the smooth setup, but maybe it is still interesting to compare a bit.

In the context of differential nonabelian cohomology, for every space $X$ there is a notion of its [[schreiber:path  ∞-groupoid]] $\Pi(X)$ and differential cohomology of $X$ is effectively the obstruction theory to extended morphisms out of $X$ (which are [[cocycle]]s for [[principal  ∞-bundle]]s and [[schreiber:∞-vector bundle]]s) to cocycles on $\Pi(X)$, which are [[schreiber:flat differential cohomology|flat connections]] or [[local system]]s on these. 

In general this extension of course does not exists -- therefore the interest in its obstruction theory -- but lets assume for the  moment that we do have a flat cocycle as a background [[gauge field]], a morphism

$$
  \nabla : \Pi(X) \to n Vect
  \,.
$$

If we suitably coskeletalize the $\infty$-groupoid $\Pi(X)$ at degree $n$, there should be an inclusion

$$
  \Pi_n(X) \hookrightarrow Bord_n(X)
$$

into the $(\infty,n)$-category of cobordisms, identifying $\Pi_n(X)$ with the sub-thing of topoloigically trivial cobordisms.

By considering this in the case of $n = 1$, one sees that extending $\nabla$ through this inclusion amounts to writing down an action functional for the gauge-coupling term of a charged object, so that we may sesibly write this extension as

$$
  \array{
    \Pi_n(X) &\stackrel{\nabla}{\to}& n Vect
    \\
    \downarrow & \nearrow_{\mathrlap{\exp(S_\nabla(-))}}
    \\
    Bord_n(X)
  }
  \,.
$$

Of course there is also canonically the projection $Bord_n(X) \to Bord_n(*) = Bord_n$. Staring at this for a second, one can't help but feel that one should attempt to construct an extension $Z$

$$
  \array{
    \Pi_n(X) &\stackrel{\nabla}{\to}& n Vect
    \\
    \downarrow & \nearrow_{\mathrlap{\exp(S_\nabla(-))}}
    \\
    Bord_n(X)
    \\
    \downarrow & \nearrow_{\mathrlap{Z}}
    \\
    Bord_n
  }
  \,.
$$

I am not sure how exactly that should work. But comparing to the notion of [[Kan extension]] one expects that $Z$ should be given on $\Sigma \in Bord_n$ by evaluating $\exp(S_\nabla(-))$ on all ($\Sigma \to X$) and "summing up" the result. That certainly begins to look like the [[path integral]] prescription.

In fact, it seems to me that the above construction in terms of $Fam_n(C)$ might be just another way for thinking about this extension. 

For notice that $\Pi_n(X)$ is essentially the colimit over all ways of throwing disk-shaped cobordisms into $X$. Similarly, I imaging that one should be able to conceived $Bord_n(X)$ as a colimit over a huge diagram of multi-cospans that indicate how all the cobordisms sit inside each other via boundary inclusins (something like the category of cells of $Bord_n(X)$)

If we think of $Bord_n(X)$ as arising as a colimit over the cell-structure of cobordisms this way, then by the universal property of colimits a morphism $\exp(S_\nabla(-)) : Bord_n(X) \to n Vect$ will induce a system of morphisms out spans, as indicated here:

<a href="http://www.codecogs.com/eqnedit.php?latex=$$%20\xymatrix@R=23pt@C=12pt{%20%26E_\Sigma%20\ar[rr]^{E_\mathrm{out}}%20\ar[dd]_{E_\mathrm{in}}%20\ar[ddr]%20%26%26%20E_{\Sigma_{\mathrm{out}}}%20\ar[ddr]%20\\%20\\%20%26E_{\mathrm{in}}%20\ar[ddr]%20%26%20[\Sigma,X]%20\ar[dd]^{\mathrm{in}}%20\ar[rr]^{\mathrm{out}}%20\ar[ddrr]%20%26%26%20[\Sigma_{\mathrm{out}},X]%20\ar[dd]%20\ar@/^1pc/[rrdddd]^{\exp(S_\nabla)|_{\Sigma_\mathrm{out}}}%20\\%20\\%20%26%26%20[\Sigma_{\mathrm{in}},X]%20\ar[rr]%20\ar@/_1pc/[ddrrrr]_{\exp(S_\nabla)|_{\Sigma_\mathrm{in}}}%20%26%26%20\mathrm{Bord}(X)%20\ar[ddrr]|{\exp(S_\nabla)}%20\\%20\\%20%26%26%26%26%20%26%26%20V%20}%20$$"><img src="http://latex.codecogs.com/gif.latex?$$%20\xymatrix@R=23pt@C=12pt{%20%26E_\Sigma%20\ar[rr]^{E_\mathrm{out}}%20\ar[dd]_{E_\mathrm{in}}%20\ar[ddr]%20%26%26%20E_{\Sigma_{\mathrm{out}}}%20\ar[ddr]%20\\%20\\%20%26E_{\mathrm{in}}%20\ar[ddr]%20%26%20[\Sigma,X]%20\ar[dd]^{\mathrm{in}}%20\ar[rr]^{\mathrm{out}}%20\ar[ddrr]%20%26%26%20[\Sigma_{\mathrm{out}},X]%20\ar[dd]%20\ar@/^1pc/[rrdddd]^{\exp(S_\nabla)|_{\Sigma_\mathrm{out}}}%20\\%20\\%20%26%26%20[\Sigma_{\mathrm{in}},X]%20\ar[rr]%20\ar@/_1pc/[ddrrrr]_{\exp(S_\nabla)|_{\Sigma_\mathrm{in}}}%20%26%26%20\mathrm{Bord}(X)%20\ar[ddrr]|{\exp(S_\nabla)}%20\\%20\\%20%26%26%26%26%20%26%26%20V%20}%20$$" title="$$%20\xymatrix@R=23pt@C=12pt{%20%26E_\Sigma%20\ar[rr]^{E_\mathrm{out}}%20\ar[dd]_{E_\mathrm{in}}%20\ar[ddr]%20%26%26%20E_{\Sigma_{\mathrm{out}}}%20\ar[ddr]%20\\%20\\%20%26E_{\mathrm{in}}%20\ar[ddr]%20%26%20[\Sigma,X]%20\ar[dd]^{\mathrm{in}}%20\ar[rr]^{\mathrm{out}}%20\ar[ddrr]%20%26%26%20[\Sigma_{\mathrm{out}},X]%20\ar[dd]%20\ar@/^1pc/[rrdddd]^{\exp(S_\nabla)|_{\Sigma_\mathrm{out}}}%20\\%20\\%20%26%26%20[\Sigma_{\mathrm{in}},X]%20\ar[rr]%20\ar@/_1pc/[ddrrrr]_{\exp(S_\nabla)|_{\Sigma_\mathrm{in}}}%20%26%26%20\mathrm{Bord}(X)%20\ar[ddrr]|{\exp(S_\nabla)}%20\\%20\\%20%26%26%26%26%20%26%26%20V%20}%20$$" /></a>

Certainly, this system of component morphisms is reminiscent of the [[ni-brane]] structure that we see in $Fam_n(C)$ in the above. So I am wondering: 

might the Freed-Hopkins-Lurie-Teleman quantization prescription as indicated above maybe be regarded as a way to construct the "universal" extension $Z$ of $\exp(S_\nabla(-)) : Bord_n(X) \to n Vect$ along the projection $Bord_n(X) \to Bord_n$ ?


=--

category: reference
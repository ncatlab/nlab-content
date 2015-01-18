
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[equations of motion]] of [[supergravity]] typically imply, or are even equivalent to (e.g. [Howe 97](#Howe97)), that some -- but not all -- of the components of the [[supertorsion|super-]][[torsion of a Cartan connection|torsion]] of the super-[[vielbein fields]] vanish. 



### From the canonical torsion of super-Minkowski spacetime
 {#CanonicalTorsionOfSuperMinkowskiSpacetime}

The torsion constraint is naturally understood by regarding [[supergravity]] as [[Cartan geometry]] for the inclusion of the [[orthogonal group]] into a [[super Poincare group]] and by noticing that the corresponding local model space, which is [[super-Minkowski spacetime]] $\mathbb{R}^{d|N}$, canonically has non-vanishing torsion.

Let $(x^a, \theta^\alpha)$ be the canonical [[coordinates]] on the [[supermanifold]] $\mathbb{R}^{d|N}$ underlying the [[super translation group]]. Then the [[left-invariant 1-forms]] are

* $\psi^\alpha = d \theta^\alpha$.

* $e^a = d x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta$.

Here the extra summand in the equation for $e^a$ (necessary to make it left-invariant) causes it to be non-closed:

$$ 
  \begin{aligned}
    d e^a & = d (d x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta)
    \\
    & = \frac{i}{2} d \overline{\theta}\Gamma^a d \theta
    \\
    & = \frac{i}{2} \overline{\psi}\Gamma^a \psi
  \end{aligned}
  \,.
$$

Taking the [[spin connection]] $(\omega^a{}_b)$ on $\mathbb{R}^{d|N}$ to vanish, as usual, this means that there is non-vanishing [[torsion]]:

$$
  \begin{aligned}
    \tau^a & = \mathbf{d} e^a + \omega^a{}_b \wedge e^b 
    \\
    & = \mathbf{d} e^a
    \\
    & = \frac{i}{2} \overline{\psi}\Gamma^a \psi
  \end{aligned}
$$

Depending on perspective one might say that it is the [[supertorsion]] that vanishes (see at _[[super-Minkowski spacetime]]_ and at _[[D'Auria-Fre formulation of supergravity]]_ for this perspective), or, alternatively, that one is dealing with [[Cartan geometry]]/[[G-structure]] whose local model space carries non-vanishing torsion, see [below](#InTermsOfTorsionTwistedGStructure). 

Notice that the torison-full but left-invariant forms are of course obtained from the torsion-free but non-left-invartiant forms by a $GL(\mathbb{R}^{d|N})$-valued function:

$$
  \left(   
     \array{
        e^a
        \\
        \psi^\alpha
     }
  \right)
  =
  \left(
    \array{
      id & \tfrac{i}{2}\Gamma^a{}_{\alpha \beta} \theta^\alpha
      \\
      0 & id
    }
  \right)
  \left(  
    \array{
      \mathbf{d}x^a
      \\
      \mathbf{d}\theta^\alpha
    }
  \right)
$$

$$
  \left(  
    \array{
      \mathbf{d}x^a
      \\
      \mathbf{d}\theta^\alpha
    }
  \right)
  =
  \left(
    \array{
      id & -\tfrac{i}{2}\Gamma^a{}_{\alpha \beta} \theta^\alpha
      \\
      0 & id
    }
  \right)
  \left(   
     \array{
        e^a
        \\
        \psi^\alpha
     }
  \right)
$$

This shows that regarding

$$
  (E^A) \coloneqq (E^a, E^\alpha) \coloneqq (e^a, \Psi^\alpha)
$$

as a [[super-vielbein]] is consistent: this is indeed a [[homotopy]] in

$$
  \array{
     \mathbb{R}^{d|N} &\to& \ast &\to& \mathbf{B}O(\mathbb{R}^{d|N})
     \\
     & 
     {}_{\mathllap{\tau_{\mathbb{R}^{d|N}}}}\searrow 
     &
     \swArrow_{E}
     & 
     \swarrow_{\mathrlap{O(\mathbb{R}^{d|N})\mathbf{Struc}}}
     \\
     && \mathbf{B}GL(\mathbb{R}^{d|N})
  }
$$

but not the tautological one given by

$$
  \array{
     \mathbb{R}^{d|N} &\to& \ast &\to& \mathbf{B}O(\mathbb{R}^{d|N})
     \\
     & 
     \searrow 
     &
     \downarrow
     & 
     \swarrow
     \\
     && \mathbf{B}GL(\mathbb{R}^{d|N})
  }
$$

where the left triangle is that which exhibits the canonical trivialization of the [[frame bundle]] of $\mathbb{R}^{d|N}$.


### Examples

In accord with the [above](#CanonicalTorsionOfSuperMinkowskiSpacetime), typically the [[equations of motion]] of a [[supergravity]] theory constrain the spinorial part of the torsion to have components $(\Gamma^a)_{\alpha \beta}$.

For instance in [[11-dimensional supergravity]] this is ([Bergshoeff-Sezgin-Townsend 87, equation (14)](#BergshoeffSezginTownsend87)).


### In terms of torsion-twisted $G$-structure
 {#InTermsOfTorsionTwistedGStructure}

Given a [[subgroup]] $G\hookrightarrow GL(V)$ of the [[general linear group]] of a linear model space $V$ (e.g. [[super-Minkowski spacetime]] $\mathbb{R}^{d|N}$), then a [[G-structure]] is [[integrability of G-structure|first-order integrable]] if on the first-order [[infinitesimal neighbourhoods]] of any point it is equal to the canonical (trivial) $G$-structure on $V$. Ordinarily the standard [[torsion]] on $V$ vanishs, and if so then so does that of any first-order integrable $G$-structire, which is the reason why for these the [[torsion of a G-structure]] vanishes.

But in the situation of $V$ being [[super-Minkowski spacetime]] as [above](#CanonicalTorsionOfSuperMinkowskiSpacetime), the torsion of the local model space does not vanish, and so accordingly neither does that of a first-order integrable $G$-structure in this case.

This perspective on the torsion constraints in supergravity is adopted in ([Lott 01](#Lott01)), see there around (38) of the original article or section 4 of the review on the arXiv.


## Related concepts

* [[D'Auria-Fre formulation of supergravity]]

## References

The formulation of supergravity equations of motion in terms of constraints on the torsion tensor goes back to 

* [[Julius Wess]] [[Bruno Zumino]], _Superspace formulation of supergravity_, Phys. Lett. B66 (1977), 361&#8211;364.

Discussion of torsion constrains for [[11-dimensional supergravity]] from the point of view of consistency of the [[membrane]] [[Green-Schwarz action functional]] is in

* {#BergshoeffSezginTownsend87}  [[Eric Bergshoeff]], [[Ergin Sezgin]], [[Paul Townsend]], _Supermembranes and eleven dimensional supergravity_, Phys.Lett. B189 (1987) 75-78, In [[Mike Duff]],  (ed.), _The world in eleven dimensions_ 69-72 ([pdf](http://streaming.ictp.trieste.it/preprints/P/87/010.pdf), [spire](http://inspirehep.net/record/248230?ln=en))

A mathematical formulation in terms of [[G-structures]] on [[supermanifolds]] is given in

* {#Lott01} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_ Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

which is followed up in

* Michel Egeileh, Fida El Chami, _Some remarks on the geometry of superspace supergravity_, _J.Geom.Phys. 62 (2012) 53-60_ ([spire](http://inspirehep.net/record/1333125))


See also

* {#Howe97} P.S. Howe, _Weyl Superspace_ ([arXiv:hep-th/9707184](http://arxiv.org/abs/hep-th/9707184))

* [[Suresh Govindarajan]], [[Burt Ovrut]], _A geometric interpretation for the torsion constrains of $(2,0)$-heterotic worldhseet supergravity_, Mod. Phys. Lett. A6(1991), 3341. ([pdf](http://www.physics.iitm.ac.in/~suresh/sgtalk/talk_html/torsion.pdf))

[[!redirects supergravity torsion constraint]]
[[!redirects supergravity torsion constraints]]

[[!redirects torsion constraints of supergravity]]


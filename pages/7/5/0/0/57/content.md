
<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Lie integration is a process in that assigns to a [[Lie algebra]] $\mathfrak{g}$ -- or more generally an [[L-∞-algebra|∞-Lie algebra]] or [[∞-Lie algebroid]] -- a [[Lie group]] -- or more generally [[∞-Lie groupoid]] -- that is [[infinitesimal space|infinitesimally]] modeled by $\mathfrak{g}$.

It turns out that if the [[∞-Lie algebroid]]s $\mathfrak{a}$ involved are incarnated dually in the form of their [[Chevalley-Eilenberg algebra]]s $CE(\mathfrak{a})$ then the bare [[∞-groupoid]] integrating them (i.e. ignoring the smooth structure) is effectively given by the [[Sullivan construction]] applied to the [[dg-algebra]] $\mathfrak{a}$.

This statement was made explicit for [[dg-Lie algebra]]s in

* [[Vladimir Hinich]], _Descent of deligne groupoids_ . Internat. Math. Res. Notices, 5:223&#8211;239, 1997.

and for general [[L-∞-algebra|∞-Lie algebra]]s 

* [[Ezra Getzler]], _Lie theory for nilpotent $L_\infty$ algebras_, ([arXiv](http://arxiv.org/abs/math/0404003))

(whose main point is the discussion of a gauge condition applicable for nilpotent $L_\infty$-algebras that cuts down the result of the Sullivan construction to a much smaller but equivalent model)

and

* [[Andre Henriques]], _Integrating $L_\infty$ algebras_,([arXiv](http://arxiv.org/abs/math.AT/0603563))

(whose origin possibly preceeds that of the previous article and which considers [[Banach manifold]] structure on the resulting [[∞-groupoid]]s).

For general [[∞-Lie algebroid]]s the general idea has been indicated in 

* [[Pavol Severa]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math.SG/0105080)).

There is an evident generalization of the [[Sullivan construction]] viewed this way that yields [[∞-Lie groupoid]]s (i.e. including the smooth structure). This is discussed at <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieIntegrated">∞-Lie groupoid</a>.

That the traditional Lie integration of [[Lie algebra]]s and [[Lie algebroid]]s to [[Lie group]]s and [[Lie groupoid]]s (including the smooth structure) is indeed a special case of this becomes more or less explicitly manifest in

* [[Marius Crainic]], [[Rui Fernandes]], _Integrability of Lie brackets_ ([arXiv](http://arxiv.org/abs/math/0105033))


## Definition

Given an [[∞-Lie algebroid]] $\mathfrak{a}$ (for instance a [[Lie algebra]], or a [[Lie algebroid]] or an [[L-∞-algebra]]) and $d \in \mathbb{N}$, a **$d$-path** in the $\infty$-Lie algebroid is a morphism of $\infty$-Lie algebroids


$$
  \Sigma : T \Delta^d_{Diff} \to \mathfrak{a}
$$ 

from the [[tangent Lie algebroid]] $T \Delta^d_{Diff}$ of the standard smooth $d$-[[simplex]] to $\mathfrak{a}$.


These $d$-paths naturally form a [[simplicial set]] 

$$
  \exp(\mathfrak{a})
  :=
  \left(
   \cdots    
   Hom(T \Delta^2, \mathfrak{a})
   \stackrel{\t}{\stackrel{\to}{\to}}
   Hom(T \Delta^1, \mathfrak{a})
   \stackrel{\to}{\to}
   Hom(T \Delta^0, \mathfrak{g})
  \right)
$$

which is a [[Kan complex]] under mild technical fine-tuning of the definition of $d$-paths.

Since morphisms of [[∞-Lie algebroid]]s are dually equivalent to [[dg-algebra]] morphisms of their [[Chevalley-Eilenberg algebra]], the above is equivalent to

$$
   \exp(\mathfrak{a})
   :=
   (
   \cdots 
   Hom(CE(\mathfrak{a}), \Omega^\bullet(\Delta^2))
   \stackrel{\to}{\stackrel{\to}{\to}}
   Hom(CE(\mathfrak{a}), \Omega^\bullet(\Delta^1))
   \stackrel{\to}{\to}
   Hom(CE(\mathfrak{a}), \Omega^\bullet(\Delta^0))
   )
  \,.
$$

Here we used that the Chevalley&#8211;Eilenberg algebra of the [[tangent Lie algebroid]] is the [[de Rham complex]] of differential forms.
This is recognized as the [[Sullivan construction]] in [[rational homotopy theory]] for $CE(\mathvrak{a})$.

This gives the universal $\infty$-groupoid integrating $\mathfrak{a}$. If $\mathfrak{a}$ is $n$-[[truncated]] then this construction will not yield in general an $n$-truncated [[∞-groupoid]] $\exp(\mathfrak{a})$. Instead one wants to truncate it to

$$
  \tau_n \exp(\mathfrak{a})  
  \,.
$$


## Examples

For more on this see (for the moment) <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieIntegrated">Lie integrated ∞-Lie groupoids</a>.


### Integration of Lie algebras

In 

* [[Marius Crainic]], [[Rui Fernandes]], _Integrability of Lie brackets_ ([arXiv](http://arxiv.org/abs/math/0105033))

it is effectively shown that for $\mathfrak{g}$ a (finite-dimensional) [[Lie algebra]] we have

$$
  \tau_1 \exp(\mathfrak{g}) = \mathbf{B}G
$$

is the [[delooping]] one-object groupoid of the simply connected [[Lie group]] $G$ corresponding to $G$ under [[Lie's three theorems]].



### Integration of Lie 2-algebras

For $\mathfrak{g}_\mu$ the [[string Lie 2-algebra]] it is effectively shown in 

* Andr&eacute; Henriques, _Integrating $L_\infty$ algebras_,([arXiv](http://arxiv.org/abs/math.AT/0603563))

that 

$$
  \tau_2 \exp(\mathfrak{g}_\mu) \simeq \mathbf{B}String(G)
$$

is the [[string 2-group]]. 


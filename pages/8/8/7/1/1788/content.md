
**Obstructions to globalizing higher WZW terms over Cartan geometries**

#Contents#
* table of contents
{:toc}


## WZW-Terms on infinitesimal Klein geometries

Given a [[Lie algebra]] $\mathfrak{g}$.

and [[Lie algebra cocycle|Lie algebra 3-cocycle]] $\omega_{WZW}^{\mathfrak{g}} \in \Omega^3_{LI}(\mathfrak{g})$

consider a potential 2-form $B\in \Omega^2(\mathfrak{f})$ [[B-field]] i.e. $\mathbf{d} B = \omega_{WZW}^{\mathfrak{g}}$.

For $\Sigma$ a 2-dimensional [[manifold]], consider on the space of [[smooth functions]]

$$
  \phi \colon \Sigma \longrightarrow \mathfrak{g}
$$

the [[functional]] ("[[action functional]]") 

$$
   \phi \mapsto \exp(\tfrac{i}{\hbar} \int_{\Sigma}\phi^\ast B )
$$

taking this as the [[interaction]] term defines a
a 2-dimension [[sigma-model]] called the [[Wess-Zumino-Witten model]] or WZW model for short. 


Ubiquity of WZW-models

* string on group manifold

* chiral part: [[E8]]-[[current algebra]] of the [[heterotic string]] (i.e. the [[GUT]] group in [heterotic model building](string+phenomenology#HeteroticStandardModels))

* [[rational conformal field theory]]: the part of [[2d CFT]] theory that has been pretty thoroughly studied with mathematical precision (notably: [[FRS formalism]])

But in fact as we pass from the [[NSR superstring]] ([[worldsheet]] [[supersymmetry]]) to the [[Green-Schwarz superstring]] ([[target space]] [[supersymmetry]]), then _every_ model is  WZW model

here $\mathfrak{g} = \mathbb{R}^{d-1,1|N}$ [[super translation Lie algebra]], i.e. [[super Minkowski spacetime]] and $\omega_{WZW}$ is a [[super differential form|super 3-form]]

But of course the general idea of WZW models works in other dimensions, too.

Curious: There is a 2-cocycle on [[Galilei group]] induces a 1-d WZW model which gives the jet-space Lagrabgian of the free non-relativistic massive particle. 

[[Green-Schwarz super p-brane sigma models]]:

whenever there is a [[super p-brane]] in [[string theory]]/[[M-theory]] on a [[target spacetime]] of [[dimension]] $d$ with [[supersymmetry]] "number" $N$ (i.e. real [[spin representation]] $N$), then there is a WZW curvature $\omega_{WZW}$ of degree $p+2$ on the [[super-Minkowski spacetime]] $\mathbb{R}^{d-1,1|N}$. 

The viable combinations $(p,d,N)$ are the content of the _[[brane scan]]_, or rather, the [[schreiber:The brane bouquet]]. Quuite a bit of the usual lore of [[M-theory]] is captured this way in [[super Lie algebra|super]] [[Lie algebra cohomology]] ([[super L-infinity algebra]] [[L-infinity algebra cohomology]]) 

finally: often WZW curvature invariant under sub-Lie algebra $\mathfrak{h} \hookrightarrow \mathfrak{g}$. Then defined on quotient $\mathfrak{g}/\mathfrak{h}$.

Indeed, this is precisely what happens for the super-$p$-branes where $\mathfrak{g} = $ [[super Poincaré Lie algebra]] $\mathfrak{iso}(\mathbb{R}^{d-1,1|N})$ and $\mathfrak{h} $ is the [[Lorentz Lie algebra]] $\mathfrak{o}(\mathbb{R}^{d-1,1|N})$ with

$$
  \mathbb{R}^{d-1,1|N} \simeq \mathfrak{iso}(\mathbb{R}^{d-1,1|N})/\mathfral{o}(\mathbb{R}^{d-1,1|N})
$$

## WZW-terms on Klein geometry



global definitition of action functional requires refining differential forms to [[differential cohomology]]

besides giving a more general definition that the curvature trick, this is also necessary to retain the [[higher gauge field]] symmetry ([[ghosts]] of ghost), which is key in the second globalization to follow.

often WZW models pass to [[coset]] $G/H$ "coset models" [[gauged WZW models]]

indeed the [[Green-Schwarz action functionals]] are just of this form, since [[super Minkowski spacetime]] is the quotient of the [[super-Poincaré  group]] by the [[Lorentz group]]

$$
  \mathbb{R}^{d-1,1|N} \simeq Iso(\mathbb{R}^{d-1,1|N})/O(\mathbb{R}^{d-1,1|N})
$$

## WZW-Terms on Cartan geometry

this is a [[Klein geometry]]... makes one want to consider the globalization to [[Cartan geometries]]

indeed, again this is just what happens for the super $p$-branes: one really wants to them to propagate not on super-Minkowski spacetime, but on surved [[super-spacetimes]] that are solutions to the relevant [[supergravity]] [[equations of motion]]


the Cartan-geometry globalization of the curvature/flux terms is well known, follows the pattern of [[G2-manifolds]] etc.

$$
  \omega_{a_1 a_2 \cdots a_{p+1}} E^{a_1} \wedge E^{a-2}
$$

* covariantly closed

* [[torsion]] is constrained: vielbein must locally be [[left-invariant 1-forms]].


open question: how do the two globalizations combine? Need to find full differential cocycles on Cartan geometry such that on the local model $\mathfrak{g}/\mathfrak{h}$ they restrict to presribed system.

or a little easier: extend WZW term on $G$ to $G$-principal bundle:

Example/Theorem

structure needed to globalize canonical WZW term on semisimple G to G-bundle is [[string structure]]

observe: [[String 2-group]] is the [[Heisenberg 2-group]] of the canonical 2-cocycle, its [[stabilizer 2-group]] under the $G$-action on itself.

Let's understand this one dimension down:

for $p = 0$ then 

* a WZW term is a [[line bundle with connection]]

* refining curvature 2-form to WZW is [[prequantization]];

the action functional is the [[holonomy]]

the [[stabilizer group]] under the [[diffeomorphism group]] action is the [[quantomorphism group]], the thing the [[Lie integration|Lie integrates]] the [[Poisson algebra]]

if $X$ is [[symplectic vector space]], hence abelian group with [[Hamiltonian action]] on itself, then restriction of quantomorphisms to those translations is [[Heisenberg group]]  $Heis(nabla)$

More generally, if a group $G$ acts by [[Hamiltonian action]] then -- for lack of established term -- we call the part of the quantomorphism group covering this the [[Heisenberg group]] $\mathbf{Heis}_G(\nabla)$


These concepts generalize to WZW terms in all dimensions [[schreiber:Higher geometric prequantum theory]]

Using this we may state the general theorem:


The obstruction to globalizing a higher WZW term on $G/H$ to a $G/H$-Cartan geometry is a first-order integrable $\mathbf{Heis}_{O(\mathfrak{g}/\mathfrak{h})}(\mathbf{L}_{WZW}^{inf})$-structure.

Notice: first order integrable but not torsion free: instead vielbein restricted to be first-order left-invariant. This means torsion for the sugra case! [[torsion constraints of supergravity]]

Notice: this statement holds in [[higher differential geometry]]. $X$ may be [[orbifold]] or worse. In fact for the [[M5-brane]] sigma model with its B-field, then $X$ is itself modeled on the [[supergravity Lie 3-algebra]]!

Thanks.

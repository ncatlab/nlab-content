**Obstructions to globalizing higher WZW terms over Cartan geometries**

#Contents#
* table of contents
{:toc}


## WZW-Terms on infinitesimal Klein geometries


Given a [[Lie algebra]] $\mathfrak{g}$.

and [[Lie algebra cocycle|Lie algebra 3-cocycle]] 
$\omega_{WZW}^{\mathfrak{g}} \in \Omega^3_{LI}(\mathfrak{g})$

consider a potential 2-form $B\in \Omega^2(\mathfrak{g})$ (a _[[B-field]]_) i.e. $\mathbf{d} B = \omega_{WZW}^{\mathfrak{g}}$.

For $\Sigma$ a 2-dimensional [[manifold]], consider on the space of [[smooth functions]]

$$
  \phi \colon \Sigma \longrightarrow \mathfrak{g}
$$

the [[functional]] ("[[action functional]]") 

$$
   \phi \mapsto \exp(\tfrac{i}{\hbar} \int_{\Sigma}\phi^\ast B )
$$

taking this as the [[interaction]] term defines a
a 2-dimensional [[sigma-model]] [[quantum field theory]] called the _[[Wess-Zumino-Witten model]]_ or _WZW model_ for short. 

At first sight this may seem exotic, but on second sight WZW models are ubiquitous.

First of all, they are the [[worldsheet]] theory of the [[NSR string]] propagating on a patch of a group manifold.

These are [[rational conformal field theories]], that part of the field of [[2d conformal field theory]] that has been mathematically understood und classified (see at _[[FRS formalism]]_).

Specifically the _chiral part_ of the [[E8]]-WZW model gives the [[current algebra]]-sector of the [[heterotic string]], i.e. that piece that gives the [[gauge group]] in [[GUT|grand unified]] [heterotic model building](string+phenomenology#HeteroticStandardModels)).

But, in fact, as we pass from the [[NSR superstring]] (with [[worldsheet]] [[supersymmetry]]) to the [[Green-Schwarz superstring]] (with [[target space]] [[supersymmetry]]), then _every_ model is a WZW model!

Here $\mathfrak{g}/\mathfrak{h} = \mathbb{R}^{d-1,1|N}$ [[super translation Lie algebra]], i.e. [[super Minkowski spacetime]] and $\omega_{WZW}$ is a [[super differential form|super 3-form]]. 

Now for any [[target spacetime]] any curved [[super-spacetime]], the [[Green-Schwarz superstring]], _remaiins_ a super-WZW model -- to first order around every point. This is what we come to [below](#WZWTermsOnCartanGeometry).

But of course the general idea of WZW models works in other dimensions, too. Let $\omega_{WZW}$ be a $(p+2)$-form, then it defines a [[sigma-model]] for [[p-branes]].

Curious: For $p = 0$ there is a 2-cocycle on [[Galilei group]] which induces a 1-d WZW model which gives the jet-space Lagrangian of the free non-relativistic massive particle. 

More relevant: there are the [[Green-Schwarz super p-brane sigma models]]:

whenever there is a [[super p-brane]] in [[string theory]]/[[M-theory]] on a [[target spacetime]] of [[dimension]] $d$ with [[supersymmetry]] "number" $N$ (i.e. real [[spin representation]] $N$), then there is a WZW curvature $\omega_{WZW}$ of degree $p+2$ on the [[super-Minkowski spacetime]] $\mathbb{R}^{d-1,1|N}$. 

The viable combinations $(p,d,N)$ are the content of the _[[brane scan]]_, or rather, the [[schreiber:The brane bouquet]]. Quite a bit of the usual lore of [[M-theory]] is captured this way in [[super Lie algebra|super]] [[Lie algebra cohomology]] ([[super L-infinity algebra]] [[L-infinity algebra cohomology]]) this way.

Finally: often WZW curvature invariant under sub-Lie algebra $\mathfrak{h} \hookrightarrow \mathfrak{g}$. Then defined on quotient $\mathfrak{g}/\mathfrak{h}$.

Indeed, this is precisely what happens for the super-$p$-branes where $\mathfrak{g} = $ [[super Poincaré Lie algebra]] $\mathfrak{iso}(\mathbb{R}^{d-1,1|N})$ and $\mathfrak{h} $ is the [[Lorentz Lie algebra]] $\mathfrak{o}(\mathbb{R}^{d-1,1|N})$ with

$$
  \mathbb{R}^{d-1,1|N} \simeq \mathfrak{iso}(\mathbb{R}^{d-1,1|N})/\mathfrak{o}(\mathbb{R}^{d-1,1|N})
$$



## WZW-terms on Klein geometry

For reasonable applications WZW models need to be generalized from target spaces of the form $\mathfrak{g}/\mathfrak{h}$ to curved manifolds only whose [[tangent spaces]] look like this. 

These are first of all the [[Klein geometries]] given by the [[coset]] manifolds $G/H$, for $H \to G$  [[Lie group]] [[Lie integration|Lie integrating]] $\mathfrak{h} \to \mathfrak{g}$.

There is a very popular trick to define the globalization:

for $\phi \colon \Sigma \longrightarrow G/H$ a sigma-model configuration, find -- if possible -- an extension $\widehat \phi$ to a [[3-manifold]] $\Sigma_3$ with [[boundary]] $\Sigma$ and then take the WZW term to be

$$
  \phi \mapsto \exp(\tfrac{i}{\hbar} \int_{\Sigma_3} \widehat \phi^\ast \omega_{WZW})
 \,.
$$

As with many simple solutions, this is deceptively simple. First of all, $\Sigma_3$ might not exist (particularly if one requires extra structure on $\Sigma$ and $\Sigma_3$). 

But worse: this hack does not reflect the [[higher gauge field|higher gauge symmetry]] of the WZW term: it has

1. [[gauge transformations]] $B \mapsto B + \mathbf{d} A$ ([[ghosts]]);

1. [[higher gauge transformations]] $A \mapsto A + \mathbf{d}f$ ([[ghosts-of-ghosts]]) 

But as we globalize, WZW term need to be glued together by gauge transformations, and so it will be all-important to keep these around.

The solution is familar in one dimension down: for $\omega$ a closed 2-form, then the solution to the problem of assigning $U(1)$-elements to curves $\Sigma_1$ such that whenever the curve bounds a disk $\Sigma_2$ the element is $\exp(\tfrac{i}{\hbar}\int_{\Sigma_2}\omega)$ is to find a [[line bundle with connection]] $\mathbf{L}$ with [[curvature]] $\omega$ and have the assignment be its [[holonomy]] (i.e. to find a [[prequantization]] of $\omega$).

This has an [[analog]] in all higher dimensions: given a closed $(p+2)$-form $\omega$, one may ask for a [[line n-bundle with connection|line (p+1)-bundle with connection]] such that $\omega$ is its [[curvature]]. This defines a [[volume holonomy]] for $(p+1)$-dimensional volumes. This is a [[prequantum n-bundle|higher prequantization]].

These [[line n-bundle with connection|line (p+1)-bundles]] are equivalently [[cocycles]] in [[ordinary differential cohomology]] of degree $(p+2)$. For $p = 1$ these are also knwon as [[bundle gerbes with connection]].

So then a proper _WZW term_ is a [[line n-bundle with connection|line (p+1)-bundle with connection]] $\mathbf{L}_{WZW}$ on $G/H$ whose [[curvature]] is $\omega_{WZW}$. Then the WZW [[interaction]] functional is simply the [[higher holonomy]] map

$$
  \phi \mapsto Hol_{\mathbf{L}_{WZW}}(\phi)
  \,.
$$

For $H \to G$ ordinary [[Lie groups]] and $p =1$, the possible WZW terms in this sense have been classified in great detail in the literature. Importantly, to a given curvature, there may be none, one, or (in general) many inequivalent full WZW terms. Under [[quantization]] these in general induce different [[2d CFTs]]. So the extra information here crucially matters!

We are after a more subtle classification which hasn't found attention yet:

## WZW-Terms on Cartan geometry
 {#WZWTermsOnCartanGeometry}


The [[Klein geometries]] $G/H$ are the canonical globalizations of $\mathfrak{g}/\mathfrak{h}$.

The general globalization are $(H \to G)$-[[Cartan geometries]].

Indeed, again this is just what happens for the super $p$-branes: one really wants to them to propagate not on super-Minkowski spacetime, but on surved [[super-spacetimes]] that are solutions to the relevant [[supergravity]] [[equations of motion]]. But such a curved spacetime with [[super-vielbein]] is precisely a $(O(\mathbb{R}^{d-1,1|N}) \to Iso(\mathbb{R}^{d-1,1|N}))$-Cartan geometry.


The Cartan-geometry globalization of the curvatures $\omega_{WZW}$ is well known. it follows the pattern of [[G2-manifolds]] etc.

If $(\omega_{a_1 a_2 \cdots a_{p+1}})$ denote the components of $\omega_{WZW}$ on $G/H$ in the [[basis]] of [[left invariant 1-forms]], then the globalization over a superspacetime has to satisfy

1. [[definite form|definiteness]]: $\omega_{WZW} = \omega_{a_1 a_2 \cdots a_{p+1}} E^{a_1} \wedge E^{a_2} \wedge \cdots \wedge E^{a_{p+1}}$ for $(E^a)$ the [[vielbein]] field ([[super-vielbein]]) which encodes the field of [[gravity]].

1. [[covariant derivative|covariantly constancy]]: $\nabla \omega_{WZW} = 0$ ;

1. [[supergravity torsion constraint|torsion constraint]]: on first-order [[infinitesimal neighbourhoods]] $\mathfrak{g}/\mathfrak{h} \hookrightarrow X$, vielbein must restric to [[left-invariant 1-forms]].


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


The obstruction to globalizing a higher WZW term on $\mathfrak{g}/\mathfrak{h}$ over an $(H \to G)$-Cartan geometry is a first-order integrable $\mathbf{Heis}_{O(\mathfrak{g}/\mathfrak{h})}(\mathbf{L}_{WZW}^{inf})$-structure.

Notice: first order integrable but not torsion free: instead vielbein restricted to be first-order left-invariant. This means torsion for the sugra case! [[torsion constraints of supergravity]]

Notice: this statement holds in [[higher differential geometry]]. $X$ may be [[orbifold]] or worse. And $\mathbf{Heis}_{O(\mathfrak{g}/\mathfrak{h})}(\mathbf{L}_{WZW}^{inf})$ is a [[smooth infinity-group]]
In fact for the [[M5-brane]] sigma model with its B-field, then $X$ is itself modeled on the [[supergravity Lie 3-algebra]]!

Thanks.


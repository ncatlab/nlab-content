
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 
  {#Idea}

### Traditional

Multisymplectic geometry is a generalization of [[symplectic geometry]] in the context of [[variational calculus]] and [[mechanical systems]] in which the [[symplectic form]] is generalized from a closed 2-form to a closed $n+1$-form, for $n \geq 1$ -- the [[n-plectic form]]. 

It is closely related to the [[de Donder-Weyl formalism]] of [[variational calculus]]. In the context of [[quantization]] it is meant to provide a refinement of [[geometric quantization]] which is well-adapted to $n$-dimensional [[quantum field theory]]. However, details of the multisymplectic quantization procedure remain under investigation.

### From the $n$POV

We comment a bit on how to, presumably, think of multisymplectic geometry 
from the [[nPOV]], in the context of [[higher geometric quantization]]. Readers may want to skip ahead to traditional technical discussion at _[Extended phase space](#extended phase space)_.

+-- {: .standout}

Multisymplectic geometry is (or should be) to [[symplectic geometry]] as [extended quantum field theory](http://ncatlab.org/nlab/show/FQFT#Extended) is to non-extended [[quantum field theory]]:

in the multisymplectic **extended phase space** of an $n$-dimensional [[classical field theory|field theory]] a state is not just a point, but an $n$-dimensional subspace.

=--

See also [[n-plectic geometry]].

**Multisymplectic geometry** is a generalization of [[symplectic geometry]] to cases where the symplectic 2-form is generalized to a higher degree [[differential form]].

In as far as [[symplectic geometry]] encodes [[Hamiltonian mechanics]], multisymplectic geometry may be regarded as resolving the symplectic geometry of the [[Hamiltonian mechanics]] of [[classical field theory]]: the kinematics of an $n$-dimensional field theory may be encoded in an degree $(n+1)$ symplectic form. 

In this application to physics, multisymplectic geometry is also known as the **covariant symplectic approach** to field theory (e.g. [section 2 here](http://arxiv.org/PS_cache/physics/pdf/9801/9801019v2.pdf#page=18)).


The idea is that under a suitable fiber integration multisymplectic geometry becomes ordinary symplectic form on the ordinary phase space of the theory, similar to, and in fact as a special case of, how for instance a [[line bundle]] on a [[loop space]] with a 2-form [[Chern class]] may arise by [[transgression]] from a [[bundle gerbe]] down on the original space, with a 3-form class.

By effectively undoing this implicit transgression in the ordinary [[Hamiltonian mechanics]] of [[classical field theory]], multisymplectic geomtry provides a general framework for a geometric, covariant formulation of [[classical field theory]], where _covariant formulation_ means that spacelike and timelike directions on a given space-time be treated on equal footing. 




## Extended phase spaces in covariant field theory 
 {#extended phase space}

We discuss here the refinement in multisymplectic geometry of the [[covariant phase spaces]] of [[classical field theory]]/[[prequantum field theory]] from ([[presymplectic manifold|pre]]-)[[symplectic manifolds]] of initial value data in a [[Cauchy surface]] to multisymplectic manifolds of local initial value data.


Recall that an ordinary [[phase space]] of a [[physical system]] is a [[symplectic manifold]] whose points correspond to the _[[states]]_ of the system. The **extended phase space** of an $n$-dimensional quantum field theory is a multisymplectic space whose points correspond to pairs consisting of

* a point in the field theory's parameter space -- an "event";

* a state of the theory "at that event".

So **extended phase spaces _localizes_ the information about states** : a point in here encodes not just the entire state of the system, but remembers explcitly what that state is like over any point in parameter space.

### Covariant configuration bundle

Consider [[classical field theory]] over a **parameter space** $\Sigma$. From the point of view of [[FQFT]] $\Sigma$ will be one fixed [[cobordism]] on which we want to understand the (classical) field theory.

We assume that a **[[field (physics)|field configuration]]** on $\Sigma$ is a [[section]]  $\phi : \Sigma \to E$ of some prescribed [[bundle]] $E \to \Sigma$: the _[[field bundle]]_. 

+-- {: .num_example}
###### Example

For instance an $n$-dimensional [[sigma-model]] [[quantum field theory]] is one whose field configurations on $\Sigma$ are given by maps 

$$
  \phi : \Sigma \longrightarrow X
$$ 

into some prescribed **[[target space]]** $X$. This is the case where $E = \Sigma \times X$ is a **trivial [[bundle]]**.

=--

+-- {: .num_remark}
###### Remark 

Beware of the standard source of confusion here when correlating this formalism with actual physics: the physical [[spacetime]] that we inhabit may be given either by $\Sigma$ or by $X$:

* in the description of the [[quantum mechanics]] of objects propagating _in_ our physical [[spacetime]], subject to [[forces]] exerted by fixed 
[[background gauge fields]] (such as electrons propagating in our particle accelerator, subject to the electromagnetic field in the accelerator tube), physical spacetime is identifid with target space $X$, while $\Sigma$ is the **worldvolume** of the object that propagates through $X$. The _field configurations_ on $\Sigma$ are really the maps $\Sigma \to X$ that determine how the object sits in spacetime.

* in quantum mechanics of fields on spacetime, such as the quantized electromagnetic field in a laser, it is $\Sigma$ which represents physical spacetime, and $X$ is some abstract space, for instance a smooth version of the [[classifying space]] $\mathcal{B}U(1)$, so that a field configuration $\Sigma \to X$ encodes a [[line bundle]] [[connection on a bundle|with connection]] that encodes a configuration of the [[electromagnetic field]].

=--


+-- {: .num_defn}
###### Definition

The **configuration space** of the system is the space of all field configurations, hence the space $\Gamma_\Sigma(E)$ of [[sections]] of the [[bundle]] $E$.

=--

In the [[sigma-model]] example this is some incarnation of the 
[[mapping space]] $[\Sigma,X]$.



+-- {: .num_remark}
###### Remark

Beware that in low dimensions one often distinguishes between the space of _configurations_ $\Sigma \to X$ and that of _trajectories_ or _histories_ $\Sigma \times \mathbb{R} \to X$. This comes from the case $\Sigma = *$ where for a particle propagating on $X$ the maps $[*,X] \simeq X$ are the possible configurations of the particle at a given parameter times, while maps $[* \times \mathbb{R}, X] = [\mathbb{R}, X]$ are the trajectories. But for the higher dimensional and [[FQFT|extended]] field theories under discussion here, this distinction becomes a bit obsolete and trajectories become just a special case of configurations.

=--

+-- {: .num_remark}
###### Remark

In the **non-covariant** approach one would try to consider the a [[cotangent bundle]] of the configuration space $\Gamma(E)$ as _phase space_ . Contrary to that, in the **covariant approach** one considers the much smaller space $E$ instead. This is then called the **covariant configuration space** or **covariant configuration bundle**.

=--

+-- {: .num_defn}
###### Definition


Write $J^1 E \to \Sigma$ for the first order [[jet bundle]] of the configuration space bundle $E \to \Sigma$. Its [[fiber]] over $s \in \Sigma$ are equivalence classses of [[germs]] of [[sections]] at $x$, where two germs are identified if their first derivatives coincide. 

=--

### Covariant phase space

+-- {: .num_defn #DualFirstJetBundle}
###### Definition

Given a [[vector bundle]] $E \to \Sigma$ over a [[smooth manifold]] of [[dimension]] $dim(\Sigma)  = n+1$, the **dual first jet bundle** $(J_1 E)^\ast \to \Sigma$ is the [[vector bundle]] whose [[fiber]] at $e \in E_s$ is the set of [[affine maps]]

$$
  J_e^1 E \longrightarrow \Lambda_s^{n+1} \Sigma
$$

from the first [[jet bundle|jets]] at $e$ to the degree-$(n+1)$ [[differential forms]] at $s$ on $\Sigma$.


=--

+-- {: .num_defn}
###### Definition

Given a [[spacetime]]/[[worldvolume]] $\Sigma$ and a [[field bundle]] $E \to \Sigma$, the **extended covariant phase space** is the multisymplectic manifold 

* whose underlying manifold is the dual first jet bundle, def. \ref{DualFirstJetBundle}, of the field bundle 

  $$
    (J^1 E)^* \to E
    \,,
  $$ 

* equipped with the canonical degree-$(n+2)$ [[differential form]]

  $$
    \omega = d \alpha
    \,,
  $$

  where $\alpha$ is the canonical $(n+1)$-form

=--

Given $\pi \colon E \to \Sigma$, with $\mathrm{dim} \Sigma =n+1$, the dual jet bundle $(J^1 E)^*$ is isomorphic to a particular vector sub-bundle of the $n+1$-form bundle $\Lambda^{n+1}T^{*}E$.
To see this, first consider the following

+-- {: .num_defn #nHorizontalForms}
###### Definition

Given a point $y \in E$, a tangent vector $v \in T_{y} E$ 
is said to be **[[vertical vector field|vertical]]** if $d \pi(v) = 0$.   Define 

$$
  \Lambda^{n+1}_{1}T^{\ast}E
  \hookrightarrow
  \Lambda^{n+1} T^{\ast} E
$$ 

to be the subbundle of the $n+1$-form bundle whose fiber at $y \in E$ 
consists of all $\beta \in \Lambda^{n+1} T^{*}_{y} E$ such that
$$          
  \iota_{v_1}\iota_{v_2} \beta =0   
$$
for all [[vertical vector field|vertical vectors]] $v_1,v_2 \in T_{y}E$.
Sections of $\Lambda^{n+1}_{1}T^{*}E$ are called **$n$-horizontal** $\mathbf{n+1}$**-forms**. 
  
=--

In words, an $n$-horizontal $(n+1)$-form is one which has at most one "leg" not along $\Sigma$. This is made very explicit in the proof of the following proposition.

+-- {: .num_prop}
###### Proposition

Let $E \to \Sigma$ be a [[vector bundle]] over a [[smooth manifold]] $\Sigma$ of [[dimension]] $dim \Sigma = (n+1)$ and assume that  $\Sigma$ is [[orientation|orientable]], then there is an [[isomorphism]] 

$$
  (J^1 E)^{\ast} \simeq \Lambda^{n+1}_{1} T^{\ast}E
$$ 

of [[vector bundles]] over $\Sigma$ between the dual first jet bundle of $E$, def. \ref{DualFirstJetBundle}, and the bundle of $n$-horizontal $(n+1)$-forms on $E$, def. \ref{nHorizontalForms}.

=--

+-- {: .proof}
###### Proof


It suffices to work locally with respect to a [[good open cover]], so we reduce the statement to the special case of the [[sigma model]] i.e. the trivial bundle  $E = \Sigma \times X$ over $\Sigma$. By the assumoption that $\Sigma$ admits an [[orientation]] we may pick a [[volume form]] $\vol \in \Gamma(\Lambda^{n+1}T^\ast \Sigma)$.

Let $q^1, \dots, q^{n+1}$ be local [[coordinates]] on $\Sigma$ and let
$u^1, \dots , u^d$ be local coordinates on $X$.  Then $\Lambda_1^{n+1} T^* E$ has a local [[basis]] of sections given by $(n+1)$-forms of two types: first, the wedge product of all $n+1$ [[cotangent vectors]] of type $\mathbf{d}q^i$: 

$$    
  \vol = \mathbf{d}q^1 \wedge \cdots \wedge \mathbf{d}q^{n+1}  
$$

and second, wedge products of $n$ cotangent vectors of type $\mathbf{d}q^i$ and a single one of type $\mathbf{d}u^a$:

$$   
  \mathbf{d}q^1 \wedge \cdots \wedge 
   \mathbf{d} q^{i-1}
   \wedge
   \mathbf{d}q^{i+1}
   \wedge \cdots \wedge \mathbf{d}q^{n+1} \wedge \mathbf{d}u^a 
  \,. 
$$


  
If $y = (p,u) \in \Sigma \times X$, this basis gives an isomorphism

$$   
  \Lambda^{n+1}_1 T^*_y E 
   \;\; \simeq\;\; 
  \left(\Lambda^{n+1} T^*_p \Sigma \right)
    \; \oplus \;
  \left(\Lambda^{n} T^*_p \Sigma \otimes T^*_u X \right) 
  \,.
$$

The [[volume form]] on $\Sigma$ also determines isomorphisms

$$  
  \mathbb{R} \overset{\simeq}{\longrightarrow} 
  \Lambda^{n+1} T^*_p \Sigma
$$

$$ 
                 c \mapsto  c \, \vol_p  
$$ 

and 

$$
  T_p \Sigma   \overset{\simeq}{\longrightarrow}  \Lambda^{n} T^*_p \Sigma
$$

$$
         v      \mapsto     \iota_v \vol_p  
  \,.
$$

We thus have obtained an isomorphism 

$$   
  \Lambda^{n+1}_1 T^*_y E \;\; \cong \;\; \mathbb{R} \; \oplus \; 
T_p \Sigma \otimes T^*_u X 
  \,.
$$

On the other hand, the trivialization $E = \Sigma \times X$ gives
an isomorphism of [[affine spaces]]

$$ 
  J^1_y E \; \; \cong \; \; T^*_p \Sigma \otimes T_u X   
$$

which has the side-effect of exhibiting on $J^1_y E$ the structure of a  [[vector space]]. Since we've identified

$\Lambda^{n+1} T^*_p \Sigma$ with $\mathbb{R}$, an affine map from $J^1_y E$ to $\Lambda^{n+1} T^*_p \Sigma$ is just
an element of $T_x \Sigma \otimes T^*_u X$ plus a constant.
So, we obtain
$$   (J^1_y E)^* \; \; \cong \; \; \mathbb{R} \; \oplus \; 
T_p \Sigma \otimes T^*_u X .$$
This gives a specific vector bundle isomorphism
$(J^1 E)^* \cong \Lambda_1^{n+1} T^* E$, as desired. 

=--


+-- {: .num_remark}
###### Remark

In practice it is better to use the [[pullback of differential forms|pulled back]] [[volume form]] $\pi^* \vol$ as a substitute for the coordinate-dependent $n+1$-form $\mathbf{d}q^1 \wedge \cdots \wedge \mathbf{d}q^{n+1}$ on $E$.  This gives another [[basis]] of
sections of $\Lambda_1^{n+1} T^* E$, whose elements we write suggestively 

$$  
  dQ \coloneqq \pi^* \vol   
$$

and

$$  
  dQ_i^a 
  \coloneqq
  \left(\pi^* \iota_{\partial/\partial q^i} \vol\right) 
   \wedge 
   \mathbf{d}u^a 
  \,.
$$

Corresponding to this [[basis]] then there are
local [[coordinates]] $P$ and $P^i_a$ on $\Lambda_1^{n+1} T^* E$, which combined with the coordinates $q^i$ and $u^a$ pulled back from $E$ give a local coordinate system on $\Lambda_1^{n+1} T^* E$.  

In these [[coordinates]] the canonical $n+1$-form on $(J^1 E)^* \cong \Lambda_1^{n+1} T^* E$ is:

$$
  \alpha = P \wedge dQ + P^i_a \wedge dQ_i^a, 
$$

and the $n+2$ [[multisymplectic form]] is

$$ 
  \omega = \mathbf{d}P \wedge dQ + \mathbf{d}P^i_a \wedge dQ_i^a.
$$

=--

### Examples

#### Bosonic particle propagating on a manifold

Ordinary point [[particle]] [[mechanics]] on a [[manifold]] $X$ involves [[trajectories]] $\mathbb{R} \to X$ in $X$, with parameter space $\Sigma = \mathbb{R}$ the [[real line]], thought of as the abstract "[[worldline]]" of the particle.

* parameter space: $\Sigma = \mathbb{R}$, the **worldline**;


* target space: $X$, some [[manifold]] -- **spacetime**;

* configuration bundle: $(E \to \mathbb{E}) = (\mathbb{R}\times X \to \mathbb{R})$;

* jet bundle: $J^1 E = \mathbb{R} \times T X$ .

for $U \subset E = \mathbb{R} \times X$ a local patch with coordinate functions $\{t, q^i\}$, there are canonically induced coordinates on $J^1 E$ written $\{t,q^i, v^i\}$.

Here a collection of vaues $(q^i_0)$ is a **position** of the particle and $(v^i_0)$ is a **velocity** of the particle. Notice that in this covariant approach these are not positions and velocities "at a given time". Rather, a point in $J^1 E$ specified a parameter time and a corresponding position and velocity.

....


Let $U \to X$ be a local patch of $X$ with canonical coordinates $\{x^i\}$.

The canonical 2-form on the extended phase space in this case is traditionally locally written as

$$
  \omega|_U = \mathbf{d} \alpha|_U = \mathbf{d}( p_i \wedge \mathbf{d} q^i + H \wedge d t )
  \,.
$$


... blah-blah-blah...




#### Electromagnetism

* parameter space: $\Sigma$ is spacetime;

A field configuration of the [[electromagnetic field]] is a [[line  bundle]] [[connection on a bundle|with connection]] on $\Sigma$. If we assume the corresponding bundle to be trivial, then this is just a [[differential form|1-form]] on $\Sigma$. So in this simplified case we can take

* configuration bundle: $T^* \Sigma$ is the [[cotangent bundle]] of $\Sigma$.


#### Bosonic string propagating on a manifold

* parameter space: $\Sigma$ some 2-dimensional manifold -- the **worldsheet** -- for instance $\Sigma = S^1 \times \mathbb{R}$ models
a closed string propagating without interaction.

* target space. $X$ spacetime;

* covariant configuration bundle $E = \Sigma \times X$.


We will work out the covariant Hamiltonian formalism (also known as the **[[de Donder-Weyl formalism]]**) for this example in detail. We follow here the exposition found in ([H&#233;lein 02](#Helein02)).

For simplicity we will only consider the case where $\Sigma$ is the
cylinder $\mathbb{R}\times S^1$ and $X$ is $d$-dimensional Minkowski spacetime, $\mathbb{R}^{1,d-1}$.
A solution of the classical bosonic string is then a map $\phi : \Sigma \to X$ which is a critical point of the area subject to certain boundary conditions.

Equivalently, by exploiting symmetries
in the variational problem, one can describe solutions $\phi$ by equipping $\mathbb{R} \times S^{1}$ with its standard Minkowski metric and then solving the
$1+1$ dimensional field theory specified by the Lagrangian density
$$
\mathcal{L}=\frac{1}{2} g^{ij}\eta_{ab} \frac{\partial
  \phi^{a}}{\partial q^i}\frac{\partial \phi^{b}}{\partial q^j}.
$$

Here $q^i$ $(i = 0,1)$ are standard coordinates on $\mathbb{R} \times S^1$ and
$g=\mathrm{diag}(1,-1)$ is the Minkowski metric on $\mathbb{R} \times S^1$, while
$\phi^a$ are the coordinates of the map $\phi$ in $\mathbb{R}^{1,d-1}$ and $\eta =
\mathrm{diag}(1,-1,\cdots,-1)$ is the Minkowski metric on $\mathbb{R}^{1,d-1}$. The corresponding Euler-Lagrange equation is just a version of the
wave equation:
$$
g^{ij}\partial_{i} \partial_{j} \phi^a =0.
$$

The space $E=\Sigma \times X$ can be thought of as a trivial bundle over $\Sigma$, and the graph of a function $\phi : \Sigma \to X$ is a smooth section of $E$.  We write the coordinates of a
point $(q,u)\in E$ as $\left(q^i,u^a \right)$.
Let $J^1 E \to E$ be the first jet bundle of $E$.
We may regard $J^1 E$ as a vector bundle whose
fiber over $(q,u)\in E$ is $T^*_q \Sigma \otimes T_u X$.  
The Lagrangian density for
the string can be defined as a smooth function on $J^1 E$:
$$
\mathcal{L}=\frac{1}{2} g^{ij}\eta_{ab}u^{a}_{i}u^{b}_{j},
$$
which depends in this example only on the fiber coordinates $u^a_{i}$.  

From the Lagrangian $\mathcal{L} : J^{1}E \to \mathbb{R}$, the **[[de 
Donder-Weyl Hamiltonian]]** $\mathcal{H} : T \Sigma \otimes T^*X \to \mathbb{R}$ can be constructed via a Legendre transform.   It is given as follows:
$$
\mathcal{H}= p^{i}_{a}u^{a}_{i}- \mathcal{L} =\frac{1}{2} \eta^{ab}g_{ij}p_{a}^{i}p_{b}^{j},
$$
where $u^a_{i}$ are defined implicitly by
$p_a^{i}=\partial \mathcal{L} / \partial u^{a}_{i}$,
and $p_a^{i}$ are coordinates on the
fiber $T^{*}_{u}X \otimes T_{q}\Sigma$.
Note that $\mathcal{H}$ differs from the standard (non-covariant) Hamiltonian density for a field theory: 
$$
p^{0}_{a}u^{a}_{0} - \mathcal{L}.
$$

Let $\phi$ be a section of $E$ and let $\pi$ be a smooth section of $T \Sigma \otimes T^*X$ restricted to $\phi(\Sigma)$ with fiber coordinates $\pi_{a}^{i}$.  It is then straightforward to show
that $\phi$ is a solution of the Euler-Lagrange equations 
if and only if $\phi$ and $\pi$ satisfy the following system of equations:
$$
\frac{\partial \pi^{i}_{a}}{\partial q^i} = 
  -  \left.\frac{\partial \mathcal{H}}{\partial
  u^{a}} \right \vert_{u=\phi,p=\pi} 
$$
$$
\frac{\partial \phi^{a}}{\partial q^i} = \left.\frac{\partial \mathcal{H}}{\partial
  p^i_{a}} \right \vert_{u=\phi,p=\pi}.
$$


This system of equations is a generalization of Hamilton's equations for the point particle.

As explained above, the covariant phase space for the bosonic string is the dual jet bundle 
$(J^1 E)^*$, and this space is equipped with a canonical 2-form $\alpha$ 
whose exterior derivative $\omega = d \alpha$ is a [[multisymplectic form|multisymplectic 3-form]].
Using the isomorphism
$$         (J^1 E)^* \cong  T \Sigma \otimes T^*X \times \mathbb{R} ,$$
a point in $(J^1 E)^{*}$ gets coordinates $(q^i,u^a,p^{i}_{a},e)$. 
In terms of these coordinates, 
$$
\alpha= e dq^{0} \wedge dq^{1} +
\left(p_{a}^{0} du^{a} \wedge dq^{1} - 
p_{a}^{1} du^{a} \wedge dq^{0} \right) .
$$
The multisymplectic structure on $(J^1 E)^*$ is thus
$$   
\omega = 
de \wedge dq^0 \wedge dq^{1} +
\left(dp_a^0 \wedge du^a \wedge dq^{1} - 
dp_a^1 \wedge du^a \wedge dq^{0} \right) .  
$$
So, the variable $e$ may be considered as canonically conjugate to the area form $dq^{0} \wedge dq^{1}$.  

As before, let $\phi$ be a section of $E$ and let $\pi$ be a smooth section of $T \Sigma \otimes T^*X$ restricted to $\phi(\Sigma)$.  Consider the submanifold $S \subset (J^1 E)^*$ with coordinates:
$$
(q^i,\phi^{a}(q^j),\pi_{a}^{i}(q^j),-\mathcal{H}).
$$
Note that $S$ is constructed from $\phi$, $\pi$ and
from the constraint $e + \mathcal{H}=0$. This constraint is analogous to the one that is used in finding constant energy solutions in the extended phase space approach to classical mechanics.  At each point in
$S$, a tangent bivector $v=v_{0} \wedge v_{1}$ can be defined as
$$
v_{0} =\frac{\partial}{\partial q^{0}} + 
\frac{\partial \phi^a}{\partial q^{0}}\frac{\partial}{\partial u^a} + 
\frac{\partial \pi_{a}^{i}}{\partial q^{0}}
\frac{\partial}{\partial p_{a}^{i}}
$$
$$
v_{1} = \frac{\partial}{\partial q^{1}} + 
\frac{\partial \phi^a}{\partial q^{1}}
\frac{\partial}{\partial u^a} + 
\frac{\partial \pi_{a}^{i}}{\partial q^{1}}
\frac{\partial}{\partial p_{a}^{i}}.  
$$

Explicit computation reveals that the submanifold $S$ is
generated by solutions to Hamilton's equations if and only if
$$
\omega(v_{0},v_{1},\cdot)=0. 
$$


## Hamiltonian $n$-dimensional flow

* [[Hamiltonian n-vector field]]



## Relation to $n$-symplectic manifolds

There is also the notion of

* [[n-symplectic manifold]]s. 

Which is different, but related...

....blah-blah....


## Survey of developments in the field {#SurveyDevelopments}

There is in this sense a covariant form of the [[Legendre transformation]] which associates to every field variable as many conjugated momenta -- the multimomenta -- as there are space-time dimensions. These, together with the field variables, those of $n$-dimensional space-time, and an extra variable, the energy variable, span the multiphase space [1]. For a recent exposition on the differential geometry of this construction, see [2]. Multiphase space, together with a closed, nondegenerate differential $(n+1)$-form, the [[multisymplectic form]], is an example of a multisymplectic manifold [3]. 

Among the achievements of the multisymplectic approach is a geometric formulation of the relation of infinitesimal symmetries and covariantly conserved quantities ([[Noether's theorem]]), see [4] for a recent review, and [5,6] for a clarification of the improvement techniques ("Belinfante-Rosenfeld formula") of the energy-momentum tensor in classical field theory. 

Multisymplectic geometry also provides convenient sets of variational integrators for the numerical study of partial differential equations [7].

Since in multisymplectic geometry, the symplectic 2-form of classical [[Hamiltonian mechanics]] is replaced by a closed [[differential form]] of higher tensor degree, multivector fields and differential forms have their natural appearance. (See [8] for an interpretation of multivector fields as describing solutions to field equations infinitesimally.) Multivector fields form a [[graded Lie algebra]] with the [[Schouten bracket]] (see [9] for a review and unified viewpoint). Using the multisymplectic $(n+1)$-form, one can construct a new bracket for the differential forms, the Poisson forms [10], generalizing a well-known formula for the Poisson brackets related to a symplectic 2-form. 

A remarkable fact is that in order to establish a Jacobi identity, the multisymplectic form has to have a potential, a condition that is not seen in symplectic geometry. Further, the admissible differential forms, the Poisson forms, are subject to the rather strong restrictions on their dependence on the multimomentum variables [11]. In particular, $(n-1)$-forms in this context can be shown to arise exactly from the covariantly conserved currents of Noether symmetries [11], which allows their pairing with spacelike hypersurfaces to yield conserved charges in a geometric way.

Not much is known about the interpretation of Poisson forms of form degree between zero and n-1. However, as $(n-1)$-forms describe vector fields and hence collections of lines [2, 10], and as (certain) functions describe n-vector fields and hence collections of bundle sections [8], it seems natural to speculate that the intermediate forms may be useful for the [[brane]]s of [[string theory]].

The Hamiltonian, infinite dimensional formulation of [[classical field theory]] requires the choice of a spacelike hypersurface ("Cauchy surface") [12] which manifestly breaks the general covariance of the theory at hand. For $(n-1)$-forms, the above mentioned new bracket reduces to the Peierls-deWitt bracket after integration over the spacelike hypersurface [13]. With the choice of a hypersurface, a constraint analysis [14] _&#224; la_ Dirac [15,16] can be performed [17]. Again, the necessary breaking of general covariance raises the need for an alternative formulation of all this [18]; first attempts have been made to carry out a [[Marsden-Weinstein reduction]] [19] for multisymplectic manifolds with symmetries [20]. However, not very much is known about how to quantize a multisymplectic geometry, see [21] for an approach using a path integral.

This discussion so far concerns field theories of first order, i.e. where the Lagrangian depends on the fields and their first derivatives. Higher order theories can be reduced to first order ones for the price of introducing auxiliary fields. A direct treatment would involve higher order jet bundles [22]. A definition of the covariant Legendre transform and the multiphase space has been given for this case [3].

## References

### On classical multisymplectic geometry

A comprehensive source on covariant field theory with plenty of further references is

* Mark J. Gotay, James Isenberg, [[Jerrold Marsden]], Richard Montgomery, _Momentum Maps and Classical Relativistic Fields. Part I: Covariant Field Theory_ ([arXiv:physics/9801019](http://arxiv.org/abs/physics/9801019))

Much of the material in the [section on covariant field theory](#extended phase space) is based on this.

Other discussions include

* [[Frédéric Hélein]], _Hamiltonian formalisms for multidimensional calculus of variations and perturbation theory_ ([arXiv:math-ph/0212036](http://arxiv.org/abs/math-ph/0212036))
  {#Helein02}


* Narciso Rom&#225;n-Roy, _Multisymplectic Lagrangian and Hamiltonian Formalisms of Classical Field Theories_, SIGMA 5 (2009), 100 ([journal](http://www.emis.de/journals/SIGMA/2009/100/), [arXiv:math-ph/0506022](http://arxiv.org/abs/math-ph/0506022)) 


The relation to [[covariant phase space]] methods is discussed in 

* [[Frédéric Hélein]], _Multisymplectic formalism and the covariant phase_ ([arXiv:1106.2086](http://arxiv.org/abs/1106.2086))
  {#Helein}

A discussion of [[Hamiltonian n-forms]] as [[observables]] is in 

* [[Frédéric Hélein]], _The notion of observable in the covariant Hamiltonian formalism for the calculus of variations with several variables_ ([arXiv:math-ph/0401047](http://arxiv.org/abs/math-ph/0401047))

Other texts include

* [[Carlo Rovelli]], _Covariant hamiltonian formalism for field theory: Hamilton-Jacobi equation on the space $\mathcal{G}$_ ([arXiv:gr-qc/0207043](http://arxiv.org/abs/gr-qc/0207043))


* xyz...




Much of the above [survey of recent developments](#SurveyDevelopments) and of the following list of references is reproduced from the web-page

* [[Cornelius Mertzlufft-Paufler]], _[Multisymplectic geometry](http://www.mertzlufft-paufler.de/multisymplectic_geometry.html)_

References mentioned above are

* [1] J. Kijowski, W. Szczyrba, _A Canonical Structure For Classical Field Theories_ . Commun. Math. Phys. 46 (1976) 183.

* [2] M. J. Gotay, J. Isenberg, J. E. Marsden: _Momentum maps and classical relativistic fields. I: Covariant field theory_ [arXiv:physics/9801019v2](http://arxiv.org/abs/physics/9801019v2).

* [3] M. J. Gotay, _A multisymplectic framework for classical field theory and the calculus of variations. I: Covariant Hamiltonian formalism_ 
In M. Francaviglia (ed.), _Mechanics, analysis and geometry: 200 years after Lagrange_ Amsterdam etc.: North-Holland (1991), 203--235.

* [4] M. de Leon, D. Martin de Diego, A. Santamaria-Merino, _Symmetries in Classical Field Theory_ [arXiv:math-ph/0404013](http://arxiv.org/abs/math-ph/0404013).

* [5] M. J. Gotay, J. E. Marsden: _Stress-energy-momentum tensors and the Belinfante--Rosenfeld formula_ Contemp. Math. vol. 132, AMS, Providence, 1992, 367--392.

* [6] M. Forger, H. R&#246;mer, _Currents and the energy-momentum tensor in classical field theory: a fresh look at an old problem_ Ann. Phys. (N.Y.) 309 (2004) 306--389. [arXiv:hep-th/0307199](http://arxiv.org/abs/hep-th/0307199).

* [7] A. Lew, J. E. Marsden, M. Ortiz, M. West, _An overview of variational integrators_
In L. P. Franca (ed.), Finite Element Methods: 70's and Beyond. Barcelona (2003).

* [8] C. Paufler, H. R&#246;mer, _The Geometry of Hamiltonian $n$-vector fields in Multisymplectic Field Theory_ J. Geom. Phys. 44, No.1(2002), 52--69. [arXiv:math-ph/0102008](http://arxiv.org/abs/math-ph/0102008).

* [9] Y. Kosmann-Schwarzbach: Derived brackets. Lett. Math. Phys. 69 (2004) 61--87 [arXiv:math.DG/0312524](http://arxiv.org/abs/math.DG/0312524).

* [10] M. Forger, C. Paufler, H. R&#246;mer: _The Poisson Bracket for Poisson Forms in Multisymplectic Field Theory_ Rev. Math. Phys. 15 (2003) 705 [arXiv:math-ph/0202043](http://arxiv.org/abs/math-ph/0202043).

* [10] M. Forger, C. Paufler, H. R&#246;mer, _Hamiltonian Multivector Fields and Poisson Forms in Multisymplectic Field Theory_ [arXiv:math-ph/0407057](http://arxiv.org/abs/math-ph/0407057).

* [11] M. J. Gotay, _A multisymplectic framework for classical field theory and the calculus of variations. II: Space + time decomposition_ Differ. Geom. Appl. 1(4) (1991), 375--390.

* [12] M. O. Salles, _Campos Hamiltonianos e Colchete de Poisson na Teoria Geom&#233;trica dos Campos_ , PhD thesis, IME-USP, June 2004.

* [13] M. J. Gotay, J. M. Nester, _Generalized constraint algorithm and special presymplectic manifolds_
In G. E. Kaiser, J. E. Marsden, Geometric methods in mathematical physics, Proc. NSF-CBMS Conf., Lowell/Mass. 1979, Berlin: Springer-Verlag, Lect. Notes Math. 775 (1980) 78--80.

* [14] P. A. M. Dirac, _Lectures on Quantum Mechanic_ Belfer Graduate School of Science, Yeshiva University, N.Y., 1964.

* [15] M. Henneaux, C. Teitelboim, _Quantization of Gauge systems_ Princeton University Press, 1992.

* [16] M. J. Gotay, J. Isenberg, J. E. Marsden, R. Montgomery, _Momentum Maps and Classical Relativistic Fields II: Canonical Analysis of Field Theories_ (2004) [arXiv:math-ph/0411032](http://arxiv.org/abs/math-ph/0411032).

* [17] N. P. Landsman, _Against the Wheeler-DeWitt equation_ Class. Quan. Grav. 12 (1995) L119-L124. [arXiv:gr-qc/9510033](http://arxiv.org/abs/gr-qc/9510033).

* [18] J. E. Marsden, A. Weinstein _Reduction of symplectic manifolds with symmetry_ Rept. Math. Phys. 5 (1974) 121--130.

* [19] F. Munteanu, A. M. Rey, M. Salgado, _The G&#252;nther's formalism in classical field theory: momentum map and reduction_ J. Math. Phys. 45, No. 5 (2004) 1730--1750.

* [20] D. Bashkirov, G. Sardanashvily, _Covariant Hamiltonian Field Theory. Path Integral Quantization_
[arXiv:hep-th/0402057](http://arxiv.org/abs/hep-th/0402057).

* [21] D. J. Saunders, _The Geometry of Jet Bundles_ Lond. Math. Soc. Lect. Notes Ser. 142, Cambr. Univ. Pr., Cambridge, 1989.

A [[higher category theory|higher categorial]] interpretation of [[2-plectic geometry]] is given in

* [[John Baez]], [[Chris Rogers]], _Categorified Symplectic Geometry and the String Lie 2-Algebra_. [arXiv:0901.4721](http://arxiv.org/abs/0901.4721).

* [[John Baez]], Alexander E. Hoffnung, [[Chris Rogers]], _Categorified Symplectic Geometry and the Classical String_ ([arXiv:0808.0246](http://arxiv.org/abs/0808.0246/))

* [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis (2011) ([arXiv:1106.4068](http://arxiv.org/abs/1106.4068))


Higher order [[moment map]]s are considered in

* Thomas Bruun Madsen, Andrew Swann, _Closed forms and multi-moment maps_ ([arXiv:1110.6541](http://arxiv.org/abs/1110.6541))
 

### Relation to covariant phase space formalism

The relation of multisymplectic formalism to [[covariant phase space]] and [[variational bicomplex]] methods is discussed in 

* [[Michael Forger]], S. Romero, _Covariant Poisson Brackets in Geometric Field Theory._, Commun. Math. Phys. 256 (2005) 375-410, ([arXiv:math-ph/0408008](http://arxiv.org/abs/math-ph/0408008))
 {#ForgerRomero}


### On quantization of multisymplectic geometry {#RefsonQuantization}

The following articles discuss the [[quantization]] procedure for multisymplectic geometry, generalizing [[geometric quantization]] of [[symplectic geometry]].

* I.V. Kanatchikov, _Geometric (pre)quantization in the polysymplectic approach to field theory_ , ([arXiv:hep-th/0112263](http://arxiv.org/abs/hep-th/0112263)).

* I.V. Kanatchikov, _DeDonder-Weyl theory and a hypercomplex extension of quantum mechanics to field theory_ , ([arXiv:hep-th/9810165](http://arxiv.org/abs/hep-th/9810165))


Kanatchikov's "algebra of observables" is what he calls a "higher-order Gerstenhaber algebra". (The "bracket" in this structure fails to satisfy Leibniz's rule as a derivation of the product.) The relationship between it and the [[Lie superalgebra]] of observables constructed by Forger, Paufler, and Roemer is discussed in this paper:


* [[Michael Forger]], C. Paufler, and H. Roemer, _The Poisson Bracket for Poisson Forms in Multisymplectic Field Theory_ , ([arXiv:math-ph/0202043](http://arxiv.org/abs/math-ph/0202043v1))

and ([Forger-Romero](#ForgerRomero)) above. 

Kanatchikov's formalism was used by S.P. Hrabak to propose a multisymplectic refinement of [[BV-BRST formalism]]. See there for more details.

[[!redirects covariant field theory]]

[[!redirects extended phase space]]
[[!redirects extended phase spaces]]

[[!redirects multisymplectic manifold]]
[[!redirects multisymplectic manifolds]]


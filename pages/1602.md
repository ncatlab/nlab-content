
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

A **Green-Schwarz mechanism** (named after [[Michael Green]] and [[John Schwarz]]) is a modification of an [[action functional]] of a [[quantum field theory]] involving higher [[gauge field]]s that makes a [[quantum anomaly]] of the original action functional disappear.

More in detail:

* An [[action functional]] in [[path integral|path integral quantization]] is said to be [[quantum anomaly|anomalous]] if it is only locally identified with a function on the configuration space of fields, but is globally instead a section of a line [[bundle]] (usually equipped with [[connection on a bundle|connection]]).

* Given two anomalous action functionals in this sense, it may happen that while the two corresponding line bundles on configuration space are each nontrivial, their [[tensor product]] becomes trivializable. In this case one can consider the non-anomalous action function given by the sum of the two anomalous action functionals. This is what is called **anomaly cancellation** of one piece of an action functional against another. 

* The two main sources of examples for action functionals that are anomalous are

  * the standard [[fermionic action functional]] (see there for details) for chiral fermions 

    * this is a section of the [[Pfaffian line bundle]] for the 
      [[Dirac operator]]

  * the action functional for [[differential cohomology|differential cocycles]] (higher connection, higher [[gauge theory]]) in the presence of [[electric charge|electric]] and [[magnetic charge]]s: 

    * this is a [[section]] of the [[transgression]] of the 
      [[line bundle]] arising as the [[cup product]] of 
      the [[electric charge|electric]] and 
      [[magnetic charge|magnetic differential cocycles]].


A **Green--Schwarz mechanism** is the addition of an action functional for higher differential cocycles with [[magnetic charge]]s such that their [[quantum anomaly]] cancels a given [[Pfaffian line bundle]]: so it is a choice of by itself ill-defined action functional for higher gauge theory that cancels the ill-definedness of an action functional for chiral fermions.

In the more strict and original sense of the word, _the_ Green--Schwarz mechanism is the application of this procedure in the theory called [[heterotic string theory|heterotic supergravity]]: there it so happens that the Pfaffian line bundle of the fermionic action has as [[Chern class]] the [[transgression]] of a degree-12 class in [[ordinary differential cohomology]] that factorizes as $I_8 \wedge I_4$. Since heterotic supergravity contains a higher gauge field that couples to [[string theory|strings]], this is precisely of the form $J_{electric} \wedge J_{magnetic}$ that the anomaly for the corresponding higher gauge theory in the presence of magnetic charges gives rise to. So the original Green--Schwarz anomaly cancellation mechanism consist of modifying the "naive" action functional for heterotic supergravity by adding the contribution that corresponds to adding a magnetic current of the form

$$
  j_B := I_4
  \,.
$$


## The higher magnetic charge anomaly


### The higher abelian Yang-Mills action functional...
  {#YMactionfunctional}

Consider on some [[spacetime]] $X$ a [[gauge field]] $[\nabla] \in H_{diff}^{n+1}(X)$ modeled in [[ordinary differential cohomology]] in degree $n+1$: a [[circle n-bundle with connection]]. For instance

* in degree $n=1$ this is an [[electromagnetic field]];

* in degree $n=2$ this is a [[Kalb-Ramond field]];

* in degree $n = 3$ a [[supergravity C-field]].

Canonically associated to the [[gauge field]] is its [[field strength]]: the [[curvature]] [[differential form]]

$$
  F_\nabla \in \Omega^{n+1}_{cl}(X)
  \,.
$$

The abelian [[Yang-Mills action functional]] for our gauge field (the [[action functional]] of higher order [[electromagnetism]]) is the [[function]]

$$
  \exp(i S_{YM}(-)) : H_{diff}^{n+1}(X) \to \mathbb{C}
$$

that sends the field $\nabla$

$$
  \exp(i S_{YM}(-))
    : 
  [\nabla] 
   \mapsto 
  \exp(-i \int_X F_\nabla \wedge \star F_\nabla)
$$

to the [[exponential]] of the [[integral]] over the [[spacetime]] $X$ of the  [[differential form]] obtained as the [[wedge product]] of the [[curvature form]] with its image under the [[Hodge star operator]] correspondonding to the [[pseudo-Riemannian manifold|pseudo-Riemannian metric]] on $X$.

The fact that this map [[function]] defined in terms of [[cocycle]]s is a well defined function on [[cohomology]] means that the [[action functional]] is [[gauge transformation|gauge invariant]]. At this point this is just the trivial statement that under a [[gauge transformation]]

$$
  \nabla \stackrel{g}{\to} \nabla'
$$

the [[curvature]] invariant: $F_\nabla = F_{\nabla'}$.



### ... with electric charge ...
  {#WithElectricCharge}

The [above](#YMactionfunctional) [[action functional]] describes the dynamics of the [[gauge field]] all by itself, with no interactions with other fields or with [[relativistic particle|fundamental particle]]s/[[brane|fundamental brane]]s.

A distribution of  $n$-[[electric charge]] on $X$ is modeled itself by a [[cocycle]] $\hat j_E$ in [[ordinary differential cohomology]] in degree $dim X - n$

$$
  [\hat j_E] \in H_{diff}^{dim X - n}(X)
  \,.
$$

The [[curvature]] $j_E$ of $\hat j_E$ is the [[electric current]] form. The [[action functional]] that encodes the [[force]] of the [[gauge field]] exerted on this electric charge distribution is locally on [[coordinate chart]]s $U \subset X$ given by the [[integral]] $\int_X A_U \wedge j_E$, where $A_U$ is the local [[connection on an infinity-bundle|connection]] $n$-form of the gauge field $\nabla$.

Globally, this contribution is given by the push-forward 

$$
  2 \pi i\int_X (-) : H_{diff}^{dim X}(X) \to H_{diff}^0(*) = U(1)
$$ 

of the [[cup product]] $\hat j_E \cdot \nabla$ in [[ordinary differential cohomology]].

In total the [[action functional]] of higher abelian [[Yang-Mills theory]] in the presence of [[electric charge]] is the [[function]]

$$
  \exp(i S_{YM}(-) + i S_{el}(-)) 
    :
  H^{n+1}_{diff}(X) 
   \times
  H^{dim X - n}_{diff}(X)
   \to
  \mathbb{C}
$$

given by

$$
  ([\nabla], [\hat j_E]) 
     \mapsto
  \exp(i \int_X F_\nabla \wedge \star F_\nabla)
  \exp(2 \pi i \int_X \hat j_E \cdot \nabla)
  \,.
$$


### ... and with magnetic charge.

We now consider one more additional term in the [[action functional]], one that describes moreover the interaction of our [[gauge field]] with a distribution of $n$-[[magnetic charge]] on $X$, in addition to the interaction with the distribution of [[electric charge]] described 
[above](#WithElectricCharge).

The [[magnetic charge]] distribution itself is also modeled as a  [[cocycle]] $\hat j_B$ in [[ordinary differential cohomology]]. As opposed to the [[electric charge]] it is however not part of the dynamics but of the kinematics of the system: it does not manifestly show up in the integral expression for the [[action functional]], but does modify the nature of the configuration space that this action functional is defined on.

Namely the kinematic higher [[Maxwell equations]] is a condition of the form

$$
  d F_\nabla = j_B
  \,,
$$

where $j_B$ is the [[magnetic charge]] distribution. If $F_\nabla$ is the [[curvature]] of a [[circle n-bundle with connection]], then necessarily $d F_\nabla = 0$. Therefore the system of higher electromagnetism in the presence of magnetic charge cannot be modeled any more by [[cocycle]]s in [[ordinary differential cohomology]].

One finds instead that one has to model $\nabla$ not as a [[circle n-bundle with connection]], but as an $n$-[[twisted bundle]] with connection, where the [[twisted cohomology|twist]] is $\hat j_B$. 

We shall write $C^{n+1}_{diff}(X)_{\hat j_B}$ for the [[∞-groupoid]] of twisted cocycles for this fixed twist. The crucial point is now the following:

the [above](#WithElectricCharge) expression 

$$
  \exp(i S_{el}(\nabla, \hat j_E)) 
    :
    \exp(2 \pi i \int_X \hat j_E \cdot \nabla)
$$

for the electric coupling can still be given sense, even with $\nabla \in C^{n+1}_{diff}(X)_{\hat j_B}$, but it no longer has the interpretation of a [[circle group]]-valued [[function]]. Rather, it has now the interpretation of a [[section]] of a [[line bundle]] 

$$
  \array{
    && Anom_{\hat j_B}
    \\
     & {}^{\mathllap{\exp(S_{el})}}\nearrow & \downarrow
    \\
    Conf &=& Conf
  }
$$

on configuration space. The [[characteristic class]] of this line bundle -- its  [[Chern class]] -- is hence the _magnetic anomaly_ in higher gauge theory.

In the next section we formalize properly the notion of this line bundle on configuration space.


### The anomaly line bundle

In order to formalize this we have to refine the formalization of the structure of the configuration space. So far we had regarded the [[set]] $H^{dim X - n}_{diff}(X) \times H_{diff}^{n+1}(X)$ of gauge equivalence classes of field configurations. This is the set of connected components of the full [[cocycle]] [[∞-groupoid]]

$$
  C^{dim X - n}_{diff}(X) \times C_{diff}^{n+1}(X)
  \in
  \infty Grpd
$$

whose

* [[object]]s are field configurations on $X$;

* [[morphism]]s are [[gauge transformation]]s;

* [[2-morphism]]s are gauge transformations of gauge transformation, 

* and so on.

Moreover this cocycle [[∞-groupoid]] is not just a [[discrete ∞-groupoid]] but it naturally has _smooth structure_ : it is naturally a [[smooth ∞-groupoid]]: an [[∞-stack]] over the [[category]] [[SmoothMfd]]. We shall write

$$
  Conf :=
  [X,(\mathbf{B}^{n}U(1) \times \mathbf{B}^{dim X - n-1}U(1))_{conn}]
  \in 
  Smooth\infty Grpd
$$

for this smooth $\infty$-groupoid of configuration of the physical system -- defined as the [[internal hom]] in terms of the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-topos#ClosedMonoidalStructure">closed monoidal structure on the (∞,1)-topos</a> [[Smooth∞Grpd]] of $X \in SmoothMfd \hookrightarrow Smooth\infty Grpd$ into the target object of the higher [[gauge theory]], (this object is discussed in detail <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#StrucDifferentialCohomology">here</a>; it is presented under the [[Dold-Kan correspondence]] by the [[Deligne complex]] of sheaves on [[CartSp]]).

This smooth structure is characterized by saying that for any $U \in$ [[SmoothMfd]] the $U$-parameterized smooth families of field configurations, gauge transformations, etc. form the [[∞-groupoid]] 

$$
  Conf(U) 
   \simeq 
  C^{dim X - n}_{diff}(U \times X) \times C_{diff}^{n+1}(U \times X )
$$

of gauge fields on the [[product]] of [[spacetime]] $X$ with the parameter space $U$. (See for instance [[Lie integration]] and [[connection on an ∞-bundle]] for details on how differential forms on $U \times X$ encode $U$-families of forms on $X$).

This way the configuration space of higher electromagnetism in the presence of electric and magnetic charge is naturally incarnated as an object in the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoid]]s, and accordingly all the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Structures">differential geometric structures</a> in cohesive $(\infty,1)$-topos are available. In particular we may speak of [[circle n-bundle with connection|line bundle with connection]] on $Conf$, given for instance by morphisms

$$
  Anom_{\hat j_B} : Conf \to \mathbf{B} U(1)_{conn}
$$

in [[Smooth∞Grpd]].

We say

* the underlying class in [[ordinary cohomology]]

  $$
    [Anom_{\hat j_B}] \in H^1(Conf, U(1))
  $$

  is **the anomaly** of the system of higher electromagnetism coupled to electric and magnetic charge;

* its [[curvature]] 2-form

  $$
    Curv_{Anom_{\hat j_B}} : Conf \to \mathbf{\flat}_{dR} \mathbf{B}^2 \mathbb{R}
  $$

  is the **differential anomaly**.

One finds that this curvature 2-form is given by the [[fiber integration]] of the wedge product of the [[electric charge]] $(n+1)$-form with the [[magnetic charge]] $dim X - n$-form over $X$:

$$
  Curv_{Anom_{\hat j_B}}
   =
   \int_X j_E \wedge j_B
  \,.
$$

This means that for every parameter space $U \in $ [[SmoothMfd]] and every morphism $\phi : U \to Conf$ -- which corresponds by the nature of the [[∞-stack]] $Conf$ to a field configuration $(\nabla, \hat j_E) \in C^{n+1}_{diff}(U \times X) \times C^{dim X - n}_{diff}(U \times X)$ -- the pullback of this differential form to $U$ yields the ordinary differential form $\int_X j_E \wedge j_B$ in the image of $(\nabla, \hat j_E)$ under the [[fiber integration]] map

$$
  \int_X(-) : \Omega^\bullet(U \times X) \to \Omega^\bullet(U)
  \,.
$$




### The Green-Schwarz mechanism

We can now state the **Green-Schwarz mechanism** itself. 

Let $\hat Conf \in $ [[Smooth∞Grpd]] be the configuration space of a physical system that contains among its fields higher abelian gauge theory with [[electric charge]] with configuration space $Conf$

$$
  \hat Conf = Conf_{rest} \times Conf
$$

and equipped with an [[action functional]]


$$
  \exp(i S_{rest}(-) + i S_{el}(-))
  : 
  \hat Conf \to Anom_{rest}
$$

that is a [[section]] of an anomaly line bundle $Anom_{rest}$

$$
  \array{
    && Anom_{rest}
    \\
     & {}^{\mathllap{\exp(S_{tot})}}\nearrow & \downarrow
    \\
    Conf_{rest} &=& Conf_{rest}
  }
$$

such that the [[curvature]] 2-form of $Anom_{tot}$ happens to be of the form

$$
  Curv{Anom_{ref}} = \int_X I_{n+2} \wedge I_{(dim X - n)}
  \,,
$$

for some $I_{n+2} \in \Omega^{n+2}_{cl}(X)$ and 
$I_{dim X - n} \in \Omega^{dim X - n}(X)$.


Then the **Green-Schwarz mechanism** is the map that changes this physical system by adding magnetic charge to it, given by a cocycle 
$\hat j_B$ with

$$
  [\hat j_B] = - [Anom_{rest}]
$$

$$
  j_B = - I_{dim X - n}
  \,.
$$

This means by the above that the new [[action functional]] is now a section 

$$
  \exp(i S_{rest}(-) + i S_{el}(-))
  : 
  Conf_{rest} \times Conf \to Anom_{rest} \otimes Anom_{\hat j_B} 
$$

of the [[tensor product]] of the two anomaly line bundles. 
The [[Chern class]] of the tensor product is the sum of the two Chern-classes, hence by definition of $j_B$ they cancel, so that $Anom_{rest} \otimes Anom_{\hat j_B}$ is trivializatable as a line bundle with connection.

A choice of such trivialization identifies the section then with an ordinary function

$$
  \exp(i S_{rest}(-) + i S_{el}(-))
  : 
  Conf_{rest} \times Conf \to U(1) 
  \,.
$$

This is the anomaly-free action functional after the Green-Schwarz mechanism has been applied.

## Examples

### Heterotic supergravity

The original work of Green-Schwarz concerned anomaly cancellation in the effective [[supergravity]] theory on a $dim X = 10$-dimensional target [[spacetime]] in [[heterotic string theory]].

The configurations of this theory are given by

* a [[Spin]]-[[principal bundle]] [[connection on a bundle|with connection]] $\hat \omega$ -- the [[spin connection]] 
  (the [[graviton]]);

* a [[unitary group]]-[[principal bundle]] [[connection on a bundle|with connection]] $\hat A$ (the [[Yang-Mills field]]);

* a [[circle n-bundle with connection|circle 2-bundle with connection]] $\hat B$ -- the [[Kalb-Ramond field]].

* [[section]]s of the [[associated bundle|associated]] [[spinor bundle]]s: the fermions $\psi$ ([[gravitino]], [[gaugino]], [[dilatino]]).

The [[path integral]] over the fermionic part of the action 

$$
  \exp(i S_{ferm}(-)) : (\omega, A, B, \psi) \mapsto   \exp(i \int_X \bar \psi D_{\omega,A} \psi)
$$ 

is an anomalous action functional on the configuration space of the remaining bosonic fields $(\hat A, \hat \omega)$, a [[section]] of a [[Pfaffian line bundle]], whose curvature form turns out to be

$$
  curv_{Pfaff} = \int_X I_4 \wedge I_8
$$

with 

$$
  I_4 = \frac{1}{2} p_1(F_\omega) - ch_2(F_A)
$$

the difference between the (image in [[de Rham cohomology]] of the) first fractional [[Pontryagin class]] of the $Spin$-principal bundle and second [[Chern class]] of the [[unitary group]]-[[principal bundle]]

and

$$
  I_8 = \frac{1}{48} p_2(F_\omega) - ch_4(F_A) +
  ...
$$

where the ellipses indicate decomposable [[curvature characteristic form]]s.

Therefore in this case the Green-Schwarz mechanism consists of 

1. adding to the system _fivebrane [[magnetic charge]]_ $j_B \in \Omega^{2+2}$ given by $I_4$.

   This means that the Kalb-Ramond field $\hat B$ becomes a twisted field whose [[field strength]] $H$ is no longer closed, but satisfies the kinematical [[Maxwell equation]] 

   $$
     d H = I_4
     \,.
   $$

1. adding to the system _string [[electric charge]]_ $j_E \in \Omega^{10 - 2}(X)$ .

   This means that to the [[action functional]] is added the factor

  $$
    \exp(i \int_X \hat B \cdot \hat I_8 )
  $$


  which is locally on $U \hookrightarrow X$ given in the exponent by the integral

  $$
    \int_U B_U \wedge I_8
     \,.
  $$

The nature of the field configuration obtained this way -- spin connection with twist of th Kalb-Ramond field by the Pontryagin class -- may be understood conciesely as constituting a [[differential string structure|twisted differential string structure]] on $X$. See there for more details.

### Axions and the strong CP problem in heterotic supergravity

The Green-Schwarz anomaly cancellation mechanism naturally makes the twisted [[B-field]] in [[heterotic string theory]] behave like the [[axion]] with the correct potential to serve as the [[theta angle]] and serve as the solution to the [[strong CP problem]] ([Svrcek-Witten 06](#SvrcekWitten06)):

> An obvious question about the axion hypothesis is how natural it really is. Why introduce a global PQ "symmetry" if it is not actually a symmetry? What is the sense in constraining a theory so that the classical Lagrangian possesses a certain symmetry if the symmetry is actually anomalous? It could be argued that the best evidence that PQ "symmetries" are natural comes from string theory, which produces them without any contrivance. ... the string compactifications always generate PQ symmetries, often spontaneously broken at the string scale and producing axions, but sometimes unbroken.([Svrcek-Witten 06, pages 3-4](#SvrcekWitten06))


In [[heterotic string theory]] [[KK-compactification|KK-compactified]] to 4d, the 4d [[B-field]], dualized, serves as the axion field, called the "model independent axion" ([Svrcek-Witten 06, starting p. 15](#SvrcekWitten06)).

This works as follows: By the [[Green-Schwarz anomaly cancellation]] mechanism, then [[B-field]] in [[heterotic string theory]] is a twisted 2-form field, whose [[field strength]] $H$ locally has in addition to the exact differential $d B$ also a fundamental 3-form contribution, so that

$$
  H = d B + C
$$

(locally). Moreover, the differential $d H$ is constrained to be the Pontryagin 4-form of the gauge potential $\nabla$ (minus that of the  [[Riemann curvature]], but let's suppress this notationally for the present purpose):

$$
  d H = tr \left(F_\nabla \wedge F_\nabla\right)
  \,.
$$

Now suppose [[KK-compactification]] to 4d has been taken care of, then this constraint may be implemented in the [[equations of motion]] by adding it to the [[action functional]], multiplied with a [[Lagrange multiplier]] :

$$
  S 
    =  
  \underset{
      \text{kinetic action} \atop \text{for B-field}
   }{
        \underbrace{\int_X H \wedge \star H}
   }
    +  
   \underset{
      \text{Green-Schwarz constraint}
   }{
    \underbrace{
      \int_X a \left( d H - tr(F_\nabla \wedge F_\nabla) \right)
    }
   }
  \,.
$$

Now by the usual argument, one says that instead of varying by $a$ and thus implementing the [[Green-Schwarz anomaly cancellation]] constraint, it is equivalent to fist vary with respect to the other fields, and then insert the resulting equations in terms of $a$ into the action functional.

Now since we are dealing with a twisted [[B-field]], with free 3-form component $C$, we actually vary with respect to $C$. This yields the [[Euler-Lagrange equation]] [[equation of motion|of motion]]

$$
  d a = \star H
  \,,
$$

hence the usual relation or [[electro-magnetic duality]], expressing what used to be the [[Lagrange multiplier]] now as the magentic dual [[field (physics)|field]] to the twisted [[B-field]].

Plugging this algebraic [[equation of motion]] back into the above [[action functional]] for $H$ gives

$$
  \tilde S
    =
  \underset{\text{kinetic action} \atop \text{for axion field}}{\underbrace{\int_X d a \wedge \star d a}}
  + 
  \underset{\text{axionic} \atop \text{interaction}}{\underbrace{\int_X a \, tr(F_\nabla \wedge F_\nabla)}}
  \,.
$$





## Related concepts

* [[Freed-Witten anomaly]]


## References

### General

The original articles are

* [[Michael Green]], [[John Schwarz]], _Anomaly Cancellation in Supersymmetric $D=10$ Gauge Theory and Superstring Theory_, Phys. Lett. B 149 (1984) 117-122 ([spire:15583](https://inspirehep.net/literature/15583), <a href="https://doi.org/10.1016/0370-2693(84)91565-X">doi:10.1016/0370-2693(84)91565-X</a>) 

* {#CHSW85} [[Philip Candelas]], [[Gary Horowitz]], [[Andrew Strominger]], [[Edward Witten]], _Vacuum configurations for superstrings_, Nuclear Physics B Volume 258, 1985, Pages 46-74 Nucl. Phys. B 258, 46 (1985) (<a href="https://doi.org/10.1016/0550-3213(85)90602-9">doi:10.1016/0550-3213(85)90602-9</a>)

Review (with an eye towards [[KK-compactification]] to 6d, see also at [[D=6 N=(1,0) SCFT]]):

* [[Michael Green]], [[John Schwarz]], [[Pete West]], Section 2 of: _Anomaly-free chiral theories in six dimensions_, Nuclear Physics B Volume 254, 1985, Pages 327-348 (<a href="https://doi.org/10.1016/0550-3213(85)90222-6">doi:10.1016/0550-3213(85)90222-6</a>)

* [[Augusto Sagnotti]], _A Note on the Green - Schwarz Mechanism in Open - String Theories_, Phys. Lett. B294:196-203, 1992 ([arXiv:hep-th/9210127](https://arxiv.org/abs/hep-th/9210127))


A clear and precise account of what the relevant anomalies are and what the Green-Schwarz mechanism is to cancel them is given in (see also the relevant bits at _[[eta invariant]]_)

* {#Witten99} [[Edward Witten]], section 2.2 of _World-Sheet Corrections Via D-Instantons_, JHEP 0002:030, 2000 ([arXiv:9907041](http://arxiv.org/abs/hep-th/9907041))

Review, broader context and further discussion is given in

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_ ([arXiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220))


An account of historical developments is in section 7 of

* [[John Schwarz]], _The Early Years of String Theory: A Personal Perspective_ in _[The birth of string theory](books+about+string+theory#TheBirthOfStringTheory)_ ([arXiv:0708.1917](http://arxiv.org/abs/0708.1917))


The full formula for the differential form data including the fermionic contributions is in 

* {#BBDFLPPRRTZ} L. Bonora, M. Bregola, R. D'Auria, P. Fr&eacute; K. Lechner, P. Pasti, I. Pesando, M. Raciti, F. Riva, M. Tonin and D. Zanon, _Some remarks on the supersymmetrization of the Lorentz Chern-Simons form in $D = 10$ $N= 1$ supergravity theories_, Physics Letters B 277 (1992) ([[BonoraSuperGS.pdf:file]])

and references given there.


Discussion [[higher gauge theory]]:

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Twisted differential String and Fivebrane structures_, Commun. Math. Phys. 315 (2012), 169-213 ([arXiv:0910.4001](https://arxiv.org/abs/0910.4001))

* [[Clay Cordova]], [[Thomas Dumitrescu]], [[Kenneth Intriligator]], _Exploring 2-Group Global Symmetries_ ([arXiv:1802.04790](https://arxiv.org/abs/1802.04790))


### In axion physics

Discussion relating to [[axions]] is in

* {#SvrcekWitten06} Peter Svrcek, [[Edward Witten]], _Axions In String Theory_, JHEP 0606:051,2006 ([arXiv:hep-th/0605206](http://arxiv.org/abs/hep-th/0605206))


[[!redirects Green-Schwarz mechanisms]]

[[!redirects Green Schwarz mechanism]]
[[!redirects Green-Schwarz mechanism]]
[[!redirects Green?Schwarz mechanism]]

[[!redirects Green--Schwarz mechanism]]
[[!redirects Green Schwartz mechanism]]
[[!redirects Green-Schwartz mechanism]]
[[!redirects Green?Schwartz mechanism]]
[[!redirects Green--Schwartz mechanism]]

[[!redirects Green-Schwarz anomaly cancellation]]
[[!redirects Green-Schwarz quantum anomaly cancellation]]

[[!redirects Green-Schwarz anomaly]]

[[!redirects Green–Schwarz mechanism]]
[[!redirects Green–Schwarz mechanisms]]



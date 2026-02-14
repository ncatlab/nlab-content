
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential geoemtry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the context of [[electromagnetism]], _Maxwell's equations_ are the [[equations of motion]] for the electromagnetic [[field strength]] [[electric current]] and [[magnetic current]]. 

(This is the specialization of the *[[Yang-Mills equations]]* for the case that the [[structure group]] is [[abelian group|abelian]], see [there](Yang-Mills+equation#AbelianCase)).


## Three dimensional formulation 

$E$ is here the (vector of) strength of electric field and $B$ 
the strength of magnetic field; $Q$ is the charge and $j_{el}$ the density of the electrical current; $\epsilon_0$, $c$, $\mu_0$ are constants (electrical permeability, speed of the light, and magnetic permeability; all of/in vacuum: $\mu_0 \epsilon_0  = 1/c^2$).  

### Integral formulation in vacuum

__[[Gauss' law]] for electric fields__
$$
\textstyle{\int}_{\partial V} E\cdot d A =  \frac{Q}{\epsilon_0}
$$
where $\partial V$ is a closed surface which is a boundary of a 3d domain $V$ (physicists say "volume") and $Q = \textstyle{\int}_V \rho d V$ the charge in the domain $V$; $\cdot$ denotes the scalar (dot) product. Surface element $d A$ is $\vec{n} d |A|$, i.e. it is the scalar surface measure times the unit vector of normal outwards. 

__No magnetic monopoles__ (Gauss' law for magnetic fields)
$$
\textstyle{\int}_\Sigma B\cdot d A =  0
$$
where $\Sigma$ is any closed surface.

__Faraday's law of induction__
$$
\textstyle{\oint}_{\partial \Sigma} E\cdot d s = - \frac{d}{d t} \textstyle{\int}_\Sigma B\cdot d A
$$

The line element $d s$ is the differential (or 1-d measure on the boundary) of the length times the unit vector in counter-circle direction (or parametrize the curve with $s$ being a vector in 3d space, express magnetic field in the same parameter and calculate the
integral as a function of parameter: $\cdot$ is a scalar ("dot") product).

__Amp&#232;re-Maxwell law__ (or generalized Amp&#232;re's law; Maxwell added the second term involving derivative of the flux of electric field
to the Amp&#232;re's law which described the magnetic field due electric current).
$$
\textstyle{\oint}_{\partial \Sigma} B\cdot d s = \mu_0 I + \mu_0 \epsilon_0 \frac{d}{d t} \textstyle{\int}_\Sigma E\cdot d A
$$
where $\Sigma$ is a surface and $\partial \Sigma$ its boundary; $I$ is the total current through $\Sigma$ (integral of the component of $j_{el}$ normal to the surface). 



### Differential equations
 {#DifferentialEquations}

Here we put units with $c = 1$. By $\rho$ we denote the density of the charge.

In [[pre-metric electromagnetism|pregeometric form]], Maxwell's equations are [[differential equations]] for *four* fields ([[vector fields]]) called

* *electric field* $\vec E$

* *magnetic flux density* $\vec B$

* *magnetic field* $\vec H$

* *displacement field* $\vec D$ (or similar)

and state:

* **([[magnetic Gauss law]])** 

  $div B = 0$

  ("there is no source for magnetic [[flux]], hence no [[magnetic monopoles]]")

* **Faraday's law**: 

  $\frac{d}{d t} B + rot E = 0$

* **([[electric Gauss law]])**: 

  $div D = \rho$ 

  ("the source of electric [[flux]] is electric current")

* **generalized Amp&#232;re's law** 
 
  $- \frac{d}{d t} D + rot H = j_{el}$

In order to complete this [[pregeometric electromagnetism|pregeometric]] form to the actual [[equations of motion]] of the [[electromagnetic field]], these four fields are to be subjected to a constraint called the *[[constitutive equation]]* which expresses $(\vec D, \vec H)$ as a [[function]] of $(\vec E, \vec B)$. 

In [[vacuum]] and in the absence of [[background field|background]] [[gravity]], this [[constitutive relation]]: 

* equates the displacement field $\vec D$ with the electric field $\vec E$ times a constant $\epsilon_0$ 

  called the "*permitivity of the vacuum*", 

* equates the magnetic flux $\vec B$ with the magnetic field $\vec H$ times a constant $\mu_0$ 

  called the "*permeability of the vacuum*". 

But for [[electromagnetic fields]] inside [[dielectric media]] other [[constitutive relations]] appear. For small field strengths these are typically [[linear functions]] $C$ (e.g. [de Lange & Raab 2006 (19)](#deLangeRaab06))

$$
  (\vec D, \vec H) 
    \;\overset{!}{=}\; 
  C\big((\vec E, \vec B)\big)
  \,,
$$

but in general the constitutive [[relation]] can be a non-linear or even be a "[[multi-valued function]]" (namely when there are *hysteresis* effects in the [[dielectric medium]]).

Similarly (interestingly), in the presence of [[background field|background]] [[gravity]] (such as for [[electromagnetic fields]] in and around a star) there is a linear such relation depending on the [[pseudo-Riemannian metric]]. This is most transparently expressed in terms of the [[Hodge star operator]] acting on the electromagnetic fields re-packaged as a [[Faraday tensor]] [[differential 2-form]] (see [below](#InTermsOfFaradayTensor)).



## In terms of Faraday tensor $F$
 {#InTermsOfFaradayTensor}

This is adapted from _[electromagnetic field -- Maxwell's equations](electromagnetic+field#MaxwellEquations)_, for more see the references [below](#ReferencesForMaxwellEquationsViaDifferentialForms).

In modern language, the insight of ([Maxwell, 1865](#Maxwell1865)) is that locally, when physical [[spacetime]] is well approximated by a patch of its tangent space, i.e. by a patch of 4-dimensional [[Minkowski space]] $U \subset (\mathbb{R}^4, g = diag(-1,1,1,1))$, the electric field $\vec E = \left[ \array{E_1 \\ E_2 \\ E_3} \right]$ and magnetic field $\vec B = \left[ \array{B_1 \\ B_2 \\ B_3} \right]$ combine into a differential [[differential form|2-form]]

$$
  \begin{aligned}
    F & \coloneqq E \wedge d t + B
      \\
      & \coloneqq 
        E_1 d x^1 \wedge d t + 
        E_2 d x^2 \wedge d t + 
        E_3 d x^3 \wedge d t  
     \\
& \phantom{\coloneqq} +
        B_1 d x^2 \wedge d x^3 +
        B_2 d x^3 \wedge d x^1 +
        B_3 d x^1 \wedge d x^2
  \end{aligned}
$$

in $\Omega^2(U)$ and the [[electric charge]] density and current density combine to a differential 3-form

$$
\begin{aligned}
    j_{el} & \coloneqq j\wedge dt - \rho d x^1 \wedge d x^2 \wedge d x^3 \\
& \coloneqq    j_1 d x^2 \wedge d x^3 \wedge d t +
        j_2 d x^3 \wedge d x^1 \wedge d t +
        j_3 d x^1 \wedge d x^2 \wedge d t
        -
        \rho \; d x^1 \wedge d x^2 \wedge d x^3
\end{aligned}
$$
 
in $\Omega^3(U)$ such that the following two equations of differential forms are satisfied

$$
  \begin{aligned}
    d F = 0
    \\
    d \star F  = j_{el}
  \end{aligned}
  \,,
$$

where $d$ is the de Rham differential operator and $\star$ the [[Hodge star]] operator. If we decompose $\star F$ into its components as before as 

$$
\begin{aligned}
\star F 
&= -D + H\wedge dt \\
&= -D_1 \; d x^2 \wedge d x^3 
   -D_2 \; d x^3 \wedge d x^1
   -D_3 \; d x^1 \wedge d x^2
     \\
& \phantom{=} +
     H_1 \; d x^1 \wedge d t
     +
     H_2 \; d x^2 \wedge d t
     +
     H_3 \; d x^3 \wedge d t
  \end{aligned}
$$

then in terms of these components the Maxwell equations  read as follows:

$d F = 0$ gives the [[magnetic Gauss law]] and Faraday's law

$d \star F = j_{el}$ gives [[Gauss's law]] and Amp&#232;re-Maxwell law

## In terms of the Faraday bivector $F$

In the [[geometric algebra]] formalism of electromagnetism, one works in the 4-dimensional [[Clifford algebra]] $\mathrm{Cl}^{1, 3}(\mathbb{R})$ representing [[spacetime]], where the orthonormal basis vectors $\{\gamma_i\}$ have signature $(+, -, -, -)$ with $\gamma_0$ representing the time dimension and the other three basis vectors representing the spacial dimensions. The pseudoscalar of $\mathrm{Cl}^{1, 3}(\mathbb{R})$ is represented by the product of all the basis vectors 
$$I = \prod_{i} \gamma_i = \gamma_0 \gamma_1 \gamma_2 \gamma_3$$ 
The basis [[bivectors]] of $\mathrm{Cl}^{1, 3}(\mathbb{R})$ come in two sets, the *timelike bivectors* $\sigma_1 = \gamma_1 \gamma_0$, $\sigma_2 = \gamma_2 \gamma_0$, $\sigma_3 = \gamma_3 \gamma_0$, and the *spacelike bivectors* $I \sigma_1 = -\gamma_2 \gamma_3$, $I \sigma_2 = \gamma_1 \gamma_3$, $I \sigma_3 = \gamma_1 \gamma_2$. The bivector subalgebra of $\mathrm{Cl}^{1, 3}(\mathbb{R})$ is equivalent to the three-dimensional [[Clifford algebra]] $\mathrm{Cl}^{3, 0}(\mathbb{R})$ corresponding to the relative space in the rest frame defined by $\gamma_0$, where the basis timelike bivectors correspond to the basis relative vectors and the basis spacelike bivectors correspond to the basis relative bivectors of the rest frame. 

Let $x$ be a vector in $\mathrm{Cl}^{1, 3}(\mathbb{R})$. Then we define the coordinates of $x$ relative to the basis $\{\gamma_i\}$ to be $x^i = \gamma_i \cdot x$. $x^0$ is also denoted as $t$ since it represents the time coordinate. The spacetime vector derivative is defined as the operator

$$\nabla = \gamma_0 \frac{\partial}{\partial t} + \gamma_1 \frac{\partial}{\partial x^1} + \gamma_2 \frac{\partial}{\partial x^2} + \gamma_3 \frac{\partial}{\partial x^3}$$

The relative vector derivative is defined as the operator

$$\mathbf{\nabla} = \sigma_1 \frac{\partial}{\partial x^1} + \sigma_2 \frac{\partial}{\partial x^2} + \sigma_3 \frac{\partial}{\partial x^3}$$

Assuming the use of [[natural units]] where $c = \epsilon_0 = 1$ and ignoring the polarization and magnatization fields for the time being, Maxwell's equations are written as:

* electric Gauss's law:
$$\mathbf{\nabla} \cdot E = \rho$$

* Faraday's law: 
$$\mathbf{\nabla} \wedge E = -\frac{\partial}{\partial t}\left(I B\right)$$

* magnetic Gauss's law:
$$\mathbf{\nabla} \cdot B = 0$$

* Ampère-Maxwell law:
$$\mathbf{\nabla} \wedge B = I\left(\mathbf{J} + \frac{\partial}{\partial t}\left(E\right)\right)$$

where $E$ and $B$ are the relative electric and magnetic relative fields, $\rho$ is the density of the charge, and $\mathbf{J}$ is the relative current of the charge. 

The *Faraday bivector* is the bivector $F = E + I B$. By multiplying the last two equations by the pseudoscalar, one gets 
$$\mathbf{\nabla} \cdot (I B) = 0$$
$$\mathbf{\nabla} \wedge (I B) = -\mathbf{J} - \frac{\partial}{\partial t}\left(E\right)$$

and by adding the four equations together, one gets the equation 
$$\mathbf{\nabla} \cdot (E + I B) + \mathbf{\nabla} \wedge (E + I B) = \rho -\mathbf{J} -\frac{\partial}{\partial t}\left(E + I B\right)$$

which then becomes 

$$\mathbf{\nabla} \cdot F + \mathbf{\nabla} \wedge F + \frac{\partial}{\partial t}\left(F\right) = \rho - \mathbf{J}$$

Given a timelike bivector $v$ and a general bivector $M$ in $\mathrm{Cl}^{1, 3}(\mathbb{R})$, $v M = v \cdot M + v \wedge M$. Thus, the above equation could be simplified even further to 

$$\mathbf{\nabla} F + \frac{\partial}{\partial t}\left(F\right) = \rho - \mathbf{J}$$

or 

$$\left(\mathbf{\nabla} + \frac{\partial}{\partial t}\right)\left(F\right) = \rho - \mathbf{J}$$

Now, the spacetime current is given by $J = \gamma_0 (\rho - \mathbf{J})$, which is a vector in spacetime. The spacetime vector derivative is related to the relative vector derivative by the following equation:

$$\nabla = \gamma_0 (\mathbf{\nabla} + \frac{\partial}{\partial t})$$

Thus, by left multiplying each side by $\gamma_0$, one gets 

$$\gamma_0 \left(\mathbf{\nabla} + \frac{\partial}{\partial t}\right)\left(F\right) = \gamma_0 (\rho - \mathbf{J})$$

or

$$\nabla F = J$$

where $\nabla$ is the spacetime vector derivative, $F$ is the Faraday bivector, and $J$ is the spacetime current. 

## Related concepts

* [[Hodge-Maxwell theorem]]

* [[Kirchhoff's laws]]

* [[Yang-Mills equations]]

## References

For more see the references at *[[electromagnetism]]*.

### General

Maxwell's equations originate in:

* {#Maxwell1865} [[James Clerk Maxwell]], *A Dynamical Theory of the Electromagnetic Field*, Philosophical Transactions of the Royal Society of London **155** (1865) 459-512 &lbrack;[doi:10.1098/rstl.1865.0008](https://doi.org/10.1098/rstl.1865.0008), [jstor:108892](https://www.jstor.org/stable/108892), [Wikipedia entry](http://en.wikipedia.org/wiki/A_Dynamical_Theory_of_the_Electromagnetic_Field)&rbrack;

* [[James Clerk Maxwell]], *A Treatise on Electricity and Magnetism*, Clarendon Press Series, Macmillan & Co. (1873),  Cambridge University Press (2010) &lbrack;[ark:/13960/t9s17v886](https://archive.org/details/electricandmagne01maxwrich), [doi:10.1017/CBO9780511709333](https://doi.org/10.1017/CBO9780511709333), [pdf](https://www.aproged.pt/biblioteca/MaxwellI.pdf), [Wikipedia entry](https://en.wikipedia.org/wiki/A_Treatise_on_Electricity_and_Magnetism)&rbrack;

Some history and reflection:

* A. C. T. Wu, [[Chen Ning Yang]]: *Evolution of the concept of vector potential in the description of the fundamental interactions*,  International Journal of Modern Physics A **21** 16 (2006) 3235-3277 &lbrack;[doi:10.1142/S0217751X06033143](https://doi.org/10.1142/S0217751X06033143)&rbrack;

* {#Dyson07} [[Freeman J. Dyson]], _Why is Maxwell’s Theory so hard to understand?_, Proceedings of [The Second European Conference on Antennas and Propagation, EuCAP 2007](https://ieeexplore.ieee.org/xpl/mostRecentIssue.jsp?punumber=4446147) ([doi: 10.1049/ic.2007.1146](https://ieeexplore.ieee.org/xpl/mostRecentIssue.jsp?punumber=4446147))

* [[Chen Ning Yang]], *The conceptual origins of Maxwell’s equations and gauge theory*, Phyics Today **67** 11 (2014) &lbrack;[doi:10.1063/PT.3.2585](https://doi.org/10.1063/PT.3.2585), [pdf](http://home.ustc.edu.cn/~lxsphys/2021-3-18/The%20conceptual%20origins%20of%20Maxwell%27s%20equations%20and%20gauge%20theory.pdf)&rbrack;

See also:

* [[Freeman J. Dyson]]: *Feynman's proof of Maxwell's equations*,  American Journal of Physics **58** (1990) 209-211 &lbrack;[pdf](https://physics.csuchico.edu/kagan/435B/problems/FeynmanPaper.pdf), [[DysonOnFeynmanOnMaxwell.pdf:file]]&rbrack;
  > (recounting an observation by [[Richard Feynman]])

  comment by N. Dombey: Am. J. Phys. **59** 1 (1991) 85 &lbrack;[journal](https://pubs.aip.org/aapt/ajp/article-abstract/59/1/85/1053837/Comment-on-Feynman-s-proof-of-the-Maxwell?redirectedFrom=fulltext), [[DombeyOnDysonOnFeynmanOnMaxwell.jpg:file]]&rbrack;

  comment by I. E. Farquhar: Am. J. Phys. **59** 1 (1991) 87 &lbrack;[journal](https://pubs.aip.org/aapt/ajp/article-abstract/59/1/87/1053797/Comment-on-Feynman-s-proof-of-the-Maxwell?redirectedFrom=fulltext), [[FarquharOnDysonOnFeynmanOnMaxwell.jpg:file]]&rbrack;



For Maxwell's equations in the generality of [[dielectric media]], see the references there, such as:

* G. Russakoff, *A Derivation of the Macroscopic Maxwell Equations*, American Journal of Physics **38** (1970) 1188–1195 &lbrack;[doi:10.1119/1.1976000](https://doi.org/10.1119/1.1976000)&rbrack;

* {#deLangeRaab06} O. L. de Lange, R. E. Raab *Surprises in the multipole description of macroscopic electrodynamics*, American Journal of Physics **74** (2006) 301–312 &lbrack;[doi:10.1119/1.2151213](https://doi.org/10.1119/1.2151213)&rbrack;

On the Maxwell [[Green's function]] ([[propagator]]) and numerical solutions:

* Boris Lo, Victor Minden, Phillip Colella, *A real-space Green's function method for the numerical solution of Maxwell's equations*,  **11** 2 (2016) 143–170 &lbrack;[doi:10.2140/camcos.2016.11.143](https://doi.org/10.2140/camcos.2016.11.143), [pdf](https://msp.org/camcos/2016/11-2/camcos-v11-n2-p01-s.pdf)&rbrack;



[[!include electromagnetism in terms of differential forms -- references]]




### Via "geometric algebra: (Clifford algebra)

Formulation of Maxwell's equations via "[[geometric algebra]]":

* {#DoranLasenby03} [[Chris Doran]], Anthony Lasenby: _Geometric algebra for physicists_, Cambridge University Press (2003) ([pdf](http://catdir.loc.gov/catdir/samples/cam033/2002035182.pdf))

* {#Arthur11} John W. Arthur, *Understanding Geometric Algebra for Electromagnetic Theory*, John Wiley & Sons Inc. (2011). (ISBN:978-0470941638, [doi:10.1002/9781118078549](https://doi.org/10.1002/9781118078549))


[[!redirects Maxwell equation]]
[[!redirects Maxwell's equation]]

[[!redirects Maxwell equations]]
[[!redirects Maxwell's equations]]

[[!redirects permittivity of the vacuum]]



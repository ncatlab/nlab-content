+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--

# Sandbox
* table of contents
{: toc}

# Section

# Another section

***

$\twoheadrightarrow$
  


#### Deformation of Algebraic Varieties #### 

Let $X$ be a smooth algebraic variety over a field $\mathbb{k}$ of characteristic $0$. The analogue of the HKR Theorem here is this:

+-- {: .num_theorem #SwYe}
###### Theorem 
**(Swan, [Yekutieli](http://dx.doi.org/10.4153/CJM-2002-051-8)).** 
There is a canonical isomorphism 
\[ \operatorname{Ext}^i_{X^2}(\mathcal{O}_X, \mathcal{O}_X) \cong 
\bigoplus_q \operatorname{H}^{i - q}(X, \bigwedge^q (\mathcal{T}_X)) . \]
=--

Here $\mathcal{T}_X$ is the tangent sheaf of $X$, and $X$ is embedded diagonally in $X^2$. 

This is a consequence of the following result. Let $\mathcal{C}_{cd, X}$ be the sheaf of continuous Hochschild cochains of $X$. It is a bounded below complex of quasi-coherent $\mathcal{O}_X$-modules.

+-- {: .num_theorem #Yek1}
###### Theorem 
**([Yekutieli](http://dx.doi.org/10.4153/CJM-2002-051-8)).** 

1. There is a canonical isomorphism 
\[ \operatorname{R} \mathcal{Hom}_{X^2}(\mathcal{O}_X, \mathcal{O}_X) \cong 
\mathcal{C}_{cd, X} \]
in the derived category of $\mathcal{O}_X$-modules. 

2. There is a canonical quasi-isomorphism of complexes of sheaves 
\[  \bigoplus_q \bigwedge^q (\mathcal{T}_X)[-q] \to \mathcal{C}_{cd, X}  . \] 

3. Therefore there is a  canonical isomorphism 
\[ \operatorname{R} \mathcal{Hom}_{X^2}(\mathcal{O}_X, \mathcal{O}_X) \cong 
\bigoplus_q \bigwedge^q (\mathcal{T}_X)[-q] \]
in the derived category of $\mathcal{O}_X$-modules. 
=--


The relation to deformation quantization is this: $\mathcal{C}_{cd, X}$ is a shift by $1$ of the sheaf of $\mathcal{D}_{poly, X}$ of polydifferential operators (viewed only as a complex of quasi-coherent $\mathcal{O}_X$-modules). Similarly, 
$\bigoplus_q \bigwedge^q (\mathcal{T}_X)[-q]$
is the shift by $1$ of the sheaf $\mathcal{T}_{poly, X}$ of polyvector fields. Thus item 2 in the theorem above says that there is a canonical $\mathcal{O}_X$-linear quasi-isomorphism 
\[ \mathcal{T}_{poly, X} \to \mathcal{D}_{poly, X} . \]
Trying to replicate the global formality theorem of Kontsevich, one would like to upgrade this to an $\mathrm{L}_{\infty}$ quasi-isomorphism. 
However, it seems that in general this cannot be done directly, but only after a suitable resolution. 

Here is our result. (See also [Van den Bergh](http://dx.doi.org/10.1016/j.jalgebra.2007.02.012).) 
Any quasi-coherent sheaf $\mathcal{M}$ on $X$ admits a canonical flasque resolution called the mixed resolution:
\[ \mathcal{M} \to \operatorname{Mix}(\mathcal{M}) . \]
This "mixes" the jet resolution with the Cech resolution (corresponding to an affine open covering of $X$ that we supress). 
In particular we get quasi-isomorphisms of sheaves of DG algebras 
\[ \mathcal{T}_{poly, X} \to \operatorname{Mix}(\mathcal{T}_{poly, X}) \]
and 
\[ \mathcal{D}_{poly, X} \to \operatorname{Mix}(\mathcal{D}_{poly, X}) . \]

+-- {: .num_theorem #Yek2}
###### Theorem 
**([Yekutieli](http://www.math.bgu.ac.il/~amyekut/publications/def-quant/def-quant.html)).** 
There is an  $\mathrm{L}_{\infty}$ quasi-isomorphism
\[ \Psi : \operatorname{Mix}(\mathcal{T}_{poly, X}) \to 
\operatorname{Mix}(\mathcal{D}_{poly, X}) \]
whose $1$-st order term commutes with the HKR quasi-isomorphism above. It is independent on choices up to homotopy. 
=--

A Poisson deformation of $\mathcal{O}_X$ is a sheaf $\mathcal{A}$ of Poisson 
$\mathbb{k}[[\hbar]]$-algebras on $X$, with an isomorphism
$\mathbb{k} \otimes_{\mathbb{k}[[\hbar]]} \mathcal{A} \cong \mathcal{O}_X$
called an augmentation. Likewise an associative deformation of $\mathcal{O}_X$ is a sheaf $\mathcal{A}$ of associative unital (but noncommutative) 
$\mathbb{k}[[\hbar]]$-algebras on $X$, with an augmentation to $\mathcal{O}_X$.

[Theorem 3](#Yek2) implies:

+-- {: .num_theorem #Yek3}
###### Theorem 
**(Yekutieli).** 
Assume that the cohomology groups
$\operatorname{H}^{1}(X, \mathcal{O}_X)$ and 
$\operatorname{H}^{2}(X, \mathcal{O}_X)$ vanish. Then there is a canonical bijection 
\[ \mathrm{quant} : \quad
\frac{ \{ \text{ Poisson deformations of} \; \mathcal{O}_X \} }{\text{isomorphism}} \quad \xrightarrow{\, \simeq \,} \quad 
\frac{ \{ \text{ associative deformations of} \; \mathcal{O}_X \} }{\text{isomorphism}} . \] 
=--

A proof of this theorem when $X$ is affine is 
[here](http://www.math.bgu.ac.il/~amyekut/publications/def-quant/def-quant.html). 
For the full statement see 
[this paper](http://www.math.bgu.ac.il/~amyekut/publications/twisted-defs/twisted-defs.html). 

For twisted (or stacky) deformations there is a corresponding (but much more difficult to state and prove). See the 
[paper](http://www.math.bgu.ac.il/~amyekut/publications/twisted-defs/twisted-defs.html)
and the 
[survey](http://www.math.bgu.ac.il/~amyekut/publications/tw-defs-surv/tw-defs-surv.html).



***

<table markdown="1">
<tr markdown="1"><td markdown="1">*hello* $x_2^3$</td><td>*hello* $x_2^3$</td></tr>
<tr><td markdown="1">*hello* $x_2^3$</td><td>*hello* $x_2^3$</td></tr>
</table>

<table>
<tr markdown="1"><td markdown="1">*hello* $x_2^3$</td><td>*hello* $x_2^3$</td></tr>
<tr><td markdown="1">*hello* $x_2^3$</td><td>*hello* $x_2^3$</td></tr>
</table>

***

$$
  \begin{array}{c}      \cdots &\to& C_3 &\stackrel{\delta}{\to} & C_2      & \stackrel{\delta}{\to} &      C_1 &     \stackrel{\overset{\delta_t}{\to}} {\underset{\delta_s}{\to}} &     C_0     \\
  & & \downarrow & & \downarrow & & \downarrow^{\rlap{\delta_s}} & & \downarrow^{\rlap{=}}     \\
 \cdots &\to&     C_0    &\stackrel{=}{\to}&    C_0    &\stackrel{=}{\to}&    C_0    &\stackrel{=}{\to}&    C_0   \end{array}
$$


*** 

$$\underset{\circlearrowleft}{\bullet} \underset{}{\leftrightarrow} \underset{\circlearrowleft}{\bullet}$$ 


|  | [[type theory]] | [[category theory]] |
|--|--|--|
|  | [[syntax]]                 | [[semantics]] |
|  |  [[natural deduction]]     |  [[universal construction]] |
|  | **[[dependent sum type]]** | **[[dependent sum]]** |

|  | [[type theory]] | [[category theory]] |
|--|--|--|
|  | [[syntax]]                 | [[semantics]] |
|  |  [[natural deduction]]     |  [[universal construction]] | 
|  | **[[dependent sum type]]** | **[[dependent sum]]** |

***
[[?]] [[Grothendieck inequality]] $&lt;>$
***
1. $[\mathcal{I},\mathcal{A}]$ is really just the underlying category with hom-collections given by $A_0(A,B)=V_0(I,\mathcal{A}(A,B))$.
2. $\mathcal{A}(-,-)$ is the fully faithful two-variable hom-functor from $A_0^{op}\times A_0\to V_0$, with $\mathcal{A}(f,g)$ defined as the composite $\mathcal{A}(B,C)\stackrel{l^{-1}r^{-1}}{\to}I\otimes\mathcal{A}(B,C)\otimes I\stackrel{f\otimes id\otimes g}{\to}\mathcal{A}(C,D)\otimes\mathcal{A}(B,C)\otimes\mathcal{A}(A,B)\stackrel{(\circ^{\mathcal{A}})^2}\mathcal{A}(A,D)$ in $V_0$
3. $[\mathcal{I},F]$ is the functor from $A_0$ to $B_0$ underlying the enriched functor $F$. This is defined by letting $Ff$ be the composite $I\stackrel{f}{\to}\mathcal{A}(A,B)\stackrel{F_{A,B}}\mathcal{B}(FA,FB)$ where $F_{A,B}$ is the family of morphisms in $V_0$ defining the enriched functor $F$.
4. The natural transformation $\bar F\colon\cat A(-,-)\to\cat B(F-,F-)$ has for its components exactly the maps $F_{A,B}$ above: i.e. $\bar F_{A,B}=F_{A,B}$.
*
*
category: meta

[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects ??? ????]]
[[!redirects Featured math : Quora]]
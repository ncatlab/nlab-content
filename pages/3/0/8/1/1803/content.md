
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

[[Shahn Majid]] has introduced a notion of __bialgebra cocycles__ which as special cases comprise [[group cohomology|group cocycles]], nonabelian Drinfel'd 2-cocycle and 3-cocycle, abelian [[Lie algebra cohomology]] and so on. 

Besides this case, by "bialgebra cohomology" many authors in the literature mean the abelian cohomology ([[Ext|Ext-groups]]) in certain category of "tetramodules" over a fixed bialgebra, which will be in $n$Lab referred as [[Gerstenhaber-Schack cohomology]]. 

## Definition

Let $(B,\mu,\eta,\Delta,\epsilon)$ be a $k$-[[bialgebra]]. 
Denote $\Delta_i : B^{\otimes n}\to B^{\otimes (n+1)} := \id_B^{\otimes (i-1)}\otimes\Delta\otimes\id_B^{\otimes(n-i+1)}$, for $i = 1,\ldots, n$, and $\Delta_0 := 1_B\otimes \id_B^{\otimes n}$, $\Delta_{n+1} := \id_B^{\otimes n}\otimes 1_B$. Notice that for the compositions $\Delta_i\circ\Delta_j = \Delta_{j+1}\circ\Delta_i$ for $i\leq j$.

Let $\chi$ be an invertible element of $B^{\otimes n}$. We define the __coboundary__ $\partial\chi$ by

$$\partial \chi = (\prod_{i=0}^{i \mathrm{ even}} \Delta_i\chi) (\prod_{i=1}^{i \mathrm{ odd}} \Delta_i \chi^{-1})$$

This formula is symbolically also written as $\partial\chi = (\partial_+\chi)(\partial_-\chi^{-1})$. 

An invertible $\chi\in B^{\otimes n}$ is an __$n$-cocycle__ if $\partial\chi = 1$. The cocycle $\chi$ is __counital__ if
for all $i$, $\epsilon_i\chi=1$ where $\epsilon_i =\id_B^{\otimes i-1}\otimes\epsilon\otimes\id_B^{\otimes n-i}$. 


## Examples

### Low dimensions

$\chi\in H$ is a 1-cocycle iff it is invertible and [[grouplike element|grouplike]] i.e. $\Delta\chi=\chi\otimes\chi$ (in particular it is counital).  A 2-cocycle is an invertible element $\chi\in H^{\otimes 2}$ satisfying

$$
(1\otimes\chi)(id\otimes\Delta)\chi = (\chi\otimes 1)(\Delta\otimes id)\chi,
$$
which is counital if $(\epsilon\otimes id)\chi = (id\otimes\epsilon)\chi = 1$ (in fact it is enough to require one out of these two counitality conditions). Counital 2-cocycle is hence the famous [[Drinfel'd twist]].

The 3-cocycle condition for $\phi\in H^{\otimes 3}$ reads:

$$
(1\otimes\phi)((id\otimes\Delta\otimes id)\phi)(\phi\otimes 1) = ((id\otimes id\otimes\Delta)\phi)((\Delta\otimes id\otimes id)\phi)
$$

A counital 3-cocycle is the famous __Drinfel'd associator__ appearing in CFT and quantum group theory. The coherence for monoidal structures can be twisted with the help of Drinfel'd associator; Hopf algebras reconstructing them appear then as quasi-Hopf algebras where the comultiplication is associative only up to twisting by a 3-cocycle in $H$.  

### For particular Hopf algebras

If $G$ is a finite group and $H=k(G)$ is the 
[[Hopf algebra]] of $k$-valued functions on the group, then we recover the usual notions: e.g. the 2-cocycle is a function $\chi:G\times G\to k$ satisfying the cocycle condition

$$
\chi(b,c)\chi(a,b c) = \chi(a,b)\chi(a b,c)
$$
and the condition for a 3-cocycle $\phi:G\times G\times G\to k$ is 

$$
\phi(b,c,d)\phi(a,b c,d)\phi(a,b,c) = \phi(a,b,c d)\phi(a b,c,d)
$$

$n$-cocycles can be in low dimensions twisted by $(n-1)$-cochains (I think it is in this context not know for hi dimensions), what gives an equivalence relation:

For example, if $\chi\in H\otimes H$ is a counital 2-cocycle, and $\partial\gamma\in H$ a counital coboundary, then

$$ \chi^\gamma =  (\partial_+\gamma)\chi(\partial_-\gamma^{-1})= (\gamma\otimes\gamma)\chi\Delta\gamma^{-1} $$

is another 2-cocycle in $H\otimes H$. In particular, if $\chi = 1$ we obtain that $\partial\gamma$ is a cocycle (that is every 2-coboundary is a cocycle). 

## A dual theory

In addition to cocycles "in" $H$ as above, Majid introduced a dual version -- cocycles on $H$. The usual Lie algebra cohomology $H^n(L,k)$, where $L$ is a $k$-Lie algebra, is a special case of that dual construction. 

Instead of $\Delta_i$ one uses multiplications $\cdot_i$ defined analogously ($\cdot_i$ is the multiplication in $i$-th place for $1\leq i\leq n$ and $\psi\circ\cdot_0 =\epsilon\otimes\psi$, $\psi\circ\cdot_{n+1} = \psi\otimes\epsilon$).
An $n$-cochain on $H$ is a linear functional $\psi:H^{\otimes n}\to k$, invertible in the [[convolution algebra]]. An $n$-cochain $\psi$ on $H$ is a __coboundary__ if
 
$$
\partial\psi = (\prod_{i=0}^{\mathrm{even}}\psi\circ \cdot_i))(\prod_{i=1}^{\mathrm{odd}}\psi^{-1}\circ\cdot_i)
$$

If $\psi\in H$ then this condition reads

$$
(\partial\psi)(a\otimes b) = \sum \psi(b_{(1)})\psi(a_{(1)})\psi^{-1}(a_{(2)}b_{(2)})
$$

and, for $\psi\in H\otimes H$, the condition is

$$
(\partial\psi)(a\otimes b\otimes c) = \sum \psi(b_{(1)}\otimes c_{(1)})\psi(a_{(1)}\otimes b_{(2)}c_{(2)})\psi^{-1}(a_{(2)}\otimes b_{(3)}c_{(3)})\psi^{-1}(a_{(3)}b_{(4)})
$$

If one looks at the [[group algebra]] $kG$ of a finite group then the cocycle conditions above can be obtained by a Hopf algebraic version of the $k$-linear extension of the cocycle conditions for the group cohomology in the form appearing in Schreier's theory of extensions. 

However for all $n$ the Lie algebra cohomology also appears as a special case. 

(to be completed later)

## References

* [[Shahn Majid]], _Cross product quantisation, nonabelian cohomology and twisting of Hopf algebras_, in H.-D. Doebner, V.K. Dobrev, A.G. Ushveridze, eds., Generalized symmetries in Physics. World Sci. (1994) 13-41; ([arXiv:hep.th/9311184](http://front.math.ucdavis.edu/9311.3184))

* [[Shahn Majid]], _Foundations of quantum group theory_, Cambridge UP

[[!redirects bialgebra cocycles]]
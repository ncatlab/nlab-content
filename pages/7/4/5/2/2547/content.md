
#Contents#
* table of contents
{:toc}


## Smash product algebra

### Definition

Given a $k$-[[bialgebra]] $H$, and a left [[Hopf action]] $\triangleright$ of $H$ on a $k$-algebra $A$, one defines the **crossed product algebra** $A\sharp H$ (in [[Hopf algebra]] literature also called the **smash product algebra** or Hopf smash product; distinguish from the rather different [[smash product]] in topology) as the $k$-algebra whose underlying vector space is $A\otimes H$ and the product is given by

$$
(a\otimes h)(a'\otimes h') =
\sum a (h_{(1)}\triangleright a')\otimes h_{(2)}h'.
$$

The idea is that if the bialgebra $H$ is in fact a [[Hopf algebra]] embedded as $1\otimes H\subset A\sharp H$ -- whatever the product in the latter is (but assumed to satisfy $(a\otimes 1)(1\otimes h) = a\otimes h$) -- and if the action is inner within $A\sharp H$, i.e. $h\triangleright a = \sum h_{(1)} a S(h_{(2)})$, then we have

$$
  \sum (h_{(1)}\triangleright a) h_{(2)} = \sum h_{(1)} a S(h_{(2)}) h_{(3)} = \sum h_{(1)} a \epsilon(h_{(2)})= h a
  \,,
$$ 

and hence the formula for the product above is a tautology: $a h a' h' = a(h_{(1)}\triangleright a') h_{(2)} h'$.  

Similarly, given a right Hopf action of $H$ on $A$, one defines the crossed product algebra $H\sharp A$ whose underlying space is $H\otimes A$. The left and right versions are isomorphic if $H$ has an invertible antipode; this extends the correspondence between the left and right actions obtained by composing with the antipode map. 

### Properties

Every smash product algebra of the form $A\sharp H$ is naturally equipped with a [[monomorphism]] $A\mapsto A\sharp 1\hookrightarrow A\sharp H$ of algebras and with a right $H$-coaction $a\otimes h\mapsto a\otimes \Delta(h)\in (A\sharp H)\otimes H$ making $A\sharp H$ into a right $H$-comodule algebra. Map $\gamma: h\mapsto 1\otimes h$, $H\hookrightarrow A\sharp H$ is then a map of right $H$-comodule algebra (where the coaction on $H$ is $\Delta$), and $A\otimes 1\subset A\sharp H$ is the subalgebra of $H$-coinvariants. 

If $H$ is a Hopf algebra, then the homomorphism $\gamma$ is a convolution invertible linear map with convolution inverse $\gamma^{-1}$ defined by $\gamma^{-1}(h)=\gamma(Sh)$ for $h\in H$, where $S$ is the antipode of $H$. Conversely, 

**Proposition** _Let $H$ be a Hopf algebra, $E$ a right $H$-comodule algebra, and $\gamma:H\to E$ a map of right $H$-comodule algebra. Clearly $H$ acts on $E^{co H}$ by $h\triangleright a = \sum \gamma(h_{(1)}) a\gamma(Sh_{(2)})$ for $a\in E^{co H}$ and $h\in H$, where the product on the right-hand side is in $E$. Conclusion: 
$E\cong E^{co H}\sharp H$ where the smash product is with respect to that action.

## Cocycled crossed product

There is also a more general cocycled crossed product. For a bialgebra $H$ and an algebra $U$, if we consider the category $C(U,H)$ of extensions $U\hookrightarrow E$ which are compatibly left $U$-modules and right $H$-comodules, and where $U=E^{\mathrm{co}H}$, then the crossed product algebras are the canonical representatives of [[cleft Hopf-Galois extension]]s  which are a more invariant concept.

Let $U$ be an algebra, $H$ a Hopf algebra, $\triangleright : H\otimes U\to U$ a [[measuring]], i.e. a $k$-linear map satisfying $h\triangleright(u v)=\sum (h_{(1)}\triangleright u)(h_{(2)}\triangleright v)$ for all $h\in H$, $u,v\in U$, and which we assume unital, i.e. $h\triangleright 1 = \epsilon(h)1$ for all $h\in H$. We do _not_ assume that $\triangleright$ is an action. 

Let further a (convolution) *invertible*  $k$-linear map $\sigma \in Hom_k(H\otimes H,U)$ be given. For readability in longer calculations, one usually writes $\sigma(h,k)$ rather than $\sigma(h\otimes k)$.

We say that $\sigma$ is a **2-cocycle** (relative to the measuring $\triangleright$) if the following two cocycle identities hold

$$
h\triangleright (k\triangleright u) = \sum \sigma(h_{(1)},k_{(1)})
((h_{(2)}k_{(2)})\triangleright u) \sigma^{-1}(h_{(3)},k_{(3)})
$$

$$
\sum [h_{(1)}\triangleright\sigma(k_{(1)},m_{(1)})]\sigma(h_{(2)},k_{(2)}m_{(2)})=\sum \sigma(h_{(1)},k_{(1)})\sigma(h_{(2)}k_{(2)},m)
\,.
$$
The 2-cocycle $\sigma$ is normalized if $\sigma(h,1) =
\epsilon(h)1 = \sigma(1,h)$.

These identities clearly generalize the classical [[factor system]]s in group theory (linearly extended to the case of group algebras, for the finite groups at least). Therefore it is an  example of a nonabelian cocycle in Hopf algebra theory. However, its role in the general theory is less well understood than the group case. 

Define the **cocycled crossed product** on $U\otimes H$ by

$$
(u \sharp h)(v\sharp k) = \sum u (h_{(1)}\triangleright v)
\sigma(h_{(2)},k_{(1)})\sharp h_{(3)} k_{(2)}
$$

for all $h,k\in H$, $u,v\in U$. The cocycled crossed product is an associative algebra iff $\sigma$ is a cocycle. 

If so, we call $U\sharp_\sigma H$ **cocycled crossed product algebra**. Map $1\otimes\Delta_H:U\sharp_\sigma H\to (U\sharp_\sigma H)\otimes H$ is a right $H$-coaction, making $U\sharp_\sigma H$ into a right $H$-comodule algebra, which is cleft extensions]] are always isomorphic (as $H$-extensions) to the cocycled crossed product algebras. 

If $\sigma(h,k)=\epsilon(h)\epsilon(k)1_U$ then we say that $\sigma$ is a trivial cocycle and then the compatibility conditions above reduce to demanding that the measuring $\triangleright$ is an action. The cocycled crossed product then reduces to the usual smash product algebra.  

**Theorem.** Suppose we are given two measurings $\triangleright,\triangleright':H\otimes U\to A$ with normalized cocycles $\sigma, \tau$ respectively. Then there exists an isomorphism of $H$-extensions of $U$, $i: U\sharp_\sigma H\cong U\sharp_\tau H$ (i.e. an isomorphism of $k$-algebras, left $U$-modules and right $H$-comodules) iff there is an invertible element $f\in Hom_k(H,U)$ such that for all $u\in U$, $h,k\in H$

$$h\triangleright' u = \sum f^{-1}(h_{(1)})(h_{(2)}\triangleright u) f(h_{(3)}),$$

$$\tau(h,k) = \sum f^{-1}(h_{(1)})[h_{(2)}\triangleright f^{-1}(k_{(1)})]\sigma(h_{(3)},k_{(2)})f(h_{(4)}k_{(3)}).$$

The isomorphism $i$ is then given by
$$i(u\sharp_\sigma h) = \sum u f(h_{(1)})\sharp_\tau h_{(2)}$$

## Literature

Related $n$Lab entres include [[cleft extension]], [[crossed product C*-algebra]], [[noncommutative torsor]], [[Hopf-Galois extension]]

* Y. Doi, M. Takeuchi, _Cleft comodule algebras for a bialgebra_, Comm. Alg. __14__ (1986) 801--818
* Y. Doi, _Equivalent crossed products for a Hopf
algebra_, Comm. Alg. __17__ (1989), 3053--3085, [MR91k:16027](http://www.ams.org/mathscinet-getitem?mr=1030610), [doi](ttp://dx.doi.org/10.1080/00927878908823895)

* S. Montgomery, _Hopf algebras and their actions on
rings_, CBMS Regional Conference Series in Mathematics __82__, AMS 1993.
* S. Majid, _Foundations of quantum group theory_, Cambridge University Press 1995.

category: algebra, noncommutative geometry

[[!redirects crossed product algebras]]
[[!redirects Hopf smash product]]
[[!redirects smash product algebra]]
[[!redirects cleft extension]]
[[!redirects cleft Hopf-Galois extension]]
[[!redirects cleft comodule algebra]]
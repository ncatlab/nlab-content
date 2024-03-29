
+-- {: .standout}
rough notes from a talk by [[Bruno Vallette]] -- **raw material** to be polished

see also [[framed little 2-disk operad]] 

=--

#Contents#
* automatic table of contents goes here
{:toc}

## Homotopy theory for $A_\infty$-algebras

**[[homotopy theory]] for $A_\infty$-[[A-infinity algebra|algebras]]**


for $V$ a complex with the structure of an $A_\infty$-[[A-infinity algebra|algebra]] and for $V \to W$ a morphism of chain cmoplexes, we get an induced $A_\infty$-structure on $W$.

Application: for $V$ a [[differential graded algebra]] its [[chain homology and cohomology|chain cohomology]] inherits the structure of an $A_\infty$-[[A-infinity algebra|algebra]]. The product operations are the [[Massey product]]s.

+-- {: .un_theorem}
###### Theorem (Getzler--Jones, Hinich, Berger--Moerdijk, Spitzweck)
There is a [[cofibrantly generated model category|cofibrantly generated]] [[model category]] structure on the [[category]] of differential graded [[operad]]s (operads in the monoidal cateory of [[chain complex]]es or [[cochain complex]]es).
=--

+-- {: .un_prop}
###### Proposition
If $P_\infty$ is a cofibrant dg-operad, then under some assumptions $P_\infty$-[[algebra for an operad]] structures are preserved by weak equivalences.
=--

+-- {: .un_defn}
###### Definition
A quasi-free dg-operad is one that is free after forgetting the differential
=--

+-- {: .un_prop}
###### Proposition
Cofibrant operads are the retracts of quasi-free operads.
=--

In particular quasi-free operads are cofibrant.

So we look for quasi-free resolutions.



+-- {: .un_defn}
###### Definition
Gerstenhaber algebra: essentially a [[Poisson algebra]] in the dg context.
=--

+-- {: .un_remark}
###### Question
How to define a Gerstenhaber algebra up to homotopy?
=--

Extend the operations dfined by Gerstenhaber on $CH(A,A)$ whjich induce the Gerstenhaber algebra on $HH(A,A)$ to a **Gerstenhaber algebra up to homotopy**.

So we have a strict structure on Hochschild homology $HH(A,A)$ and are asking for from which homotopy structure it may come on Hochschild chains in $CH(A,A)$.

So we define the [[Gerstenhaber algebra operad]] whose [[algebra for an operad]] are [[Gertsenhaber algebra]]s.

It is generated of course from the product operation and the bracket operation modulo the associativity constraint for the product, the Jacobi identity for the bracket and the Leibnitz property for their interaction.

These relations are always encoded in _quadratic_ expressions. 


### Koszul duality theory for operads 

the dual notion of [[operad]] is that of [[cooperad]] (reverse all arrows)

+-- {: .un_theorem}
###### Theorem (Ginzburg--Kapranov, Getzler--Jones)

There exist [[adjoint functors]]

$$
  B : \{dg operads\} \leftrightarrow \{dg cooperads\} : \Omega
$$

given by [[bar and cobar construction]]

under this equivalence

$$
  quadratic operad P \stackrel{Koszul duality}{\to}
  cooperad P'
$$

with $P_\infty := \Omega P' \to P$ morphism of [[dg-operad]]s.
=--

+-- {: .un_defn}
###### Definition (Koszul operad)

$P$ is Koszul if $P_\infty = \Omega P' \stackrel{\simeq}{\to} P$ is a quasi-isomorphism, i.e. a cofibrant replacement.
=--

+-- {: .un_prop}
###### Proposition (Ginzburg--Kapranov, Getzler--Jones)

If $P = F(V)/(R)$ be a quadratic operad with $dim(V) \lt + \infty$ The _linear dual_ $P'^*$ is a quadratic operad aabd the suspension of $P'^* \simeq ' := F(V^* \otimes sgn)/(R^{\perp})$.
=--

+-- {: .proof}
###### Method

Compute $P'$ and its operadic structure with this formula, then dualize everything to get this formula.
=--

+-- {: .un_prop}
###### Proposition (Getzler--Jones, Markl)
The Gerstenhaber operad $G$ is Koszul.
=--


### Homotopy Gerstenhaber or $G_\infty$-algebras

$$
  G = G' = Com \circ Lie^1
$$

+-- {: .un_defn}
###### Definition (Batalin--Vilkovisky algebra)

This is a [[Gerstenhaber algebra]] $A$ with a unary operator $\Delta : A \to A$ of degree +1 such that 

* $\Delta^2 = 0 $

* $[-,-]$ measures failure of $\Delta$ to be a derivation with respect to the product $\cdot$.
=--

This also is the algebra over an operad. But this operad is no longer a [[quadratic operad]].

So we define:

+-- {: .un_defn}
###### Definition (quadratic BV-algebra)

As above but now demand $\Delta$ a derivation of both the product $\cdot$ and the bracket $[-,-]$.
=--

This is a first step in the resolution process.

Now the corresponding operad is Koszul. So we get

$$
  \Rightarrow qBV_\infty := \Omega q BV' \stackrel{\simeq}{\to}
$$

as a quasi-free resolution.

+-- {: .un_defn}
###### Definition-proposition** A homotopy BV-algebra is an [[algebra over an operad]] for that.

In terms of this we have a homotopy BV-algebra structure on $CH(A,A)$.
=--

+-- {: .un_remark}
###### Idea
Add a suitable differential $d_1 : qBV' \to qBV'$.
=--


### Koszul duality theory 

Let $P = F(V)/(R)$ be a quadratic and linear presentation of a dg-operad

let $q : F(V) \to F(V)^{(2)}$ the quadratic projection

and $qP := F(V)/(qR)$ the quadratic analogue of $P$

+-- {: .un_defn}
###### Definition (quadratic-linear Koszul operad)

$P = F(V)/(R)$ is a Koszul operad if

* $R \cap V = \{0\} \Leftrightarrow V is minimal$

* (more ...)

* $q P$ is Koszul
=--

This now yields a good machinery for cofibrant resolutions for Koszul operads.

+-- {: .un_theorem}
###### Theorem

When $P$ is a quadratic linear Koszul operad then 

$$
  P_\infty := \Omega P' \stackrel{\simeq}{\to} P
$$
=--

+-- {: .un_theorem}
###### Theorem

This applies to the BV operad.
=--

+-- {: .un_defn}
###### Definition
A **$BV_\infty$-algebra** is an algebra over this cofibrant replacement for the BV operad.
=--


### Applications

+-- {: .un_theorem}
###### Theorem (Ginzburg, Tradler, Menichi)

* $A$ a [[Frobenius algebra]].

* Its [[Hochschild cohomology]] $HH(A,A)$ is a [[BV-algebra]].
=--

+-- {: .un_theorem}
###### Theorem (Cyclic Deligne conjecture)

...
=--


### Comparison to other definitions 

Another definition of homotopy BV-algebra by Kravchenko -- this turns out to be a special case of the definition here by setting some operations to $0$ (her algebra is not an algebra over a cofibrant operad).

Another definition by Tamarkin--Tsygan: this is more general than the one here. TT have many more operations, namely operations with sevearl outputs.

The notion here also difers from that in Beilinson--Drinfeld.


### PBW isomorphism 

The free operad $F(V)$ is filtered $\Rightarrow P = F(V)/(R)$ is filtered. There is then a morphism of operads $q P \to gr P$.

+-- {: .un_theorem}
###### Theorem
For $P$ Koszul we have

$$
  q P \simeq gr P
$$

For instance

$$
  q BV \simeq gr P
$$
=--


### Relation with framed little disks 

Let $dD$ be the [[framed little disk operad]]; then:

Getzler: $H_\bullet(fD) \simeq BV$.

+-- {: .un_theorem}
###### Theorem (Gianciracusa--Salvatore--Severa)

$fD$ is formal, i.e. quasi-isomorphic by zig-zags to its homology
=--


### Relation with TCFT 

A [[topological conformal field theory]] is an algebra over the [[PROP]] $C_\bullet(\mathcal{R})$ of [[Riemann surface]]s.

+-- {: .un_theorem}
###### Theorem
Any [[TCFT]] carries a homotopy BV-algebra structure which lifts the [[BV-algebra]] structure of Getzler in its [[homology]].
=--


### Homotopy theory for $P_\infty$ algebras 


### Deformation theory 

+-- {: .un_prop}
###### Proposition

In some sense homotopy BV is a formal extension of homotopy Gerstenhaber.
=--

+-- {: .un_theorem}
###### Theorem (generalized Lian--Zuckermann conjecture)

For any [[topological vertex algebra]] $A$ with $\mathbb{N}$-graded conformal weight there exists an expliciit $BV_\infty$-algebra structure on $A$ which extends Lian--Zuckermann operations on $A$ and which lifts the [[BV-algebra]] structure on $H(A)$.
=--

## Related entries

* [[quantum L-infinity algebra]]

## References

The above material probably roughly follows the talk slides

* [[Bruno Vallette]], _Homotopy Batalin-Vilkovisky algebras_ , [slides](https://www.math.univ-paris13.fr/~vallette/download/Homotopy%20BV.pdf))

The corresponding article is

* [[Imma Galvez-Carrillo]], [[Andy Tonks]], [[Bruno Vallette]], _Homotopy Batalin-Vilkovisky algebras_ ([arXiv:0907.2246](http://arxiv.org/abs/0907.2246))

See also 

* Imma G&#225;lvez, Vassily Gorbounov, Andrew Tonks, _Homotopy Gerstenhaber structures and vertex algebras_, [math/0611231.QA](http://arxiv.org/abs/math/0611231)

[[!redirects homotopy BV algebra]]
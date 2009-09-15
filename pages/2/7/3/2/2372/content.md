
> rough notes from a talk for the moment -- **raw material** to be polished 

[[homotopy theory]] for [[A-infinity algebra]]s


for $V$ a complex with the structure of an [[A-infinity algebra]] and for $V \to W$ a morphism of chain cmoplexes, we get an induced $A_\infty$-structure on $W$.

Application: for $V$ a [[differential graded algebra]] its [[chain homology and cohomology|chain cohomology]] inherits the structure of an [[A-infinity algebra]]. The product operations are the [[Massey product]]s.

**Theorem** (Getzler-Jones, Hinich, Berger-Moerdijk, Spitzweck)
There is a [[cofibrantly generated model category|cofibrantly generated]] [[model category]] structure on the [[category]] of differential graded [[operad]]s (operads in the monoidal cateory of [[chain complex]]es or [[cochain complex]]es).

**Proposition** if $P_\infty$ is a cofibrant dg-operad, then under some assumptions $P_\infty$-[[algebra for an operad]] structures are preserved by weak equivalences.

**Definition** A quasi-free dg operad is one that is free after forgetting the differential

**proposition** cofibrant operads are the retracts of quasi-free operads.

in particular quasi-free operads are cofibrant

so we look for quasi-free resolutions



**definition** Gerstenhaber algebra: essentially a [[Poisson algebra]] in the dg-context.

**Question**: how to define a Gerstenhaber algebra up to homotopy?

extend the operations dfined by Gerstenhaber on $CH(A,A)$ whjich induce the erstenhaber algebra on $HH(A,A)$ to a **Gerstenhaber algebra up to homotopy**.

So we have s trict structure on Hchschild homology $HH(A,A)$ and are asking for from which homotopy-structure it may come on Hochschild chains in $CH(A,A)$.

So we define the [[Gerstenhaber algebra operad]] whose [[algebra for an operad]] are [[Gertsenhaber algebra]]s

it is generated of course from the product operation and the bracket operation modulo the associativity constraint for the product, the Jacobi identity for the bracket and the Leibnitz property for their interaction

these relations are always encoded in _quadratic_ expressions. 

## Koszul duality theory for operads ##

the dual notion of [[operad]] is that of [[cooperad]] (reverse all arrows)

**Theorem* (Ginzburg-Kapranov, Getzler-Jones)

there exist [[adjoint functor]]s

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

**Definition** Koszul operad

$P$ is Koszul if $P_\infty = \Omega P' \stackrel{\simeq}{\to} P$ is a quasi-isomorphism, i.e. a cofibrant replacement

**proposition** (Ginzburg-Kapranov, Getzler-Jones)

if $P = F(V)/(R)$ be a quadratic operad with $dim(V) \lt + \infty$ The _linear dual_ $P'^*$ is a quadratic operad aabd the suspension of $P'^* \simeq ' := F(V^* \otimes sgn)/(R^{\perp})$

**methof** compute $P'$ and its operadic structure with this formula, then dualize everything to get this formula

**proposition** (Getzler-Jones, Markl) the Gerstenhaber operad $G$ is Koszul

**homotopy Gerstenhaber or $G_\infty$-algebras**

$$
  G = G' = Com \circ Lie^1
$$

**Definition** (Batalin-Vilkovisky algebra)

This is a [[Gerstenhaber algebra]] $A$ with a unary operator $\Delta : A \to A$ of degree +1 such that 

* $\Delta^2 = 0 $

* $[-,-]$ measures failure of $\Delta$ to be a derivation with respect to the product $\cdot$.

This also is the algebra over an operad. But this operad is no longer a [[quadratic operad]].

So we define

**definition** **quadratic BV-algebra**

as above but now demand $\Delta$ a derivation of both the product $\cdot$ and the bracket $[-,-]$.

This is a first step in the resolution process.

Now the corresponding operad is Koszul. So we get

$$
  \Rightarrow qBV_\infty := \Omega q BV' \stackrel{\simeq}{\to}
$$

a quasi-free resolution

**definition-proposition** homotopy BV algebra is [[algebra over an operad]] for that

in terms of this we have a homotopy BV algebra structure on $CH(A,A)$.

**idea** add a suitable differential $d_1 : qBV' \to qBV'$

## Koszul duality theory ##

Let $P = F(V)/(R)$ be a quadratic and linear presentation of a dg-operad

let $q : F(V) \to F(V)^{(2)}$ the quadratic projection

and $qP := F(V)/(qR)$ the quadratic analogue of $P$

**definintion** quadratic-linear Koszul operad:

$P = F(V)/(R)$ is a Koszul operad if

* $R \cap V = \{0\} \Leftrightarrow V is minimal$

* ...

* $q P$ is Koszul

this now yields a good machinery for cofibrant resolutions for Koszul operads

**theorem**

When $P$ is a quadratic linear Koszul operad then 

$$
  P_\infty := \Omega P' \stackrel{\simeq}{\to} P
$$

**theorem**

this applies to the BV-operad

**definition** a **$BV_\infty$-algebra** is an algebra over this cofibrant replacement for the BV-operad.

**applications** 

**theorem** (Ginzburg, Tradler, Menichi)

* $A$ a [[Frobenius algebra]]

* its [[Hochschild cohomology]] $HH(A,A)$ is a [[BV-algebra]]

**theorem** (Cyclic Dligne conjecture)

## comparison to other definitions ##

another definition of homotopy BV algebra by Kravchenko -- this turns out to be a specialcase of the definition here by setting some operations to 0 (her algebra is not an algebra over a cofibrant operad)

another definition by Tamarkin-Tsygan: this is more general than the one here. TT have many more operations, namely operations with sevearl outputs.

the notion here also difers from that in Beilinson-Drinfeld

## PBW isomorphism ##

the free operad $F(V)$ is filtered $\Rightarrow P = F(V)/(R)$ is filtered. There is then a morphism of operads $q P \to gr P$


**theorem** for $P$ Koszul we have

$$
  q P \simeq gr P
$$

for instance

$$
  q BV \simeq gr P
$$

## relation with framed little disks ##

let $dD$ be the [[framed little disk operad]] then

Getzler: $H_\bullet(fD) \simeq BV$

**theorem** (Gianciracusa-Salvatore-Severa )

$fD$ is formal, i.e. quasi-isomorphic by zig-zags to its homology

## relation with TCFT ##

a [[topological conformal field theory]] is an algebra over the [[PROP]] $C_\bullet(\mathcal{R})$ of [[Riemann surface]]s

**theorem* any [[TCFT]] carries a homotopy BV-algebra structure which lifts the [[BV-algebra]] structure of Getzler in its [[homology]]

## homotopy theory for $P_\infty$ algebras ##

## deformation theory ##

**proposition**


* in some sense homotopy BV is a formal extension of homotopy Gerstenhaber


**theorem**  generalized Lian-Zuckermann conjecture

For any [[topological vertex algebra]] $A$ with $\mathbb{N}$-graded conformal weight there exists an expliciit $BV_\infty$-algebra structure on $A$ which extends Lian-Zuckermann operations on $A$ and which lifts the [[BV-algebra]] structure on $H(A)$


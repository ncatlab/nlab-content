
> This article is about of groups of Witt vectors and rings of Witt vectors; which are often called just Witt groups and Witt rings. However, there is also a different notion of [[Witt group]] and [[Witt ring]].  


#Contents#
* table of contents
{:toc}




## Idea

Rings of _Witt vectors_ are the [[co-free functor|co-free]] [[Lambda-rings]]. Depending on whether one defines the latter via Frobenius lifts at a single [[prime number]] $p$ one speaks of _$p$-typical Witt vectors_, or of _big Witt vectors_ if all primes are considered at once.

In [[arithmetic geometry]] the impact of rings of Witt vectors $W(R)$ of a given ring $R$ is that they are like rings [[formal power series]] on $Spec(R)$, such as rings of [[p-adic numbers]]. For more on this see at _[[arithmetic jet space]]_ and at _[[Borger's absolute geometry]]_.

In components, a _Witt vector_ is an infinite sequence of elements of a given [[commutative ring]] $k$. There is a [[ring]] structure on the set $W(k)$ of Witt vectors of $k$ and $W(k)$ is therefore called *the Witt ring of $k$*. The multiplication is defined by means of [[Witt polynomials]] $w_i$ for every [[natural number]] $i$. If the [[characteristic]] of $k$ is $0$ the Witt ring of $k$ is sometimes called *universal Witt ring* to distinguish it from the case where $k$ is of prime characteristic and a similar but different construction is of interest.

A [[Witt vector|p-adic Witt vector]] is an infinite sequence of elements af a commutative ring of [[prime]] [[characteristic]] $p$. There exists a ring structure whose construction parallels that in characteristic $0$ except that only [[Witt polynomials]]  $w_{p^l}$ whose index is a power of $p$ are taken.

More abstractly, the ring of Witt vectors carries the structure of a [[Lambda-ring]] and the construction $W \colon k\mapsto W(k)$ of the Witt ring $W(k)$ on a [[commutative ring]] $k$ is [[right adjoint]] to the [[forgetful functor]] from [[Lambda-rings]] to [[commutative rings]]. Hence rings of Witt vectors are the _[[co-free functor|co-free]] [[Lambda-rings]]_.

Moreover $W(-)$ is [[representable functor|representable]] by ring of [[symmetric function|symmetric functions]], $\Lambda$.   The reason is that $\Lambda$ is the free Lambda-ring on the commutative ring $\mathbb{Z}$.   Since $\Lambda$ is a [[Hopf algebra]], $W$ is a [[group scheme]]. This is explained at [[Lambda-ring]].

The construction of Witt vectors gives a functorial way to lift a commutative ring $A$ of [[prime]] [[characteristic]] $p$ to a commutative ring $W(A)$ of [[characteristic]] 0. Since this construction is functorial, it can be applied to the [[structure sheaf]] of an [[algebraic variety]].
In interesting special cases the resulting ring $W(A)$ has even more desirable properties: If $A$ is a [[perfect field]] then $W(A)$ is a [[discrete-valuation ring|discrete valuation]]. This is partly due to the fact that the construction of $W(A)$ involves a ring of [[power series]] and a ring of power series over a field is always a discrete valuation ring.

There is a generalization, $W_G$, to any profinite group, $G$, due to Dress and Siebeneicher ([DS88](#DS88)), known as [[Witt-Burnside functors|Witt-Burnside functor]].

There is a generalization to [[non-commutative Witt vectors]], however these only carry a group- but no ring structure.

The [[Lubin-Tate ring]] in [[Lubin-Tate theory]] is a [[polynomial ring]] on a ring of Witt vectors and this way Witt vectors control much of [[chromatic homotopy theory]].

## Motivation

In an *expansion* of a $p$-adic number $a=\Sigma a_i p^i$ the $a^i$ are called *digits*. Usually these digits are defined to be taken elements of the set $\{0,1,\dots,p-1\}$.

Equivalently the digits can be defined to be taken from the set $T_p:=\{x|x^{p-1}=1\}\cup \{0\}$. Elements from this set are called *Teichm&#252;ller digits* or *Teichm&#252;ller representatives*.

The set $T$ is in bijection with the [[finite field]] $F_p$. The set $W(F_p)$ of (countably) infinite sequences of elements in $F_p$ hence is in bijection to the set $\mathbb{Z}_p$ of $p$-adic integers. There is a ring structure on $W(F_p)$ called *Witt ring structure* such that all ''truncated expansion polynomials'' $\Phi_n=X^{p^n}+pX^{p^{n-1}}+p^2X^{p^{n-2}}+\dots +p^n X$ called *Witt polynomials* are morphisms

$$\Phi_n:W(F_p)\to \mathbb{Z}_p$$

of groups.



## Definition
 {#Definituion}

We first give the

* [Explicit definition in components](#DefinitionInComponents)

and then discuss the

* [Universal characterization](DefinitionUniversalCharacterization)

### In components
 {#DefinitionInComponents}

#### The ring structure

+-- {: .num_defn}
###### Definition

Let $k$ be a [[commutative ring]].

If the [[characteristic]] of $k$ is $0$ then the Witt ring $W(k)$ of $k$ is defined defined by the addition

$$(a_1, a_2, \ldots, )+(b_1, b_2, \ldots) :=(\Sigma_1(a_1,b_1), \Sigma_2(a_1,a_2,b_1,b_2), \ldots)$$

and the multiplication

$$(a_1, a_2, \ldots )\cdot (b_1, b_2, \ldots ) :=(\Pi_1(a_1,b_1), \Pi_2(a_1,a_2,b_1,b_2), \ldots )$$

If $k$ is of prime characteristic $p$ we index the defining formulas by $p^1,p^2,p^3,\dots$ instead of $1,2,3,\dots$.

Here the $\Sigma_i$  are called *addition polynomials* and the $\Pi_i$  are called *multiplication polynomials*, these are described [below](#AdditionAndMultiplicationPolynomials).

=--


#### The Witt polynomials{#Witt polynomials}, the $\Sigma_i$, the $\Pi_i$, phantom components

let $x_1, x_2, \ldots $ be a collection of [[variables]]. We can define an infinite collection of [[polynomial]]s in $\mathbb{Z}[x_1, x_2, \ldots ]$ using the following formulas:

$w_1(X)=x_1$

$w_2(X)=x_1^2+2x_2$

$w_3(X)=x_1^3+3x_3$

$w_4(X)=x_1^4+2x_2^2+4x_4$

and in general $\displaystyle w_n(X)=\sum_{d|n} dx_d^{n/d}$. The value $w_n(w)$ of the $n$-th Witt polynomial in some element $w\in W(k)$ of the Witt ring of $k$ is sometimes called the *$n$-th phantom component of $w$* or *the $n$-th ghost component of $w$.


Now let $\phi(z_1, z_2)\in\mathbb{Z}[z_1, z_2]$. This just an arbitrary two variable polynomial with coefficients in $\mathbb{Z}$. 

We can define new polynomials $\Phi_i(x_1, \ldots x_i, y_1, \ldots y_i)$ such that the following condition is met $\phi(w_n(x_1, \ldots ,x_n), w_n(y_1, \ldots , y_n))=w_n(\Phi_1(x_1, y_1), \ldots , \Phi_n(x_1, \ldots x_n, y_1, \ldots , y_n))$.

In short we'll notate this $\phi(w_n(X),w_n(Y))=w_n(\Phi(X,Y))$. The first thing we need to do is make sure that such polynomials exist. Now it isn't hard to check that the $x_i$ can be written as a $\mathbb{Q}$-linear combination of the $w_n$ just by some linear algebra.

$x_1=w_1$, and $x_2=\frac{1}{2}w_2+\frac{1}{2}w_1^2$, etc. so we can plug these in to get the existence of such polynomials with coefficients in $\mathbb{Q}$. It is a fairly tedious lemma to prove that the coefficients $\Phi_i$ are actually in $\mathbb{Z}$, so we won't detract from the construction right now to prove it.

#### The addition- and multiplication polynomials
 {#AdditionAndMultiplicationPolynomials}


Define yet another set of polynomials $\Sigma_i$, $\Pi_i$ and $\iota_i$ by the following properties:

$w_n(\Sigma)=w_n(X)+w_n(Y)$, $w_n(\Pi)=w_n(X)w_n(Y)$ and $w_n(\iota)=-w_n(X)$.

We now can construct $W(A)$, the ring of generalized Witt vectors over $A$. Define $W(A)$ to be the set of all infinite sequences $(a_1, a_2, \ldots)$ with entries in $A$. Then we define addition and multiplication by $(a_1, a_2, \ldots, )+(b_1, b_2, \ldots)=(\Sigma_1(a_1,b_1), \Sigma_2(a_1,a_2,b_1,b_2), \ldots)$ and $(a_1, a_2, \ldots )\cdot (b_1, b_2, \ldots )=(\Pi_1(a_1,b_1), \Pi_2(a_1,a_2,b_1,b_2), \ldots )$.


### Universal characterization
 {#DefinitionUniversalCharacterization}


+-- {: .num_theorem}
###### Theorem

The assignment 

$$
  W
  \;\colon\;
  k\mapsto W(k)
$$ 

is a [[functor]]

$$
  W \;\colon\; CRing \longrightarrow \Lambda Ring
$$


from the [[category]] of [[commutative rings]] to that of [[Lambda-rings]].


Composed with the [[forgetful functor]] 

$$
  U \;\colon\;
  \Lambda Ring \longrightarrow CRing
$$

this is the unique [[endofunctor]] $W \;\colon\; CRing \longrightarrow CRing$ such that all [[Witt polynomials]]

$$
  w_n
  :
  \begin{cases}
    W(A)\to A
   \\
    a\mapsto w_n(a)
  \end{cases}
$$

are [[homomorphisms]] of [[rings]]. 

=--

+-- {: .proof}
###### Proof

There is a nice trick to prove that $W(A)$ is a ring when $A$ is a $\mathbb{Q}$-algebra. Just define $\psi: W(A)\to A^\mathbb{N}$ by $(a_1, a_2, \ldots) \mapsto (w_1(a), w_2(a), \ldots)$. This is a [[bijection]] and the addition and multiplication is taken to component-wise addition and multiplication, so since this is the standard ring structure we know $W(A)$ is a ring. Also, $w(0,0,\ldots)=(0,0,\ldots)$, so $(0,0,\ldots)$ is the additive identity, $W(1,0,0,\ldots)=(1,1,1,\ldots)$ which shows $(1,0,0,\ldots)$ is the multiplicative identity, and $w(\iota_1(a), \iota_2(a), \ldots)=(-a_1, -a_2, \ldots)$, so we see $(\iota_1(a), \iota_2(a), \ldots)$ is the additive inverse.

We can actually get this idea to work for any characteristic $0$ ring by considering the embedding $A\to A\otimes\mathbb{Q}$. We have an induced injective map $W(A)\to W(A\otimes\mathbb{Q})$. The addition and multiplication is defined by polynomials over $\mathbb{Z}$, so these operations are preserved upon tensoring with $\mathbb{Q}$. We just proved above that $W(A\otimes\mathbb{Q})$ is a ring, so since $(0,0,\ldots)\mapsto (0,0,\ldots)$ and $(1,0,0,\ldots)\mapsto (1,0,0,\ldots)$ and the map preserves inverses we get that the image of the embedding $W(A)\to W(A\otimes \mathbb{Q})$ is a subring and hence $W(A)$ is a ring.

Lastly, we need to prove this for positive [[characteristic]] rings. Choose a characteristic $0$ ring that surjects onto $A$, say $B\to A$. Then since the induced map again preserves everything and $W(B)\to W(A)$ is [[surjective]], the image is a ring and hence $W(A)$ is a ring. 

=--

+-- {: .num_prop}
###### Proposition

The construction of the ring of Witt vectors $W(k)$ on a given [[commutative ring]] $k$ is the [[right adjoint]] to the [[forgetful functor]] $U$ from [[Lambda-rings]] to [[commutative rings]]

$$
  (U \dashv W)
  \;\colon\;
  CRing
  \stackrel{\overset{U}{\leftarrow}}{\underset{W}{\longrightarrow}}
  \Lambda Ring
  \,.
$$

Hence rings of Witt-vectors are the _[[co-free functors|co-free]] [[Lambda-rings]]_.

=--

This statement appears in ([Hazewinkel 08, p. 87, p. 97](#Hazewinkel08)). 

+-- {: .num_remark}
###### Remark

On the other hand, the [[free construction|free]] [[Lambda-ring]] (on one generator) (hence the [[left adjoint]] construction to the [[forgetful functor]]) is the ring of [[symmetric functions]].

=--

This statement appears in ([Hazewinkel 08, p. 98](#Hazewinkel08)). 



## Properties

### Operations on the p-adic Witt vectors

On untruncated $p$-adic Witt vectors there are two operations, the [[Frobenius morphism]] and the [[Verschiebung morphism]] satisfying relations ([Lemma 1](#FVrelations)) being constitutive for the definition of the [[Dieudonné ring]]: In fact the Dieudonn&#233; ring is generated by two objects satisfying these relations.

Also the $n$-truncations of a Witt ring are rings since by definition the ring operations (addition and multiplication) of the first $n$ components only involve the first $n$ components. We have $W\simeq lim_n W_n$ and the projection map $W(A)\to W_n(A)$ is a [[ring homomorphism]]. We also have operations on the truncated Witt rings.

#### The shift map

For $W(k)$ as for every $k$-scheme we have the [[Verschiebung morphism]]. It  is defined to be the adjoint operation to the [[Frobenius morphism]]. For $W(k)$ the Verschiebung morphism coincides with the shift $(a_0, a_1,\dots)\mapsto (0, a_0, a_1,\dots)$

For the truncated Witt rings and the shift operation $V:W_n(k)\to W_{n+1}(k)$ the Verschiebung morphism equals the $VR=RV$ where $R$ is the restriction map.

#### The restriction map

The restriction map $R: W_{n+1}(A)\to W_n(A)$ is given by $(a_0, \ldots, a_n)\mapsto (a_0, \ldots, a_{n-1})$. 

#### The Frobenius morphism

The Frobenius endomorphism $F: W_n(A)\to W_n(A)$ is given by $(a_0, \ldots , a_{n-1})\mapsto (a_0^p, \ldots, a_{n-1}^p)$. This is also a ring map, but only because of our necessary assumption that $A$ is of characteristic $p$.

Just by brute force checking on elements we see a few relations between these operations, namely that $V(x)y=V(x F(R(y)))$ and $RVF=FRV=RFV=p$ the multiplication by $p$ map.

### Duality of finite Witt groups


For a $k$-ring $R$ let $W^\prime(R)$ denote the [[ideal]] in $W(R)$ consisting of sequences $x=(x_n)_n$ of nilpotent elements in $W(R)$ such that $x_n=0$ for large $n$.

Let $E$ denote the [[Artin-Hasse exponential]]. Then we have $E(x,1)$ is a polynomial for $x\in W^\prime(R)$ and

$$E(-,1):\begin{cases}W^\prime\to \mu_k

\\
w\mapsto E(w,1)\end{cases}$$

is a morphism of [[group schemes]] to the [[multiplicative group scheme]] $\mu_k$.

+-- {: .num_prop}
###### Proposition
a) $W^\prime (R)$ is an ideal in $W(R)$.

b) $E(-,1): W^\prime\to \mu_k$ is an morphism of [[group schemes]].

c) The morphism

$$\begin{cases}
W\times W^\prime\to \mu_k
\\
(x,y)\mapsto E(xy,1)
\end{cases}$$

is bilinear and gives an isomorphism of [[group schemes]]

$$W^\prime\to D(W)$$

where $D$ denotes the [[Cartier dual]] of $W$ (maybe it is equivalently the [[Pontryagin dual]] of the underlying group of the (plain) ring $W$). That this map is a morphism of group schemes follows from the definition of the [[Cartier dual]].

d) For $x\in W(R)$ and $y\in W^\prime (R)$ we have $E(xy,1)\in R^\times$ and

$$E(V^n x y,1)=E (T^n(x F^n y),1)=E(x F^n y,1)$$
=--

+-- {: .num_defn}
###### Definition and Theorem
Let $ker(F_n^m):=ker (F^m:W_{nk}\to W_{nk})$ denote the [[kernel]] of $m$-times iterated [[Frobenius endomorphism]] of the $n$-truncated Witt ring.Let

$$\sigma_n:\begin{cases}

W_{nk}\to W_k
\\
(\alpha_0,\dots,\alpha_{n-1})\mapsto(\alpha_0,\dots,\alpha_{n-1},0,\dots)
\end{cases}$$

be the section of the restriction $R_n:W_k\to W_{nk}$. $\sigma_n$ sends $ker(F_n^m)$ in $W^\prime$. Note that $\sigma_n$ is not a morphism of groups.

We define the bilinear map

$$\lt-,-\gt:\begin{cases}
ker(F^m_n)\times ker(F^n_m)\to R^\times
\\
\lt x,y\gt\mapsto E(\sigma_n(x)\sigma_m(y),1)
\end{cases}$$
then $\lt x,y\gt$ is bilinear and gives an isomorphism

$$ker(F^m_n)\simeq D(ker(F^n_m)$$

and satisfies

$$\lt x,t y\gt=\lt f x,y\gt$$

$$\lt x,r y\gt=\lt i x,y\gt$$

where the morphisms are

$$\array{
ker(F^m_n)
&\stackrel{t}{\to}&
ker(F^m_{n+1})
\\
\downarrow^f&&\downarrow^r
\\
ker(F^{m-1}_n)
&\stackrel{i}{\hookrightarrow}&
ker(F^m_n)
}$$

where $i$ is the canonical inclusion, and $r,f,t$ are induced by $R,F,T$ where $F$ is [[Frobenius morphism|Frobenius]], $T$ is [[Witt ring|Verschiebung]] and $R:W\to W_n$ is [[Witt ring|restriction]]. $i$ and $t$ are monomorphisms, $f$ and $r$ are epimorphisms, and for $ker(F^n_m)$ we have $F=if$ and $V=rt$.
=--

References: [Pink, &#167;25](#Pink), [Demazure, III.4](#Demazure)

## Properties of the Witt group

The group of universal (i.e. not $p$-adic) Witt vectors equals $W(k)= 1+k [ [ X] ]$ i.e. the multiplicative group of power series in one variable $X$ with constant term $1$.

## Properties of the Witt ring

+-- {: .num_theorem}
###### Theorem
Let $k$ be a perfect field of prime characteristic $p$.

Then $W(k)$ is a discrete valuation ring with maximal ideal generated by $p$. From the above we see that $pW(k)=(0, a_0^p, a_1^p, \ldots )$. This clearly gives $W(k)/pW(k)\simeq k$. 

Also, $W(k)/p^nW(k)\simeq W_n(k)$. Thus the completion of $W(k)$ with respect to the maximal ideal is just $lim W_n(k)\simeq W(k)$ which shows that $W(k)$ is a complete discrete valuation ring.
=--

## Examples

### Basic examples

* $W_{p^\infty}(\mathbb{F}_p)\simeq \mathbb{Z}_p$ the $p$-adic integers.

* $W_{p^\infty}(\mathbb{F}_{p^n})$ is the unique [[unramified extension]] of $\mathbb{Z}_p$ of degree $n$.

### Lubin-Tate ring

The [[Lubin-Tate ring]] in [[Lubin-Tate theory]]  is a [[power series]] ring over a [[Witt ring]] and this way Witt rings govern much of [[chromatic homotopy theory]].

As an Abelian group $W(A)$ is isomorphic to the group of curves in the one-dimensional [[multiplicative group|multiplicative formal group]]. In this way there is a Witt-vector-like Abelian-group-valued functor associated to every one-dimensional formal group. For special cases, such as the Lubin&#8211;Tate formal groups, this gives rise to ring-valued functors called ramified Witt vectors. ([eom](#eom))

## Related concepts

* [[Witt Cohomology]]

* [[Lambda-ring]]

* [[Hochschild-Witt complex]] and Kaledin's non-commutative Witt vectors

* [[Lubin-Tate ring]]

* [[Borger's absolute geometry]]

* [[de Rham-Witt complex]]

## References

### Original texts and classical surveys

witt vectors were introduced in

* [[Ernst Witt]], _Zyklische K&#246;rper und Algebren der Characteristik $p$ vom Grad $p^n$. Struktur diskret bewerteter perfekter K&#246;rper mit vollkommenem Restklassenk&#246;rper der Charakteristik $p^n$_, J. Reine Angew. Math. , 176 (1936) pp. 126&#8211;140, ([web](http://www.digizeitschriften.de/main/dms/img/?IDDOC=504725))

In the context of [[formal group laws]] they were used in 

* [[Jean Dieudonné]], _Groupes de Lie et hyperalg&#232;bres de Lie sur un corps de charact&#233;ristique $p \gt 0$  VII" Math. Ann. , 134 (1957) pp. 114&#8211;133

See also

* [[Michiel Hazewinkel]], _Twisted Lubin-Tate formal group laws, ramified Witt vectors and (ramified) Artin-Hasse exponentials_, Transactions of the AMS (1980)

Surveys incluce

* [[eom]], _[Witt vector](http://www.encyclopediaofmath.org/index.php/Witt_vector)_
 {#eom}


* Michel Demazure, _[[Demazure, lectures on p-divisible groups|Lectures on p-divisible groups]]_ ([web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups))
  {#Demazure}


### Modern surveys

* [[Michiel Hazewinkel]],  _[[Hazewinkel, Witt vectors|Witt vectors]]_, ([arXiv](http://arxiv.org/abs/0804.3888))
  {#Hazewinkel08}

* [[Michiel Hazewinkel]], _Formal Groups and Applications_, review in [projecteuclid](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183548600)


* Joseph Rabinoff, _The theory of Witt vectors_ ([pdf](http://math.stanford.edu/~rabinoff/misc/witt.pdf))

* [[Richard Pink]], finite group schemes, [pdf](http://www.math.ethz.ch/~pink/ftp/FGS/CompleteNotes.pdf){#Pink}

Review in the context of the [[Kummer-Artin-Schreier-Witt exact sequence]] is in 

* {#MezardRomagnyTossici11} Ariane M&#233;zard, Matthieu Romagny, Dajano Tossici, section 2 of _Sekiguchi-Suwa theory revisited_ ([arXiv:1104.2222](http://arxiv.org/abs/1104.2222))


### Further development of the theory

* [[Dmitri Kaledin]], [[non-commutative Witt vectors]]

* [[Dmitri Kaledin]], universal Witt vectors and the ''Japanese cocycle'', [pdf](http://imperium.lenin.ru/~kaledin/math/jap.pdf)

* [[Lars Hesselholt]], [[Ib Madsen]], _On the de Rham-Witt complex in [[mixed characteristic]]_, [pdf](http://www.math.uiuc.edu/K-theory/0551/paper.pdf)

* [[Lars Hesselholt]], Witt vectors of non-commutative rings and topological cyclic homology, [pdf](http://www.math.uiuc.edu/K-theory/0135/derived.pdf)

* {#DS88} A. Dress, C. Siebeneicher, _The Burnside ring of profinite groups and
the Witt vector construction_, Adv. Math., 70, (1988), 87&#8211;132.


In the context of [[Borger's absolute geometry]]:

* {#Borger08} [[James Borger]], _The basic geometry of Witt vectors, I: The affine case_ ([arXiv:0801.1691](http://arxiv.org/abs/0801.1691))

* {#Borger10} [[James Borger]], _The basic geometry of Witt vectors, II: Spaces_ ([arXiv:1006.0092](http://arxiv.org/abs/1006.0092))


[[!redirects rings of Witt vectors]]
[[!redirects rings of Witt-vectors]]



[[!redirects Witt ring]]
[[!redirects Witt rings]]
[[!redirects Witt polynomial]]
[[!redirects Witt polynomials]]
[[!redirects group of Witt vectors]]
[[!redirects Witt vector]]
[[!redirects Witt vectors]]
[[!redirects ring of Witt vectors]]

[[!redirects big-Witt-vectors functor]]
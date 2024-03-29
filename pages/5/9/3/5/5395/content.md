
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Statement ##

+-- {: .un_theorem}
###### Theorem
**(The adjoint lifting theorem)**. Consider the following [[commutative diagram|commutative square]] of [[functor]]s:
$$
\begin{array}{cccc}\mathcal{A} & \overset{Q}{\to}  & \mathcal{B}    \\
^{U}\downarrow     &                   & \downarrow^{V} \\
\mathcal{C}        & \underset{R}{\to} & \mathcal{D}
\end{array}
$$

and suppose that
 
* $U$ and $V$ are [[monadic functor|monadic]], and 

* $\mathcal{A}$ has [[coequalizer]]s of reflexive pairs.

Then, if $R$ has a [[left adjoint]], then $Q$ also has a [[left adjoint]]. 
=--

A detailed proof may be found in Sec. 4.5 of Vol. 2 of [Borceux](#Borceux)
(see especially Theorem 4.5.6 on p. 226 and Ex. 4.8.6 on p. 252). Also ([Johnstone, prop. 1.1.3](#Johnstone)) For a sketch of proof, see ahead. 

+-- {: .un_cor}
###### Corollary
If the bottom functor $R$ of the above square is the
identity arrow (so that $U=V\circ Q$), if $U$ and $V$ are monadic, and
if $\mathcal{A}$ has coequalizers of reflexive pairs, then $Q$ is monadic.
=--

+-- {: .proof}
###### Proof
The adjoint lifting theorem implies the existence of a left
adjoint, and the rest is a straightforward application of the
[[monadicity theorem]].
=--

## Sketch of proof ##

We may assume the situation of the following diagram (with $V Q = R U$):
$$
\begin{array}{cccc}\mathcal{C}^\mathbb{T} & \underoverset{Q}{K(?)}{\leftrightarrows}  & \mathcal{D}^\mathbb{S}    \\
^{U}\downarrow \uparrow^{F}    &                   & ^{G}\uparrow\downarrow^{V} \\
\mathcal{C}        & \underoverset{R}{L}{\leftrightarrows}  & \mathcal{D}
\end{array}
$$
where 
$\mathbb{T}=\langle T,\varepsilon\colon 1_{\mathcal{C}}\Rightarrow
T,\mu \rangle$ is a monad on
$\mathcal{C}$, $\mathbb{S}=\langle S,\zeta\colon 1_{\mathcal{D}}\Rightarrow
S,\eta\rangle$ is a monad on
$\mathcal{D}$, $U$ and $V$ are the forgetful functors, and $F$ and $G$
are the free algebra functors.

Let us write $\tau\colon F U\Rightarrow 1_{\mathcal{C}^{\mathbb{T}}}$ for
the counit of the adjunction $F\dashv U$ and $\sigma\colon
G V\Rightarrow 1_{\mathcal{D}^{\mathbb{S}}}$ for the counit of the
adjunction $G\dashv V$. As usual, we have $T = U F$, $S = V G$,
$\mu=U\tau F$, and $\eta=V\sigma G$.  

Finally, let $L$ be a left adjoint to $R$ (which
exists by assumption), and let $\alpha\colon
1_{\mathcal{D}}\Rightarrow R L$ and $\beta\colon LR\Rightarrow
1_{\mathcal{C}}$ be the unit and counit (respectively) of the
adjunction $L\dashv R$. 

We would like to construct a functor $K\colon
\mathcal{D}^{\mathbb{S}}\to \mathcal{C}^{\mathbb{T}}$. To get a hint
of what $K$ should look like, let us assume for a moment that such a
$K$ already exists.  In this case, we have $K G\dashv V Q(=R U)$. But
$F L$ is also left adjoint to $R U$, and by the uniqueness of a left
adjoint we must have $K G = F L$ (at least up to a natural isomorphism).

From this, we already know how to define $K$ on free algebras. Also,
being a left adjoint, $K$ preserves in particular all coequalizers. But
every $\mathbb{S}$-algebra $\langle D,\xi\colon SD\to D\rangle$ is
the (object part) of a reflexive coequalizer, namely, the [[canonical
presentation]] 
$$
G S(D)\underoverset{G\xi}{\sigma_{G D}}{\rightrightarrows}G(D)\overset{\sigma_{\langle
D,\xi\rangle}=\xi}{\rightarrow}\langle D,\xi \rangle
$$
Applying $K$ and using $K G=F L$, we see that $K\langle D,\xi\rangle$
should be the object part of a reflexive coequalizer in
$\mathcal{C}^{\mathbb{T}}$ of the form
$$
F L S(D)\underoverset{F L\xi}{?}{\rightrightarrows}F L(D)\overset{x}{\rightarrow}K\langle
D,\xi \rangle 
$$
(recall that we assume that $\mathcal{C}^{\mathbb{T}}$ has
coequalizers of reflexive pairs). 

To eventually define $K\langle D,\xi \rangle$ as a coequalizer (as above),
we first need some reasonable guess for the ∞-arrow. For this, we will
need a lemma.

+-- {: .un_lemma}
###### Lemma
There exists a natural transformation $\lambda\colon S R
\Rightarrow R T$ for which the following diagram of functors and
natural transformations is commutative:

$$
\begin{array}{ccccccc} R & \overset{\zeta R}{\to} & S R &
 &  \overset{\eta R}{\leftarrow}& & S S R \\
 & ^{R\varepsilon}\searrow & ^{\lambda}\downarrow & & & & ^{S\lambda}\downarrow\\
 & & R T & \overset{R\mu}{\leftarrow} & R T T & \overset{\lambda T}{\leftarrow} & S R T
\end{array}
$$
=--

+-- {: .proof}
###### Proof
Define $\lambda := V\sigma Q F \circ V G R\varepsilon$, so that
$$
\lambda \colon
S R = V G R\overset{V G R\varepsilon}{\to}V G R T = V G R U F = V G V Q
F\overset{V\sigma Q F}{\to} V Q F = R U F = R T.
$$
The required commutativity may be verified by using the commutative
diagrams in the definitions of a monad and an EM-algebra, 
naturality, and the triangular identities. For details, see the proof
of Lemma 4.5.1 of [Borceux](#Borceux), 
pp. 222-223. (Note that this lemma does not depend on the
existence of a left adjoint for the bottom horizontal arrow, nor on
the existence of coequalizers. Only the commutativity is required.) 
=--

We may now return to our task of defining the ∞-arrow in the diagram
preceding the lemma. We would like to get from $F L S(D)$ to $F L(D)$,
and for this, we will construct a natural transformation
$F L S\Rightarrow F L$ in the following way.  First, we have 
$$
S\overset{S\alpha}{\to} S R L \overset{\lambda L}{\to} R T L.
$$
Applying $L$ and composing with $\beta T L$, we get
$$
LS\overset{L\lambda L\circ LS\alpha}{\longrightarrow}L R T L \overset{\beta TL}{\to} TL.
$$
Applying $F$ and composing with $\tau F L$, we finally get
$$
F L S\overset{F\beta T L\circ F L\lambda L\circ F L
S\alpha}{\longrightarrow}F T L = F U F L\overset{\tau F L}{\to} F L
$$
Let us call the resulting natural transformation $\omega$, that is, 
$$
\omega:=\tau F L \circ F\beta T L\circ F L\lambda L\circ F L S\alpha.
$$

Now we take the sought for ∞-arrow to be $\omega_D$, and
*define* $K\langle D,\xi\rangle$ as the object of some fixed
coequalizer of $\omega_D$ and $F L\xi$:
$$
F L S(D)\underoverset{F L\xi}{\omega_D}{\rightrightarrows}F
L(D)\overset{x}{\rightarrow}K\langle D,\xi \rangle.
$$
In order to do this, we must first verify that the parallel
arrows above have a common section (since we only assume that
$\mathcal{C}^{\mathbb{T}}$ has coequalizers of reflexive pairs). To
find a guess for a common section, note that the common section
for the parallel pair in the above canonical presentation in
$\mathcal{D}^{\mathbb{S}}$ is $G\zeta_{V\langle
D,\xi\rangle}=G\zeta_D$, and if $K$ exists, then applying $K$ gives
$K G\zeta_D=F L\zeta_D$. Having this guess, it is now straightforward
to verify that $F L\zeta_D$ is indeed a common section, as required. 

So, we have defined an object function of a would be left adjoint $K$.
To make it into a functor left adjoint to $Q$, we will build a
universal arrow from $\langle D,\xi\rangle$ to $Q$, whose object part
is $K\langle D,\xi\rangle$ (Theorem IV.1.2(ii) of [[Categories
Work]]). 

To get an arrow $\langle D,\xi\rangle\to Q K\langle D,\xi\rangle$ ,
suppose for a moment that we have a natural 
transformation $\varphi\colon G\Rightarrow Q F L$ such that  $\varphi\circ
\sigma G = Q\omega\circ \varphi S$.  Then the left square in the following
diagram commutes:
$$
\begin{array}{ccccc}G S(D)&
\underoverset{G\xi}{\sigma_{G D}}{\rightrightarrows} & G(D) &\overset{\sigma_{\langle
D,\xi\rangle}=\xi}{\rightarrow}&\langle D,\xi \rangle \\
^{\varphi_{S D}}\downarrow && ^{\varphi_D}\downarrow && ^{\chi}\downarrow\\
Q F L S D &\underoverset{Q F L\xi}{Q\omega_D}{\rightrightarrows} & Q F
L D &\overset{Q x}{\rightarrow}&Q K\langle D,\xi\rangle
\end{array}
$$
Since both rows are forks, it follows that $Q x\circ \varphi_D$ has
the same composition with the arrows of the upper  
parallel pair, and hence there exists a unique arrow $\chi\colon
\langle D,\xi\rangle\to Q K\langle D,\xi\rangle$ making the right
square commutative (recall that the upper row is a coequalizer). 

It is now possible to prove that the pair $\langle K\langle
D,\xi\rangle,\chi \rangle$ is a universal arrow from $\langle
D,\xi\rangle$ to $Q$, showing that $K$ is indeed (the object
function) of a left adjoint (for details, see the proof of Theorem
4.5.6, pp. 226-227 in [Borceux](#Borceux)).

But we still have to prove the existence of a natural
transformation $\varphi\colon G\Rightarrow Q F L$ such that  $\varphi\circ
\sigma G = Q\omega\circ \varphi S$. For this, we define
$\varphi:=\sigma Q F L \circ G R\varepsilon L \circ G\alpha$. Since
$V$ is faithful, to prove the required property of $\varphi$, it is
enough to prove that $V\varphi \circ V\sigma G = V Q\omega\circ
V\varphi S$, and this is a long, yet straightforward,
computation (noting that $V\varphi = \lambda L \circ VG\alpha$ and using
the commutative diagram from Lemma 1; see Lemma 4.5.3, p. 224 of [Borceux](#Borceux)).


## Examples ##

### Forgetful functors between varieties of algebras ###
Since varieties of algebras are [[cocompleteness of varieties of algebras|cocomplete]] and monadic over
$\mathbf{Set}$, the corollary implies that forgetful functors between
varieties of algebras (e.g., the forgetful functor
$\mathbf{Rng}\to\mathbf{Ab}$) are monadic.   

### Sufficient conditions for cocompleteness of monadic categories ###
Let $\mathcal{J}$ be an arbitrary category, and consider the commutative diagram 
$$
\begin{array}{ccccc}\mathcal{A} & \overset{\Delta}{\to} & \mathcal{A}^\mathcal{J}    \\
^{U}\downarrow                 &                        & \downarrow^{U^{\mathcal{J}}} \\
\mathcal{C}                    & \underset{\Delta}{\to} & \mathcal{C}^\mathcal{J}
\end{array}
$$
where $U$ is monadic, $\Delta$ is the [[diagonal functor]] and $U^{\mathcal{J}}=U\circ
-$. If $F$ is left adjoint   
to $U$, then $F^\mathcal{J}$ is left adjoint to $U^{\mathcal{J}}$ (using
the unit and counit of the original adjunction, one can construct
appropriate natural transformations that satisfy the triangular
identities, see, e.g., p. 119 of [[Categories Work]]).  Also, the
conditions of the monadicity theorem for $U$ imply those for
$U^\mathcal{J}$ (basically because the definition of a split fork involves only
compositions and identities, and because natural transformations are composed
componentwise).  

Now, if $\mathcal{C}$ is $\mathcal{J}$-cocomplete (so that the
bottom horizontal functor has a left adjoint) and $\mathcal{A}$ has
coequalizers of reflexive pairs, then the adjoint lifting theorem
implies that $\mathcal{A}$ is $\mathcal{J}$-cocomplete. In particular,
if $\mathcal{A}$ has coequalizers of reflexive pairs and $\mathcal{C}$
is small-cocomplete, then $\mathcal{A}$ is small cocomplete.


## Related pages

* The adjoint lifting theorem is a corollary of the [[adjoint triangle theorem]].

* [[adjoint functor theorem]]

## References ##


* [[Michael Barr]], [[Charles Wells]], section 3.7, pp.131 in: *[[Toposes, Triples, and Theories]]*, Springer (1985), Reprints in Theories and Applications of Categories **12** (2005) 1-287 &lbrack;[tac:tr12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)&rbrack; 


* [[Francis Borceux]], _[[Handbook of Categorical Algebra]] II_ , Cambridge UP 1994. (section 4.5, pp.221ff) 
{#Borceux}

* {#Johnstone} [[Peter Johnstone]], *Adjoint lifting theorems for categories of algebras*, Bull. London Math. Soc. **7** (1975) 294-297 &lbrack;[doi:10.1112/blms/7.3.294](https://doi.org/10.1112/blms/7.3.294)&rbrack;


* [[Peter Johnstone]], section A1.1, p.5 in: *[[Sketches of an Elephant]] I*, Oxford UP 2002

On the dual theorem for [[comonads]]:

* William F. Keigher, _Adjunctions and comonads in differential algebra_, Pacific J. Math. **59,** 1 (1975) 99-112 &lbrack;[euclid:pjm/1102905501](http://projecteuclid.org/euclid.pjm/1102905501)&rbrack;


* [[John Power]], _A unified approach to the lifting of adjoints_, [[Cahiers]] **XXIX**  1 (1988)  67-77 &lbrack;[numdam](http://www.numdam.org/item/CTGDC_1988__29_1_67_0)&rbrack;

[[!redirects adjoint lifting theorems]]


$\sfrac{1}{2}$

$$
  \cdots
$$

$$
  \{\Gamma_{\mu}, \Gamma_\nu\} = \pm 2 g_{\mu \nu}
$$

$$
  (\Gamma_0)^2 = \pm 1
$$

$$
  \wedge \;\; \Leftrightarrow
$$

$$
\array{
  & (M \otimes M) \otimes M
    & \stackrel{\alpha}{\longrightarrow}
  & M \otimes (M \otimes M)
    & \stackrel{1 \otimes \mu}{\longrightarrow}
  & M \otimes M
  \\
  & {}_{\mu \otimes 1}\searrow
    &&
    && \swarrow_{\mu}
  &
  \\
  &&
  M \otimes M
    & \stackrel{\mu}{\longrightarrow}
  M
  &&
}
$$


| $H \subset G$ | $N_G H$ | $W_G H$ | $\left\vert W_G H\right\vert$ |
|---------------|---------|-------|-------------------------------|
| $1 \subset \mathbb{Z}_2$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $2$ |
| $\mathbb{Z}_2 \subset \mathbb{Z}_2$ | $\mathbb{Z}_2$ | $1$ | $1$ |



| [[Dynkin diagram]]/ <br/> [[Dynkin quiver]]  | [[dihedron]],<br/> [[Platonic solid]] | [[classification of finite rotation groups|finite subgroups of SO(3)]] | [[classification of finite rotation groups|finite subgroups of SU(2)]] | [[simple Lie group]] |
|---------------------|---|-----|---------------|----------------------|
|  [[A0]] <br/> = <br/> [[D1]]  |   |    |  | [[U(1)]] <br/> $\simeq$ <br/> [[Spin(2)]] |
|  [[A1]]$\times$[[A1]] <br/> = <br/> [[D2]]  |   |    |  | [[SU(2)]]$\times$[[SU(2)]] <br/> $\simeq$ <br/> [[Spin(4)]] |
|  [[A3]] <br/> = <br/> [[D3]]  |   | [[cyclic group of order 4]] <br/> $\mathbb{Z}_4$  | [[cyclic group of order 4]] <br/> $2 D_2 \simeq \mathbb{Z}_4$  | [[SU(4)]] <br/> $\simeq$ <br/> [[Spin(6)]] |
|  [[D4]]  | [[dihedron]] on <br/> [[bigon]] | [[Klein four-group]] <br/> $D_4 \simeq \mathbb{Z}_2 \times \mathbb{Z}_2$ |  [[quaternion group]] <br/> $2 D_4 \simeq$ [[Q8]] | [[SO(8)]], [[Spin(8)]] |
|  [[D5]]  | [[dihedron]] on <br/> [[triangle]] | [[dihedral group of order 6]] <br/> $D_6$ |  [[binary dihedral group of order 12]] <br/> $2 D_6$  | [[SO(10)]], [[Spin(10)]] |
|  [[D6]]  | [[dihedron]] on <br/> [[square]] | [[dihedral group of order 8]] <br/> $D_8$ |  [[binary dihedral group of order 16]] <br/> $2 D_{16}$  | [[SO(12)]], [[Spin(12)]] |
|  $D_{n \geq 4}$  | [[dihedron]], <br/> [[hosohedron]] | [[dihedral group]] <br/> $D_{2(n-2)}$ | [[binary dihedral group]] <br/> $2 D_{2(n-2)}$ | [[special orthogonal group]], [[spin group]] <br/> $SO(2n)$, $Spin(2n)$ |
|  $E_6$  | [[tetrahedron]] | [[tetrahedral group]] <br/> $T$ | [[binary tetrahedral group]] <br/> $2T$ | [[E6]] |
|  $E_7$  | [[cube]], <br/> [[octahedron]] | [[octahedral group]] <br/> $O$ | [[binary octahedral group]] <br/> $2O$ | [[E7]] |
|  $E_8$  | [[dodecahedron]], <br/> [[icosahedron]] | [[icosahedral group]] <br/> $I$ | [[binary icosahedral group]] <br/> $2I$ | [[E8]] |


\begin{tikzpicture}

  \node (Spin6) at (0,1.4)  {$\mathrm{Spin}(6)$};
  \node (SU4) at (3.4,1.4)  {$\mathrm{SU}(4)$};

  \draw[white] (Spin6) to node {\color{black}$\simeq$} (SU4);

  \node (center) at (0,0) {};
  \node (topright) at (30:1) {};
  \node (left) at (180-30:1) {};
  \node (botright) at (0,-1) {};
  
  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (topright) circle (.1);
  \draw[draw=lightgray, fill=lightgray] (botright) circle (.1);
  \draw[fill=black] (left) circle (.1);


  \draw (center) to (topright);
  \draw[lightgray] (center) to (botright);
  \draw (center) to (left);
    
  \begin{scope}[shift={(3.4,0)}]
  \node (center) at (0,0) {};
  \node (left) at (-1,0) {};
  \node (right) at (+1,0) {};

  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (left) circle (.1);
  \draw[fill=black] (right) circle (.1);

  \draw (center) to (left);
  \draw (center) to (right);
  \end{scope}
\end{tikzpicture}



\begin{tikzpicture}
  \node (center) at (0,0) {};
  \node (topright) at (60:1) {};
  \node (botright) at (-60:1) {};
  \node (left) at (180:1) {};
  
  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (topright) circle (.1);
  \draw[fill=black] (botright) circle (.1);
  \draw[fill=black] (left) circle (.1);

  \draw (center) to (topright);
  \draw (center) to (botright);
  \draw (center) to (left);
\end{tikzpicture}

$\left\vert \nabla \phi \right\vert = const$

| $n=$ | 0 | 1 | 2 | 3 | 4 | 
|--|--|--|--|--|--|
| $DI(n)=$ | [[trivial group|1]] |  [[Z/2]] | [[SO(3)]] | [[G2]] | [[G3]] |
|          | = Aut(R) | [= Aut(C)](complex+number#AutomorphismsOfComplexNumbersIsZ2)        | [= Aut(H)](quaternion#AutomorphismsOfQUatrnionsAlgebraIsSO3)       |  [= Aut(O)](octonion#AutomorphismsOfOctonionAlgebraIsG2)  |   |


\begin{tikzpicture}
  \draw node at (0,0) {$X$};
\end{tikzpicture}

$\varnothing$

$\to$

# Coend calculus

_Guest post by [Fosco Loregian](http://tetrapharmakon.github.io/) and [Bryce Clarke](https://twitter.com/8ryceClarke)._

> Pastro, Craig, and Ross Street. [Doubles for monoidal categories.](http://www.tac.mta.ca/tac/volumes/21/4/21-04abs.html) Theory and applications of categories 21.4 (2008): 61-75.


_Coend calculus_ rules the behaviour of certain universal objects associated to functors of two variables $T : C^{op}\times C \to D$; intuitively, $end(T)$ stands to $T$ as the limit $\lim\, F$ of $F : A \to B$ stands to $F$; the major difference is that $end(T)$ takes into account the fact that $T$ eats at the same time two "terms" of the same "type" $C$, once covariantly in the second component, and once contravariantly in the first: on arrows $f : c\to c'$ the functor $T$ acts in fact as follows:
$$
\begin{array}{ccccc}
&& T(c',c) && \\
&\overset{T(f,c)}\swarrow && \overset{T(c',f)}\searrow &\\
T(c,c) &&&& T(c',c')
\end{array}
$$
Now, a distinguising feature of the objects that depend contra-covariantly on the same variable is that they can be _integrated_: given a sufficiently regular function $f(x)$, its dependence from $x$ can be thought as "covariant" (and defined, say, on a topological vector space $V\cong \mathbf{R}^n$), whereas the "$d x$" in the symbol
$$
\int f(x)d x
$$
is contravariant (it belongs to a certain dual space of covectors on $V$); altogether, the integral can be thought as exhibiting a contra-covariant dependence from $x$.

Ends and coends are associated to functors $T : C^{op}\times C \to D$ in a similar fashion that resembles integration: they are certain objects $\int_c T(c,c)$ (the end) and $\int^c T(c,c)$ (the coend), canonically associated to $T$, treating $c$ as a mute variable (meaning that $\int_c T(c,c)$ and $\int_{c'} T(c',c')$ are the same object), and satisfying a "commutative rule of integrals" analogous to
$$
\int f(x,y) d x d y = \int \Big(\int f(x,y)d x\Big) d y = \int \Big(\int f(x,y)d y\Big) d x
$$
The end of $T$ is endowed with projections on the "symmetrized components" $\int_c T(c,c) \to T(c',c')$, one for each object $c'$; dually, the coend $\int^c T(c,c)$ is endowed with injections $T(c',c') \to \int^c T(c,c)$.

All in all, this happens also for colimits, so the two constructions are -at least intuitively- tightly related: this intuition can of course be made more precise. Every universal object built in category theory can be thought either as a subobject of a product (a limit), or as a quotient of a coproduct (a colimit), and co/ends make no exception:

- An _end_ arises as an "object of invariants" $\int_c T$ for the action of $T$ given by the functions on arrows $T_{x y} : \hom_{C^{op}\times C}(x,y) \to \hom_D(T x, T y)$, and it is defined as the subobject of $\prod_{c\in C} T(c,c)$ of those elements invariant under this action.
- Dually, a _coend_ arises as a "quotient space" of $\coprod_{c\in C}T(c,c)$ by a suitable equivalence relation generated by the same functions $T_{x y} : \hom_{C^{op}\times C}(x,y) \to \hom_D(T x, T y)$, i.e. as a _space of orbits_ for the action.

More on this will be explained later on in the discussion.

What is more important now, and quite astounding, is that such contra-covariant actions arise at every corner of category theory: using co/ends it is possible to re-state the Yoneda lemma and the theory of Kan extensions, and to find plenty of applications to algebra, topology, geometry... and functional programming. :-)

## Dinaturality

As already said, a functor $T : C^{op}\times C \to D$ acts on morphisms as
$$
\begin{array}{ccccc}
&& T(c',c) && \\
&\overset{T(f,c)}\swarrow && \overset{T(c',f)}\searrow &\\
T(c,c) &&&& T(c',c')
\end{array}
$$
given _two_ such functors, say $P,Q : C^{op}\times C \to D$, we can consider the two diagrams
$$
\begin{array}{ccccc}
&& P(c',c) && \\
&\overset{P(f,c)}\swarrow && \overset{P(c',f)}\searrow &\\
P(c,c) &&&& P(c',c')
\end{array}
$$
and
$$
\begin{array}{ccccc}
Q(c,c)&&&& Q(c',c')\\
&\underset{Q(c,f)}\searrow&& \underset{Q(f,c')}\swarrow& \\
&&Q(c,c')&&
\end{array}
$$
Given two functors $F,G : A \to B$ a natural transformation can be seen as a family of maps that "fill the gap" between $F(f)$ and $G(f)$ in a commutative square; in a similar fashion, a _dinatural_ transformation between the above $P,Q$ can be seen as a way to close a certain diagram that testifies a transformation from the arrow action of $P$ to the arrow action of $Q$:
$$
\begin{array}{ccccc}
&& P(c',c) && \\
&\overset{P(f,c)}\swarrow && \overset{P(c',f)}\searrow &\\
P(c,c) &&&& P(c',c')\\
\!\!\!\!{\color{red} \alpha_c\downarrow} &&&&\,\,\,\,\,\,\,{\color{red}\downarrow\alpha_{c'}} \\
Q(c,c)&&&& Q(c',c')\\
&\underset{Q(c,f)}\searrow&& \underset{Q(f,c')}\swarrow& \\
&&Q(c,c')&&
\end{array}
$$
Just as co/limits are defined via suitable transformation to/from a constant, so are co/ends:

- If $Q : C^{op}\times C \to D$, a _wedge for $Q$ with base $x$_ consists of a dinatural transformation from the constant functor on $x\in D$, i.e. of a family of morphisms $\alpha_c : x\to Q(c,c)$ such that for each $f :c\to c'$ the above hexagon reduces to a commutative square:
  $$
  \begin{array}{ccc}
  x &\to& Q(c,c)\\
  \downarrow && \downarrow\\
  Q(c',c') &\to & Q(c,c')
  \end{array}
  $$
- If $P : C^{op}\times C \to D$, a _cowedge for $P$ with tip $y$_ consists of a dinatural transformation to the constant functor on $y\in D$, i.e. of a family of morphisms $\alpha_c : P(c,c) \to y$ such that for each $f :c\to c'$ the above hexagon reduces to a commutative square:
  $$
  \begin{array}{ccc}
  P(c',c) &\to& P(c,c)\\
  \downarrow && \downarrow\\
  P(c',c') &\to & y
  \end{array}
  $$
  There exists a category $Wd(Q)$ of wedges, defined with an obvious choice of morphisms between bases; similarly, there is a category of cowedges $Cwd(P)$.

The _end_ $\int_c Q(c,c)$ of $Q$ is now defined as a terminal object in the category of its wedges; dually, the _coend_ $\int^c P(c,c)$ of $P$ is the initial object of the category of its cowedges. Of course, we say "the" end because such an initial object is unique up to unique isomorphism when it exists.

So far, so good. In fact, we didn't stray much far from plain old category theory, as it is possible to show the following:

_Lemma (co/ends are colimits)_: Given $Q : C^{op}\times C \to D$ there exist a category $\text{tw}\, C$ and a functor $Q^\tau : \text{tw}\, C \to D$ such that
$$
\int_c Q(c,c) \cong \lim \,Q^\tau
$$
For those who know: the end of $Q$ is the [weighted colimit](https://ncatlab.org/nlab/show/weighted+limit) of $Q : C^{op}\times C \to D$ with the $\hom_C$ functor $C^{op}\times C \to Set$, and thus the category $\text{tw}\, C$ is nothing more, nothing less than the [category of elements](https://ncatlab.org/nlab/show/category+of+elements) of $\hom_C$; this allows for a very explicit presentation of $\text{tw}\, C$:

- objects: the arrows of $C$, $f : c \to c'$;
- morphisms: the commutative squares
  $$
  \begin{array}{ccc}
  c &\leftarrow& d \\
  {}^f\downarrow && \downarrow^g\\
  c' &\to& d'
  \end{array}
  $$

_Corollary (hom commutes with all ends):_ As a consequence of the fact that $\int_c Q$ is a limit, there is an isomorphism
$$
\hom_C\Big(y, \int_c P(c,c)\Big) \cong \int_c \hom_C(y, P(c,c)) \qquad\qquad{(ccnt)}
$$
natural in $y$. Dually,
$$
\hom_C\Big( \int^c P(c,c), y \Big )\cong \int_c \hom_C(P(c,c), y). \qquad\qquad{(ccnt)}
$$
natural in $y$.

(of course, a coend is just an end in the opposite category!)

But why are co/ends denoted as integrals? The notation dates back to Yoneda,

> Yoneda, Nobuo. "[On Ext and exact sequences.](http://alpha.math.uga.edu/~lorenz/YonedaExtExactSequences.pdf)" J. Fac. Sci. Univ. Tokyo Sect. I 8.507-576 (1960): 1960.

(in particular, see §4 but beware that the notation is reversed; a coend is denoted $\int_a$ and an end $\int_a^\ast$!) and it is essentially motivated by the fact that an end behaves like an integral:

_Theorem (Fubini rule):_ Let $P : C^{op}\times C \times D^{op}\times D \to E$ be a functor; then
$$
\int^c\left(\int^d P(c,c,d,d)\right) \cong
\int^{(c,d)}P(c,d,c,d)
\cong \int^d\left(\int^c P(c,c,d,d)\right) \qquad\qquad{(Fub)}
$$
in the sense that if one of the three objects exists, so do the other two, and they are all canonically isomorphic (the category $C^{op}\times C \times D^\text{op}\times D$ is of course equal to $(C\times D)^\text{op}\times( C \times D)$). Similarly, there is such a rule for ends.

Thus, in category theory integration with respect to a variable is a process that can happen in whatever order we desire: given a permutation $\sigma$ of the set $\{1,\dots,n\}$, whenever the integral
$$
\int^{c_{\sigma 1}}\int^{c_{\sigma 2}}\cdots \int^{c_{\sigma n}} P(c_{\sigma 1},  c_{\sigma 1}, c_{\sigma 2}, c_{\sigma 2}, \dots, c_{\sigma n}, c_{\sigma n})
$$
exists, then so does
$$
\int^{(c_1,\dots, c_n)} P(c_1, c_1, c_2, c_2, \dots, c_n, c_n)
$$
_Proof._ The slickest proof I know for this goes as follows: assume all coends exist; then, sending a functor $P : C^{op}\times C \to D$ to its coend is a functor $\int^C : [C^{op}\times C, D] \to D$, and it is easy to see that it is a left adjoint (for those who know, $\int^C$ is a particular kind of weighted colimit, and every such weighted colimit admits a right adjoint expressed in terms of the weight: but now it's easy to prove that these right adjoints commute, thus yielding the Fubini rule by uniqueness of adjoints).

## The building blocks of co/end calculus

Here we explore how co/ends allow to rediscover category theory from scratch.

### Natural transformations

_Theorem (Natural transformations as an end)_ Let $F,G : C \to D$ be two functors; then, there is an isomorphism
$$
Nat(F,G) \cong \int_c \hom_D(F c,G c) \qquad\qquad{(nat)}
$$
_Proof._ There is a natural choice for a wedge $\omega : Nat(F,G) \to \hom(F c,G c)$, that sends a natural transformation to its $c$-component; it remains to show that this is indeed a terminal wedge. Given another wedge $\alpha : A \to \hom(F c, G c)$, the wedge condition translates into the equation
$$
\begin{array}{ccc}
A &\overset{\alpha_{a c}}\to& \hom(F c,G c) \\
{}_{\alpha_{a c'}}\downarrow && \downarrow_{G f \circ -} \\
\hom(F c', G c') &\underset{- \circ F f}\to & \hom(F c, G c')
\end{array}
$$
valid for every $a\in A$; but this is only a convoluted way to say that for every $a\in A$ the family
$$
\{\alpha_{a,c} : F c \to G c\}
$$
is a natural transformation.

Two important remarks:

1. In an additive setting, the wedge condition for $\alpha$ can be easily translated into the fact that natural transformations appear form the kernel of a certain map; the intuition that naturality is a cocycle condition is more or less what led Yoneda to study ends and coends in homological algebra.

2. Even in a non-additive setting, one can easily see that a natural transformation $\alpha : F \Rightarrow G$ is a map that equalizes the action of $F,G$ on arrows; this means that the following diagram
   $$
   Nat(F,G) \to \prod_{c\in C} \hom(F c, G c) \underset{G f_\ast}{\overset{F f^\ast}\rightrightarrows} \prod_{c\to c'} \hom(F c, G c')
   $$
   is an equalizer; there is nothing special here, as for _every_ functor $T : C^{op}\times C \to D$ there is a similar equalizer diagram
   $$
   \int_c T(c,c) \to  \prod_{c\in C} T(c,c) \underset{T f_\ast}{\overset{T f^\ast}\rightrightarrows} \prod_{c\to c'} T(c, c')
   $$

[Here](https://mathoverflow.net/questions/20580/coend-computation-continued/20592)'s a discussion on what is the coend of the hom functor; I claim that the following object represents the coend of $\hom(F-,G-)$, perhaps you know where the same object appears under a different name, and where it is used for some purpose? I find this particularly intriguing in the case of a monoid $M$ regarded as single-object category:

- the end of $\hom_M$ is the _center_ of the monoid, i.e. the subset $\{m\in M\mid mx=xm \forall x\in M\}$;
- the coend of $\hom_M$ corresponds to something like the $\pi_0$ of the monoid.

I didn't expect these construction to be dual, and yet they are!

_Claim_ (but also: exercise for the reader). Let $C$ be a small category. The coend
$$
\int^c \hom_C(c,c)
$$
is the set of connected components of the "endo-comma" category whose objects are endomorphisms of $C$, and whose morphisms $(u : x \to x) \to (v : y \to y)$ are the $f : x \to y$ such that $f u = v f$. More generally, if $F,G: C \to D$ are functors there is an isomorphism
$$
\int^c \hom(F c, G c) \cong \pi_0((F/G)_{end})
$$
where the endomorphism comma is defined similarly.

### The Yoneda lemma and Kan extensions

> On the first day He created the Yoneda lemma, and He saw that it was good:

_Theorem (The ninja Yoneda lemma)_ Let $F : C^{op} \to Set$; then for every object $a\in C$,
$$
F a\cong \int^c F c \times \hom_C(a,c) \cong
\int_c \Set(\hom_C(c,a), F c)
$$
_Proof._ The set $\int_c \Set(\hom_C(c,a), F c)$ is the set of natural transformations from $\hom(-,c)$ to $F$, and thus the non-ninja Yoneda lemma yields an isomorphism between this set and $F a$. Dually, call $F\otimes y$ the functor
$$
a\mapsto \int^x F x\times \hom_C(a,x)
$$
Then, we have
$$
\begin{array}{rl}
Nat(F\otimes y, G) &\cong \int_a Set(F x\times \hom_C(a,x), G a)\\
&\displaystyle\cong\int_a\int_x Set(F x\times \hom_C(a,x), G a)\\
&\displaystyle\cong\int_a\int_x Set(F x, [\hom_C(a,x), G a])\\
&\displaystyle\cong\int_x Set(F x, \int_a[\hom_C(a,x), G a])\\
&\displaystyle\cong\int_x Set(F x, Nat(y(x), G))\\
&\displaystyle\cong Nat(F, G)
\end{array}
$$
Each of these steps can be easily justified in light of what we already proved:

- the fact that the hom functor preserves ends;
- the Fubini rule for ends;
- the fact that the set of natural transformations between two functors is an end.

This natural deduction-style kind of proof is half-jokingly called "coend-fu" ((端楔術 : literally “the art [of handling] terminal wedges”) in [my note, soon-ish a book, on coends](https://arxiv.org/abs/1501.02503).

Incidentally, the isomorphism $F a\cong \int^c F c \times \hom_C(a,c)$ is precisely the sense in which "every presheaf is a colimit of representable functors"; the colimiting diagram has domain the category of elements of $F$, and the natural functor $\Sigma : El(F) \to C \to [C^{op},Set]$ has colimit $F$.

> On the second day, He created Kan extensions, and category theory was complete.

_Theorem (Kan extensions are co/ends)_ Let $A \xleftarrow{G} B\xrightarrow{F} C$ be a span of functors; if the coend
$$
\int^b \hom_A(G b, a) \times F b
$$
exists, then it is the value at $a$ of the left Kan extension of $F$ along $G$; dually, is the end
$$
\int_b F b ^ {\hom_A(a, G b)}
$$
exists, then it is the value at $a$ of the right Kan extension of $F$ along $G$.

_Proof._ The proof is another lengthy, but completely straightforward, kata using the coend-fu we already know:
$$
 \begin{array}{rl}
  Nat(\text{Lan}_G F, H) &\textstyle \cong \int_a  \hom(\text{Lan}_G F( a ), H  a ) \\
    & \textstyle \cong \int_a     \hom\Big( \int^c \hom(G c, a )\times F c, H a  \Big)  \\
  Fub  & \textstyle \cong \int_{ a  c} \hom\Big( \hom(G c, a )\times F c, H a  \Big)         \\
    & \textstyle \cong \int_{ a  c} \hom\Big( F c,[\hom(G c, a ), H a ] \Big)       \\
  ccnt & \textstyle \cong \int_c    \hom\Big( F c,\int_a  [\hom(G c, a ), H a ] \Big)   \\
  nat  & \textstyle \cong \int_c    \hom\Big( F c,Nat(\hom(G c,-), H) \Big)      \\
  nat  & \textstyle \cong \int_c    \hom\Big( F C,H G C \Big) = Nat(F, H G)   \\
 \end{array}
$$

# Bimodules

[This](http://www.tac.mta.ca/tac/volumes/21/4/21-04abs.html) Pastro and Street paper makes heavy use of the theory of _bimodules_. Let's dig deeper into their structure. First of all, let us define a bicategory as follows:

- objects are (unitary) rings $R,S,\dots$
- 1-cells $M : R \to S$ are modules ${}_S M_R$, left over $R$ and right over $S$.
- 2-cells $\varphi : {}_R M_S \to {}_R N_S$ are $R$-$S$-linear homomorphisms of modules.

The composition of 1-cells is the tensor product of modules: ${}_R M \otimes_S N_T$ is a $R$-$T$-bimodule for every $R$-$S$bimodule $M$ and every $S$-$T$-bimodule $N$ (so in particular this is not a strict 2-category); 2-cells are composed horizontally and vertically, using the obvious function composition, and bifunctoriality of the $\otimes$ operation.

Good! There is a 2-categorical characterization of modules. What is good for? Well: rings are monoids in the category of abelian groups. We could have done the very same thing taking (plain) monoids, i.e. monoids in the category of sets, and defining a category of "bimodules" as sets with a left action of some monoid, and a right action of some other monoid.

What is interesting now is that we can generalize the same construction, with no additional cognitive loading, and take $X,Y,Z\dots$ to be multi-object monoids: we define a bicategory $Mod$ as follows:

- objects are categories $C,D, E,\dots$
- 1-cells $P : C \mathrel{&#8696;} D$ are functors $P : D^{op}\times C \to Set$
- 2-cells are natural transformations between functors.

A functor $P : D^{op}\times C \to Set$ is a multiobject module on which the multiobject monoids $C,D$ act.

So categories really are monoids, and are also eager to act on sets.

A bimodule is also called a profunctor, a distributor, a correspondence, a span,... and possibly with many other names; each of these names comes from a certain intuition behind their nature that leads to the definition of the same bicategory:

- they are called _profunctors_ because they generalize functors: some profunctors are called _representable_, and they are the ones of the form $\hom(b, F a)$ for some functor $F : A \to B$ between categories. A pro-functor thus works "[on behalf](https://www.etymonline.com/word/pro-) of a functor", as well as a relation generalizes a function.
- ...which is why some people prefer to call them _relators_: just as a func-tion is a special kind of rela-tion, a func-tor is a special kind of rela-tor.
- they are called _distributors_: as the nLab says,

    > Jean Bénabou, who invented the term and originally used “profunctor,” now prefers “distributor,” which is supposed to carry the intuition that a distribut*or* generalizes a funct*or* in a similar way to how a distribution generalizes a function.

    There's in fact a beautiful story about this: Lawvere defined a notion of [distribution](https://ncatlab.org/nlab/show/Lawvere+distribution) between toposes, such that the points of a topos $p : Set \to \mathcal{E}$ behave like Dirac delta functions, and such that distributions between presheaf toposes are exactly profunctors.

- they are called _correspondences_ or _spans_ because of the [Grothendieck construction](https://ncatlab.org/nlab/show/Grothendieck+construction): every presheaf $P : D^{op}\times C \to Set$ has a category of elements $El(P)$ that in this case is a discrete fibration over $D^{op}\times C$

Well... until now we cheated a bit. In order to get a bicategory we need to define a composition law for 1-cells and show that it is bifunctorial, and I didn't tell you how to do it: but it turns out it is really easy, if you know coend-fu! Indeed, the intuition of a bimodule as a "matrix indexed by its domain" and the rule to compose two relations guide us to find an expression to meaningfully compose $Q : A \mathrel{&#8696;} B, P : B \mathrel{&#8696;} C$. We can define
$$
(P \diamond Q) (a,c) = \int^b P(a,b)\times Q(b,c)
$$
boils down, on discrete domains $A,B\in\Set$ to a "matrix product of sets" like
$$
(P \diamond Q)_{a c} = \sum_{b\in B} P_{a b}\times Q_{b c}
$$
There is also a connection between the ways in which profunctors compose, and the way in which _relations_ do. Indeed, look how the two concepts closely resemble each other:
$$
\begin{array}{cccccc}
(x,z)\in S\circ R & \iff & \exists y\in Y & \big((x,y)\in R\big) & \wedge & \big((y,z)\in S\big) \\
  (P\diamond Q)(x,z) & = & \int^y & Q(x,y) & \times & P(y,z) \\
\end{array}
$$
Finally: yes, you can make this precise by saying that sets are discrete categories, or even more precisely categories enriched over [truth values](https://ncatlab.org/nlab/show/%28-1%29-categoryhttps://ncatlab.org/nlab/show/%28-1%29-category), and that relations are precisely the $\{0,1\}$-enriched version of profunctors, as they are functions $A\times B \to \{0,1\}$!

# Doubles for monoidal categories

One of the key results of the paper
[Doubles for Monoidal Categories](http://www.tac.mta.ca/tac/volumes/21/4/21-04abs.html)
is the canonical equivalence of categories:
$$
\mathbf{Tamb}(\mathcal{C}) \simeq [\mathbf{Doub}(\mathcal{C}), \mathbf{Set}]
$$
This theorem has since been labelled by some as the
"fundamental theorem of optics", as it provides the
link between the category of Tambara modules
$\mathbf{Tamb}(\mathcal{C})$ and the double $\mathbf{Doub}(\mathcal{C})$ of the monoidal category $\mathcal{C}$, now also known as the *category of optics*.
To unpack this theorem, we first begin with the definition of a Tambara module.

## Tambara modules

The category of (bi)modules $\mathbf{Mod}$ forms a bicategory, however when we choose a particular category
$\mathcal{C}$ we may instead consider the monoidal category $\mathbf{Mod}(\mathcal{C})$ whose:

- objects are endomodules $P \colon \mathcal{C}^{op} \times \mathcal{C} \rightarrow \mathbf{Set}$;
- morphisms are natural transformations;
- monoidal product is module composition:
  $$
  (P \diamond Q) (X,Y) = \int^Z P(X,Y)\times Q(Y,Z)
  $$
  One may ask the question: *what happens when $\mathcal{C}$ has the structure of a monoidal   category?*

**Definition**: Let $\mathcal{C}$ be a monoidal category.
A (left) *Tambara module* on $\mathcal{C}$ consists of:

- a profunctor $P \colon \mathcal{C}^{op} \times \mathcal{C} \rightarrow \mathbf{Set}$;
- a family of functions
$\tau_{A}(X,Y) \colon P(X, Y) \rightarrow P(A \otimes X, A \otimes Y)$ called the *Tambara structure maps*, which
are natural in $X, Y$ and dinatural in $A$, satisfying
the equations:


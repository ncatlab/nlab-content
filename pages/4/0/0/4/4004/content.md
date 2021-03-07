
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $T\colon A\to B$ be a [[functor]] such that $A$ has a [[terminal object]] $1$.  Then $T$ can canonically be factored as the composite

$$ 
  A \overset{T_1}{\to} B/T1 \overset{\Sigma_{T1}}{\to} B
$$

of $T$ applied to the [[slice category]] $A \simeq A/1$, followed by [[dependent sum]] (projection on the source). 

We say that $T$ is a **parametric right adjoint**, or **p.r.a.**, if the functor $T_1$ is a [[right adjoint]].  Parametric right adjoints are also called **local right adjoints**.

A [[monad]] is called **p.r.a.** if its functor part is p.r.a. and moreover its unit and multiplication are [[cartesian natural transformation|cartesian]].  Thus in particular it is a [[cartesian monad]].  A p.r.a. monad is also called a **strongly cartesian monad**.

## Properties

* Since $\Sigma_{T1}$ [[created limit|creates]] [[connected limits]], if $T$ is p.r.a. then it [[preserved limit|preserves]] connected limits, and in particular preserves [[pullbacks]].  It follows that any p.r.a. monad is a [[cartesian monad]].

* Conversely, an [[accessible functor]] between [[presheaf categories]] is p.r.a. if and only if it preserves [[connected limits]].

* Any [[polynomial functor]] $\Sigma_h \Pi_g f^*$ is p.r.a., since then $T_1$ can be identified with $\Pi_g f^*$, which has the left adjoint $\Sigma_f \; g^*$.

* If $E$ is a [[presheaf category]] and $T\colon E \to Set$ is p.r.a., then the [[comma category]] $Set/T$ (also called the [[Artin gluing]] in this context) is again a presheaf category.  Conversely, if $Set/T$ is a presheaf category, then $T$ preserves connected limits, and thus is p.r.a. if it is accessible.

* A parametric right adjoint functor has in particular a left [[multi-adjoint]], which sends each object $b\in B$ to the family of all units $\eta_{b,i} : b \to T L(b,i)$, where $i$ ranges over all morphisms $b\to T 1$ and $L : B/T1 \to A$ is the left adjoint of $T_1$.  This is because any morphism $b\to T a$ induces a unique composite $i:b \to T a \to T 1$, and hence a unique factorization through $L(b,i)$.

## Generic morphisms

Central to the theory of parametric right adjoints is the notion of *$T$-generic* morphisms.  For any functor $T$, a morphism $f\colon B\to T A$ is (strictly) **$T$-generic** if any commutative square of the following form:
$$\array{B & \overset{\alpha}{\to} &T X \\
  ^f\downarrow && \downarrow^{T\gamma}\\
  T A& \underset{T \beta}{\to} & T Z}$$
has a unique filler of the form $T\delta : T A \to T X$.  A **generic factorization** of a map $f\colon B\to T A$ is a factorization
$$ B \overset{g}{\to} T D \overset{T h}{\to} T A $$
such that $g$ is $T$-generic.  Note that by the definition of genericity, generic factorizations are unique whenever they exist.  If $T$ is a monad and any map $B \to T A$ has a generic factorization, then there is an induced [[orthogonal factorization system]] on the [[Kleisli category]] of $T$ in which $T$-generic maps are the left class and the right class are the "free" maps, i.e. those which factor through the unit of $T$.

+-- {: .un_prop}
###### Proposition
A functor $T$ is a parametric right adjoint iff every map $B\to T A$ has a generic factorization.
=--
+-- {: .proof}
###### Proof
This is Proposition 2.6 of [(Weber08)](#Weber08).
=--

P.r.a. functors between presheaf categories have an especially nice form.

+-- {: .un_prop}
###### Proposition
A functor $T\colon [I^{op},Set] \to [J^{op},Set]$ between presheaf categories is p.r.a. iff any map $y(j)\to T 1$ has a generic factorization, where $y(j)$ is the representable presheaf on an object $j\in J$.
=--
+-- {: .proof}
###### Proof
This is Proposition 2.10 of "Familial 2-functors and parametric right adjoints."  The "only if" direction is the previous proposition, while for the "if" direction, the given hypothesis allows us to define the functor
$$ E_T \colon y/T1 \to [I^{op},Set] $$
sending an object $(y(j) \to T 1)$ to the object occurring in its generic factorization.  Note that $y/T1$ is equivalently the opposite of the [[category of elements]] of $T1$.  The definition of genericity, along with the Yoneda lemma, then shows that
$$ T(Z)(j) = \coprod_{x\in T1(j)} [I^{op},Set](E_T(x),Z) $$
which preserves connected limits, since it is a coproduct of representables.
=--

In particular, a p.r.a. functor $T\colon [I^{op},Set] \to [J^{op},Set]$ is determined by giving the object $T1\in [J^{op},Set]$ together with the functor $E_T\colon y/T1 = el(T1)^{op} \to [I^{op},Set]$.  We can think of $T1(j)$ as the setof all possible "shapes" which $T$ allows us to "glue together" to obtain an element of shape $j$, and $E_T$ as specifying exactly what each of those shapes looks like.  Then the above formula for $T(Z)(j)$ says that we look at all possible shapes $x\in T1(j)$ we can glue to get something of shape $j$, and for each such $x$ we look at all the "diagrams" in $Z$ of the corresponding shape $E_T(x)$.

We can extract from this a description that is clearly a generalization of a [[polynomial functor]].

+-- {: .un_prop}
###### Proposition
A functor $T\colon [I^{op},Set] \to [J^{op},Set]$ between presheaf categories is p.r.a. iff when expressed in terms of [[discrete fibrations]], it is the composite
\[ DFib/I \xrightarrow{d^*} DFib/E \xrightarrow{c_*} DFib/K \xrightarrow{p_!} DFib/J \]
for a polynomial in $Cat$
\[ I \xleftarrow{d} E \xrightarrow{c} K \xrightarrow{p} J \]
where $p$ is a discrete fibration and $(d,c)$ is a [[two-sided discrete fibration]] (with in particular $d$ a discrete fibration and $c$ a discrete opfibration).
=--
+-- {: .proof}
###### Proof
Let $p$ be the [[Grothendieck construction]] of $T1$, so that $K = el(T1)^{op}$, and $(d,c)$ the two-sided Grothendieck construction of $E_T\colon el(T1)^{op} \to [I^{op},Set]$ regarded as a profunctor from $K$ to $I$.  The above formula tells us that $T = Lan_p \circ Hom(E_T,-)$, and when rewritten in terms of discrete fibrations this gives the above formula.  More details are in Remark 2.12 of [(Weber08)](#Weber08).
=--

That is, a p.r.a. functor between presheaf categories is the restriction to discrete fibrations of a certain kind of polynomial functor between slices of $Cat$.  When $I$ and $J$ are discrete categories, then so are $K$ and $E$, so that p.r.a. functors between presheaf categories are a direct generalization of polynomial functors between slices of $Set$.  But on the other hand, we can also say that polynomial functors between slices of *Cat* are a direct generalization of p.r.a. functors between presheaf categories.


## Examples

### Free categories

Consider the [[free category]] monad $T$ on the category $Quiv$ of [[quivers]], such that $T A$ is the quiver with the same objects as $A$ and whose arrows are finite composable strings of arrows in $A$..  Here $T 1$ is the monoid $\mathbb{N}$ regarded as a one-object category, and thus an object of $Quiv/T1$ is a quiver together with a natural number assigned to each edge.  For any quiver $A$, the natural augmentation $T A \to T 1$ assigns to each composable string of arrows its length.

The left adjoint of this functor $T_1\colon Quiv \to Quiv/T1$ takes as input a quiver with natural number "lengths" assigned to each of its arrows, and creates a new quiver by gluing together a copy of the quiver $[n] = (0 \to 1 \to\dots \to n)$ (with no arrows other than those drawn) for each arrow of "length" $n$.  Thus $T$ is a parametric right adjoint.

$Quiv$ is of course a presheaf category $[Q^{op},Set]$, where $Q$ is the category $0 \rightrightarrows 1$.  The category $y/T1$, i.e. the opposite of the category of elements of $T1$, has objects $\mathbb{N} \sqcup \{\bot\}$ and nonidentity arrows $\bot \rightrightarrows n$ for all $n\in\mathbb{N}$.  Finally, the functor $E_T \colon y/T1 \to Quiv$ sends $\bot$ to the quiver with one object and no arrows, and $n$ to the quiver $[n] = (0 \to 1 \to\dots \to n)$ described above.

## References

* [[Aurelio Carboni]] and [[Peter Johnstone]], _Connected limits, familial representability and Artin glueing_, [MR](http://www.ams.org/mathscinet-getitem?mr=1377312)

* [[Mark Weber]], _Generic morphisms, parametric representations, and weakly cartesian monads_, Theory and applications of categories, 13:191&#8211;234, 2004. [link](http://www.tac.mta.ca/tac/volumes/13/14/13-14abs.html)

* [[Mark Weber]], _Familial 2-functors and parametric right adjoints_, 2008 [link](http://www.tac.mta.ca/tac/volumes/18/22/18-22abs.html)
 {#Weber08}

* {#BMW} [[Clemens Berger]], [[Paul-André Melliès]], [[Mark Weber]], _Monads with Arities and their Associated Theories_ (2011) ([arXiv:1101.3064](http://arxiv.org/abs/1101.3064))

[[!redirects parametric right adjoints]]
[[!redirects p.r.a. functor]]
[[!redirects p.r.a. functors]]
[[!redirects p.r.a. monad]]
[[!redirects p.r.a. monads]]

[[!redirects local right adjoint]]
[[!redirects local right adjoints]]
[[!redirects strongly cartesian monad]]
[[!redirects strongly cartesian monads]]

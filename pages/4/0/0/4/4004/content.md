
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

Let $T\colon A\to B$ be a [[functor]] such that the [[category]] $A$ has a [[terminal object]] $1$.  Then $T$ can canonically be factored as the composite

$$ 
  A 
   \overset{\;\;T_1\;\;}{\longrightarrow} 
  B/T1 
   \overset{\;\;\Sigma_{T1}\;\;}{\longrightarrow} 
  B
$$

of $T$ applied to the [[slice category]] $A \simeq A/1$, followed by [[dependent sum]] (projection on the source). 

We say that $T$ is a **parametric right adjoint**, or **p.r.a.**, if the functor $T_1$ is a [[right adjoint]].  Parametric right adjoints are also called **local right adjoints**, though this terminology conflicts with that of [[local adjunctions]] (see [[locally]]). It is equivalent to the notion of right [[multi-adjoint]], but [[multi-adjoints]] can be formulated without assuming $A$ has a terminal object.

A [[monad]] is called **p.r.a.** if its functor part is p.r.a. and moreover its unit and multiplication are [[cartesian natural transformation|cartesian]].  Thus in particular it is a [[cartesian monad]].  A p.r.a. monad is also called a **strongly cartesian monad**.

## Properties

* Since $\Sigma_{T1}$ [[created limit|creates]] [[connected limits]], if $T$ is p.r.a. then it [[preserved limit|preserves]] connected limits, and in particular preserves [[pullbacks]].  It follows that any p.r.a. monad is a [[cartesian monad]].

* Conversely, a [[functor]] between [[presheaf categories]] is p.r.a. if it preserves [[connected limits]]. The reason is that (in the notation above), if $T$ preserves connected limits, then $T_1$ preserves all small limits, and a limit-preserving functor from a [[cototal category]] such as a presheaf category to a locally small category is a right adjoint. 

* Any [[polynomial functor]] $\Sigma_h \Pi_g f^*$ is p.r.a., since then $T_1$ can be identified with $\Pi_g f^*$, which has the left adjoint $\Sigma_f \; g^*$.

* If $E$ is a [[presheaf category]] and $T\colon E \to Set$ is p.r.a., then the [[comma category]] $Set/T$ (also called the [[Artin gluing]] in this context) is again a presheaf category.  Conversely, if $Set/T$ is a presheaf category, then $T$ preserves connected limits, and thus is p.r.a.

* A parametric right adjoint functor (with [[locally small category|locally small]] codomain) has in particular a left [[multi-adjoint]], which sends each object $b\in B$ to the family of all units $\eta_{b,i} : b \to T L(b,i)$, where $i$ ranges over all morphisms $b\to T 1$ and $L : B/T1 \to A$ is the left adjoint of $T_1$.  This is because any morphism $b\to T a$ induces a unique composite $i:b \to T a \to T 1$, and hence a unique factorization through $L(b,i)$.  Conversely, if $A$ has a terminal object and $T:A\to B$ has a left multi-adjoint, then it is a parametric right adjoint.

## Generic morphisms

Central to the theory of parametric right adjoints is the notion of *$T$-generic* morphisms:

\begin{definition}
\label{TGenericMorphisms}
For any [[functor]] $T$, a morphism $f \colon B\to T A$ is (strictly) **$T$-generic** if any [[commutative square]] of the following form:
$$
  \array{
    B 
    & 
    \overset{\alpha}{\longrightarrow} & 
    T X 
    \\
    \mathllap{{}^f}
    \big\downarrow 
    && 
    \big\downarrow
    \mathrlap{{}^{T\gamma}}
    \\
    T A
    & 
    \underset{T \beta}{\longrightarrow} 
    & 
    T Z
  }
$$
has a (unique) [[lift]] of the form $T\delta \colon T A \longrightarrow T X$ such that also $\gamma \circ \delta = \beta$; this lift then called a *$T$-fill*.  
\end{definition}
(cf. [Weber 2004 Def 5.2](#Weber2004)).

\begin{definition}
A **generic factorization** of a map $f\colon B\to T A$ is a factorization
$$ 
  B 
    \overset{g}{\longrightarrow} 
  T D 
    \overset{T h}{\longrightarrow} 
  T A 
$$
such that $g$ is $T$-generic (Def. \ref{TGenericMorphisms}).
\end{definition}
(cf. [Weber 2004 Def 5.4](#Weber2004)).

Note that by the definition of genericity, generic factorizations are unique whenever they exist.  If $T$ is a monad and any map $B \to T A$ has a generic factorization, then there is an induced [[orthogonal factorization system]] on the [[Kleisli category]] of $T$ in which $T$-generic maps are the left class and the right class are the "free" maps, i.e. those which factor through the unit of $T$.

+-- {: .un_prop}
###### Proposition
A functor $T$ is a parametric right adjoint iff every map $B\to T A$ has a generic factorization.
=--
+-- {: .proof}
###### Proof
This is Proposition 2.6 of [(Weber08)](#Weber08).  In fact, the generic factorizations are precisely the universal maps in the left multi-adjoint of $F$ mentioned above.
=--

P.r.a. functors between presheaf categories have an especially nice form.

+-- {: .un_prop}
###### Proposition
A functor $T\colon [I^{op},Set] \to [J^{op},Set]$ between presheaf categories is p.r.a. iff any map $y(j)\to T 1$ has a generic factorization, where $y(j)$ is the representable presheaf on an object $j\in J$.
=--
+-- {: .proof}
###### Proof
This is Proposition 2.10 of [(Weber08)](#Weber08). The "only if" direction is the previous proposition, while for the "if" direction, the given hypothesis allows us to define the functor
$$ E_T \colon y/T1 \to [I^{op},Set] $$
sending an object $(y(j) \to T 1)$ to the object occurring in its generic factorization.  Note that $y/T1$ is equivalently the opposite of the [[category of elements]] of $T1$.  The definition of genericity, along with the Yoneda lemma, then shows that
$$ T(Z)(j) = \coprod_{x\in T1(j)} [I^{op},Set](E_T(x),Z) $$
which preserves connected limits, since it is a coproduct of representables.
=--

In particular, a p.r.a. functor $T\colon [I^{op},Set] \to [J^{op},Set]$ is determined by giving the object $T1\in [J^{op},Set]$ together with the functor $E_T\colon y/T1 = el(T1)^{op} \to [I^{op},Set]$.  We can think of $T1(j)$ as the setof all possible "shapes" which $T$ allows us to "glue together" to obtain an element of shape $j$, and $E_T$ as specifying exactly what each of those shapes looks like.  Then the above formula for $T(Z)(j)$ says that we look at all possible shapes $x\in T1(j)$ we can glue to get something of shape $j$, and for each such $x$ we look at all the "diagrams" in $Z$ of the corresponding shape $E_T(x)$.

We can extract from this a description that is clearly a generalization of a [[polynomial functor]].

+-- {: .num_prop #AsPolynomial}
###### Proposition
A functor $T\colon [I^{op},Set] \to [J^{op},Set]$ between presheaf categories is p.r.a. iff when expressed in terms of [[discrete fibrations]], it is the composite
\[ DFib/I \xrightarrow{d^*} DFib/E \xrightarrow{c_*} DFib/K \xrightarrow{p_!} DFib/J \]
for a polynomial in $Cat$
\[ I \xleftarrow{d} E \xrightarrow{c} K \xrightarrow{p} J \]
where $p$ is a discrete fibration and $(d,c)$ is a [[two-sided discrete fibration]] (with in particular $d$ a fibration and $c$ an opfibration).
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

* [[Aurelio Carboni]] and [[Peter Johnstone]], _Connected limits, familial representability and Artin glueing_, Mathematical Structures in Computer Science **5(4)**, 1995, pp. 441 - 459. ([MR:1377312](http://www.ams.org/mathscinet-getitem?mr=1377312), [doi:10.1017/S0960129500001183](https://doi.org/10.1017/S0960129500001183))

Parametric right adjoints were introduced in:

* [[R. Street]], _The petit topos of globular sets_ , Journal of Pure and Applied Algebra **154**, 2000, pp. 299-315. (<a href="https://doi.org/10.1016/S0022-4049(99)00183-8">doi:10.1016/S0022-4049(99)00183-8</a>)

See also:

* {#Weber2004} [[Mark Weber]]: _Generic morphisms, parametric representations, and weakly cartesian monads_, Theory and Applications of Categories **13** 14 (2004) 191-234. &lbrack;[tac:13-14](http://www.tac.mta.ca/tac/volumes/13/14/13-14abs.html)&rbrack;

* {#Weber08} [[Mark Weber]]: _Familial 2-functors and parametric right adjoints_, Theory and Applications of Categories **18** 22 (2007) 665-732 &lbrack;[tac](http://www.tac.mta.ca/tac/volumes/18/22/18-22abs.html)&rbrack;
 
* {#BMW} [[Clemens Berger]], [[Paul-André Melliès]], [[Mark Weber]], _Monads with Arities and their Associated Theories_, Journal of Pure and Applied Algebra **216**, 2011. ([arXiv:1101.3064](http://arxiv.org/abs/1101.3064), [doi:10.1016/j.jpaa.2012.02.039](https://doi.org/10.1016/j.jpaa.2012.02.039))

In [[database theory]] p.r.a.s between copresheaf categories, known as _data migration functor_, are treated in

* {#Spivak10} [[David Spivak]], _Functorial Data Migration_, Information and Computation **217**, 2012. ([arXiv:1009.1166](https://arxiv.org/abs/1009.1166), [doi:10.1016/j.ic.2012.05.001](https://doi.org/10.1016/j.ic.2012.05.001))

For a discussion of the extension of the [[orthogonal factorisation system]] on the [[Kleisli category]] to the [[Eilenberg–Moore category]], see the discussion in:

* [Pullback-homomorphisms](https://golem.ph.utexas.edu/category/2010/08/pullbackhomomorphisms.html), n-Category Café (2010)

[[!redirects parametric right adjoints]]
[[!redirects p.r.a. functor]]
[[!redirects p.r.a. functors]]
[[!redirects p.r.a. monad]]
[[!redirects p.r.a. monads]]

[[!redirects local right adjoint]]
[[!redirects local right adjoints]]
[[!redirects strongly cartesian monad]]
[[!redirects strongly cartesian monads]]

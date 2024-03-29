
# Alternating functions
* table of contents
{: toc}

## Idea

In [[linear algebra]], alternating [[multilinear functions]] are well known, and are in many cases (over the [[real numbers]], for example) are equivalent to [[antisymmetric multifunction|antisymmetric functions]].  In cases where they differ (such as in [[characteristic]] $2$), it is often the alternating functions that behave better.

Actually, being alternating is not, in itself, really about linearity, and we can abstract away to a nonlinear concept of _alternating function_.  (That said, there is one bit of very mild linear structure that is needed: a [[basepoint]] in the [[target]] set.)

The property of being alternating is called _alternation_ (rather than alternatingess), although in principle one could also use _alternating_ as a noun.


## Definitions

Let $X$ be a [[set]], and let $(Y,0)$ be a [[pointed set]] (so $Y$ is a set and $0$ is one of its elements).  Let $n$ be a [[natural number]] (or indeed any [[cardinal number]]).  Recall that a [[multifunction]] of [[arity]] $n$ to $Y$ from $X$ is the same thing as a [[function]] to $Y$ from the $n$-fold [[cartesian power]] $X^n$.

An __alternating multifunction__ (or simply _alternating function_) of arity $n$ from $X$ to $(Y,0)$ is a multifunction of arity $n$ from $X$ to $Y$ such that, whenever two of the function\'s arguments are equal, the value of the function is $0$.  In arity $0$ or $1$, every multifunction is trivially alternating; in arity $2$, we can write this as the [[equational law]] $f(a,a) = 0$; in arity $3$, we have the equational laws $f(a,a,b) = 0$, $f(a,b,a) = 0$, and $f(a,b,b) = 0$; etc.


## Properties

There are many nice properties of alternating *[[multilinear function|multilinear]]* functions.  So suppose that $X$ and $Y$ are [[modules]] over a [[base rig]] $K$ and that $f$ is a multilinear function from $X$ to $Y$; use the usual [[zero]] element of the module $Y$ as the basepoint $0$.  In the case where $Y$ is $K$ itself, we speak of an __alternating form__ (a phrase which is usually taken to include multilinearity).

We will sometimes want to assume that scalar multiplication by $2$ is cancellable in $Y$ (which for example is always the case when $2$ is invertible in $K$, in particular when $K$ is a [[field]] of [[characteristic]] other than $2$), but only when stated.  Since alternation requires looking at two arguments of $f$, we will often, when this leads to no loss of generality, assume that these are the first two arguments, writing $\vec{z}$ to represent all of the other arguments.

+-- {: .num_prop #alterationImpliesAntisymmetry}
###### Proposition

An alternating [[multilinear function]] is [[antisymmetric function|antisymmetric]].
=--

+-- {: .proof}
By multilinearity,
$$ f(x+y,x+y,\vec{z}) = f(x,x,\vec{z}) + f(x,y,\vec{z}) + f(y,x,\vec{z}) + f(y,y,\vec{z}) .$$
Applying alternation, most of these terms vanish:
$$ 0 = 0 + f(x,y,\vec{z}) + f(y,x,\vec{z}) + 0 .$$
Therefore,
$$ f(x,y,\vec{z}) + f(y,x,\vec{z}) = 0 ,$$
which is antisymmetry.
=--

+-- {: .num_prop #antisymmetryImpliesAlternation}
###### Proposition

If multiplication by $2$ is cancellable in $Y$, then an [[antisymmetric function|antisymmetric]] function to $Y$ is alternating.
=--

+-- {: .proof}
###### Proof

By antisymmetry,
$$ f(x,x,\vec{z}) + f(x,x,\vec{z}) = 0 ,$$
or equivalently
$$ 2 f(x,x,\vec{z}) = 2 \cdot 0 .$$
Cancelling $2$,
$$ f(x,x,\vec{z}) = 0 ,$$
which is alternation.
=--

+-- {: .num_remark #antisymmetryWarning}
###### Remark

It is false in both directions to state in general that alternating functions and antisymmetric functions are the same, but for different reasons.  An alternating function must be antisymmetric *if* it is multilinear, regardless of the behaviour of $2$, but not when it is nonlinear; an antisymmetric function must be alternating *if* multiplication by $2$ is cancellable in the target, regardless of linearity, but not when $2$ is noncancellable.

The simplest strongest-possible counterexamples are
$$ (x,y \mapsto |y-x|)\colon \mathbb{R}^2 \to \mathbb{R} ,$$
which is alternating but not antisymmetric, and
$$ (x,y \mapsto x y)\colon \mathbb{F}_2^2 \to \mathbb{F}_2 ,$$
which is antisymmetric but not alternating.

Of course, alternating and antisymmetric functions *are* the same in the context of multilinear functions to a module in which $2$ is cancellable, in particular for multilinear functions between [[vector fields]] over the [[real numbers]].
=--

+-- {: .num_remark}
###### Remark

The [[alternating groups]] are really about antisymmetric functions rather than alternating functions as such.  (Whereas a [[symmetric function]] is preserved by the application of any element of the [[symmetric group]], an antisymmetric function is preserved by and only by the elements of the alternating group.)  Nevertheless, this precise distinction between 'alternating' and 'antisymmetric' is well established in the theory of vector spaces over a field of [[characteristic]] $2$ (in which multiplication by $2$ is as uncancellable as possible).
=--


## Constructive aspects

In [[constructive mathematics]], we usually assume that the arity $n$ of $f$ has [[decidable equality]], which is true if $n$ is a [[natural number]] (which is most common) or even a (possibly infinite) [[extended natural number]].  However, as long as the arity is equipped with an [[inequality]], then we can state the definition: whenever equal arguments have inequal indices, the value of the multifunction $f$ there is zero.  If $X$ and $Y$ are also equipped with inequalities, then $f$ is __strongly alternating__ if, whenever its value is inequal to $0$ in $Y$, then arguments with inequal indices must be inequal in $X$.  (In arity $2$, for example, if $f(a,b) \ne 0$, then $a \ne b$.)  If the inequality on $Y$ is [[tight relation|tight]] (so that its [[negation]] is [[equality]] in $Y$), then every strongly alternating function is alternating, but the reverse requires [[excluded middle]] in general.


[[!redirects alternating multifunction]]
[[!redirects alternating multifunctions]]
[[!redirects alternating multimap]]
[[!redirects alternating multimaps]]

[[!redirects alternating function]]
[[!redirects alternating functions]]
[[!redirects alternating map]]
[[!redirects alternating maps]]


[[!redirects alternating multilinear function]]
[[!redirects alternating multilinear functions]]
[[!redirects alternating multilinear map]]
[[!redirects alternating multilinear maps]]


[[!redirects alternating form]]
[[!redirects alternating forms]]

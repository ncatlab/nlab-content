#Definition

Let $(T, \mu, \nu)$ be a
[[monad]] on a category $C$.
Specifically, $T: C \to C$ is a functor,
and $\mu: T^2 \to T$ and 
$\nu: \mathrm{Id}_C \to T$ are natural
transformations, satisfying unital and associative
axioms making $T$ a monoid in the (strict)
monoidal category $\mathrm{End}(C)$.
This monad is cartesian if

* the category $C$ has all pullbacks,
* the functor $T$ preserves pullbacks,
* the natural transformations $\mu$ and $\nu$
  are cartesian.
  A natural transformation $\alpha: S \to T$
  between functors $C \to D$
  is cartesian if for each map $f: A \to B$
  in $C$, the naturality square
  \[\array{
    S A & \overset{S f}{\to} & S B \\
    \alpha_A \downarrow & & \downarrow \alpha_B \\
    T A & \underset{T f}{\to} & T B
  }\]
  is a pullback.

# Examples

* The free [[monoid]] monad $(-)^*: Set \to Set$ is cartesian. 

* The free [[category]] monad acting on [[directed graph]]s is cartesian.

* The free strict $\omega$-[[strict omega-category|category]] monad acting on [[globular set]]s, $T: Set^{G^{op}} \to Set^{G^{op}}$, is cartesian. 

#Remarks

There is some slight inconsistency in the use of
the word _cartesian_ in category theory.
Typically, a category (resp. functor)
is called cartesian if it has (resp. preserves)
all finite limits.
In most examples of cartesian monads, the category
$C$ has a terminal object, and hence finite limits.
However, the functor $T$ almost never preserves
terminal objects.
For example, the free monoid monad on
$\mathrm{Set}$ is cartesian, as can be checked
directly, but $T 1 \simeq \mathbb{N}$ is not
a terminal object.

+--{.query}
I would call a category with all pullbacks 'locally cartesian'.  Shouldn\'t a cartesian category at least have a terminal object?  Would a terminal object make any difference here?  &#8212;[[Toby Bartels|Toby]]

I think you're right about the standard terminology.
Both Tom Leinster and Jurgen Koslowski ([pdf](http://www.tac.mta.ca/tac/volumes/14/7/14-07.pdf))
use the terminology above.
I'm not sure how we want to resolve this here.
I'll think about it, and look at the standard references, and fix the terminology on this page if nobody else does first.  -Patrick

How is this?  -Patrick

_[[Mike Shulman|Mike]]_: The [[Elephant]] definitely uses "cartesian" to mean "all finite limits."  However, I'm not sure how universal that is; I think at least in the past, some people have used "cartesian" to refer only to finite _products_.  I'm sure that a "cartesian object" in a 2-category has been defined to be one such that $A\to A\times A$ and $A\to 1$ have right adjoints.  Also the notion of "cartesian bicategory" refers only to finite products (and extra stuff too).  And [[cartesian monoidal category]] and [[cartesian closed category]] certainly only means finite products.  On the other hand, of course as you say, in this context "cartesian monads" only refer to pullbacks, not terminal objects and hence not products.  There is also the use of "cartesian square" to mean a pullback square, which generalizes to "cartesian morphism" in a [[Grothendieck fibration|fibration]].
=--

#References

* Tom Leinster, _Higher Operads, Higher Categories_ 
  ([arXiv](http://arxiv.org/abs/math.CT/0305049)),
  section 4.1


# Racks
* table of contents
{: toc}

## Idea

A rack is a set equipped with a binary operation satisfying axioms analogous to the second and third [[Reidemeister moves]] in knot theory.  The most commonly appearing racks in nature are [[quandle|quandles]], which satisfy an additional axiom analogous to the first Reidemeister move.

While mainly used to obtain invariants of framed knots, racks are interesting algebraic structures in their own right: they capture the idea of an algebraic structure where every element acts as an automorphism of that structure.


## Definition

A **rack** may be defined as a set $R$ with a binary operation $\triangleright$ such that
for every $a, b, c \in R$ the **[[self-distributive law]]** holds:

$$a \triangleright (b \triangleright c) = (a  \triangleright b)\triangleright (a \triangleright  c)$$

and for every $a,b \in R$ there exists a unique
$c \in R$ such that 

$$a \triangleright c = b$$

This definition, while terse and commonly used, is suboptimal for certain purposes because it contains an [[existential quantifier]] which is not really necessary. To avoid this,  we may write the unique $c \in R$ such that $a \triangleright c = b$ as $b \triangleleft a$.  We then have

$$ a \triangleright c = b \iff  c = b \triangleleft a $$

and thus 

$$ a \triangleright (b \triangleleft a) = b$$ 

and

$$(a \triangleright b) \triangleleft a = b$$

Using this idea, a rack may be equivalently defined as a set $R$ with two binary operations $\triangleright$ and $\triangleleft$ such that for all $a, b, c \in R$:

\[ a \triangleright (b \triangleright c) = (a \triangleright b)\triangleright (a \triangleright  c)   \]

\[ (c \triangleleft b) \triangleleft a = (c \triangleleft a)\triangleleft (b \triangleleft a)  \]

\[ (a \triangleright b)\triangleleft a = b \]

\[ a \triangleright (b \triangleleft a) = a \]

It is convenient to say that the element $a \in R$ is **acting from the left** in the expression $a \triangleright b$, and **acting from the right** in the expression $b \triangleleft a$.  The third and fourth rack axioms then say that these left and right actions are inverses of each other.  Using this, we can eliminate either one of these actions from the definition of rack.  If we eliminate the right action and keep the left one, we obtain the terse definition given initially.   However, the longer definition makes it clear that racks are algebras of [[Lawvere theory]].


## Notations and Conventions

Many different conventions are used in the literature on racks and quandles.  For example, many authors prefer to work with just the _right_ action.  Furthermore, the use of the symbols $\triangleright$ and $\triangleleft$ is by no means universal: many authors use exponential notation 

$$ a \triangleright b = {}^a b $$

and

$$ b \triangleleft a = b^{a} $$

while many others write

$$ b \triangleleft a = b \star a $$

We may equivalently define a rack in the following more conceptual manner: it is a set where each element acts on the left and right as [[automorphism|automorphisms]] of the rack, with the left action being the inverse of the right one.  In this definition, the fact that each element acts as automorphisms encodes the left and right self-distributivity laws, and also these laws:

$$ a \triangleright (b \triangleleft c) = (a \triangleright b)\triangleleft (a \triangleright  c)$$ 

$$(c \triangleright b) \triangleleft a = (c \triangleleft a)\triangleright (b \triangleleft a)$$

which are consequences of the definition(s) given earlier.

## Shelves 

Even simpler than a rack is a **shelf**.  A set with a binary operation $\triangleright$ obeying the left self-distributive law

$$ a \triangleright (b \triangleright c) = (a \triangleright b)\triangleright (a \triangleright  c)   $$

is called a **left shelf**, and similarly a set with a binary operation $\triangleleft$ obeying the right self-distributive law is called a **right shelf**.

A unital left shelf is the same as a graphic monoid: for a proof see [[graphic category]]. 

Shelves make an appearance in set theory via [[large cardinal]] axioms. Let $(V, \in)$ be a model of [[ZFC]], and let $V_\lambda \subseteq V$ be the collection of elements of rank less than an [[ordinal]] $\lambda$ of $V$. One (rather strong) large cardinal axiom on (limit ordinals) $\lambda$ is: 

> There exists an [[elementary embedding]] $j: V_\lambda \to V_\lambda$ on the [[structure]] $(V_\lambda, \in)$ that is not the identity. 

Then, for $A \subseteq V_\lambda$, let $j(A)$ denote the [[image]] under $j$; if we regard $A$ as an unary relation on $V_\lambda$, then $j$ induces an elementary embedding $(V_\lambda, \in, A) \to (V_\lambda, \in, j(A))$. In particular, if $k$ is any elementary embedding $(V_\lambda, in) \to (V_\lambda, \in)$, which as a set of ordered pairs we may regard as a subset of $V_\lambda$, then $j(k)$ as a set of ordered pairs is also an elementary embedding. We get in this way a binary operation $(j, k) \mapsto j(k)$ on elementary embeddings, which we denote as $(j, k) \mapsto j \cdot k$, and it is not difficult to verify that $\cdot$ is left self-distributive. 

Let $F_1$ denote the [[free object|free]] left shelf generated by 1 element. If $E_\lambda$ denotes the collection of elementary embeddings on the structure $(V_\lambda, \in)$, then the preceding observations imply that $E_\lambda$ is a left shelf, so any $j \in E_\lambda$ induces a shelf homomorphism 

$$\phi_j: F_1 \to E_\lambda.$$ 

+-- {: .num_theorem} 
###### Theorem 
**(Laver)** 
If $j \in E_\lambda$ is not the identity, then $\phi_j$ is injective. 
=-- 

The famous *Laver tables* (derived from set-theoretic considerations which we omit for now) describe certain [[finite set|finite]] quotients of $F_1$. Letting $x$ denote the generator of $F_1$, define $x_n$ by $x_1 = x$ and $x_{n+1} = x_n \cdot x$. The quotient of $F_1$ by the single relation $x_{m+1} = x$ is a shelf of cardinality $2^k$, the largest power of $2$ dividing $m$; it is denoted $A_k$. It can be described alternatively as the unique left shelf on the set $\{1, 2, \ldots, 2^k\}$ such that $p \cdot 1 = p + 1 \mod 2^k$ (here $p$ represents the image of $x_p$ under the quotient $F_1 \to A_k$). 

The "multiplication table" of an $A_k$ is called a Laver table. The behavior of Laver tables is largely unknown, but we mention a few facts. The first row consisting of entries $1 \cdot p$ is periodic (of some order dividing $2^k$); under the large cardinal assumption that a nontrivial elementary self-embedding on a $V_\lambda$ exists, this period $f(k)$ tends to $\infty$ as $k$ does, but whether it actually does (as a consequence of ZFC alone) is not known. What *is* known is that this period, even if it increases to $\infty$, does so slowly: if we define $g(m)$ to be the smallest $k$ such that $f(k) \geq m$, then $g$ grows more quickly than say the Ackermann function. 


## References

* Gavin Wraith, [A personal story about knots](http://www.wra1th.plus.com/gcw/rants/math/Rack.html).

* Wikipedia, [Racks and quandles](http://en.wikipedia.org/wiki/Racks_and_quandles)

* Colin Rourke, Roger Fenn, (1992). _Racks and links in codimension 2_. J. Knot Theory and Its Ramifications 1 (4): 343&#8211;406. 

* Roger Fenn, Colin Rourke, Brian Sanderson, _Trunks and classifying spaces_, Appl. Categ. Structures __3__ (1995), no. 4, 321&#8211;356 [MR1364012](http://www.ams.org/mathscinet-getitem?mr=1364012)[doi](http://dx.doi.org/10.1007/BF00872903); _The rack space_, Trans. Amer. Math. Soc. __359__ (2007), no. 2, 701&#8211;740 [MR2255194](http://www.ams.org/mathscinet-getitem?mr=2255194)

* Sam Nelson, [Quandle theory](http://www.esotericka.org/cmc/quandles.html).

* J. Scott Carter, _A survey of quandle ideas_, [arXiv](http://arxiv.org/abs/1002.4429).

* Seiichi Kamada, _Knot invariants derived from quandles and racks_, [arXiv](http://arxiv.org/abs/math/0211096).

* Alissa Crans, _Shelves, racks, spindles and quandles_, [arXiv](http://arxiv.org/PS_cache/math/pdf/0409/0409602v1.pdf#page=56), in _Lie 2-Algebras_, p. 56.

The last reference makes it clear that racks are algebras of a [[Lawvere theory]], so that racks may be defined in any [[cartesian monoidal category]] (a category with finite [[products]]).

* Nicol&#225;s Andruskiewitsch, Mati&#225;s Gra&#241;ab, _From racks to pointed Hopf algebras_, Adv. Math. __178__(2):177--243 (2003, [arxiv](http://arxiv.org/abs/math/0202084) (<a href="http://dx.doi.org/10.1016/S0001-8708(02)00071-3">doi</a>)

A generalization of [[Lie integration]] to conjectural Leibniz groups has been conjectured by [[J-L. Loday]]. A local version via local Lie racks has been proposed in

* Simon Covez, _The local integration of Leibniz algebras_, [arXiv](http://arxiv.org/abs/1011.4112); _On the conjectural cohomology for groups_, [arXiv](http://arxiv.org/abs/1202.2269); _L'int&#233;gration locale des alg&#232;bres de Leibniz_, Thesis (2010), [pdf](http://tel.archives-ouvertes.fr/docs/00/49/54/69/PDF/THESE_Simon_Covez.pdf)

There are also crossed modules for racks:

* Alissa S. Crans, Friedrich Wagemann, _Crossed modules of racks_, [arXiv](http://arxiv.org/abs/1310.4705)

[[!redirects rack]]
[[!redirects racks]]
[[!redirects shelf]]
[[!redirects shelves]]
[[!redirects left shelf]]
[[!redirects left shelves]]
[[!redirects right shelf]]
[[!redirects right shelves]]

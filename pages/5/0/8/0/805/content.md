* here i am...&lt;http://math.ucr.edu/~alex

category: people

## Things I need to work out ##

* Centers

I can not seem to figure out what the idea of Drinfeld center is supposed to be about over at the [[geometric infinity-function theory]] journal club page.  There are probably tons of other things I should be trying to really understand instead, but I am going to be stubborn and fixate on this one.

I want to know what the Drinfeld center is and also why
"the Drinfeld center is not a "sub" in any reasonable sense (except in the loose sense that it's a categorical limit)."

So maybe I should just start listing off different notions of center and trying to understand these and just hope for the best.

What types of centers do I know about?

A monoid $M$ has a center.

A group $G$ has a center.

A ring/algebra $A$ has a center.

These can all be interpreted as $1$-object categories where a morphism is in the center iff it commutes with all other morphisms.  This, of course, makes sense since all morphisms have the same source and target.

Each of these algebraic objects $\mathcal{C}$ has an injection from the center $Z(\mathcal{C})\hookrightarrow \mathcal{C}$.

+-- {: .query}
Bruce, can we finish our conversation here?

"center of Rep(G) = Rep (loop groupoid of G)"
which seems to summarize everything

In this case, it's more like we have
Rep(G) embedding inside Rep (/\G)
=--

In these cases, we interpeted the composition in the category as the binary operation which we could query for commutativity.  As these are all cases of monoids with extra structure, we really want to think of the composition as a monoidal product.  This leads us to a more general notion of the center of a category.

We consider the periodic table of $k$-tuply monoidal $n$-categories described here &lt;http://math.ucr.edu/home/baez/week121.html>.  This generalized center takes us vertically down the columns of the periodic table.  Taking one object versions of the gadget in a certain square takes us southwest down the chart.

From poking around a bit it seems that having these ideas down we are supposed now start thinking about Hopf algebras.

Gotta go eat and for a walk...be back soon.  I had a meatball sub, tea, orange juice and now I am back.

Braided Hopf algebras provide solutions to the braid equation.  The Drinfel'd quantum double construction is a way to get our hands on these starting with finite dimensional Hopf algebras with invertible antipodes.

The quantum double $D(H)$ is the [[bicrossed product]] of the Hopf algebra $H$ and its dual $H^*$.  See Kassel for definitions.  The quantum double contains $H$ and its dual as Hopf subalgebras.  Given a finite group $G$ there is a double construction for its group algebra.

Theorem: Left $D(H)$-modules are the same as crossed $H$-bimodules.

(Need to say what this means and possible relationship to Drinfel'd double.)

See &lt;http://math.ucr.edu/home/baez/neuchl.ps> for the categorification of the Drinfel'd double of a finite group.


## Things I will forget to keep reading if I do not write down some notes here. ##

* Lurie on [Structured spaces](http://arxiv.org/abs/0905.0459)

commutative rings $\rightarrow$ categorical rings

Keep track of extra information (e.g. quotients) by adding extra isomorphisms 
to the obvious discrete categorification of the ring

+-- {: .query}
What is Serre's intersection formula?
=--

To understand the entire formula we need commutative ring structures on $\infty$-groupoids

Two approaches:
1. topological spaces (or simplicial sets) w. comm ring structure axioms satisfied on nose and addition, multiplication are
given by continuous maps

This forms the $\infty$-category SCR (see section 4.1)

2. commutative ring structures on $\infty$-groupoids, axioms hold up to coherent homotopy

This gives theory of (connective $E_\infty$-rings)


For a topological ring we care about homotopy structure not topology

What is correct notion of "generalized rings"?

1. $E_\infty$-ring spectra - apply algebraic topology to commutative algebra

2. simplicial commutative rings - apply commutative algebra to algebraic topology (in particular, stable homotopy theory)

K-theory and other cohomology theories can be endowed with $E_\infty$-structures

DERIVED SCHEMES

scheme - "locally looks like Spec $A$, for some commutative ring $A$"

derived scheme - "locally looks like Spec $A$, for some commutative simplicial ring $A$"

Given a geometry $G$ and a topological space $X$, there is an associated theory of $G$-structures on $X$.

"A $G$-structure on $X$ is a sheaf $O_X$ endowed with some operations."

For appropriate $G$, we recover the classical theory of ringed and locally ringed spaces.


Page 6 gives some general overview for the paper which will be helpful.


#Talk by Sunil Chebolu#

*Life after the Bloch-Kato Conjecture

1. Motivation
Galois theory:  $F \leftarrow K$ Gal. extension

What is $Gal(K/F)$?

Inverse Galois theory: Given base field $F$ and finite group $G$, is there a Galois ext. over $K/F$ such that $Gal(K/F) = G$?

Often $F = \mathbb{Q}$

If yes, then we say $G$ is realizable over $F$.

Example: Is $C_n$ realizable over $\mathbb{Q}$?  Yes.

Proof: Choose a prime $p$ such that $p\cong 1(mod n)$.  Let $\mu$ be a primitive $p^{th}$ root of unity.
\[ 1 + x + x^2 +\cdots + x^{p-1}\]
$n|(p-1)$
\[\mathbb{Q} \leftarrow \mathbb{Q}(\mu)\]

is a field ext. of order $p-1$.
There exists a cyclic subgroup $H$ with
\[|H| = (p-1)/n \leq Gal(\mathbb{Q}(\mu)/\mathbb{Q}) = C_{p-1}\]

So our extension factors through $\mathbb{Q}(\mu)^H$.

\[Gal(\mathbb{Q}(\mu)^H/\mathbb{Q}) = C_n.\]

Theorem: (Kronecker-Weber) Every finite abelian group is realizable over $\mathbb{Q}$.

Theorem: (Safarevich) Every solvable group is realizable over $\mathbb{Q}$  (This is a very deep theorem.)

Absolute Galois group over $\mathbb{Q} = Gal(\bar{\mathbb{Q}}/\mathbb{Q})$ = G_{\mathbb{Q}}.

A finite group $G$ is realizable over the rationals if and only if there exists a (closed) normal subgroup $N &lt; G_{\mathbb{Q}}$ such that $G_{\mathbb{Q}}/N = G$.

So the extension $\bar{\mathbb{Q}}$ over $\mathbb{Q}$ factors through an extension $L$.

2. Absolute Galois groups

$G_F = Gal(F_{sep}/F)$, the absolute Galois group of $G$, which is further equal to 
\[\lim_{[L:F]&lt;\infty}Gal(L/F)\]
the inverse limit of finite groups (pro-finite group).

$G_F$ gives us $H^*(G_F,\mathbb{F}_p)$, Galois cohomology of $F$.
This is equal to
\[\lim_{[L:F]&lt;\infty}H^*(Gal(L/F),\mathbb{F}_p)\]
a graded commutative ring. (This in not the inverse limit)

* Problem: How do we characterize absolute Galois groups amongst the class of all pro-finite groups?

Theorem: (Artin-Schreier)
The only finite subgroup of an absolute Galois group is $\leftbrace 1\rightbrace$ or $C_2$.
In particular, the only finite absolute Galois group is $C_2$,
\[Gal(\mathbb{C}/\mathbb{R}) = C_2.\]

3. Bloch-Kato conjecture

$H^*(G_F,\mathbb{F}_p)$ has generators in degree $1$ and relations in degree $2$.

Milnor $K$-theory

$K_*(F) = T^*(F^*)/&lt;a\otimes b|a+b=1>$

We can construct
\[\eta:K_*(F)\stackrel{\cong}\rightarrow H^*(G_F,\mathbb{F}_p)\]

We start with the Kummer sequence
\[ 1\rightarrow \mu_p\rightarrow F^*_{sep}\stackrel{*^p}\rightarrow F^*_{sep}\rightarrow 1\]
and we get a long exact sequence in cohomology

\[H^0(G_F,F^*_{sep)\rightarrow H^1(G_F,\mathbb{F}_p)\]
=
\[F^*\rightarrow H^1(G_F,\mathbb{F}_p)\]
inclusion
\[T(F^*)\rightarrow H^*(G_F,\mathbb{F}_p)\]
arrow and equals
\[K_*(F)\rightarrow H^*(G_F,\mathbb{F}_p) (Bass-Tate)\]
arrow and equals
\[\eta:K_*(F)\stackrel{\cong}\rightarrow H^*(G_F,\mathbb{F}_p) (Norm residue map)\]

The last isomorphism is the Bloch-Kato conjecture.

4. History

* (1970) Milnor's conjecture ($\eta$) for $p=2$.
* (1980's) Murkurjev & Saslin proved for $*=2$.
* (1996) Voevodsky proved for $p=2$.
* Voevodsky-Rost-Weibel

Joint [work](http://arxiv.org/abs/0905.1364) with Minac and Efrat.

Descending central sequence:
\[G_F = G_F^{(1)}\superset G_F^{(2)}\superset\cdots\]
\[G_F^{(2)} = [G_F,G_F]G_F^p\]
\[G_F^{(n)} = [G_F,G_F^(n-1)]G_F^{(n-1)^p}&lt;G\]

$G_F$ extends $F_{sep}$ over $F$ and factors through the Witt closure of $F$, $F^{(3)}$.

\[G_F^{(3)}:F_{sep}\rightarrow F^{(3)}\]
\[G_F^{[3]}:F^{(3)}\rightarrow F\]

\[G_F\rightarrow G_F^{[3]}\]
gives an inflation map
\[H^*(G_F^{[3]})\rightarrow H^*(G_F)\]

Theorem: (C. Efrat, Minac)
$inf$ (or a closely related map) is an isomorphism.

$H^*(G_F)$ is controlled by a relatively small quotient of $G_F$.

Theorem: (application)

$F(p)$ extends $F$ and is the maximal $p$-extension of $F$ (the composite of all Galois extension over $F$ which have degree power of $p$.

\[A_F = Gal(F(p)/F)\]
is pro-$p$-group, i.e., an inverse limit of $p$-groups.

Let $T$ be a group such that
\[A_F\rightarrow T\rightarrow G_F^{[3]}.  Then $H^*(T,\mathbb{F}_p)$ is NOT generated by $1$-dimensional classes.  In particular, this gives a cohomological characterization of maximal $p$-xtensions (i.e. $F(p)$ is the smallest sufield of $F_{sep}$ whose cohomology is generated by $1$-dimensional classes).
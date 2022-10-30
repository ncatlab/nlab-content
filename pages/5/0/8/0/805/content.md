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


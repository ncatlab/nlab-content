
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Explicit substitutions
* table of contents
{: toc}

## Idea

Ordinary [[substitution]] is a meta-level notion, i.e. an operation *on* [[syntax]].  By contrast, *explicit substitutions* incorporate a notion of substitution as *part* of a syntax.

## Definition/Example

A paradigmatic (and in some sense universal) example is given by adding explicit substitutions to [[simply typed lambda calculus]].  For this we add a new term constructor

$$M\langle x\coloneqq N\rangle$$

denoting internally "the substitution of $N$ for $x$ in $M$".  That this is a term constructor means, for instance, that $x\langle x\coloneqq y\rangle$ is a term distinct from $y$; whereas for the ordinary notion of substitution as an *operation*, $x[x\coloneqq y]$ would be a notation for the result of the operation of substituting the term $y$ for the variable $x$ in the term $x$, which is precisely the term $y$.

The relation between $x\langle x\coloneqq y\rangle$ and $y$ is recovered by modifying the [[reduction]] relation.  We modify the usual [[beta-reduction]] rule $(\lambda x.M)(N) \to M[x\coloneqq N]$ to use an explict substitution instead:

$$(\lambda x.M)(N) \to M\langle x\coloneqq N\rangle$$

and then give reduction rules that mimic the *inductive definition* of the usual *operation* of substitution on terms:

$$\begin{aligned}
x\langle x\coloneqq N\rangle &\to N\\
y \langle x\coloneqq N\rangle &\to y \quad (x\neq y)\\
(M_1 M_2)\langle x\coloneqq N\rangle &\to (M_1 \langle x\coloneqq N\rangle)(M_2 \langle x\coloneqq N\rangle) \\
(\lambda y.M)\langle x\coloneqq N\rangle &\to \lambda y. (M\langle x\coloneqq N\rangle) \quad (x\neq y \;\text{and}\; y \;\text{not free in}\; N)
\end{aligned}$$

(We are being somewhat cavalier about [[variables]]; one can also implement explicit substitutions using [[de Bruijn indices]].)

## Combining substitutions and strong normalization

Note that there is no rule for reducing a term of the form $(M \langle x\coloneqq N\rangle) \langle y\coloneqq P\rangle$.  Instead we have to first reduce $M \langle x\coloneqq N\rangle$ until its "head" is no longer an explicit substitution, and then we can apply reduction rules for the "outer" substitution $\langle y\coloneqq P\rangle$.  We might be tempted to assert a rule such as

$$ (M \langle x\coloneqq N\rangle) \langle y\coloneqq P\rangle \to (M\langle y\coloneqq P\rangle) \langle x\coloneqq N\langle y\coloneqq P\rangle \rangle$$

but such a rule is undesirable because it destroys the [[strong normalization]] property of the reduction system: although every term still *can* be reduced to a [[normal form]], there are also infinite reduction sequences that simply interchange pairs of substitutions forever.

One might hope that this could be avoided by introducing "explicit simultaneous substitutions" with a reduction rule

$$ (M \langle x\coloneqq N\rangle) \langle y\coloneqq P\rangle \to M \langle x\coloneqq N, y\coloneqq P\rangle. $$

Apparently for a long time it was hoped that this would work, but [Mellies](#Mellies) showed that it doesn't: explicit simultaneous substitutions with a rule of this sort also yield infinite reduction sequences.  Note that Mellies worked with a de Bruijn version, so his rules look somewhat different; a version of the counterexample using named variables can be found in [Bloo-Rose](#BlooRose), along with a proof that without any way to "combine substitutions" strong normalization is preserved.

## Categorical Models of Explicit Substitutions

The original calculus of explicit substitutions, considered as a type theory, can be given sound and complete categorical models, in terms of indexed categories. This explicit substitutions construction is parametric in the kind of logic that your terms stand for: the Calculus of Constructions [Ritter] (#Ritter), Intuitionistic Linear Logic [Ghani2000] (#Ghani2000) and propositional Constructive Necessity [Ghani1998] (#Ghani1998) can be given formalizations in terms of explicit substitutions calculi, which helps to show the correctness of the implementation of these type theories.

## The linear substitution calculus

More recently, in 2010 the *linear substitution calculus* was introduced by Delia Kesner and Beniamino Accattoli, which according to Damiano Mazza is based on two fundamental ideas:

> *Explicit substitutions in the $\lambda$-calculus come from [[linear logic]]*: if you write down a term calculus for the $\{\multimap,!\}$ fragment of ILL, however you do it, you're going to see let binders pop up, and these behave very much like explicit substitutions, in the sense that normalization needs commuting conversions. Now, if you take Girard's (call-by-name) embedding of the $\lambda$-calculus in ILL, you see that $\beta$-reduction decomposes exactly along the lines of what an ES calculus would do, with the explicit substitutions corresponding to the let binders for exponentials. While I think that this had been noticed immediately after the introduction of linear logic, Delia and Beniamino took it a step further and designed an ES calculus (the structural $\lambda$-calculus, a precursor to the LSC) by mimicking the behavior of ILL terms which are in the image of Girard's embedding. The upshot is that, since Girard's embedding preserves SN, so does the structural $\lambda$-calculus: linear logic is the "right" way of implementing explicit substitutions.

> *Explicit substitutions should behave like boxes in proof nets*: the let binders mentioned above correspond to what are known as "exponential boxes" in proof nets. Cut-elimination in proof nets has the amazing property (from the rewriting viewpoint) that it does not need commuting conversions. In terms of explicit substitutions, this means that ESs should not need to "move" through a term in order to be applied, one should be able to apply them just where they are created. Rewriting should happen "remotely" or, as they say, "at a distance". Beniamino and Delia noticed that there's a consistent way of generalizing redexes in a term calculus with ESs (no need for proof nets!) so that they are transparent to the presence of ESs. Combine this with the above idea (that ESs should behave like in linear logic, i.e., be "linear", substituting one occurrence at a time) and you obtain the LSC.

The LSC has found applications in:

> **abstract machines**: Beniamino Accattoli, Pablo Barenbaum, and Damiano Mazza showed how the LSC may be related in a very sharp way to a host of abstract machines, for any reduction strategy you can think of (call by name, call by value, call by need). Each strategy in the LSC "distills" an abstract machine, in the sense that the rewriting rules of the LSC are in bijection with the actual computational transitions of the machines, while the "administrative" transitions (needed by the machine to navigate through the term in search for the next redex) sort of "evaporate" and become structural equivalences in the LSC (they relate syntactically different terms which are behaviorally equal). In particular, the LSC gives a slick formulation of (weak) call-by-need.

> **complexity**: for decades, people had been wondering whether $\beta$-reduction is a reasonable cost model for [[computational complexity]].  Most were convinced that the answer was "no", because $\beta$-reduction may make an arbitrary number of duplications in just one step.  Suprisingly, Beniamino Accattoli and Ugo Dal Lago showed that the answer is in fact "yes", and their proof uses the LSC in a crucial way, in particular its capability of succinctly expressing computation thanks to sharing.


## References
* Martín Abadi, Luca Cardelli, Pierre-Louis Curien, and Jean-Jacques Lévy. *Explicit Substitutions*. J. Funct. Program., 1(4):375–416, 1991. doi:10.1017/S0956796800000186.

* [[Paul-André Melliès]], *Typed $\lambda$-calculi with explicit substitution may not terminate*.  In M. Dezani (ed.), Int. Conf. on Typed Lambda Calculus and Applications, Lecture Notes in Computer Science, 1995.

* Roel Bloo and Kristoffer H. Rose, *Preservation of Strong Normalisation in Named Lambda Calculi with Explicit Substitution and Garbage Collection*.  In CSN-95: Computer Science in the Netherlands 1995, [citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.51.5026)
 {#BlooRose}

* Eike Ritter, *Categorical abstract machines for higher-order typed lambda calculi*, Theoretical Computer Science, vol 136, p.125–162, 1994.

* Neil Ghani, Valeria de Paiva and Eike Ritter, *Linear Explicit Substitutions*, Journal of the IGPL, Vol, 8(1), pp.7-31, 2000.

* Neil Ghani, Valeria de Paiva and Eike Ritter, *Explicit substitutions for constructive necessity*, In Larsen, Kim G. and Skyum, Sven and Winskel, Glynn (eds.), Automata, Languages and Programming, 1998.

The linear substitution calculus is discussed in:

* Beniamino Accattoli, _An abstract factorization theorem for explicit substitutions_, [link](https://hal.archives-ouvertes.fr/hal-00780344)

* Beniamino Accattoli, Eduardo Bonelli, Delia Kesner, Carlos Lombardi, _A nonstandard standardization theorem_, [link](https://dl.acm.org/doi/10.1145/2535838.2535886)

* Beniamino Accattoli, Pablo Barenbaum, Damiano Mazza, _Distilling Abstract Machines_, [arxiv](https://arxiv.org/abs/1406.2370)

* Beniamino Accattoli and Ugo Dal Lago, _(Leftmost-outermost) beta reduction is invariant, indeed_, [lmcs](https://lmcs.episciences.org/1627/pdf)

[[!redirects explicit substitutions]]
[[!redirects linear substitution calculus]]
[[!redirects LSC]]

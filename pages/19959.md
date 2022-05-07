
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

but such a rule is undesirable because it destroys the [[strong normalization]] property of the reduction system: although every term still *can* be reduced to a normal form, there are also infinite reduction sequences that simply interchange pairs of substitutions forever.

One might hope that this could be avoided by introducing "explicit simultaneous substitutions" with a reduction rule

$$ (M \langle x\coloneqq N\rangle) \langle y\coloneqq P\rangle \to M \langle x\coloneqq N, y\coloneqq P\rangle. $$

Apparently for a long time it was hoped that this would work, but [Mellies](#Mellies) showed that it doesn't: explicit simultaneous substitutions with a rule of this sort also yield infinite reduction sequences.  Note that Mellies worked with a de Bruijn version, so his rules look somewhat different; a version of the counterexample using named variables can be found in [Bloo-Rose](#BlooRose), along with a proof that without any way to "combine substitutions" strong normalization is preserved.

## References
* Martín Abadi, Luca Cardelli, Pierre-Louis Curien, and Jean-Jacques Lévy. *Explicit Substitutions*. J. Funct. Program., 1(4):375–416, 1991. doi:10.1017/S0956796800000186.

* [[Paul-André Melliès]], *Typed $\lambda$-calculi with explicit substitution may not terminate*.  In M. Dezani (ed.), Int. Conf. on Typed Lambda Calculus and Applications, Lecture Notes in Computer Science, 1995.

* Roel Bloo and Kristoffer H. Rose, *Preservation of Strong Normalisation in Named Lambda Calculi with Explicit Substitution and Garbage Collection*.  In CSN-95: Computer Science in the Netherlands 1995, [citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.51.5026)
 {#BlooRose}

[[!redirects explicit substitutions]]

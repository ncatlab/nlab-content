
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



\tableofcontents

## Idea

The *$\pi$-calculus* is a [[computational]] model for concurrent processes that communicate messages through named channels. It subsumes [[λ-calculus]].

In the monadic (here meaning: *[[unary]]*) $\pi$-calculus, outputs and inputs only send and receive single names, while the polyadic (here meaning: *[[n-ary|$n$-ary]]*) $\pi$-calculus allows outputs of tuples of names and corresponding inputs.

This calculus permits non-[[confluent]] reductions by design, as opposed to other process calculi such as the Interactive Lambda Calculus (ILC).

## Syntax

A process is either:

* an inactive process $0$;
* the parallel composition of two processes $P\mid Q$;
* the replication of a process $!P$;
* a restriction $(\nu n)\,P$ (that is the generation of a fresh name only known to $P$);
* prefixed by an input $n(m).P$;
* prefixed by an output $\overline{n}\langle m\rangle.P$.

Sometimes an [[nondeterministic computation|indeterministic]] choice operator $+$ is added to the syntax.

## Example

* a server that increments the value it receives: $S=!\mathrm{incr}(a,x).\overline{a}\langle x+1\rangle$;
* a client that calls to the $\mathrm{incr}$ server: $C=(\nu a)\bigl(\overline{\mathrm{incr}}\langle a,4\rangle\mid a(y)\bigr)$;
* the final process by composing the server and the client: $S\mid C$.

## Reduction-based operational semantics

The central reduction rule of the $\pi$-calculus is the following:
$$\overline{n}\langle a\rangle.P\mid n(b).Q\longrightarrow P\mid Q_{a\mapsto b}\,.$$

## Typed $\pi$-calculus

Several attempts have been made to give the $\pi$-calculus [[typing systems]]. It is crucial for $\mathrm{HO}\pi$, a [[higher-order  logic|higher-order]] $\pi$-calculus in which messages can be processes themselves.

### Simple types

Simple types are defined by the following grammar:
$$T\longrightarrow\sharp\widetilde{T}$$
where $\widetilde{T}$ ranges over (possibly empty) tuples of simple types.

[[typing context|Typing contexts]] are lists of hypotheses of the form $n:T$ where $n$ is a channel name and $T$ is a simple type.

Simply typed $\pi$-calculus corresponds to a [[distributed logic]]: using a property proven at some place supposes therefore a call to that property under a name. Theorems can be used many times, but lemmas are limited to one use.

Typing | Intuitive signification
-------|------------------------
$a(x,y).P:p,q\to r$ | **Lemma 1.** Under hypotheses $p$, $q$, then $r$.
$\overline{a}\langle M,N\rangle:r$ | Use Lemma 1, knowing that $p$ and $q$, to prove $r$.

### Session types

[[session type|Session types]] were introduced by Kohei Honda. A session links exactly two subprocesses that interact with each other, and multiple sessions can run simultaneously.

\begin{example}
The process
$x(n).\overline{x}\langle n+1\rangle.0$
may be given type
$x:?\mathsf{int}.!\mathsf{int}.\mathsf{end}$.
\end{example}

[Caires and Pfenning 2010](#Caires2010) established a correspondence between [[dual intuitionistic linear logic]] (DILL) and session typed $\pi$-calculus.
Later on, [Wadler 2012](#Walder2012) established a correspondence between [[classical linear logic]] (CLL) and the same calculus.

## Other process calculi

The Calculus of Communicating Systems (CCS) is an important predecessor of the π-calculus. It can be seen as a restriction of π in which only a dummy name $w$ is exchanged in communications, and $w$ cannot be used in subject position ([Hirschkoff 2003](#Hirschkoff03)).

### The applied π-calculus

The *applied π-calculus* is an extension of the π-calculus with [[terms]] (representing messages in security protocols) instead of names. In addition, function symbols represent cryptographic primitives and are related by an equational [[theory]].

## References

* [[Robin Milner]], Joachim Parrow and David Walker, _A Calculus of Mobile Processes_, Information and Computation, **100** (1992) 1-40.
* Peter Sewell, _Applied $\pi$ – A Brief Tutorial_, (2000) ([pdf](https://www.cl.cam.ac.uk/~pes20/apppi.pdf)).
* Jeannette M. Wing, _FAQ on $\pi$-Calculus_, (2002) ([pdf](https://www.cs.cmu.edu/~wing/publications/Wing02a.pdf)).
* {#Hirschkoff03} Daniel Hirschkoff, _A brief survey of the theory of the $\pi$-calculus_, (2003) ([pdf](https://hal-lara.archives-ouvertes.fr/hal-02101985/file/RR2003-13.pdf)).
* [[Pierre-Louis Curien]], *Introduction to CCS and $pi$-calculus*, (2003) ([ps](https://www.irif.fr/~curien/CCS-DEA.ps.gz)).

On types:

* Kohei Honda, _Types for dyadic interaction_, 4th International Conference on Concurrency Theory (1993) 509–523.
* Noël Bernard, _Investigating the Logical Aspects of the Pi-calculus_, Schedae Informaticae, **12** (2003) 57-66 ([hal-00386109](https://hal.science/hal-00386109)).
* {#Caires10} Luís Caires and [[Frank Pfenning]], _Session Types as Intuitionistic Linear Propositions_, 21st International Conference on Concurrency Theory (2010) 222-236 ([pdf](https://www.cs.cmu.edu/~fp/papers/concur10.pdf)).
* {#Walder2012} Philip Wadler, _Propositions as Sessions_ ([pdf](https://homepages.inf.ed.ac.uk/wadler/papers/propositions-as-sessions/propositions-as-sessions.pdf), [doi:10.1145/2398856.2364568](https://dl.acm.org/doi/10.1145/2398856.2364568)).

Other process calculi:

* Kevin Liao, Matthew A. Hammer and Andrew Miller, _ILC: A Calculus for Composable, Computational Cryptography_, Proceedings of the 40th ACM SIGPLAN Conference on Programming Language Design and Implementation, (2019) 640-654 ([doi:10.1145/3314221.3314607](https://dl.acm.org/doi/10.1145/3314221.3314607), [pdf](https://eprint.iacr.org/2019/402.pdf)).

[[!redirects π-calculus]]
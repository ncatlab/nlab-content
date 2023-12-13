\tableofcontents

## Idea

The $\pi$-calculus is a [[computational]] model for concurrent processes that communicate messages through named channels. It subsumes [[λ-calculus]].

In the monadic $\pi$-calculus, outputs and inputs only send and receive single names, while the polyadic $\pi$-calculus allows outputs of tuples of names and corresponding inputs.

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

## Typed $\pi$-calculus as a logic

Several attempts have been made to give the $\pi$-calculus [[typing systems]]. It is crucial for $\mathrm{HO}\pi$, a [[higher-order  logic|higher-order]] $\pi$-calculus in which messages can be processes themselves.

Typed $\pi$-calculus corresponds to a [[distributed logic]]: using a
property proven at some place supposes therefore a call to that property under a name. Theorems can be used many times, but lemmas are limited to one use.

Typing | Intuitive signification
-------|------------------------
$a(x,y).P:p,q\to r$ | **Lemma 1.** Under hypotheses $p$, $q$, then $r$.
$\overline{a}\langle M,N\rangle:r$ | Use Lemma 1, knowing that $p$ and $q$, to prove $r$.

## References

* [[Robin Milner]], Joachim Parrow and David Walker, _A Calculus of Mobile Processes_, Information and Computation, **100** (1992) 1-40.
* Peter Sewell, _Applied $\pi$ – A Brief Tutorial_, (2000) ([pdf](https://www.cl.cam.ac.uk/~pes20/apppi.pdf)).
* Jeannette M. Wing, _FAQ on $\pi$-Calculus_, (2022) ([pdf](https://www.cs.cmu.edu/~wing/publications/Wing02a.pdf)).
* Noël Bernard, _Investigating the Logical Aspects of the Pi-calculus_, 
Schedae Informaticae, **12** (2003) 57-66 ([hal-00386109](https://hal.science/hal-00386109)).

[[!redirects π-calculus]]
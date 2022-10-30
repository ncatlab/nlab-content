
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A question that is traditionally of some debate in [[type theory]] is,

> What does it mean for a [[term]] to have more than one [[type]]?

One place where this question becomes relevant is in the interpretation of [[polymorphism]].  Another is for type systems with a non-trivial [[subtyping]] relation, in which case it becomes pertinent to consider the meaning of the _subsumption_ rule:

$$\frac{e:A \qquad A \le B}{e:B}$$

One possibility (sometimes called the **inclusion interpretation** of subtyping) is based on the idea of interpreting types as _properties_ of terms (what is also sometimes called "types &#224; la Curry", or the [[intrinsic and extrinsic views of typing|extrinsic]] view of typing).  Under this interpretation, the subsumption rule can be read more or less literally, as asserting that if $e$ satisfies the property $A$, and $A$ entails $B$, then $e$ also satisfies the property $B$.  One potential drawback of this interpretation, though, is that it seems to commit you to giving a meaning to "untyped" terms (although these terms may of course intrinsically have some more coarse-grained type structure, as in models of pure [[lambda calculus]] by [[reflexive object]]s).

A different possibility (sometimes called the **coercion interpretation** of subtyping) is to read the subsumption rule as introducing an implicit _coercion_ from $A$ to $B$.  Under this interpretation, subtyping can be seen as simply providing a convenient shorthand notation, when having to write out these coercions explicitly would be too burdensome.  This interpretation allows one to maintain an [[intrinsic and extrinsic views of typing|intrinsic]] ("&#224; la Church") view of typing, but on the other hand it introduces a subtle issue of _coherence_: if there is more than one way of deriving the subtyping judgment $A \le B$, we would like to know that all of these result in equivalent coercions from $A$ to $B$, so that the meaning of a well-typed term is independent of its typing derivation.

### In dependent type theory

Consider a [[dependent type|dependent]] [[proposition]] $A: Type, x:A \vdash P(x):Prop$. Then the [[dependent sum]], $\sum_{x:A} P(x)$, may be thought of as '$A$s which are $P$'. Sometimes it is convenient to identify a term of this dependent sum as though it were a term of the full type $A$. Here we can use the first projection of the dependent sum to **coerce** the identification. 

For example, we might have introduced 'Eve' as a term of type $Woman$, and then wish to form a type $Relatives(Eve)$, when $Relatives(x)$ had been introduced as a type depending on $x: Human$. If $Woman$ had been defined as $\sum_{x:Human} Female(x)$, then $Eve$ has projections to the underlying human and to a warrant for Eve's being female. It would be clumsy to insist on $Relatives(\pi_1(Eve))$. Coercion along this projection allows us to form $Relatives(Eve)$.

[Luo (1999)](#Luo99) proposed a way of formalizing coercions in dependent type theory, through what he calls the _coercive definition rule_, which when generalized to allow dependency on the coerced term is:

$$
\frac{\Gamma, x: B \vdash f(x) : C(x) \; \; \; \Gamma \vdash a : A \;\;\;\Gamma \vdash A \lt_{c} B : Type}{\Gamma \vdash f(a) = f(c(a)) : C(c(a))}
$$

In this notation, a coercion between two types $A$ and $B$ is denoted $A \lt_{c} B$, for $c: (A \to B)$.

### In HoTT

In [[homotopy type theory]], the inclusion of a smaller [[universe|universe in type theory]] in a larger one is often considered as a coercion.

### Coherence

[Reynolds (2000)](#Reynolds00) gave an interesting proof of coherence for a coercion interpretation of a language with subtyping.  The proof works by first building a [[logical relation]] between this "intrinsic semantics" and a separate untyped semantics of the language (the latter based on interpreting programs as elements of a universal [[domain theory|domain]] $U$), and then establishing a "bracketing theorem" which says that for any domain $[[A]]$ in the image of the intrinsic semantics, there are a pair of functions $\phi_A : [[A]] \to U$ and $\psi_A : U \to [[A]]$ such that

* for any $a\in [[A]]$, $a$ is logically related to $\phi_A(a)$
* if $a$ is logically related to $x$, then $a = \psi_A(x)$

Combined, the logical relations theorem and the bracketing theorem imply that the coercion $[[\alpha]] : [[A]] \to [[B]]$ associated to any derivation $\alpha$ of a subtyping judgment $A \le B$ can be factored as 

$$
\begin{matrix}
 [[A]] &\overset{\phi_A}{\to} & U & \overset{\psi_B}{\to} & [[B]]
\end{matrix}
$$

and hence in particular that any two derivations $\alpha_1,\alpha_2$ of $A \le B$ result in the same coercion $[[\alpha_1]] = [[\alpha_2]] = (\phi_A;\psi_B) : [[A]] \to [[B]]$.

## Related concepts

* [[subtype]]


## References

* {#Reynolds80} [[John C. Reynolds]], _Using Category Theory to Design Implicit Conversions and Generic Operators_, In Proceedings of the Aarhus Workshop on Semantics-Directed Compiler Generation (January 14-18, 1980), Springer-Verlag. ([pdf](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2276&context=compsci))

* {#Reynolds91} John C. Reynolds, _The Coherence of Languages with Intersection Types_. TACS 1991. ([ps](http://www.cs.cmu.edu/afs/cs/user/jcr/ftp/tempdir/coherence.ps))

* {#Reynolds00} John C. Reynolds, _The Meaning of Types: from Intrinsic to Extrinsic Semantics_. BRICS Report RS-00-32, Aarhus University, December 2000. ([pdf](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2290&context=compsci))

* {#Luo99} [[Zhaohui Luo]], Coercive subtyping. Journal of Logic and Computation, 9(1):105&#8211;130, 1999. [ps file](http://www.cs.rhul.ac.uk/~zhaohui/JLC98.ps).

* [[Zhaohui Luo]], Type-Theoretical Semantics with Coercive Subtyping, [pdf](http://www.cs.rhul.ac.uk/home/zhaohui/SALT20.pdf)
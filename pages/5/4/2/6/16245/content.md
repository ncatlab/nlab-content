### Idea

A question that is traditionally of some debate in type theory is,

> What does it mean for a term to have more than one type?

One place where this question becomes relevant is in the interpretation of [[polymorphism]].  Another is for type systems with a non-trivial [[subtyping]] relation, in which case it becomes pertinent to consider the meaning of the _subsumption_ rule:

$$\frac{e:A \qquad A \le B}{e:B}$$

One possibility (sometimes called the **inclusion interpretation** of subtyping) is based on the idea of interpreting types as _properties_ of terms (what is also sometimes called "types &#224; la Curry", or the _extrinsic_ view of typing).  Under this interpretation, the subsumption rule can be read more or less literally, as asserting that if $e$ satisfies the property $A$, and $A$ entails $B$, then $e$ also satisfies the property $B$.  One potential drawback of this interpretation, though, is that it commits you to giving a semantics to "untyped" terms (or at least commits you to a two-layer approach, where terms are assumed to be typed in some pre-existing type system).

A different possibility (sometimes called the **coercion interpretation** of subtyping) is to read the subsumption rule as introducing an implicit coercion from $A$ to $B$.  Under this interpretation, subtyping can be seen as simply providing a convenient shorthand notation, when having to write out these coercions explicitly would be too burdensome.  However, this interpretation introduces a subtle issue of _coherence_: if there is more than one way of deriving the subtyping judgment $A \le B$, we need to know that all of these result in equivalent coercions from $A$ to $B$.

### In dependent type theory

Consider a dependent proposition $A: Type, x:A \vdash P(x):Prop$. Then the [[dependent sum]], $\sum_{x:A} P(x)$, can be thought of as '$A$s which are $P$'. Sometimes it is convenient to identify a term of this dependent sum as though it were a term of the full type $A$. Here we can use the first projection of the dependent sum to **coerce** the identification. 

For example, we might have introduced 'Eve' as a term of type $Woman$, and then wish to form a type $Relatives(Eve)$, when $Relatives(x)$ had been introduced as a type depending on $x: Human$. If $Woman$ had been defined as $\sum_{x:Human} Female(x)$, then $Eve$ has projections to the underlying human and to a warrant for Eve's being female. It would be clumsy to insist on $Relatives(\pi_1(Eve))$. Coercion along this projection allows us to form $Relatives(Eve)$.

Luo (1999) proposed a way of formalizing coercions in dependent type theory, through what he calls the _coercive definition rule_:

$$
\frac{\Gamma, x: B \vdash f(x) : C(x) \; \; \; \Gamma \vdash a : A \;\;\;\Gamma \vdash A \lt_{c} B : Type}{\Gamma \vdash f(a) = f(c(a)) : C(c(a))}
$$

In this notation, a coercion between two types $A$ and $B$ is denoted $A \lt_{c} B$, for $c: (A \to B)$.

### In HoTT

In [[homotopy type theory]], the inclusion of a smaller [[universe|universe in type theory]] in a larger one is often considered as a coercion.

### Related concepts

* [[subtype]]


### References

* John C. Reynolds, _The Coherence of Languages with Intersection Types_. TACS 1991. ([ps](http://www.cs.cmu.edu/afs/cs/user/jcr/ftp/tempdir/coherence.ps))

* John C. Reynolds, _The Meaning of Types: from Intrinsic to Extrinsic Semantics_. BRICS Report RS-00-32, Aarhus University, December 2000. ([pdf](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2290&context=compsci))

* Z. Luo, Coercive subtyping. Journal of Logic and Computation, 9(1):105&#8211;130, 1999. [ps file](http://www.cs.rhul.ac.uk/~zhaohui/JLC98.ps).

* Z. Luo., Type-Theoretical Semantics with Coercive Subtyping, [pdf](http://www.cs.rhul.ac.uk/home/zhaohui/SALT20.pdf)
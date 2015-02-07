### Idea

Consider a dependent proposition $A: Type, x:A \vdash P(x):Prop$. Then the [[dependent sum]], $\sum_{x:A} P(x)$, can be thought of as '$A$s which are $P$'. Sometimes it is convenient to identify a term of this dependent sum as though it were a term of the full type $A$. Here we can use the first projection of the dependent sum to **coerce** the identification. 

For example, we might have introduced 'Eve' as a term of type $Woman$, and then wish to form a type $Relatives(Eve)$, when $Relatives(x)$ had been introduced as a type depending on $x: Human$. If $Woman$ had been defined as $\sum_{x:Human} Female(x)$, then $Eve$ has projections to the underlying human and to a warrant for Eve's being female. It would be clumsy to insist on $Relatives(\pi_1(Eve))$. Coercion along this projection allows us to form $Relatives(Eve)$.

### Definition

In general, a coercion between two types $A$ and $B$ is denoted $A \lt_{c} B$, for $c: (A \to B)$. Then we have the _coercive definition rule_


$$
\frac{\Gamma, x: B \vdash f(x) : C(x) \; \; \; \Gamma \vdash a : A \;\;\;\Gamma \vdash A \lt_{c} B : Type}{\Gamma \vdash f(a) = f(c(a)) : C(c(a))}
$$

All the coercions of a type system must be coherent in the sense that any two typing derivations of one type as a subtype of another must agree.

### Related concepts

* [[subtype]]


### References

* Z. Luo, Coercive subtyping. Journal of Logic and Computation, 9(1):105&#8211;130, 1999. [ps file](http://www.cs.rhul.ac.uk/~zhaohui/JLC98.ps).

* Z. Luo., Type-Theoretical Semantics with Coercive Subtyping, [pdf](http://www.cs.rhul.ac.uk/home/zhaohui/SALT20.pdf)

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea

The representable and corepresentable functor theorems are simple consequences of the [[general adjoint functor theorem]] and the following observations:

* Suppose $C$ is a [[cocomplete category]].  A functor $F: C^{op}\to Set$ is [[representable]] if and only if it has a [[left adjoint]] $L$.  In this case, $L(\{\ast\})=X$ is the [[representing object]].  More generally, $L(S)=X^S$ is the [[product]] of $S$ copies of $X$, which exists.

* Suppose $C$ is a [[complete category]].  A functor $F:C\to Set$ is [[corepresentable]] if and only if it has a [[left adjoint]] $L$.  In this case, $L(\{\ast\})=X$ is the [[corepresenting object]].  More generally, $L(S)=\coprod_S X$ is the [[coproduct]] of $S$ copies of $X$, which exists. 

## Statement

The __representable functor theorem__ states that:

- A [[presheaf]] $C^{op} \to Set$ on a [[cocomplete category]] $C$ is [[representable functor|representable]], i.e., of the form $C({-}, c)$ for some object $c \in C$ if and only if it sends [[colimits]] in $C$ to [[limits]] in $Set$ and has a [[solution set condition|solution set]].

The latter condition means the following: there is a set $I$, an $I$-indexed family of objects $X_i\in C$, and an $I$-indexed family of elements $f_i\in F(X_i)$ such that for every object $Y\in C$ and $h\in F(Y)$ there is $k\in I$ and $t\colon Y\to X_i$ such that $h=F(t)(f_i)$.

Dually, the __corepresentable functor theorem__ states that:

- A [[copresheaf]] $C \to Set$ on a [[complete category]] $C$ is [[corepresentable functor|corepresentable]], i.e., of the form $C(c, {-})$ for some object $c \in C$ if and only if it is [[continuous functor|continuous]] and has a [[solution set condition|solution set]].

The latter condition means the following: there is a set $I$, an $I$-indexed family of objects $X_i\in C$, and an $I$-indexed family of elements $f_i\in F(X_i)$ such that for every object $Y\in C$ and $h\in F(Y)$ there is $k\in I$ and $t\colon X_i\to Y$ such that $h=F(t)(f_i)$.

## Related facts

As representable functors are closely connected to [[adjoint functors]], this theorem is essentially equivalent to the [[adjoint functor theorem]] and to theorems guaranteeing the existence of [[limits]].

Specifically, assuming that $C$ is [[copowered]] over [[Set]] (in particular, this is true if $C$ is [[cocomplete]]), a functor $C\to Set$
is a right adjoint functor if and only if it is representable, in which case the left adjoint functor $Set\to C$ sends the [[singleton]] set to the representing object, and more generally a set $X$ to the [[copower]] of $X$ with the representing object.

## Related concepts

* [[adjoint functor theorem]]

## References
 {#References}

* {#Pareigis70} [[Bodo Pareigis]], Thm. 1 on p. 109 in: *Categories and Functors*, Pure and Applied Mathematics **39**, Academic Press (1970) &lbrack;[doi:10.5282/ubm/epub.7244](https://doi.org/10.5282/ubm/epub.7244), [pdf](https://epub.ub.uni-muenchen.de/7244/1/7244.pdf)&rbrack;

* {#MacLane97} [[Saunders MacLane]], p. 118 (2nd ed: 130) in: _[[Categories for the Working Mathematician]]_, Graduate texts in mathematics **5**, Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;


[[!redirects corepresentable functor theorem]]
[[!redirects representability theorem]]
[[!redirects corepresentability theorem]]
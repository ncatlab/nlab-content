[[!redirects existentially closed theory]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Existential closedness is a [[property]] of [[first-order structures]] (in the same way that [[model completeness]] is a [[property]] of [[first-order theory|first-order theories]]) meant to generalize the properties of the theory [[ACF]] of [[algebraically closed fields]].

As discussed in section 8.1 of ([Hodges93](#Hodges1993)):

> Take a first-order language $\mathcal{L}$ without relation symbols and a class $\mathbf{K}$ of $\mathcal{L}$-structures. For example, $\mathcal{L}$ might be the language of rings and $\mathbf{K}$ the class of fields, or $\mathcal{L}$ might be the language of groups and $\mathbf{K}$ the class of groups.

> We say that a structure $A$ in $\mathbf{K}$ is _existentially closed_ in $\mathbf{K}$ if whenever $E$ is a finite set of equations and inequations with parameters from $A$ and $E$ has a simultaneous solution in some extension $B$ of $A$ with $B$ in $\mathbf{K}$, then $E$ has a solution already in $A$.

(c.f. [[algebraically closed field]]).

## Definition

+-- {: .num_defn}
###### Definition

1. An *existential formula* is a formula of the form $\exists y \varphi(x,y)$ where $\varphi(x,y)$ is quantifier-free.

2. A *universal formula* is a formula of the form $\forall y \varphi(x,y)$ where $\varphi(x,y)$ is quantifier-free.

=--

+-- {: .num_defn}
###### Definition

We say that a model $M$ of a first-order theory $T$ is *existentially closed* if for every $N$ also modelling $T$, every embedding $M \hookrightarrow N$, every tuple $a \in M$, and every existential formula $\exists y \varphi(x,y)$, then whenever $N \models \exists y \varphi(a, y)$, we also have that $M \models \exists y \varphi(a,y)$.

=--

("The existence of witnesses in a superstructure to existential statements about points in the existentially closed model is reflected to the existentially closed model.")

In the terminology of the passage from ([Hodges93](#Hodges1993)), we say that $M \models T$ is an *existentially closed model* of $T$ if it is existentially closed in the class $\mathbf{K} \overset{\operatorname{df}}{=} \mathbf{Mod}(T)$.

We say that a theory $T$ is an "existentially closed theory" (i.e., [[model complete]]) if all of its models are existentially closed.

## Examples

The theory [[ACF]] of [[algebraically closed field|algebraically closed fields]] is existentially closed. An existential formula $\exists y \varphi(x,y)$ in $\mathsf{ACF}$ says "for a choice of coefficients $x$, there exists a point $y$ in affine space (of fixed dimension) which is in these finitely many affine varieties depending on $x$ but not these finitely many affine varieties depending on $x$".

Checking that $\mathsf{ACF}$ is existentially closed therefore means checking that if $E \hookrightarrow K$ is an embedding of algebraically closed fields, and $x$ is a choice of coefficients from $E$, then if such a point $y$ exists in affine $K$-space, then we can find a similar $y$ in affine $E$-space.

However, we can do so very cheaply after we know that $\mathsf{ACF}$ [[quantifier elimination|eliminates quantifiers]] (and therefore so does the theory of algebraically closed fields containing $E$): $\exists y \varphi(a,y)$ is equivalent to some quantifier-free sentence involving $a$, and quantifier-free sentences are always transferred by embeddings of structures, so we are done.

## Remarks

* Theories which [[quantifier elimination|eliminate quantifiers]] are model complete: all of their models are existentially closed (again, because quantifier-free sentences are always transferred by embeddings of structures).

## Related concepts

* [[model complete theory]]

* [[quantifier elimination]]

* [[model companion]]


## References

* {#Hodges1993}Wilfrid Hodges, _Model theory_, Cambridge Univ. Press 1993

[[!redirects existentially closed]]

[[!redirects existentially-closed]]

[[!redirects existentially closed theory]]

[[!redirects existentially-closed model]]

[[!redirects existential closure]]

[[!redirects existentially-closed theory]]

[[!redirects existentially closed models]]

[[!redirects existentially closed]]

[[!redirects existential closedness]]



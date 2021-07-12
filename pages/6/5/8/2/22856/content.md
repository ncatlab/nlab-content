
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A *divided power algebra* is a [[commutative ring]] $A$ together with an [[ideal]] $I$ and a collection of operations $\{\gamma_{n}\colon I\to A\}_{n\in\mathbb{N}}$ which behave like operations of taking divided powers $x\mapsto x^{n}/n!$ in [[power series]].


## Definition

A __divided power algebra__ is a triple $(A,I,\gamma)$ with

- $A$ a [[commutative ring]];

- $I$ an [[ideal]] of $A$;

- $\gamma=\{\gamma_{n}\colon I\to A\}_{n\in\mathbb{N}}$ an [[indexed set]] of [[functions]] (of [[underlying]] [[sets]]);

satisfying the following conditions:

1. For each $x\in I$, we have $\gamma_{0}(x)=1$.

1. For each $x\in I$, we have $\gamma_{1}(x)=x$.

1. For each $x\in I$ and each $n\geq2$, we have $\gamma_{n}(x)\in I$.

1. For each $x,y\in I$, we have
$$\gamma_{n}(x+y)=\sum_{k=0}^{n}\gamma_{n-k}(x)\gamma_{k}(y).$$

1. For each $\lambda\in A$ and each $x\in I$, we have
$$\gamma_{n}(\lambda x)=\lambda^{n}\gamma_{n}(x).$$

1. For each $x\in I$ and each $m,n\in\mathbb{N}$, we have
$$\gamma_{n}(x)\gamma_{m}(x)=\frac{(n+m)!}{n!m!}\gamma_{n+m}(x).$$

1. For each $x\in I$ and each $m,n\in\mathbb{N}$, we have
$$\gamma_{m}(\gamma_{n}(x))=\frac{(n m)!}{(n!)^{m}m!}\gamma_{n m}(x).$$

For a given $(A,I)$, a __divided power structure__ on $(A,I)$ is a $\gamma$ making $(A, I, \gamma)$ a divided power algebra.

If $A$ is an $R$-algebra for a ring $R$, we call it a __divided power $R$-algebra__ or __PD-$R$-algebra__.


## Properties

Genuine powers can be constructed in the expected way from the divided powers, and when $A$ is torsion free, the reverse is true:

+-- {: .num_prop} 
###### Proposition

If $(A,I,\gamma)$ is a divided power algebra, then $n! \gamma_n(x) = x^n$ for every $x \in I$ and $n \in \mathbb{N}$.
=--

+-- {: .proof} 
###### Proof 

It's true for $n=0$ and $n=1$. 
For $n \geq 2$, this follows by [[induction]], since $n! \gamma_n(x) = (n-1)! \gamma_{n-1}(x) \cdot 1! \gamma_1(x) = x^{n-1} \cdot x$.

=--
+-- {: .num_prop} 
###### Proposition

If $A$ is a commutative ring with an ideal $I$ such that $x^n$ is an $(n!)$-th multiple for every $x \in I$ and $n \geq 0$, then $(A,I)$ has a unique divided power structure, and it is given by $\gamma_n(x) = x^n / n!$.
=--

+-- {: .proof} 
###### Proof 

The hypotheses imply the quotients $x^n / n!$ are unique and well-defined, and any divided power structure on $(A,I)$ must be given by that formula. It's straightforward to check the definition does give a divided power algebra.

=--

So in the torsion free case, the divided power algebras are precisely of the motivating form. In positive characteristic, though, examples can be somewhat more exotic.


## Related concepts

* [[crystalline cohomology]]

## References

Divided power algebras were originally introduced in 

* [[Henri Cartan]], _Puissances divisées_, Séminaire Henri Cartan, Tome 7 (1954–1955) no. 1, Exposé no. 7, 11 p. [Numdam:SHC_1954–1955__7_1_A7_0](http://www.numdam.org/item/SHC_1954-1955__7_1_A7_0/).

Their theory was further developed in [[Pierre Berthelot]]'s PhD thesis (in the context of [[crystalline cohomology]]), which was later published as:

* [[Pierre Berthelot]], _Cohomologie cristalline des sch&#233;mas de caract&#233;ristique $p \gt 0$_, Lecture Notes in Mathematics, Vol. 407, Springer-Verlag, Berlin, 1974. ([doi:10.1007/BFb0068636](https://doi.org/10.1007/BFb0068636),  MR 0384804)

Review:

* [[Pierre Berthelot]], [[Arthur Ogus]], _Notes on crystalline cohomology_, Princeton Univ. Press 1978. vi+243, ([ISBN:0-691-08218-9](https://press.princeton.edu/books/hardcover/9780691648323/notes-on-crystalline-cohomology-mn-21))

* [[Aise Johan de Jong]] et al., [[The Stacks Project]], [Chapter 09PD](https://stacks.math.columbia.edu/tag/09PD).

See also:

* Wikipedia, *[Divided power structure](https://en.wikipedia.org/wiki/Divided_power_structure)*

In relation to the [[sphere spectrum]]

* [[Sanath Devalapurkar]], _Divided powers and the sphere spectrum_, [blog post](https://sanathdevalapurkar.github.io/blog/algebraic-topology/2019/02/20/divided-powers.html)


[[!redirects PD-algebra]]
[[!redirects PD-algebras]]

[[!redirects divided power structure]]
[[!redirects divided power structures]]
[[!redirects divided power algebras]]

[[!redirects divided power]]
[[!redirects divided powers]]
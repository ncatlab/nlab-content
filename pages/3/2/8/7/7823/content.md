
#Contents#
* table of contents
{:toc}

## Idea

A *Galois module* $V$ is a $G$-[[module]] for a [[Galois group]] $G$; i.e. it is an abelian group on which a Galois group acts in a way compatible with the abelian group structure.

If $V$ is a _[[vector space]]_ then this is a [[linear representation]] of $G$ and one speaks of _[[Galois representation]]_.

The category of $G$-modules is equivalent to the category of [[module|modules]] over the [[group algebra|group ring]] $\mathbb{Z}[G]$.

As always is the case, a group [[action]] $G\times A\to A$ can equivalently be written as $G\to Aut(A)$. This is why Galois modules are frequently called *Galois representations*.

## Properties

+-- {: .num_proposition}
###### Proposition
Let $K\hookrightarrow L$ be a [[Galois extension]] of a number field $K$.

Then the ring of integers $O_L$ of this extension is a [[Galois module]] of $Gal(K\hookrightarrow L)$.

(see also [[Hilbert-Speiser theorem]])

=--

## Examples

+-- {: .num_example}
###### Example
($l$-adic representation)

Let $l$ be a prime number. Let $Gal(k\hookrightarrow \overline k)$ be the [[absolute Galois group]] of a [[number field]] $k$. Then a morphism of groups

$$Gal(k\hookrightarrow \overline k)\to Aut (M)$$

is called an *$l$-adic representation of $Gal(k\hookrightarrow \overline k)$. Here $M$ is either a unit dimensional [[vector space]] over the algebraic closure $\overline \mathbb{Q}_l$ or a finitely generated module over the [[integral closure]] $\overline \mathbb{Z}_l$.

In particular the $l$-adic Tate-module is of this kind.
=--


+-- {: .num_example}
###### Example
($l$-adic [[Tate module]])
Let $l$ be a prime number. Let $A$ be an abelian group. The *$l$-adic Tate module* is defined to be the limit

$$T_l(A)=lim_n \;ker (l^n)$$

i.e. it is the [[directed limit|limit over the directed diagram]] $ker(p^{n+1})\to ker(p^n)$. Here the [[kernel]] $ker(p^n)$ of the multiplication-with-$p^n$ map $p^n:A\to A$ is called $p^n$-[[torsion]] of $A$.
=--

+-- {: .num_example}
###### Example
(*the* Tate-module)

Let $k_S$ denote the separable closure of $k$. Let $A$ be the group of [[root of unity|roots of unity]] of $k_s$ in $k$. Then the $l$-adic Tate-module of the absolute Galois group $Gal(k\hookrightarrow k_s)$ is called *the $l$-adic Tate module of $k$* or the *$l$-adic cyclotomic character of $k$.

It is equivalently the Tate-module of the [[multiplicative group scheme]] $\mu_k$.

The Tate-module is endowed with the structure of a $\mathbb{Z}$-module by $z(a_n)_n=((z\; modulo\; p^n)a_n)_n$.
=--


+-- {: .num_example}
###### Example
($l$-adic [[Tate module]] of an abelian variety)

Let $l$ be a prime number. Let $G$ be an [[abelian variety]] over a field $k$. Let $k_s$ denote the separable closure of $k$. The $k_s$-valued points of $G$ assemble to an abelian group.

Then there are classical results on the [[rank]] of the Tate-module $T_l(G)$: For example if the characteristic of $k$ is a prime number $p\neq l$ we have that $T_l(G)$ is a free $\mathbb{Z}_l$ module of rank $2dim(G)$.

A special case of the [[Tate conjecture]] can be formulated via Tate-modules:

Let $k$ be finitely generated over its prime field of characteristic $p\neq l$. Let $A,B$ be two abelian varieties over $k$. Then the conjecture states that

$$hom(A,B)\otimes \mathbb{Z}_p\simeq hom(T_l(A),T_l(B))$$

If $k$ is a finite field or a number field the conjecture is true.
=--

+-- {: .num_example}
###### Example
([[p-adic cohomology|l-adic cohomology]] of a smooth variety)

Let $l$ be a prime number. Let $X$ be a [[variety||smooth variety]] over a field $k$ of characteristic prime to $l$. Let $k_s$ denote the separable closure of $k$. 

The $l$-adic cohomology in degree $i$ is defined to be the directed limit $lim_n\; H^i_{et}(X_{k_s}, \mathbb{Z}/l^n\mathbb{Z})$. It is a Galois module where the action is given by pullback.

More specifically, given $\sigma\in Gal(k\hookrightarrow k_s)$ it acts on the $X_{k_s}=X\otimes_k k_s$ via the second factor. This is an isomorphism, since $\sigma$ is an automorphism, and hence $\sigma^*$ on cohomology is an isomorphism.

Note that since we have a equivalence $T_l A\simeq H_{et}^1(A_{k_s}, \mathbb{Z}_l)^\vee$, we have that the [[Tate module|l-adic Tate module]] is a special case of the $l$-adic cohomology.
=--

## Related concepts

* [[class field theory]]

* Every Galois representation induces an [[Artin L-function]].

## References

* Wikipedia, _[Galois module](http://en.wikipedia.org/wiki/Galois_module)_

* [[Richard Taylor]], _Galois representations_ ([pdf](http://math.stanford.edu/~lekheng/flt/taylor-long.pdf))

Review of the fact that Galois representations encode [[local systems]] are are hence analogs in [[arithmetic geometry]] of [[flat connections]] in [[differential geometry]] includes

* {#Lovering} Tom Lovering, _&#201;tale cohomology and Galois Representations_, 2012 ([pdf](http://tlovering.files.wordpress.com/2012/06/essay-body1.pdf))

See also at _[[function field analogy]]_.

[[!redirects Galois modules]]
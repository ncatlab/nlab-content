[[!redirects (2,1)-algebraic theeory of E-infinity algebras]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The [[(∞,1)-algebraic theory]] whose [[∞-algebra over an (∞,1)-algebraic theory|algebras]] are [[E-∞ algebra]]s is the [[(2,1)-category]] of [[span]]s of [[finite set]]s.


## Definition



+-- {: .num_defn}
###### Definition

Let 

$$
  2Comm := Span(FinSet)
$$ 

be the [[(2,1)-category]] of [[span]]s of [[finite set]]s:

* [[object]]s are finite sets;

* [[morphism]]s are [[span]]s $X_1 \leftarrow Y \to X_1$ in [[FinSet]];

* [[2-morphism]]s are diagrams

  $$
    \array{
        && Y
        \\
        & \swarrow && \searrow
        \\
       X_0 &&\downarrow^{\mathrlap{\simeq}}&& X_1
       \\
       & \nwarrow && \nearrow
       \\
       && Y'
    }
  $$

  in [[FinSet]] with the vertical morphism an [[isomorphism]].

=--

+-- {: .num_prop}
###### Observation

The [[homotopy category of an (infinity,1)-category|homotopy category]] of $2Comm$ is the category $Comm$ that is the [[Lawvere theory]] of commutative [[monoid]]s.

=--


+-- {: .proof}
###### Proof

The Lawvere theory of commutative monoids has as objects the free commutative monoids $F[k]$ on $k \in \mathbb{N}$ generators, and as morphisms monoid homomorphisms.

By the [[free functor|free property]], morphisms

$$
  f : F[k] \to F[l]
$$

are in natural bijection to $k$-tuples of elements of $F[l]$. Such elements in turn are sums $a_1 + a_1 + \cdots + a_1 + a_2 + a_2 + \cdots + a_2 + a_3 + \cdots$ of copies of the $l$ generators, hence are in bijection to sequences of natural numbers $(n_{1}, \cdots, n_l)$. Hence morphisms $f : F[k] \to F[l]$ are in bijection to $k \times l$-[[matrices]] with entries in the [[natural number]]s. 

One checks that under this identification composition of morphisms corresponds to matrix multiplication.

=--

+-- {: .num_remark}
###### Remark

For instance the spans

$$
  \{1,2\} \stackrel{id}{\leftarrow} \{1,2\} \to \{1\}
$$

and

$$
  \{1,2\} \stackrel{\simeq}{\leftarrow} \{2,1\} \to \{1\}
$$

describe the operation

$$
  (a,b) \mapsto a + b
$$

and the operation

$$
  (a,b) \mapsto b + a
  \,,
$$

respectively. Clearly, in $Comm$ both these operations are identified. In $2Comm$ however they the are only equivalent

$$
  \array{
      && \{1,2\}
      \\
      & {}^{\mathllap{id}}\swarrow && \searrow
      \\
     \{1,2\} &&\downarrow^{\mathrlap{\simeq}}&& \{1\}
     \\
     & {}_{\mathllap{\simeq}}\nwarrow && \nearrow
     \\
     && \{2,1\}
  }
  \,.
$$


=--



## Properties




+-- {: .num_lemma}
###### Observation

Let $Comm$ be the ordinary [[Lawvere theory]] of commutative monoids. There is a forgetful 2-functor

$$
  2Comm \to Comm
 \,.
$$

This exhibits $2Comm$ as being like $Comm$ but with some additional auto-2-morphisms of the morphism of $Comm$.

=--

This is discussed in ([Cranch, beginning of section 5.2](#Cranch)).


+-- {: .num_prop}
###### Proposition

The $(\infty,1)$-category $2Comm$ has finite [[product]]s. The products of objects $A, B$ in $2Comm$ is their [[coproduct]] $A \coprod B$ in [[FinSet]].

=--

This appears as ([Cranch, prop. 4.7](#Cranch)).


+-- {: .num_prop}
###### Proposition

An [[(∞,1)-category]] with [[(∞,1)-limit|(∞,1)-product]] is naturally an algebra over the $(2,1)$-theory $2Comm$.

=--

This appears as ([Cranch, theorem 4.26](#Cranch)).

+-- {: .num_theorem}
###### Theorem

An algebra over the $(2,1)$-theory $2Comm$ in [[(∞,1)Cat]] is
a [[symmetric monoidal (∞,1)-category]].

=--

This appears as ([Cranch, theorem 5.3](#Cranch)).

+-- {: .num_theorem}
###### Theorem

There is a $(2,1)$-algebraic theory $E_\infty$ whose algebras
are at least in parts like [[E-∞ algebra]]s.

=--

This is ([Cranch](#Cranch)), prop. 6.12, theorem 6.13 and section 8.


## Examples {#Examples}

### Free algebras

The free algebra over $2Comm$ in [[∞Grpd]] on a single generator is $2Comm(*, -) : 2Comm \to \infty Grpd$. Its underlying [[∞-groupoid]] is therefore

$$
  2Comm(*,*) = Core(FinSet)
  \,,
$$

the [[core]] groupoid of the category [[FinSet]]. This is equivalent to

$$
  \cdots \simeq \coprod_{n \in \mathbb{N}} \mathbf{B} \Sigma_n
  \,,
$$

where $\Sigma_n$ is the [[symmetric group]] on $n$ elements and $\mathbf{B}\Sigma_n$ its one-object [[delooping]] groupoid.

Notice that this is indeed the free [[E-∞-algebra]], on the nose so if we use the [[Barratt-Eccles operad]] $P$ as our model for the [[E-∞-operad]]: that has $P_n = \mathbf{E} \Sigma_n$. The free [[algebra over an operad]] is given by $\coprod_{n \in \mathbb{N}} P_n/\Sigma_n$, which here is $\cdots = \coprod_{n \in \mathbb{N}} \mathbf{E}\Sigma_n/\Sigma_n = \coprod_n \mathbf{B} \Sigma_n$. 



## References

* [[James Cranch]], _Algebraic Theories and $(\infty,1)$-Categories_ ([arXiv](http://arxiv.org/abs/1011.3243))
{#Cranch}

[[!redirects (2,1)-algebraic theory of E-∞ algebras]]
[[!redirects (2,1)-algebraic theory of E-∞-algebras]]
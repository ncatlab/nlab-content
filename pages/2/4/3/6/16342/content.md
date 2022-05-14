+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Generalizing the classical notion of [[commutative monoid]], one can define a _commutative monoid_ (or _commutative monoid object_) in any [[symmetric monoidal category]] $(C,\otimes,I)$.
These are [[monoids in a monoidal category]] whose multiplicative operation is commutative.
Classical commutative monoids are of course just commutative monoids in [[Set]] with the [[cartesian product]].

## Definition

+-- {: .num_defn #MonoidsInMonoidalCategory}
###### Definition

Given a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, then a **[[monoid in a monoidal category|monoid internal to]]** $(\mathcal{C}, \otimes, 1)$ is

1. an [[object]] $A \in \mathcal{C}$;

1. a morphism $e \;\colon\; 1 \longrightarrow A$ (called the _[[unit]]_)

1. a morphism $\mu \;\colon\; A \otimes A \longrightarrow A$ (called the _product_); 

such that

1. ([[associativity]]) the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (A\otimes A) \otimes A 
         &\underoverset{\simeq}{a_{A,A,A}}{\longrightarrow}&
       A \otimes (A \otimes A)
         &\overset{A \otimes \mu}{\longrightarrow}&
       A \otimes A
       \\
       {}^{\mathllap{\mu \otimes A}}\downarrow  
         && &&
       \downarrow^{\mathrlap{\mu}}
       \\
       A \otimes A
         &\longrightarrow&
         &\overset{\mu}{\longrightarrow}&
       A
     }
     \,,
   $$

   where $a$ is the associator isomorphism of $\mathcal{C}$;

1. ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       1 \otimes A 
         &\overset{e \otimes id}{\longrightarrow}&
       A \otimes A
         &\overset{id \otimes e}{\longleftarrow}& 
       A \otimes 1
       \\
       & {}_{\mathllap{\ell}}\searrow 
       & \downarrow^{\mathrlap{\mu}} &
       & \swarrow_{\mathrlap{r}}
       \\
       && A
     }
     \,,
   $$

   where $\ell$ and $r$ are the left and right unitor isomorphisms of $\mathcal{C}$.

Moreover, if $(\mathcal{C}, \otimes , 1)$ has the structure of a [[symmetric monoidal category]]  $(\mathcal{C}, \otimes, 1, \tau)$ with symmetric [[braiding]] $\tau$, then a monoid $(A,\mu, e)$ as above is called a **[[commutative monoid in a symmetric monoidal category|commutative monoid in]]** $(\mathcal{C}, \otimes, 1, \tau)$ if in addition

* (commutativity) the following [[commuting diagram|diagram commutes]]

  $$
    \array{
      A \otimes A 
        && \underoverset{\simeq}{\tau_{A,A}}{\longrightarrow} &&
      A \otimes A
      \\
      & {}_{\mathllap{\mu}}\searrow && \swarrow_{\mathrlap{\mu}}
      \\
      && A
    }
    \,.
  $$

A [[homomorphism]] of monoids $(A_1, \mu_1, e_1)\longrightarrow (A_2, \mu_2, f_2)$ is a morphism

$$
  f \;\colon\; A_1 \longrightarrow A_2
$$ 

in $\mathcal{C}$, such that the following two [[commuting diagram|diagrams commute]]

$$
  \array{
    A_1 \otimes A_1 
      &\overset{f \otimes f}{\longrightarrow}&
    A_2 \otimes A_2
    \\
    {}^{\mathllap{\mu_1}}\downarrow && \downarrow^{\mathrlap{\mu_2}}
    \\
    A_1 &\underset{f}{\longrightarrow}& A_2
  }
$$

and

$$
  \array{
    1_{\mathcal{c}} &\overset{e_1}{\longrightarrow}& A_1
    \\
    & {}_{\mathllap{e_2}}\searrow & \downarrow^{\mathrlap{f}}
    \\
    && A_2
  }
  \,.
$$

Write $Mon(\mathcal{C}, \otimes,1)$ for the [[category of monoids]] in $\mathcal{C}$, and $CMon(\mathcal{C}, \otimes, 1)$ for its subcategory of commutative monoids.

=--

## Examples
 {#Examples}

+-- {: .num_example}
###### Example
**([[commutative rings]])**

Write $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ for the category [[Ab]] of [[abelian groups]], equipped with the [[tensor product of abelian groups]] whose [[tensor unit]] is the additive group of [[integers]]. With the evident [[braiding]] this is a [[symmetric monoidal category]]. 

A commutative monoid in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ is equivalently a [[commutative ring]].

=--

+-- {: .num_example}
###### Example
**([[differential graded-commutative algebras]])**

The [[category of chain complexes]] $Ch(Vect)$ with its [[tensor product of chain complexes]] carries a [[symmetric monoidal category|symmetric]] monoidal [[braiding]] given on elements in definite degree $n \in \mathbb{Z}$ by

$$
  \tau \;\colon; v \otimes W \mapsto (-1)^{ n_v n_w } w \otimes v
  \,.
$$

The corresponding commutative monoid objects are the [[differential graded-commutative algebras]].

=--


+-- {: .num_example}
###### Example
**([[differential graded-commutative superalgebras]])**

The [[category of chain complexes of super vector spaces]] $Ch(SuperVect)$ with its [[tensor product of chain complexes]] carries two [[symmetric monoidal category|symmetric]] monoidal [[braidings]] given on elements in definite bidegree $(n,\sigma) \in \mathbb{Z} \times \mathbb{Z}/2$ by

1. $\tau_{Deligne} \;\colon\; v \otimes w \mapsto (-1)^{ (n_v n_w + \sigma_v \sigma_w) } w \otimes v$;

1. $\tau_{Bernst} \;\colon\; v \otimes w \mapsto (-1)^{ (n_v + \sigma_v) (n_w + \sigma_w) } w \otimes v$.

The corresponding commutative monoid objects are the [[differential graded-commutative superalgebras]].

[[!include sign rules in homological superalgebra -- table]]

Since the two braidings above are equivalent ([this Prop](chain+complex+in+super+vector+spaces#EquivalenceTwoSymmetricMonoidalStructuresOnChSuperVect)) the corresponding two categories of [[differential graded-commutative superalgebras]] are also canonically [[equivalence of categories]]:

$$
    ComMon\left(  Ch(SuperVect), \otimes, \tau_{Deligne} \right)
    \;\simeq\;
    ComMon\left(  Ch(SuperVect), \otimes, \tau_{Bernst} \right)
$$

$$
  sdgcAlg_{Deligne}
  \;\simeq\;
  sdgcAlg_{Bernst}
$$


=--

+-- {: .num_example}
###### Example
**([[commutative ring spectra]], [[E-infinity rings]])**

Write $(SymSpec(Top_{cg}),\wedge, \mathbb{S}_{sym})$ and $(OrthSpec(Top_{cg}),\wedge, \mathbb{S}_{orth})$ and $([Top^{\ast/}_{cg,fin}, Top^{\ast/}_{cg}], \wedge, \mathbb{S} )$ for the categories, respectively of [[symmetric spectra]], [[orthogonal spectra]] and [[pre-excisive functors]], equipped with their [[symmetric monoidal smash product of spectra]], whose [[tensor unit]] is the corresponding standard incarnation of the [[sphere spectrum]]. 

A commutative monoid in any one of these three categories is equivalently a [[commutative ring spectrum]] in the strong sense: via the respective [[model structure on spectra]] it represents an [[E-infinity ring]].

=--

+-- {: .num_example}
###### Example
**(in a cocartesian monoidal category)**

Every object $A$ in a [[cocartesian monoidal category]] $C$ becomes a commutative monoid in a unique way: the multiplication must be the [[fold map]] $\nabla \colon A + A \to A$, and the counit must be the unique map $! \colon 0 \to A$.  Similarly every morphism in $C$ becomes a morphism of commutative monoid objects, so the category of commutative monoid objects in $C$ is isomorphic to $C$.

=--

+-- {: .num_example}
###### Example
**(in $CommMon$)**

Since the category $CommMon$ of commutative monoids (in $Set$) is cocartesian, the category of commutative monoids in $(CommMon,+)$ is again $CommMon$.   Finite coproducts of commutative monoids are also finite products, so the category of commutative monoids in $(CommMon,\times)$ is also $CommMon$.

=--




## Related concepts

* [[monoid]], [[commutative monoid]]
* [[monoid in a monoidal category]]
* [[category of monoids]]
* [[module over a monoid]]
* [[semilattice object]]
* [[commutative monoid in a symmetric monoidal (infinity,1)-category]]

## References

Categorical properties of [[commutative monoid objects]] in [[symmetric monoidal categories]] are spelled out in sections 1.2 and 1.3 of

* Florian Marty, _Des Ouverts Zariski et des Morphismes Lisses en G&#233;om&#233;trie Relative_, Ph.D. Thesis, 2009, [web](http://thesesups.ups-tlse.fr/540/)

A summary is in section 4.1 of

* [[Martin Brandenburg]], _Tensor categorical foundations of algebraic geometry_, [arXiv:1410.1716](http://arxiv.org/abs/1410.1716).

See also [MO/180673](http://mathoverflow.net/questions/180673/category-of-modules-over-commutative-monoid-in-symmetric-monoidal-category).

[[!redirects commutative monoid object]]
[[!redirects commutative monoid objects]]

[[!redirects commutative monoids in a symmetric monoidal category]]

[[!redirects commutative monoids in a monoidal category]]
[[!redirects commutative monoids in monoidal categories]]

[[!redirects commutative monoid object in a monoidal category]]
[[!redirects commutative monoid objects in a monoidal category]]
[[!redirects commutative monoid objects in monoidal categories]]
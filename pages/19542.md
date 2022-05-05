

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Algebra
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _[[chain complex]]_ $V_\bullet$ of [[super vector spaces]] is for each $n \in \mathbb{Z}$ a [[super  vector space]] $V_n = (V_n)_\even \oplus (V_n)_odd$, equipped with a [[differential]], hence for each $n \in \mathbb{Z}$ a [[morphism]] $\partial_n \;\colon\; V_{n+1} \to V_n$ of [[super vector spaces]] such that $\partial \circ \partial = 0$.

The [[category]] $Ch(SuperVect)$ of chain complexes of super vector space is much like the [[category of chain complexes]] $Ch(Vect)$ of ordinary [[vector spaces]], in particular in that it carries the [[tensor product of chain complexes]] that makes it a [[monoidal category]]. But there is a non-trivial [[symmetric monoidal category|symmetric]] [[braiding]] on $Ch(SuperVect)$ which involves not just the signs used in the braiding in $Ch(Vect)$, but also the signs involved in the defining nonp-trivial braiding on [[super vector space|SuperVect]]. The [[commutative monoid in a symmetric monoidal category|commutative monoids]] with respect to this symmetric braiding on $Ch(SuperVect)$ are the [[differential graded-commutative superalgebras]].

In fact there are two such such non-trivial symmetric braidings on $Ch(SuperVect)$ (Prop. \ref{SymmetricStructureOnCategoryOfChainComplexesOfSuperVectorSpaces} below), but they are equivalent to each other (Prop. \ref{EquivalenceTwoSymmetricMonoidalStructuresOnChSuperVect} below).

## Definition

+-- {: .num_defn #ChainComplexesOfSuperVectorSpaces}
###### Definition
**([[chain complexes]] of [[super vector spaces]])**

Write $Ch(SuperVect)$ for the [[category of chain complexes]] inside the category of [[super vector spaces]].

Hence for $V_\bullet \in Ch(SuperVect)$ an [[object]], for each $n \in \mathbb{Z}$ there is a [[super vector space]] 

$$
  V_n = (V_n)_{even} \oplus (V_n)_{odd} \;\in SuperVect
$$

where we write the elements of the [[group of order two]] as $\mathbb{Z}/2 =\{even, odd\}$, with $even$ being the [[neutral element]].

Hence we may regard any $V_\bullet \in Ch(SuperVect)$ equivalently as a $\mathbb{Z} \times (\mathbb{Z}/2)$-[[graded object|graded]] [[vector space]] equipped with a [[differential]] of degree $(1,even)$. For $v \in V$ an element in definite ("homogeneous") bi-degree, we denote this degree by

\[
  \label{BidegreeOnChainComplexOfSuperVectorSpaces}
  deg(v) \coloneqq (n_v, \sigma_v) \;\in\; \mathbb{Z} \times (\mathbb{Z}/2) 
  \,.
\]

The category $Ch(SuperVect)$ becomes a [[monoidal category]] under the [[tensor product of chain complexes]] applied to the tensor product of [[super vector spaces]]. This means that for $V, W \in Ch(SuperVect)$, the [[differential]] on a homogeneously graded element $v \otimes w \in V \otimes W$ is

$$
  \partial(v \otimes w)
  \;=\;
  (\partial v) \otimes w 
  +
  (-1)^{ n_v } v \otimes \partial w
  \,.
$$

=--

## Properties

### Symmetric monoidal structure

+-- {: .num_prop #SymmetricStructureOnCategoryOfChainComplexesOfSuperVectorSpaces}
###### Proposition
**([[symmetric monoidal category|symmetric monoidal]] [[structure]] on category of chain complexes of super vector spaces)**

The [[monoidal category|monoidal]] category of chain complexes of super vector spaces $(Ch(SuperVect), \otimes)$ from Def. \ref{ChainComplexesOfSuperVectorSpaces} becomes a [[symmetric monoidal category|symmetric monoidal]] with each of the following two [[braiding]] [[isomorphisms]], defined on tensor products of elements in homogenous bi-degree (eq:BidegreeOnChainComplexOfSuperVectorSpaces) as follows:

1. $\tau_{Deligne} \;\colon\; v \otimes w \mapsto (-1)^{ (n_v n_w + \sigma_v \sigma_w) } w \otimes v$;

1. $\tau_{Bernst} \;\colon\; v \otimes w \mapsto (-1)^{ (n_v + \sigma_v) (n_w + \sigma_w) } w \otimes v$.

Here in the exponents we are using the canonical [[ring]]-[[structure]] on the [[integers]] $\mathbb{Z}$ and on the [[prime field]] $\mathbb{Z}/2 = \mathbb{F}_2$, the implicit [[ring homomorphism]] $\mathbb{Z} \to \mathbb{Z}/2$ and we understand that $(-1)^{even} = 1$ and $(-1)^{odd} = -1$.

=--

+-- {: .proof}
###### Proof

Since the expressions for both sign factors are symmetric in $v$ and $w$ in both cases, it is clear that $\tau_{w,v} \circ \tau_{v,w} = id_{v \otimes w}$ in both cases. Hence if $\tau$ is indeed a [[braiding]], then it is [[symmetric monoidal category|symmetric]].

To see that $\tau$ is indeed a [[braiding]] in each case, we need to check the [[hexagon identities]]

$$
  \array{
   (V_1 \otimes V_2) \otimes V_3 
   &\overset{a_{V_1, V_2, V_3}}{\longrightarrow}&
   V_1 \otimes (V_2 \otimes V_3)
   &\overset{\tau_{V_1,V_2 \otimes V_3}}{\longrightarrow}&
   (V_2 \otimes V_3) \otimes V_1
   \\
   \Big\downarrow{}^{\tau_{V_1,V_2}\otimes Id}
   &&&&
   \Big\downarrow{}^{a_{V_2,V_3,V_1}}
   \\
   (V_2 \otimes V_1) \otimes V_3
   &\overset{a_{V_2,V_1,V_3}}{\longrightarrow}&
   V_2 \otimes (V_1 \otimes V_3)
   &\overset{Id \otimes \tau_{V_1,V_3}}{\longrightarrow}&
   V_2 \otimes (V_3 \otimes V_1)
  }
$$

and

$$
  \array{
   V_1 \otimes (V_2 \otimes V_3) 
   &\overset{a^{-1}_{V_1,V_2,V_3}}{\longrightarrow}&
   (V_1 \otimes V_2) \otimes V_3
   &\overset{\tau_{V_1 \otimes V_2, V_3}}{\longrightarrow}&
   V_3 \otimes (V_1 \otimes V_2)
   \\
   \Big\downarrow{}^{id \otimes \tau_{V_2,V_3}}
   &&&&
   \Big\downarrow{}^{a^{-1}_{V_3,V_1,V_2}}
   \\
   V_1 \otimes (V_3 \otimes V_2)
   &\overset{a^{-1}_{V_1,V_3,V_2}}{\longrightarrow}&
   (V_1 \otimes V_3) \otimes V_2
   &\overset{\tau_{V_1,V_3} \otimes id}{\longrightarrow}&
   (V_3 \otimes V_1) \otimes V_2
  }
  \,.
$$

Since $\tau$ differs only by multiplication by a sign from the standard symmetric braiding on the [[category of vector spaces]], which does satisfy its hexagon identities, it just remains to check that these sign factors picked up in going both ways around these diagrams agree. 

Hence for $\tau_{Deligne}$ the two hexagon identities are equivalent to the conditions

$$
  (-1)^{ n_1 (n_2 + n_3) + \sigma_1( \sigma_2 + \sigma_3 )  }
  \;=\;
  (-1)^{ n_1 n_2 + \sigma_1 \sigma_2 + n_1 n_3 + \sigma_1 \sigma_3 }
$$

and

$$
  (-1)^{ (n_1 + n_2) n_3 + (\sigma_1 + \sigma_2) \sigma_3 }
  \;=\;
  (-1)^{ n_1 n_3 + \sigma_1 \sigma_3 + n_2 n_3 + \sigma_2 \sigma_3 }
$$

while for $\tau_{Bernst}$ they are equivalent to the conditions

$$
  (-1)^{ (n_1 + \sigma_1)( n_2 + \sigma_2 + n_3 + \sigma_3  ) }
  \;=\;
  (-1)^{ (n_1 + \sigma_1)(n_2 + \sigma_2) + (n_1 + \sigma_1)(n_3 + \sigma_3)  }
$$

and

$$
  (-1)^{ (n_1 + \sigma_1 + n_2 + \sigma_2)(n_3 + \sigma_3) }
  \;=\;
  (-1)^{ (n_1 + \sigma_1)(n_3 + \sigma_3) + (n_2 + \sigma_2)(n_3 + \sigma_3) }
$$

for all triples of bi-degrees $(n_i, \sigma_i) \in \mathbb{Z} \times (\mathbb{Z}/2)$.

In both cases this holds because already the relevant [[exponents]] are equal in each case, by the [[distributive law]] for [[multiplication]] and [[addition]] in $\mathbb{Z}/2 = \mathbb{F}_2$.

=--


+-- {: .num_prop #EquivalenceTwoSymmetricMonoidalStructuresOnChSuperVect}
###### Proposition
**(the two [[symmetric monoidal category|symmetric monoidal]] [[structures]] on the category of chain complexes of super vector spaces are equivalent)**


The two [[symmetric monoidal category]] [[structures]] $\tau_{Deligne}$ and $\tau_{Bernst}$ on the [[monoidal category|monoidal]] [[category of chain complexes of super vector spaces]] $(Ch(SuperVect), \otimes)$ from Prop. \ref{SymmetricStructureOnCategoryOfChainComplexesOfSuperVectorSpaces} are equivalent

$$
  \tau_{Deligne}
  \;\simeq\;
  \tau_{Bernst}
$$

in that the [[identity functor]] $Ch(SuperVect) \overset{id}{\longrightarrow} Ch(SuperVect)$ equipped with the following monoidal [[natural isomorphism]] 

$$
  \array{
    id(V) \otimes id(W) \overset{\mu}{\longrightarrow} id(V \otimes W)
    \\
    v \otimes w
    \;\mapsto\;
    (-1)^{ n_v \sigma_w  } \, v \otimes w
  }
$$

(the second line shows its action on elements of homogeneous bidegree $(n,\sigma) \in \mathbb{Z} \times (\mathbb{Z}/2)$)

becomes a [[nLab:strong monoidal functor|strong]] [[symmetric monoidal functor]] 

$$
  (Ch(SuperVect), \otimes, \tau_{Deligne})
  \underoverset{\simeq}{(id,\mu)}{\longrightarrow}
  (Ch(SuperVect), \otimes, \tau_{Bernst})
  \,.
$$

=--

([Deligne-Morgan 99, remark 1.2.8](#DeligneMorgan99))

+-- {: .proof}
###### Proof

First to see that we have a [[strong monoidal functor]], we need to check the [[associativity]] condition


$$
  \array{
    (id(V_1) \otimes id(V_2)) \otimes id(V_3)
      &\underoverset{\simeq}{a_{id(V_1),id(V_2),id(V_3)}}{\longrightarrow}&
    id(V_1) \otimes( id(V_2)\otimes id(V_3) )
    \\
    {}^{\mathllap{\mu_{V_1,V_2} \otimes id}}\downarrow 
      && 
    \Big\downarrow{}^{\mathrlap{id\otimes \mu_{V_2,V_3}}}
    \\
    id(V_1 \otimes V_2) \otimes id(V_3)
     &&
    id(V_1) \otimes id(V_2 \otimes V_3)
    \\
    {}^{\mathllap{\mu_{V_1 \otimes V_2 , V_3} } }\Big\downarrow 
      && 
    \Big\downarrow^{\mathrlap{\mu_{ V_1, V_2 \otimes V_3  }}}
    \\
    id( ( V_1 \otimes V_2 ) \otimes V_3  )
      &\underset{id(a_{V_1,V_2,V_3})}{\longrightarrow}&
    id( V_1 \otimes ( V_2 \otimes V_3 ) )
  }
  \,,
$$

and the [[unitality]] conditions


$$
  \array{
    1 \otimes id(V)
      &\overset{\epsilon \otimes id}{\longrightarrow}&
    id(1) \otimes id(V)
    \\
    {}^{\mathllap{\ell_{id(V)}}}\Big\downarrow 
      && 
    \Big\downarrow{}^{\mathrlap{\mu_{1, V }}}
    \\
    id(V) 
      &\overset{id(\ell_V )}{\longleftarrow}&
    id(1 \otimes V  )
  }
$$

and  

$$
  \array{
    id(V) \otimes  1
      &\overset{id \otimes \epsilon }{\longrightarrow}&
    id(V) \otimes  id(1) 
    \\
    {}^{\mathllap{r_{id(V)}}}\Big\downarrow 
      && 
    \Big\downarrow{}^{\mathrlap{\mu_{V, 1 }}}
    \\
    id(V) 
      &\overset{F(r_V )}{\longleftarrow}&
    id(V \otimes 1  )
  }
  \,,
$$

Since $\mu$ differs from the trivial monoidal isomorphism only by the sign factor, this is equivalent to the condition that the sign factors picked up in going both ways around these diagrams agree.

For [[associativity]] this is the condition

$$
  (-1)^{
    n_1 \sigma_2 + (n_1 + n_2)\sigma_3
  }
  \;=\;
  (-1)^{
    n_2 \sigma_3 + n_1 (\sigma_2 + \sigma_3)
  }
$$

for all bi-degrees $(n_i, \sigma_i) \in \mathbb{Z} \times (\mathbb{Z}/2)$,
which holds, because it already holds for the [[exponents]] themselves, as an identity in $\mathbb{Z}/2 =\mathbb{F}_2$.

For the [[unitality]] condition this is the statement that the sign given by $\mu_{1,x}$ and $\mu_{x,1}$ is the the trivial sign $(-1)^0 = 1$. This is indeed the case because the [[tensor unit]] is in degree $0 = (0,even) \in \mathbb{Z} \times (\mathbb{Z}/2)$.

Now to see that we have a [[symmetric monoidal functor]], we need to show that it intertwines the two [[symmetric monoidal category|symmetruc]] [[braiding]] [[isomorphisms]]


$$
  \array{
    id(V_1) \otimes id(V_2) 
      &\stackrel{\tau_{Bernst}}{\longrightarrow}& id(V_2) \otimes id(V_1)
    \\
    {}^{\mathllap{\mu_{V_1,V_2}}}\Big\downarrow 
    && 
    \Big\downarrow{}^{\mathrlap{\mu_{V_2,V_1}}}
    \\
    id(V_1\otimes V_2) 
      &\overset{id(\tau_{Deligne})}{\longrightarrow}& if(W \otimes V)
  }
$$

As before, this is equivalent to a condition on the signs picked up both ways, which reads:

$$
  (-1)^{ (n_1 + \sigma_1)(n_2 + \sigma_2) + n_2 \sigma_1}
  \;=\;
  (-1)^{ n_1 \sigma_2 + n_1 n_2 + \sigma_1 \sigma_2 }
  \,.
$$

Inspection shows that this is indeed the case: 

The two signs of $\tau_{Deligne}$ and $\tau_{Bernst}$ differ by the "mixed terms" that are produced in [[distributivity|multiplying out]] $(n_v + \sigma_v)(n_w + \sigma_w)$ and these two mixed terms is just what the two occurences $\mu$ provides (using that $+1 = -1 \in \mathbb{F}_2$).

=--

### Differential graded-commutative superalgebras


+-- {: .num_defn}
###### Definition

A [[differential graded-commutative superalgebra]] is a [[commutative monoid in a symmetric monoidal category|commutative monoid]] in the [[symmetric monoidal category]] of [[chain complexes of super vector spaces]], for either of the symmetric monoidal structures from Prop. \ref{SymmetricStructureOnCategoryOfChainComplexesOfSuperVectorSpaces}.

$$
  sdgcAlg_{Deligne}
  \;\coloneqq\;
  ComMon\left(  Ch(SuperVect), \otimes, \tau_{Deligne} \right)
$$

$$
  sdgcAlg_{Benrst}
  \;\coloneqq\;
  ComMon\left(  Ch(SuperVect), \otimes, \tau_{Bernst} \right)
$$

The resulting [[signs in supergeometry|sign rule]] is this:

[[!include sign rules in homological superalgebra -- table]]

Since the [[identity functor]] carries a [[strong monoidal functor|strong]] [[symmetric monoidal functor|symmetric monoidal]] [[equivalence of categories]] (Prop. \ref{EquivalenceTwoSymmetricMonoidalStructuresOnChSuperVect})

$$
    \left(  Ch(SuperVect), \otimes, \tau_{Deligne} \right)
    \;\simeq\;
    \left(  Ch(SuperVect), \otimes, \tau_{Bernst} \right)
$$

there is an induced [[equivalence of categories]] of the corresponding [[commutative monoids in a symmetric monoidal category|symmetric monoids]]

$$
    ComMon\left(  Ch(SuperVect), \otimes, \tau_{Deligne} \right)
    \;\simeq\;
    ComMon\left(  Ch(SuperVect), \otimes, \tau_{Bernst} \right)
$$

hence of these two versions of [[differential graded-commutative superalgebras]]:

$$
  sdgcAlg_{Deligne}
  \;\simeq\;
  sdgcAlg_{Bernst}
$$

=--

### Model category structure

See at _[[model structure on chain complexes of super vector spaces]]_.

## Related concepts

* [[super L-infinity algebra]]

* [[model structure on differential graded-commutative superalgebras]]

## References

* {#DeligneMorgan99} [[Pierre Deligne]], [[John Morgan]], _Notes on supersymmetry_, remark 1.2.8 in [[NotesOnNotesOnSupersymmetry.pdf:file]]

  in [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], [[John Morgan]], [[David Morrison]], [[Edward Witten|E. Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))


[[!redirects chain complexes in super vector spaces]]

[[!redirects chain complex of super vector spaces]]
[[!redirects chain complexes of super vector spaces]]

[[!redirects category of chain complexes of super vector spaces]]

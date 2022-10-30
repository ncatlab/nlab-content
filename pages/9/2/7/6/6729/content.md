
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _derived critical locus_ is the refinement of the notion of [[critical locus]] from [[geometry]] to [[derived geometry]].

The formal duals to derived critical loci are described by [[BV-BRST formalism]].

## Details

The following is a basic setup in [[dg-geometry]] aimed at exhibiting the (formal dual of) the [[BV-BRST complex]] as the derived critical locus of (the formal dual of) the [[BRST complex]] (the example [below](#ComparisonToBVBRSTExample))

### Basic dg-geometry
 {#BasicDgGeometry}

Let $k$ be a [[field]] of [[characteristic zero]]. 

Write $dgcAlg_k$ for the [[category]] of unbounded cochain [[differential graded-commutative algebras]] (dgc-algebras) over $k$.

An object in the [[opposite category]] 

$$
  C \in cdgAlg_k^{op}
$$

we may regard as an affine space in [[dg-geometry]], and hence we write

$$
  \mathcal{O}(C) \in cdgAlg_k
$$

for the corresponding dgc-algebra.

Let $\mathcal{O}(C)$[[Mod]] be the [[category of dg-modules]] over $\mathcal{O}(C)$ equipped with the standard [[model structure on dg-modules]].



+-- {: .num_defn #OCDGCAlgebras}
###### Definition
**([[dgc-algebras]] over $\mathcal{O}(C)$)**

Write

$$
  \begin{aligned}
    cdgAlg_{\mathcal{O}(C)} 
      & \coloneqq 
    CMon(\mathcal{O}(C) Mod)
    \\
      & \simeq
    \mathcal{O}(C)/_{cdgAlg_k}
  \end{aligned}
$$

for the [[category of monoids|category of commutative monoids]] in $\mathcal{O}(C)$-modules, equivalently the [[coslice category]] of $cdgAlg_k$ under $\mathcal{O}(C)$.

=--


+-- {: .num_prop #SymOCAdjunction}
###### Proposition

There is a [[model category]] structure on $cdgAlg_{\mathcal{O}(C)}$ (def. \ref{OCDGCAlgebras}) whose fibrations and weak equivalences are those of the underlying $\mathcal{O}(C)$-modules such that the [[free-forgetful adjunction]]


$$
  cdgAlg_{\mathcal{O}(C)}
   \underoverset
     {\underset{U}{\longrightarrow}}
     {\overset{Sym_{\mathcal{O}(C)}}{\longleftarrow}}
     {\bot}
  \mathcal{O}(C) Mod
$$

is a [[Quillen adjunction]].

This is 

1. [[combinatorial model category|combinatorial]];

1. [[proper model category|proper]].

=--

+-- {: .proof}
###### Proof

This follows with the general discussion at _[[dg-geometry]]_. We indicate how to see it directly.

We observe that the adjunction exhibits the [[transferred model structure]] on the left. By the statement discussed there, it is sufficient to check that

1. $\mathcal{O}(C) Mod$ is a [[cofibrantly generated model category]].

   This follows because the [[nLab:model structure on dg-modules]] (as discussed there) is itself transferred along

   $$
     U' \colon \mathcal{O}(C) Mod \to Ch^\bullet(k)
   $$

   from the cofibrantly generated [[model structure on chain complexes|model structure on cochain complexes]].

1. $U$ preserves [[filtered colimits]]. 

   This follows from the general fact $U : CMon(\mathcal{C}) \to \mathcal{C}$ creates filtered colimits for $\mathcal{C}$ closed symmetric monoidal (see [there](category+of+monoids#FilteredColimits)) and that $A Mod$ is [[closed monoidal category|closed]] [[symmetric monoidal category|symmetric monoidal]] (see [there](model+structure+on+dg-modules#Properties)).

   To check this explicitly:

   Let $A_\bullet \colon D \to cdgAlg_k$ be a [[filtered category|filtered diagram]]. We claim that there is a unique way to lift the underlying colimit $\lim_\to U A_\bullet$ to a dg-algebra cocone: for $a \in A_i \to \lim_\to U A_\bullet$ and $b \in A_j \to \lim_\to U A_\bullet$ there is by the assumption that $D$ is filtered a $A_i \to A_l \leftarrow A_j$. Therefore in order for the cocone component $U A_l \to \lim_{\to} U A_\bullet$ to be an algebra homomorphism the product of $a$ with $b$ in $\lim_\to U A_\bullet$ has to be the image of this product in $A_l$. This defines the colimiting cocone $A_l \to \lim_\to A_\bullet$.

1. The left hand has functorial fibrant replacement (this is trivial, since every object is fibrant) and functorial [[path objects]]. 

   This follows by the same argument as for the path object in $cdgAlg_k$ ([here](model+structure+on+dg-algebras#PathObjectsForUnboundedCommutative)) this can be taken to be $(-)\otimes_k \Omega^\bullet_{poly}(\Delta[1])$.

=--


### Formal cotangent bundle

Given $C \in dgcAlg_k^{op}$ as [above](#BasicDgGeometry) we want to consider  its _formal [[cotangent bundle]]_ $T^\ast_f c$, i.e. the [[infinitesimal neighbourhood]] around the [[zero section]] of the would-be actual [[cotangent bundle]]

+-- {: .num_defn}
###### Definition

Write 

$$
  Der(\mathcal{O}(C)) \in \mathcal{O}(C) Mod
$$ 

for the [[automorphism ∞-Lie algebra]] of $A$ whose underlying cochain complex is

$$
  \array{
    \cdots
      \to
    Der(\mathcal{O}(C))_k
      \overset{[d_{\mathcal{O}(C)},-]}{\longrightarrow}
    Der(\mathcal{O}(C))_{k+1}
      \longrightarrow
    \cdots
  }
  \,.
$$

where $Der(\mathcal{O}(C))_k$ is the module of [[derivations]]

$$
  v \colon \mathcal{O}(C)^\bullet \to \mathcal{O}(C)^{\bullet + k}
$$

of degree $k$ and $[d_{\mathcal{O}(C)}, -]$ is the graded commutator of derivations with the [[differential]] of $\mathcal{O}(C)$ regarded as a degree 1 derivation $d_{\mathcal{O}(C)} \colon \mathcal{O}(C) \to \mathcal{O}(C)$.

We say that $\mathcal{O}(C)$ is _smooth_ if $Der(\mathcal{O}(C))$ is cofibrant as an object on $\mathcal{O}(C) Mod$.

Write

$$
  \mathcal{O}(T^*_f C)
    \coloneqq
  Sym_{\mathcal{O}(C)} Der(\mathcal{O}(C))
   \in 
  cdgAlg_{\mathcal{O}(C)}
$$

for the free $\mathcal{O}(C)$-algebra over $Der(\mathcal{O}(C))$. 

We write

$$
  T^*_f C \in cdgAlg^{op}_k/_C
$$

for its formal dual.

=--

+-- {: .num_defn}
###### Remark

Every $S \in \mathcal{O}(C)$ defines a morphism

$$
  d S \colon C \to T^*_f C
$$

in $dgcAlg_k^{op}$ which is dually given by

$$
  \mathcal{O}(C) 
    \leftarrow 
   Sym_{\mathcal{O}(C)} Der(\mathcal{O}(C))
    \;\colon\;
   Sym_{\mathcal{O}(C)} [\hat S , -]
  \,,
$$

where $\hat S : \mathcal{O}(C) \to \mathcal{O}(C)$ is the $k$-linear multiplication operator defined by $S$ and where for 
$v \in Der(\mathcal{O}(C))$ we set

$$
  [\hat S, v] = v(S)
  \,,
$$

which may be regarded as the multiplication operator given by the commutator of $k$-linear endomorphisms of $\mathcal{O}(C)$ as indicated.

=--


### Derived critical locus


+-- {: .num_defn #DerivedCriticalLocusWithFormalCotangentBundle}
###### Definition
**(derived critical locus)**

The **derived critical locus** of a morphism  $S \colon C \to \mathbb{A}^1$ in dgcAlg_k 
is the [[homotopy pullback]] $C_{\{d S = 0\}}$ in $cdgAlg^{op}/_{C}$

$$
  \array{
    C_{\{d S = 0\}} &\to& C
    \\
    \downarrow &\swArrow& \downarrow^{\mathrlap{0}}
    \\
    C &\stackrel{d S}{\to}& T^*_f C
  }
  \,.
$$

=--


+-- {: .num_prop #PresentationByFreeDGCAlegbraOnMappingCone}
###### Proposition
**(presentation by free dgc-algebra on mapping cone)**

If $C$ is smooth in the sense that $Der(\mathcal{O}(C)) \in \mathcal{O}(C) Mod$ is cofibrant, then the derived critical locus (def. \ref{DerivedCriticalLocusWithFormalCotangentBundle}) is presented by

$$
  \mathcal{O}(C_{\{d S = 0\}})
   \simeq
  Sym_{\mathcal{O}(C)}
  \left(
     Cone\left( 
       Der(\mathcal{O}(C)) \stackrel{[\hat S , -]}{\to} \mathcal{O}(C)
    \right)
  \right)
    \underset{Sym_{\mathcal{O}(C)}(\mathcal{O}(C))  }{\otimes}
  \mathcal{O}(C)
  \,,
$$

where on the right we have the free $\mathcal{O}(C)$-algebra over the [[mapping cone]] of $[\hat S, -]$ with [[extension of scalars]] along $\mathcal{O}( C \overset{(id,0)}{\to} C \times \mathbb{A}^1 )$.

=--


+-- {: .proof}
###### Proof

Using the [[pasting law]] we may decompose the homotopy pullback into a [[pasting]] of two homotopy pullback squares as follows:

$$
  \array{
    C_{\{d S = 0\}} &\longrightarrow& &\longrightarrow& C
    \\
    \downarrow &\swArrow& \downarrow &\swArrow& \downarrow^{\mathrlap{0}}
    \\
    C 
      &\underset{(id,0)}{\longrightarrow}& 
    C \times \mathbb{A}^1 &\underset{}{\longrightarrow}& T^*_f C
  }
  \,.
$$

First consider the square on the right:

By prop \ref{SymOCAdjunction} the functor $Sym_{\mathcal{O}(C)}$ is left Quillen. Hence if $Der(\mathcal{O}(C))$ is cofibrant in $\mathcal{O}(C) Mod$ then the homotopy pushout corresponding to the square on the right may be computed as the image under $Sym_{\mathcal{O}(C)}$ of the homotopy pushout in $\mathcal{O}(C) Mod$.

By the disucssion at [[model structure on dg-modules]], for these the homotopy cofibers are given by the ordinary [[mapping cone]] construction for chain complexes.

$$
  \array{
    Cone\left(
      Der(\mathcal{O}(C)) \stackrel{[\hat S, -]}{\to} \mathcal{O}(C)
    \right)
    &\leftarrow&
    Cone\left(
      Der(\mathcal{O}(C)) \stackrel{Id}{\to} Der(\mathcal{O}(C))
    \right)
    \\
    \uparrow && \uparrow
    \\
    \mathcal{O}(C)
    &\stackrel{[\hat S, -]}{\leftarrow}&
    Der(\mathcal{O}(C))
  }
  \,.
$$

More in detail, write 

$$
  Cone\left(
    Der(\mathcal{O}(C)) \stackrel{Id}{\to} Der(\mathcal{O}(C))
  \right)
   \in 
  \mathcal{O}(C) Mod
$$

for the [[mapping cone]] on the identity:

$$
  \array{
     \cdots
     & 
     Der(\mathcal{O}(C))_k &\stackrel{-[d_{\mathcal{O}(C)}, -]}{\to}&
     Der(\mathcal{O}(C))_{k+1}
     \\
     & \oplus &\searrow^{\pm \mathrlap{Id}}& \oplus & \cdots
     \\
     \cdots
     & Der(\mathcal{O}(C))_{k-1} 
        &\stackrel{[d_{\mathcal{O}(C)}, -]}{\to}&
     Der(\mathcal{O}(C))_k    
     &
     \cdots
  }
  \,.
$$

Then the [[mapping cone]] $Cone\left(Der(\mathcal{O}(C)) \stackrel{[\hat S, -]}{\to}  \mathcal{O}(C) \right)$ is

\[
  \label{TheBVComplex}
  \array{
     \cdots
     & 
     Der(\mathcal{O}(C))_k &\stackrel{-[d_{\mathcal{O}(C)}, -]}{\to}&
     Der(\mathcal{O}(C))_{k+1}
     \\
     & \oplus &\searrow^{\pm [\hat S, -]}& \oplus & \cdots
     \\
     \cdots
     & \mathcal{O}(C)_{k-1} 
        &\stackrel{[d_{\mathcal{O}(C)}, -]}{\to}&
     \mathcal{O}(C)_k    
     &
     \cdots
  }
  \,.
\]

If we extend the graded commutators in the evident way we may write the [[nLab:differential]] in $Cone(Der(\mathcal{O}(C)) \stackrel{[\hat S, -]}{\to} \mathcal{O}(C))$ as

$$
  d  
   = 
  \left[
    \hat S 
      + 
    d_{\mathcal{O}(C)}
    \;,\; 
    -
  \right]
  \,.
$$

Here the second term will be the differential of the [[nLab:BRST-complex]] of $\mathfrak{c}$, whereas the sum is of the type of a differential in a [[nLab:BRST-BV complex]].

For that to happen, however the two copies of $\mathcal{O}(C)$ in $Sym_{\mathcal{O}(C)}(\mathcal{O}(C))$ need to be identified, this is achived by the remaining homotopy pushout corresponding to the square on the left

$$
  \array{
    \mathcal{O}(C_{\{d S = 0\}})
    &\longleftarrow&
    Sym_{\mathcal{O}(C)}
    \left(
      Cone\left(
        Der(\mathcal{O}(C)) \stackrel{[\hat S, -]}{\to} \mathcal{O}(C)
      \right)
    \right)
    \\
    \uparrow && \uparrow
    \\
    \mathcal{O}(C)
       &\underset{}{\longleftarrow}& 
    Sym_{\mathcal{O}(C)}(\mathcal{O}(C))
  }
  \,.
$$

Since here the morphism on the right is the pushout of a cofibration, it is itself still a cofibration, and by assumption $Sym_{\mathcal{O}(C)}(\mathcal{O}(C))$ is cofibrant. Therefore this homotopy pushout is given by the ordinary pushout, and that yields the [[tensor product]] as in the claim.

=--




### BV-BRST complex
 {#ComparisonToBVBRSTExample}

Traditionally the [[BV-BRST complex]] of a [[Lagrangian field theory]] is obtained by 

1. choosing a [[Koszul-Tate complex]] $s_{KT}$ resolving the [[shell]];

1. choosing a [[BRST complex]] $s_{BRST}$ exhibiting the [[gauge invariance]]

1. appealing to [[homological perturbation theory]], for extending the sum of the two differentials to a unified [[BV-BRST differential]]

   $$
     s_{BV} = s_{KT} + s_{BRST} + more
   $$


(e.g. [Henneaux 90. around (50)](BV-BRST+formalism#Henneaux90))

Vie the concept of the derived critical locus this process is systematized: Given just $s_{BRST}$ and the Lagrangian, both $s_{KT}$ and "more" follows (if $s_{BRST}$ does capture all the relevant gauge symmetries, that is) and the appearance of the [[antibracket]] finds its conceptual explanation.


Let $\mathfrak{a}$ be a [[Lie algebroid]] over a space $X$, with [[Chevalley-Eilenberg algebra]] 

$$
  \mathcal{O}(\mathfrak{a})
  \;=\;
  \left(
    Sym_{\mathcal{O}(X)}(\langle c^a\rangle)
    \;,\;
    d_{\mathfrak{a}}
  \right)
$$

with differential given by

$$
  d_{\mathfrak{a}} 
    \;:\; 
  f \mapsto c^a R^i_a \frac{\partial}{\partial x^i} f
$$

$$
  d_{\mathfrak{a}} \;:\; 
   c^a 
    \mapsto 
   \frac{1}{2} C^{a}{}_{b c} c^b \wedge c^c 
  \,.
$$

for functions $f \in \mathcal{O}(X)$, [[infinitesimal gauge symmetries]] $R^i_a \frac{\partial}{\partial x^i}$, gauge symmetry structure functions $C^{a}{}_{b c}$ and [[ghost]] generators $c^a$.

The "algebra of vector fields/[[derivations]]" $Der(\mathcal{O}(\mathfrak{a}))$ on $\mathfrak{a}$ is the [[automorphism ∞-Lie algebra]]  whose underlying cochain complex is

$$
  \array{
    \left\langle 
      \frac{\partial}{\partial c^a} 
    \right\rangle
    &
    \overset{[d_{\mathfrak{a}}, -]}{\to}
    &
    \left\langle 
      \frac{\partial}{\partial x^i} 
    \right\rangle    
    \oplus
     \left\langle 
       c^a \frac{\partial}{\partial c^b} 
     \right\rangle
    \\
    -1 && 0
  }
  \,.
$$


We check on generators that

$$
  \begin{aligned}
    \left[d_{\mathfrak{a}}, \frac{\partial}{\partial c^a} \right]  
     = 
     R_a^i \frac{\partial}{\partial x^i} 
      + 
     C^b{}_{a c} c^c \frac{\partial}{\partial c^b}
  \end{aligned}
$$

and

$$
  \begin{aligned}
    \left[
      d_{\mathfrak{a}}, \frac{\partial}{\partial x^i}
    \right]
     =
    c^a \frac{\partial R_a^j}{\partial x^i} \frac{\partial}{\partial x^j}
  \end{aligned}
  \,.
$$

Now let 

$$
  S \;\colon\; \mathfrak{a} \longrightarrow \mathbb{R}
$$

be a morphism, dually a dgc-algebra homomorphism of the form

$$
  \mathcal{O}(\mathfrak{a}) 
    \longleftarrow  
   \mathcal{O}(\mathbb{R}) 
     \;\colon\;  
   S^*
  \,.
$$

This is equivalently a function 

$$
  S \;\colon\; X \longrightarrow \mathbb{R}
$$

which is [[gauge invariance|gauge invariant]]

$$
  \begin{aligned}
    d_{\mathfrak{a}} S 
     & = 
    c^a R_a^i \frac{\partial}{\partial x^i} S 
    \\
     & = 0
   \end{aligned}
  \,.
$$

We have a contraction homomorphism of $\mathcal{O}(\mathfrak{a})$-[[modules]]

$$
  \iota_{d S} 
  \;\colon\; 
  Der(\mathcal{O}(\mathfrak{a})) 
    \longrightarrow 
  \mathcal{O}(\mathfrak{a})
  \,.
$$

and may form its [[mapping cone]] (eq:TheBVComplex) 

$$
  \array{
    \left\langle 
      \frac{\partial}{\partial c^a}
    \right\rangle
       &\stackrel{[d_{\mathfrak{a}}, -]}{\longrightarrow}&
    \left\langle 
       c^a \frac{\partial}{\partial c^b}
    \right\rangle
      \oplus
    \left\langle 
       \frac{\partial}{\partial x^i} 
    \right\rangle 
    \\
      &&
      &\searrow^{\mathrlap{\iota_{d S}}}&
    \\
      && 
      &&
    \mathcal{O}(X)
      &\stackrel{d_{\mathfrak{a}}}{\to}&
    \left\langle 
      c^a 
    \right\rangle
   \\
   -2 && -1 && 0 && 1
  }
  \,.
$$

On the free algebra of this

$$
  Sym_{\mathcal{O}(X)}
  \left(
    Der(\mathcal{O}(\mathfrak{a}))[-1] \stackrel{\iota_{d S}}{\to} \mathcal{O}(X)\oplus \langle c^a\rangle)
  \right)
$$

we have the differential given on generators by

$$
  \frac{\partial}{\partial c^a} 
   \mapsto 
  R_a^i \frac{\partial}{\partial x^i} + C^b{}_{a c} c^c 
  \frac{\partial}{\partial c^b}
$$

$$
  \frac{\partial}{\partial x^i} \mapsto \frac{\partial S}{\partial x^i}
    + 
    c^a \frac{\partial R_a^j}{\partial x^i} \frac{\partial}{\partial x^j}
$$

$$
  x^i \mapsto c^a R_a^i
$$

$$
  c^a \mapsto \frac{1}{2}C^a{}_{b c} c^b \wedge c^c
$$

and similarly after tensoring in order to identify the extra copy of $\mathcal{O}(X)$ with the base $\mathcal{O}(X)$.

If $\langle R_a\rangle$ is the full kernel of $\iota_{d S} : Der(C^\infty(X)) \to C^\infty(X)$  and there are no further relations, then this is the full [[BRST-BV complex]] of $S$.






## References

The above material is adapted from

* [[Urs Schreiber]]: _[[schreiber:derived critical locus]]_ Seminar notes, March 2011

(taking into account a correction provided by [[Vincent Schlegel]])

aimed at providing proof for the claim in

* {#CostelloGwilliam} [[Kevin Costello]], [[Owen Gwilliam]], section 4.8.1 of _[[Factorization algebras in perturbative quantum field theory]]_  ([pdf](https://pdfs.semanticscholar.org/0eb5/652340bb414869764cf5b30feed90597558d.pdf))


See also

* [[Gabriele Vezzosi]], _Derived critical loci I - Basics_, [arxiv/1109.5213](http://arxiv.org/abs/1109.5213)

* [[Tony Pantev]], [[Bertrand Toen]], M. Vaquie, G. Vezzosi, _Quantization and derived moduli spaces I: shifted symplectic structures_, [arxiv/1111.3209](http://arxiv.org/abs/1111.3209)

* [[Kevin Costello]], _Notes on supersymmetric and holomorphic field theories in dimension 2 and 4_ ([pdf](http://www.math.northwestern.edu/~costello/sullivan.pdf))

[[!redirects derived critical loci]]

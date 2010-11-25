
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}
 
## Idea

From the [[nPOV]] on [[cohomology]], the notion of Hochschild cohomology is the following.

+-- {: .standout}

Hochschild cohomology is the [[cohomology]] $\mathbf{H}(\mathcal{L}X,C)$ of [[free loop space object]]s $\mathcal{L}X$ in a [[derived stack]] [[(∞,1)-topos]] $\mathbf{H}$. 

This naturally inherits an $S^1$-action from the [[free loop space object]]. The $S^1$-[[equivariant cohomology]] refinement of Hochschild cohomology is [[cyclic cohomology]].

=--

After unwinding what this means in algebraic terms, one obtains the tradional way of conceiving Hochschild cohomology.

Hochschild homology and cohomology are characteristic objects associated to  a [[bimodule]] $N$ over a [[monoid]] $A$, in a context where $A$ is really to be thought of as a [[algebra in an (infinity,1)-category|monoid in an monoidal (∞,1)-category]].

If the [[monoid]] in  question plays the role of an _algebra of functions_ on a [[space]] $X$, $A = C(X)$,
then this has geometric interpretations. Notably
  
* the _Hochschild homology_ of $A$ regarded as a bimodule over itself 
  tends to be like the algebra of 
  [[Kähler differential]]s $\Omega^\bullet_K(A)$ on $A$, and hence is something like the algebra of [[differential form]]s on $X$;
    
* the _Hochschild cohomology_ of $A$ regarded as a bimodule over itself
  tends to be like the algebra of [[derivation]]s $Der(A)$ of $A$, 
  and hence something like the [[vector field]]s on $X$.

The seminal [[Hochschild-Kostant-Rosenberg theorem]] states that under suitable [[smooth scheme|smoothness]] conditions on $A$, these statements become exactly true.    
 
Notice that differential forms are objects in [[de Rham cohomology]] but 
are still computed by the Hochschild _homology_ of $A$. 
The terminology reflects the dualization in passing from the [[space]] $X$ to the algebra of functions $A = C(X)$ on it:
it is the Hochschild _homology_ of algebra objects that relates to the
_[[cohomology]]_ of [[space]]s.

Below in section 

* [The nPOV on Hochschild cohomology](#nPOV)

we discuss a conceptual interpretation of Hochschild homology,
that will explain _why_ this is true, and what Hochschild
homology is conceptually, from the [[nPOV]] on [[cohomology]], as 
described there.

Complementary to that, in the section 

* [More traditional description of Hochschild cohomology](#TraditionalIdeas)

we describe the original definition of Hochschild cohomology and 
the evolution of its understanding approaching the [[nPOV]].

Finally in the section titled [Details](#Details) the technical details
are spelled out.
 
 
### More traditional descriptions of Hochschild cohomology {#TraditionalIdeas}
 
Originally the notion of Hochschild cohomology was introduced as the 
[[cochain cohomology]] of a certain [[cochain complex]] associated to any [[bimodule]] $N$ over some [[algebra]] $A$: its [[bar complex]], written 
 
$$
  C_\bullet(N,A) := N \otimes_{A \otimes A^{op}} \mathrm{B}_\bullet A
  \,,
$$
  
where $N$ and $A$ are regarded as $A \otimes A^{op}$-bimodules in the obvious way.

Then it was understood that this complex is the result of tensoring the $A$-bimodules $N$ with $A$ over $A \otimes A^{op}$ but using the [[derived functor]] of the [[tensor product]] functor --  the [[Tor functor]] -- in the ambient [[model structure on chain complexes]]:
 
$$
   C_\bullet(N,A) = N \otimes^D_{A\otimes A^{op}} A = Tor^\bullet_{A\otimes A^{op}}(N,A)
   \,.
$$  
 
Then still a little later, it was understood that this is just the ordinary tensor product in the [[symmetric monoidal (∞,1)-category]] of [[chain complex]]es. If this
is understood, we can just write again simply 
$$
  C_\bullet(M,A) := N \otimes_{A \otimes A^{op}} A
  \,.
$$

This, generally, is the definition of the Hochschild homology object
of any bimodule over an [[monoid in a monoidal (∞,1)-category]]. Of special interest is the case where $N = A$. In this case this object is also called the ("$(\infty,1)$-" or "derived-")**center** of $A$:
  
$$
  Z(A) := A \otimes_{A \otimes A^{op}} A
$$
 
In parallel to this formal understanding of Hochschild homology, its
conceptual meaning has been better understood: from staring at the explicit description of $C_\bullet(N,A)$ one sees that it has something to do with [[loop space object]]s: a chain in $C_n(N,A)$ is usefully thought of as  a circle with $n$ marked points. One of these points is labeled $N$, the  other are labeled $A$. The [[differential]] on $C_\bullet(N,A)$ acts by taking tensor products over $A$ separately of all neighbour pairs of
bimodules sitting on this circle, and taking the alternating sum of this
as a collection of such circles with $(n-1)$ marked points.
 
A fully geometric understanding of these was given by Ben-Zvi/Nadler/Francis in their work on [[derived stack|derived]] [[loop space object]]s and their [[geometric ∞-function theory]]. This we unify now with our [[nPOV]]-perspective on [[cohomology]] in order to give the following [[nPOV]]-perspective on Hochschild cohomology, proper. 

 
Very concretely, Hochschild homology can be computed by the Hochschild chain complex, defined by (FILL IN). Hochschild cohomology can be computed by the Hochschild cochain complex, defined by (FILL IN). One has a cup product on the Hochschild cochain complex, defined by (FILL IN). This gives a dg algebra structure on the Hochschild cochain complex. One also has a bracket, called the Gerstenhaber bracket, defined by (FILL IN). This gives a dg Lie algebra structure on the Hochschild cochain complex. This dg Lie algebra is the one which controls the [[deformation theory|deformations]] of the algebra $A$.



### The $n$POV on Hochschild cohomology {#nPOV}

Let $\mathbf{H}$ be an [[(infinity,1)-topos]] of [[(∞,1)-category of (∞,1)-sheaves]] and let $\mathbf{K}$ the $(\infty,2)$-topos of $(\infty,2)$-sheaves on a [[site]] $C$, such that the [[quasicoherent ∞-stack]]

$$
  C : C^{op} \to (\infty,1)Cat
$$

$$
  U \mapsto Stab(C_{/U})
$$ 

as described at [[schreiber:∞-vector bundle]]
does indeed satisfy [[descent]] in that it is indeed an object 
in $\mathbf{K}$.

Recall that for $X \in \mathbf{H} \subset \mathbf{K}$ any object, its [[free loop space object]] $\mathcal{L} X$ is the $(\infty,1)$-[[pullback]]

$$
  \array{
     && \mathcal{L} X
     \\
     & \swarrow && \searrow
     \\
     X &&&& X
     \\
     & {}_{\mathllap{(Id,Id)}}\searrow && \swarrow_{\mathrlap{(Id,Id)}}
     \\
     && X \times X
  }
  \,.
$$

Notice that this is usefully thought of as the [[span trace]] of the 
[[identity]] [[span]]

$$
  \mathcal{L} X 
  = 
  Tr
  \left(
    \array{
      && X
      \\
      & {}^{\mathllap{Id}}\swarrow && \searrow^{\mathrlap{Id}}
      \\
      X &&&& X
    }
  \right)
  \,.
$$

Assume that $X$ is such that on it $C$ satisfies the axioms
of [[geometric function theory]] (see [[geometric ∞-function theory]] for more details).

Then:

The **Hochschild cohomology of $X$** is the [[cohomology]] of 
the [[free loop space object]] $\mathcal{L}X$
with coefficients in $C$:

$$
  HH(X) = \mathbf{H}(\mathcal{L}X, C) =: C(\mathcal{L}X)
  \,.
$$

$$
  HH^n(X) := HH_n(C(X)) := \pi_0\Omega^n\mathbf{H}(\mathcal{L}X, C)
  \,.
$$

By the assumption that $C(-)$ is a 
[[geometric function theory|geometric function object]] on $X$ we can rewrite 

$$
  HH(X) = \mathbf{H}(\mathcal{L}X,C) =: C(\mathcal{K}X)
$$

as 

$$
  \cdots \simeq C(X) \otimes_{C(X)\otimes C(X)^{op}}
   C(X)
  \,.
$$

This is hence indeed the Hochschild homology object $HH_\bullet(A) = A \otimes_{A \otimes A^{op}} A$ 
of the algebra object $A = \infty Mod(X)$, regarded  as a bimodule over itself.

More generally, let $f : Y \to X$ be a morphism in $\mathbf{H}$ and 
consider the [[span trace]] 

$$
  \mathcal{L}_X Y :=
  Tr
  \left(
    \array{
      && Y
      \\
      & {}^{\mathllap{f}}\swarrow && \searrow^{\mathrlap{f}}
      \\
      X &&&& X
    }
  \right)
$$

which is the $(\infty,1)$-[[pullback]]

$$
  \array{
    && \mathcal{L}_X Y
    \\
    & \swarrow && \searrow
    \\
    Y &&&& X
    \\
    & {}_{\mathllap{f,f}}\searrow && \swarrow_{\mathrlap{Id,Id}}
    \\
    && X \times X
  }
  \,.
$$

Then we take the Hochschild cohomology of $Y$ relative to $f : Y \to X$
to be 

$$
  HH(Y,X) := \mathbf{K}(\mathcal{L}_X Y, C) =: \infty Mod(\mathcal{L}_X Y)
  \,.
$$

In the case that $f$ is such that $C(-) = \mathbf{K}(-,C)$ satisfies 
[[geometric function theory]]
on it, this is

$$
  \cdots = C( Y \times_{X \times X} Y)
  \simeq
  C(Y) \otimes_{C(X) \otimes C(X)^{op}} C(X)
  \,.
$$

This is indeed the Hochschild homology object of the $C(X)$-bimodule
object structure on $C(Y)$ induced from $f^*$:

$$
  \cdots =: HH_\bullet(C(Y), C(X))
  \,.
$$

### Differential forms and Hochschild (co)homology

The above identifies Hochschild homology objects of function algebras with function algebras on a [[free loop space object]]. If one adds to this the observation that for a sufficiently wel behaved ordinary space regarded as [[derived stack]] its free loop space object is essentially the formal dual of the algebra of [[Kähler differential]] forms, one recovers from a [[higher geometry]] picture the stamenet of the Hochschild-Kostant-Rosenberg theorem mentioned above. Details are in

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Langlands Parameters_ ([arXiv:0706.0322](http://arxiv.org/abs/0706.0322))

* [[Bertrand Toen]] [[Gabriele Vezzosi]], _$S^1$-Equivariant simplicial algebras and de Rham theory_ ([arXiv:0904.3256](http://arxiv.org/abs/0904.3256))

Notice that the function algebra on the derived loop space is just the differential forms as a graded algebra, without the differential. The differential itself comes from the $S^1$-action on the loop space.




## Definition {#Details}


We start with the general-abstract definition of Hochschild homology and then look at special and more traditional cases.

### General abstract {#GeneralAbstractDefinition}

#### Hochschild homology

+-- {: .un_def}
###### Definition

Given an [[(∞,1)-topos]] $\mathbf{H}$, the **Hochschild cohomology** of an [[object]] $X \in \mathbf{H}$ is the [[cohomology]] (with whatever coefficients) of the [[free loop space object]] $\mathcal{L}X \simeq X^{S^1}$.

More generally, for $K$ any [[∞-groupoid]], the **higher order Hochschild cohomology** of $X$ given by $K$ is the [[cohomology]] of the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#Tensoring">powering</a> $X^K$.

=--

Notice that this defines Hochschild cohomology for [[∞-stack]]s. Usually Hochschild cohomology is formulated in terms of the corresponding [[function algebras on ∞-stacks]] $\mathcal{O}(X)$, under [[Isbell duality]]. The Hochschild cohomology of $X$ then corresponds to what is called the Hochschild _homology_ of $\mathcal{O}(X)$.

The following definition formalizes a special class of cases of the above general abstract definition that reproduces the notion of Hochschild homology for [[(∞,1)-algebraic theory|∞-algebra]]s as usually understood.

+-- {: .un_def}
###### Definition

Let $T$ be an [[(∞,1)-algebraic theory]] and $T Alg_\infty$ its [[(∞,1)-category]] of $\infty$-algebras. Let $C$ with $T \hookrightarrow C \hookrightarrow T Alg_\infty^{op}$ be a [[small (∞,1)-category|small]] full [[sub-(∞,1)-category]] of $T Alg_\infty^{op}$ which is closed under [[(∞,1)-limit]]s in $T Alg$ and equipped with the structure of a [[subcanonical coverage|subcanonical]] [[(∞,1)-site]]. 

Take $\mathbf{H} := Sh(C)$ the [[(∞,1)-category of (∞,1)-sheaves]] on $C$. This is an [[(∞,1)-topos]] for [[derived geometry]] modeled on $T Alg_\infty$.  Write $C \hookrightarrow \mathbf{H}$ for the [[(∞,1)-Yoneda embedding]].

For $X \in C\stackrel{}{\hookrightarrow} \mathbf{H} $ write $\mathcal{O}(X)$ for the same object regarded as an object of $T Alg_\infty$.

=--

+-- {: .un_def}
###### Proposition/Definition 

In the context of the above definition we have 

$$
  \mathcal{O} (\mathcal{L}X) \simeq S^1 \cdot \mathcal{O}(X) \in T Alg_\infty
  \,,
$$

where on the right we have the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#Tensoring">(∞,1)-tensoring</a> of $T Alg_\infty$ over $\infty Grpd$, which is the [[(∞,1)-colimit]] over the [[diagram]] $S^1$ of the [[(∞,1)-functor]] constant on $\mathcal{O}(X)$

$$
  S^1 \cdot \mathcal{O}(X) \simeq {\lim_{\to}}_{S^1} \mathcal{O}(X)
  \,.
$$

This object we call the **Hochschild homology complex** of $\mathcal{O}X$.

Generally for higher order Hochschild homology we have

$$
  \mathcal{O}(X^K) \simeq K \cdot \mathcal{O}(X) 
   \simeq
   {\lim_{\to}}_{K} \mathcal{O}(X)
   \in T Alg_\infty
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because the [[(∞,1)-Yoneda embedding]] preserves [[(∞,1)-limits]] the limit $X^K$ may be computed in $C$. By assumption $C$ is closed under limits in $T Alg_\infty^{op}$. The limit $X^K$ in $T Alg^{op}$ is the colimit $K \cdot \mathcal{O}(X)$ in the [[opposite (∞,1)-category]] of $\infty$-algebras.

=--

#### Topological chiral homology {#TopologicalChiralHomology}

Notice that the tensoring that gives the Hochschild homology is given by the $\infty$-colimit ove the constant functor

$$
  K \cdot A \simeq {\lim_\to}_K A
  \,.
$$

This generalizes to $\infty$-colimits of functors constant on an algebra, but over a genuine [[(∞,1)-category]] diagram.

Specifically let $X$ be framed $n$-manifold, $A$ an [[little k-cubes operad|En-algebra]] and $D_X$ the [[(∞,1)-category]] whose objects are framed embeddings of disjoint uniions of open discs into $X$ and morphisms are inclusions of these. Let $F_A$ be the functor that assigns $A^{k}$ to an object corresponding to $k$ discs in $X$, and iterated products/units to morphisms 

Then the [[(∞,1)-colimit]]

$$
  {\lim_\to}_{D_X} F_A
$$

is called the [[topological chiral homology]] of $X$.

For $A$ an ordinary associatve algebra, hence in particular an $E_1$-algebra, and $X$ the circle, this reproduces the ordinary Hochschild homology of $A$ (see below).

### Specific concrete

We unwind the above generall abstract definition in special classes of examples and find more explicit and more traditional definitions of Hochschild homology.

#### Pirashvili's higher order Hochschild homology

We demonstrate how the above $(\infty,1)$-category theoretic definition of higher order Hochschild homology reproduces the simplicial definition by ([Pirashvili](#Pirashvili)).

+-- {: .un_prop}
###### Proposition

Let $T$ be a [[Lawvere theory]] regarded as a 0-[[truncated]] [[(∞,1)-algebraic theory]]. 

Consider a [[model structure on simplicial T-algebras]] [[presentable (∞,1)-category|presenting]] $T Alg_\infty$ such that 

1. it is a [[simplicial model category]];

1. simplicially constant simplicial algebras are fibrant.


Then for $\mathcal{O}(X) \in T Alg \hookrightarrow T Alg_\infty$ and $K \in \infty Grpd$ the higher order Hochschild homology complex $K \cdot \mathcal{O}(X)$  is presented by the ordinary [[tensoring]] $K \cdot \mathcal{O}(X)$ in the model category, for $K$ any [[simplicial set]] incarnation of the $\infty$-groupoid.

=--

+-- {: .proof}
###### Proof

The $(\infty,1)$-tensoring in an $(\infty,1)$-category [[presentable (∞,1)-category|presented]] by a [[simplicial model category]] is modeled by the ordinary [[tensoring]] of the latter on a fibrant [[resolution]] of the given object. This is discussed in the section <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#ModelsForTensoring">∞-tensoring -- models</a>.

=--

+-- {: .un_remark}
###### Remark

We can always use the [[model structure on homotopy T-algebras]] to satisfy the assumption of the above proposition. That is a [[simplicial model category]] for every $T$ and every ordinary algebra is fibrant in this structure. 

If however we find a simplicial [[model structure on simplicial T-algebras]] then the coproduct is the tensor product of algebras, and we get explicitly Pirashvili's formulation, as described in the next example.

=--

+-- {: .un_example}
###### Example

For $T$ the theory of ordinary  commutative [[associative algebra]]s over a ring $k$, we have a standard [[simplicial model category]] structure on $CAlg_k^{\Delta^{op}}$ that presents $T Alg_\infty$ (as discussed at [[model structure on simplicial algebras]]).

Observe that the [[coproduct]] of $k$-algebras is the [[tensor product]] over $k$

$$
  A \coprod B \simeq A \otimes B
  \,.
$$

Therefore the [[tensoring]] of a $k$-algebra over a morphism $S \to T$ of [[set]]s is

$$
  ({S \to T}) \cdot A = A^{\otimes_k |S|} \to A^{\otimes_k |T|}
$$

where the product in $A$ is used to map several copies of $A$ to a single one, and the unit in $A$ is used to insert copies of $A$.

Let for instance $\Delta[1]/\partial \Delta[1]$ be a simplicial model for the circle. Then for $A$ any algebra we get the simplicial algebra

$$
  (\Delta[1]/\partial \Delta[1])A =
  \left(
     \cdots A\otimes_k A \otimes_k A\stackrel{\overset{\mu \otimes Id\circ \sigma \otimes Id}{\to}}{\stackrel{\overset{\mu \otimes Id}{\to}}{\underset{Id \otimes \mu}{\to}}} A \otimes_k A
    \stackrel{\overset{\mu}{\to}}{\stackrel{\mu}{\to}}A 
  \right)
  \,,
$$

where

* the single copy of $A$ in degree 0 corresponds to the single 0-cell of $\Delta[1]/\partial \Delta[1]$;

* the two copies of $A$ in degree 2 correspond to the two 1-cells of $\Delta[1]/\partial \Delta[1]$: the unique degenerate 1-cell coming from $\Delta[1]$ and the degenerate 1-cell on the single 0-cell.

The [[Moore complex]] of the simplicial algebra is the ordinary [[chain complex]] $C_\bullet(A,A)$ that computes Hochschild homology of $A$ with coefficients in itself. This is described in detail in the section [The Hochschild chain complex of an associative algebra](#HochschildChainComplex).

Generally, for $K$ any simplicial set, $K \cdot A$ is the simplicial algebra whose Moore complex is the complex that ([Pirashvili](#Pirashvili)) uses to define higher order Hochschild homology.

=--

## Examples

### The Hochschild chain complex of an associative algebra {#HochschildChainComplex}

We consider in detail the classical case of Hichschild (co)homology of an [[]associative algebra].


#### Elementary description 

We spell out explicitly the Hochschild chain complex for an 
[[associative algebra]] (over some ring $k$) with coefficients in a [[bimodule]].


+-- {: .un_def #PlainBarComplex}
###### Definition

The [[bar complex]] of $A$ is the [[connective]] [[chain complex]]

$$
  \mathrm{B}_\bullet A :=
  (
    \cdots \to A^{\otimes_k n}
    \stackrel{\partial}{\to}
    A^{\otimes_k n-1}
    \to \cdots
    \to A \otimes_k A \otimes_k A 
    \stackrel{\partial}{\to}
    A \otimes_k A
    \stackrel{\partial}{\to}
    A
  )
$$

which in degree $n$ has the $(n+1)$ [[tensor power]] of $A$ with itself, and whose [[differential]] is given by 

$$
  \partial(a_0, a_1, \cdots a_n)
  :=
  (a_0 a_1, a_2, \cdots, a_n)
  - 
  (a_0, a_1 a_2 , a_3, \cdots, a_n)
  + 
  \cdots
  - (-1)^n (a_0, a_1, \cdots, a_{n-1} a_n)
  \,,
$$ 

regarded as a chain complex in $A$-[[bimodule]]s for the evident bimodule structure in each degree.

=--

+-- {: .un_def}
###### Definition

Let $N$ be an $A$-[[bimodule]]. The **Hochschild chain complex** $C_\bullet(A,N)$ of $A$ with coefficients in $N$ is the chain complex obtained by taking in the [bar complex](#PlainBarComplex) degreewise the [[tensor product]] of $A$-bimodules with $N$:

$$
  C_\bullet(A,B) := N_{A \otimes A^{op}}\mathrm{B}_\bullet A
  \,.
$$

The **Hochschild homology** of $A$ with coefficients in $N$ is the [[homology]] of the Hochschild chain complex, written

$$
  HH_n(A,N) := H_n( C_\bullet(A,N))
  \,.
$$

=--


+-- {: .un_lemma}
###### Observation

At the level of the underlying $k$-[[module]]s we have natural isomorphisms

$$
  N_{A \otimes_k A^{op}} A^{\otimes_k (n+2)}
  \simeq
  N \otimes_k \otimes A^{\otimes_k n}
$$

given on elements by sending

$$
  (\nu, (a_0, a_1, \cdots, a_n, a_{n+1}))
  \sim
  (a_{n+1} \nu a_{0}, (1, a_1, \cdots, a_n, 1))
  \mapsto
  (a_0 \nu a_{n+1}, a_1, \cdots, a_n)
  \,.
$$

The action of the differential in $C_\bullet(A,N)$ on elements of the latter form is then

$$
  \partial(\nu, a_1, \cdots, a_n)
  =
  (\nu a_1, a_2, \cdots, a_n)
  -
  (\nu, a_1 a_2, a_3, \cdots)
  + 
  \cdots
  +  
  (-1)^n
  (\nu , a_1, \cdots, a_{n-1} a_n)
  - (-1)^{n}
  (a_n \nu, a_1, a_2, \cdots, a_{n-1})
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

In words this means that the Hochschild complex is obtained froms the bar complex by "gluing the two ends of a sequence of elements of $A$ to a circle by a bimodule".

The fact that the circle appears here has in fact a deep significance: the Hochschild chain complex may be understood in [[higher geometry]] as encoding functions on a [[free loop space object]] of whatever $A$ behaves like being functions on.

=--


#### As function algebra on the derived loop space {#FuncsOnDerivedLoopSpace}

We derive in an alternative way how the Hochschild complex of an ordinary associative algebra $\mathcal{O}(X)$ is the function algebra on the [[derived loop space]] object $\mathcal{L}X$ in the context of [[derived geometry]].


So let now $T$ be the [[Lawvere theory]] of ordiary commutative [[associative algebra]]s over a [[field]] $k$, regard as a 0-[[truncated]] [[(∞,1)-algebraic theory]]. 

+-- {: .un_def}
###### Proposition

The [[(∞,1)-category]] $CAlg(k)_\infty$ of [[algebras over a Lawvere theory|∞-algebras]] over $T$ is [[presentable (∞,1)-category|presented]] by the [[model structure on simplicial T-algebras|model structure on simplicial commutative k-algebras]] $(CAlg_k^{\Delta^{op}})_{proj}$.

This is [[Quillen equivalence|Quillen equivalent]] to the standard [[model structure on dg-algebras|model structure on connected dg-chain algebras]].

$$
  (CAlg_k^{\Delta^{op}})_{proj}
  \simeq
  dgAlg_k^+
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

The first statement is discussed at [[(∞,1)-algebraic theory]] and [[homotopy T-algebra]]. The second statement is discussed at [[monoidal Dold-Kan correspondence]].

=--

Let 

$$
  T \subset C \subset  T Alg_\infty^{op}
$$

be a [[subcanonical coverage|subcanonical]] [[(∞,1)-site]] that is a full 
[[sub-(∞,1)-category]] of formal duals of $\infty$-$T$-algebras, closed under [[(∞,1)-limit]]s in $T Alg_\infty^{op}$. 

Let 

$$
  \mathbf{H} := Sh_{(\infty,1)}(C)
$$ 

be the [[(∞,1)-sheaf (∞,1)-topos]] over $C$. 

Following the notation at [[Isbell duality]] and [[function algebras on ∞-stacks]] we write $\mathcal{O}(X) \in T Alg_\infty$ for an object that under the [[(∞,1)-Yoneda embedding]] $C \hookrightarrow T Alg_\infty^{op} \to \mathbf{H}$ maps to an object called $X$ in $\mathbf{H}$.

+-- {: .un_def}
###### Definition

For $\mathcal{O}(X) \in T Alg \hookrightarrow T Alg_\infty$ an ordinary $T$-algebra, we say that the [[free loop space object]] 

$$
  \mathcal{L}X := [S^1,X]
$$ 

of $X$ formed in $\mathbf{H}$ is the **[[derived loop space]]** of $X$.

=--

+-- {: .un_remark}
###### Remark

The term _derived_ is just to emphasize that we do not form the [[free loop space object]] in an [[(∞,1)-topos]] of $(\infty,1)$-sheaves over a 1-[[site]] inside the 1-category $Alg_k^{op}$. These "underived" (not embedded into [[(∞,1)-category theory]]) free loop space objects would just be equivalent to $X$. The [[derived loop space]] instead has rich interesting structure.

But if the ambient context of [[higher geometry]] over the genuine [[(∞,1)-site]] of formal duals to $\infty$-algebras is clear, we can just speakk of _free loop space objects_ . They are canonically given.

=--

+-- {: .un_prop #LimitInAlg}
###### Proposition 

We have that $\mathcal{O}(\mathcal{L}X)$ is given by the [[(∞,1)-pushout]] in $CAlg_\infty$ 

$$
  \mathcal{O}\mathcal{L}X \simeq \mathcal{O}(X) \coprod_{\mathcal{O}(X)\otimes \mathcal{O}(X) } \mathcal{O}(X)
$$

hence by the universal [[cocone]]

$$
  \array{
    \mathcal{O}\mathcal{L}X &\leftarrow&
    \mathcal{O}(X)
    \\
    \uparrow && \uparrow
    \\
    \mathcal{O}(X) &\leftarrow& \mathcal{O}(X) \otimes \mathcal{O}(X)
  }
$$

=--

+-- {: .proof}
###### Proof

Since [[∞-stackification]] $L : PSh_{(\infty,1)}(C) \to \mathbf{H}$ is a [[left exact (∞,1)-functor]] and hence preserves finite [[(∞,1)-limit]]s, we have that the defining pullback for $\mathcal{L}X$ may be computed in the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C)$. Since the [[(∞,1)-Yoneda embedding]] preserves all [[(∞,1)-limit]]s this in turn may be computed in the [[(∞,1)-site]] $C$, hence by assumption in $T Alg_\infty$. The relevant $(\infty,1)$-pullback there is the claimed $(\infty,1)$-pushout in the [[opposite (∞,1)-category]] $T Alg_\infty$. 

=--

+-- {: .un_prop}
###### Proposition

The $\infty$-algebra $\mathcal{O} \mathcal{L}X$ of functions on the derived loop space of $X$ is when modeled by a simplicial algebra in $CAlg_k^{\Delta^{op}}$ under the [[monoidal Dold-Kan correspondence]] equivalent to the Hochschild chain complex of $\mathcal{O}X$ with coefficients in itself:

$$
  \mathcal{O} \mathcal{L}X \simeq C_\bullet(\mathcal{O}(X), \mathcal{O}(X))
  \,.
$$

=--

+-- {: .proof}
###### Proof

First observe that the [[coproduct]] in $CAlg_k$ is the [[tensor product]] of commutative algebras over $k$

$$
  A \coprod B = A \otimes_k B
  \,.
$$

By the discussion at [[homotopy T-algebra]] we may model $T Alg_\infty$ by the _injective_ [[model structure on simplicial presheaves]] on $T^{op}$, [[Bousfield localization of model categories|left Bousfield localized]] at the morphisms $T[k] \otimes T[l] \to T[k+l]$. This localized model structure we write $[T, sSet]_{inj,prod}$.

By the [above proposition](#LimitInAlg) we have that $\mathcal{O}\mathcal{L}X$ is given by the [[homotopy pushout]] in $[T, sSet]_{inj,prod}$ of 

$$
  \mathcal{O}X \leftarrow \mathcal{O}(X)\otimes_k \mathcal{O}(X) \to \mathcal{O}(X)
  \,,
$$

where both morphissm are simple the product on $\mathcal{O}(X) \in CAlg_k$. By general properties of [[homotopy pushout]]s and the injective [[model structure on simplicial presheaves]] we have that this homotopy pushout is computed by an ordinary pushout once we pass to a weakly equivalent diagram in which one of the two morphism is a cofibration of simplicial algebras.

$$
  \array{
  \mathcal{O}X 
   &\leftarrow& 
    \mathcal{O}(X)\otimes_k \mathcal{O}(X) &\hookrightarrow& \mathrm{B} \mathcal{O}(X)
  \\
  \downarrow^{\mathrlap{=}} && \downarrow^{\mathrlap{=}} && 
   \downarrow^{\mathrlap{\simeq}}
   \\
  \mathcal{O}X &\leftarrow& 
    \mathcal{O}(X)\otimes_k \mathcal{O}(X) &\to& \mathcal{O}(X)
  }
  \,.
$$

It is sufficient to find a [[resolution]] $B \mathcal{O}X$ in the global model structure $[T, sSet]_{inj}$ because left Bousfield localization strictly increases the class of weak equivalences, so that every gloabl weak equivalence is also a local weak equivalence.

Since we are in the _injective_ model structure this just means that this morphism $\mathcal{O}(X) \otimes_k \mathcal{O}(X) \to \mathrm{B} \mathcal{O}X$ needs to be over each $x^n$  in $T$ a [[monomorphism]] of simplicial sets. 
If we find $\mathrm{B} \mathcal{O}X$ also as a strictly product-preserving functor (notice that the general functor in our model category need not even preserve products weakly, it will do so after fibrant replacement) then it being monomorphism over $x^1$ implies that it is monic over every $x^n$.

There is a standard resolution of the kind we need called the [[bar complex]], see for intance ([Ginzburg, page 16](#Ginzburg)) for an explicit description.
This is usually discussed as a [[chain complex]] in the category of $\mathcal{O}(X)$-[[module]]s. But in fact after applying the [[Dold-Kan correspondence]] to regard it as a simplicial module it is naturally even a [[simplicial object]] in $CAlg_k$:
 
$$
  \mathrm{B} \mathcal{O}(X) 
   :=
  \left(
     \cdots 
    \mathcal{O}(X) \otimes_k \mathcal{O}(X) \otimes_k
     \mathcal{O}(X) \otimes_k \mathcal{O}(X)
     \stackrel{\overset{\mu \otimes Id \otimes Id}{\to}}{\stackrel{\overset{Id \otimes \mu Id}{\to}}{\underset{Id \otimes Id \otimes \mu}{\to}}}
    \mathcal{O}(X) \otimes_k \mathcal{O}(X) \otimes_k
     \mathcal{O}(X) 
     \stackrel{\overset{\mu \otimes Id}{\to}}{\underset{Id \otimes \mu}{\to}} 
     \mathcal{O}(X) \otimes_k \mathcal{O}(X)
  \right)
  \in 
  CAlg_k^{\Delta^{op}}
  \,,
$$

with the evident face and degeneracy maps given by binary product operation in the algebra and insertion of units. 

Take the morphism $\mathcal{O}(X) \otimes \mathcal{O}(X) \to \mathrm{B} \mathcal{O}(X)$ degreewise to be the inclusion of $\mathcal{O}(X) \otimes \mathcal{O}(X)$ as the two outer direct summands

$$
  \mathcal{O}(X)
  \otimes_k 
  \mathcal{O}(X)
  \stackrel{Id \otimes e \otimes e \otimes \cdots \otimes e \otimes Id}{\to}
  \mathcal{O}(X) \otimes_k \mathcal{O}(X) \otimes_k \cdots 
  \otimes_k \mathcal{O}(X)
  \,,
$$

where $e : k \to \mathcal{O}(X)$ is the monoid unit.

This is clearly degreewise a [[monomorphism]], hence is a monomorphism. Under the [[Moore complex]] functor $N : Ab^{\Delta^{op}} \to Ch_\bullet^+$ it maps to the standard bar complex resolution as found in the traditional literature (as reviewed for instance in [Ginzburg](#Ginzburg)). This morphism of chain complexes is an [[isomorphism]] in [[homology]]. Since under the [[Dold-Kan correspondence]] [[simplicial homotopy group]]s are identified with [[homology]] groups, we find that indeed $\mu : \mathrm{B}\mathcal{O}(X) \to \mathcal{O}(X)$ is a weak equivalence in $[T,sSet]_{inj}$ and hence in $[T, sSet]_{inj,prod}$.

We may now compute the pushout in $[T, sSet]$ and this will compute the desired homotopy pushout. Notice that this pushout indeed takes place just in simplicial copresheaves, not in product-preserving copresheaves! 

But this ordinary pushout it manifestly the claimed one.

=--


+-- {: .un_remark}
###### Remark

This derivation

* crucially uses the assumption that $A$ is a commutative algebra;

* curiously does _not_ make use of any specific property of the set of morphisms $\{T[k] \coprod T[l] \to T[k+l] \}$ at which we are considering the left Bousfield localization. The entire construction proceeds entirely at the underlying simplicial sets of our simplicial algebras. In fact, the resulting homotopy pushout $\mathcal{O}(X) \coprod_{\mathcal{O}(X) \otimes \mathcal{O}(X)} \mathrm{B}\mathcal{O}(X)$ is a simplicial copresheaf on $T$ that no longer preserves any products: there is no manifest algebra structure.

  But also, this object is far from being fibant in the localized model structure $[T, sSet]_{proj,prod}$. The Bousfield localization, hence the information about the set of maps at which we are localizing, hence the algebra structure, kicks in only once we pass now to the fibrant [[resolution]] of our pushout. That **fibrant replacement equips the Hochschild chain complex with the structure of an $\infty$-algebra.**

=--



## Properties


### Algebra structure on $(HH^\bullet(A,A), HH_\bullet(A,A))$ {#AlgebraStrucOnHochschild}


#### Differential calculus {#DifferentialCalculus}


It turns out that

* Hochschild homology of $\mathcal{O}(X)$ encodes [[Kähler differential form]]s on $X$;

* Hochschild cohomology of $\mathcal{O}(X)$ encodes [[multivector field]]s on $X$;

* there are  natural pairings between $HH_\bullet(\mathcal{O}(X), \mathcal{O}(X))$ and $HH^\bullet(\mathcal{O}(X), \mathcal{O}(X))$ that mimic the structure of the natural pairings between vector fields and differential forms on [[smooth manifold]].

See ([TamarkinTsygan](#TamarkinTsygan)).


One way to understand or interpret this conceptually is to regard the [[derived loop space]] object of a 0-[[truncated]] object $X$ to consist of [[infinitesimal object|infinitesimal]] loops in $X$.

##### Hochschild-Kostant-Rosenberg theorem {#HochschildKostantRosenberg} 

The **[[Hochschild-Kostant-Rosenberg theorem]]** states that under suitable conditions, the Hochschild homology of an algebra (with coeficients in itself) computes the wedge powers of its [[Kähler differential]]s.

+-- {: .un_prop }
###### Proposition

For a $k$-algebra $R$, its module of [[Kähler differential]]s coincides with its first Hochschild homology

$$
  \Omega(R/k) \simeq HH_1(R,R)
  \,.
$$


=--

+-- {: .proof}
###### Proof

Write $C_\bullet(R,R) = ( \cdots \to R \otimes_k R \otimes_k R \stackrel{\partial}{\to} R \otimes_k R)$ for the chain chomplex of Hochschild chains. We claim that the identification of its homology in lowest degree with K&#228;hler differentials is established by identifying an element $(f ,g) \in R \otimes_k R$  with the K&#228;hler differential $f \wedge d g$.

For observe that under this identification with $(a,b,c) \in R \otimes_k R \otimes_k R$ any element its differential is

$$
  \begin{aligned}
    \partial (f,g,h)
    &=
    (f g, h) - (f, g h) + (h f, g)
    \\
    &
    \sim
    f g \wedge d h -  f \wedge d (g h) + f h \wedge d g
  \end{aligned}
  \,.
$$  

The term on the right is precisely the term by which one has to quotient out the module of formal expressions $f \wedge d g$ to get the module of [[Kähler differential]]s: setting it to 0 is the [[derivation]] property of $d$

$$
  (\partial (f,g,h) = 0)
  \Leftrightarrow
  f \wedge ( f(g h) = h \wedge d g + g \wdge d h )
  \,.
$$

Therefore we have manifestly

$$
  \Omega^1_K(R) \simeq C_1(R,R)/im(\partial)
  \,.
$$

=--

Write $\Omega^0(R/k) := R \simeq HH_0(R,R)$.

For $n \geq 2$ Write $\Omega^n(R/k) = \wedge^n_R \Omega(R/k)$ for the $n$-fold [[exterior algebra|wedge product]] of $\Omega(R/k)$ with itself: the degree $n$-K&#228;hler-differentials.

+-- {: .un_theorem }
###### Theorem

The isomorphism $\Omega^1(R/k) \simeq H_1(R,R)$ extends to a graded ring morphism

$$
  \psi : \Omega^\bullet(R/k) \to H_\bullet(R,R)
  \,.
$$

=--

If the $k$-algebra $R$ is sufficiently well-behaved, then this morphism is an [[isomorphism]] that identifies the Hochschild homology of $R$ in degree $n$ with $\Omega^n(R/k)$ for all $n$:

+-- {: .un_theorem }
###### Theorem
**(Hochschild-Kostant-Rosenberg theorem)**


If $k$ is a [[field]] and $R$ a commutative $k$-[[algebra]] which is 

* essentially of finite type 

* smooth over $R$

then there is an [[isomorphism]] of graded $R$-algebras

$$
  \psi : \Omega^\bullet(R/k) \stackrel{\simeq}{\to}
  HH_\bullet(R,R)
  \,.
$$

Moreover, dually, there is an isomorphism of Hochschild cohomology with wedge products of derivations:

$$
  \wedge^\bullet_R Der(R,R) \simeq HH^\bullet(R,R)
$$

=--

This is reviewed for instance as ([Weibel, theorem 9.4.7](#Weibel)) or as ([Ginzburg, theorem 9.1.3](#Ginzburg)).


#### $E_n$-algebra structure: Deligne-Kontsevich conjecture/theorem {#EnAlgebraStructure}

+-- {: .un_lemma }
###### Observation

The higher order Hochschild homology $\mathcal{O} X^{S^d}$ of an object $X$ with respect to the $n$-sphere $S^d$ and with coefficients in a [[integral transforms on sheaves|geometric function object]] is naturally an $E_{d+1}$-algebra: an [[algebra over an operad]] over the [[little k-cubes operad]] for $k = d+1$ .

For let $D^{d+1}$ be the $(d+1)$-disk and 

$$
  \array{
     && D^{d+1}
     \\
     & \nearrow && \nwarrow
     \\
     \coprod_r S^d  &&&& S^d
  }
$$

a configuration of $r$ $d$-spheres in $D^{d+1}$, with the right leg denoting the boundary of $D^{d+1}$. Interal-homming this [[cospan]] into the object $X$ produces the [[span]]

$$
  \array{
     && X^{D^{d+1}}
     \\
     & \swarrow && \searrow
     \\
     \prod_r X^{S^d} &&&& X^{S^d}
  }
  \,.
$$ 

Then the [[integral transforms on sheaves]] induced by these spans constitute the $E_n$-action on the function objects on $X^{S^d}$.

=--

This was observed in ([Ben-ZviFrancisNadler, corollary 6.8](#Ben-ZviFrancisNadler)).


#### $HH$ of constant $\infty$-stacks: String topology BV-algebra {#StringTopology}

Let $T$ be the [[algebraic theory]] of ordinary [[associative algebra]]s over a [[field]] $k$, regarded as an [[(∞,1)-algebraic theory]] and let $\mathbf{H}$ be the [[(∞,1)-topos]] of $(\infty,1)$-sheaves over a small site in $T Alg_\infty^{op}$.

Under the [[inverse image]] of the [[global section]] [[(∞,1)-geometric morphism]] and the [[homotopy hypothesis]]-equivalence

$$
  \mathbf{H} \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
  \stackrel{\overset{\Pi}{\leftarrow}}{\underset{|-|}{\to}}
  Top
$$

we may regard every [[topological space]] $X$ as a [[constant ∞-stack]] $LConst X$, an object in $\mathbf{H}$.


+-- {: .un_prop }
###### Proposition

The function algebra on $LConst X$ is the cosimplicial algebra of singular cochains on $X$. Under the [[monoidal Dold-Kan correspondence]] it identifies with the cochain [[dg-algebra]] $C^\bullet(X)$ that computes the [[singular cohomology]] of $X$.

=--

This has maybe been first made explicit by [[Bertrand Toen]]. Details are at [[function algebras on ∞-stacks]].


+-- {: .un_prop }
###### Corollary

The Hochschild homology of $C^\bullet(X)$ is the [[singular cohomology]] of the [[free loop space]] $L X$.

=--

+-- {: .proof}
###### Proof

Apply the [central identification](#GeneralAbstractDefinition) $\mathcal{O} \mathcal{L}(LConst X)  \simeq S^1 \cdot \mathcal{O}(LConst X)$. Then observe that the [[free loop space object]] $\mathcal{L} LConst X$  of the constant $\infty$-stack is the constant $\infty$-stack on the ordinary [[free loop space]], because $LConst$ is a [[left exact (∞,1)-functor]] and because $\mathcal{L}X \simeq L X$ in [[Top]]. Then use by the above remark that $\mathcal{O} LConst L X$ is singular cochains on $L X$. 

=--

This result, which follows directly from the general abstract desciption of Hichschild homology is known as **Jones' theorem**. We now review the results in the literature on this point.

Let $X$ be a [[compact manifold]] [[oriented]] [[smooth manifold]] of [[dimension]] $d$. Write $C^\bullet(X)$ for the [[dg-algebra]] of cochains for [[singular cohomology]] of $X$. Write $L X$ for the topological [[free loop space]] of $X$ and $H_\bullet(L X)$ for its [[singular homology]].


+-- {: .un_theorem }
###### Theorem

There is a linear isomorphism of degree $d$

$$
  \mathbb{D}
  :
  HH^{-p-q}(C^\bullet(X), C^\bullet(X)^{\vee})
    \simeq
  HH^{-p}(C^\bullet(X), C^\bullet(X))
  \,.
$$

=--

This is due to ([FelixThomasVigue-Poirrier, section 7](#FelixThomasVigue-Poirrier))).

+-- {: .un_theorem }
###### Theorem
**(Jones' theorem)**

There is an [[isomorphism]]

$$
  J 
  : 
  H_{p+q}(L X) 
    \stackrel{\simeq}{\to}  
  HH^{-p-d}(C^\bullet(X), C^\bullet(X)^{\vee})
$$

such that the canonical [[string topology]] [[BV-operator]] $\Delta$ of the [[BV-algebra]] $H_{\bullet + d}(L X)$ and the [[Connes coboundary]] $B^\vee$ on $HH^{\bullet-d}(C^\bullet(X), C^\bullet(X)^{\vee})$ satisfy

$$
  J \circ \Delta = B^{\vee} \circ J
  \,.
$$

=--

This is due to ([Jones](#Jones)).


+-- {: .un_theorem }
###### Theorem

The [[Connes coboundary]] defines via the isomorphism $\mathbb{D}$ from above the structure of a [[BV-algebra]] on $HH^\bullet(C^\bullet(X), C^\bullet(X))$.


=--

This is ([Menichi, theorem 3](#Menichi)).


### Relation to cyclic (co)homology

There is an evident rotation-[[action]] on Hochschild (co)chains. Passing to the cyclically invariant (co)chains yields [[cyclic (co)homology]].


### Further

#### Hochschild cohomology and extensions {#Extensions}

+-- {: .un_def }
###### Definition

An [[exact sequence]] $0 \to N \to E \to R$ of $k$-modules where
$E \to R$ is a surjective morphism of $k$-algebras is
called a **$k$-split** extension or a **Hochschild extension** of $R$ by $E$ if the sequence is a [[split sequence]] as a sequence of $k$-[[module]]s.

Two extensions are _equivalent_ if there is an isomorphism or $k$-algebra $E \stackrel{\simeq}{\to} E'$ that makes

$$
  \array{
    N &\to& E &\to& R
    \\
    \downarrow^{\mathrlap{=}} && \downarrow && \downarrow^{\mathrlap{=}}
    \\
    N &\to& E' &\to& R
  }
$$

commute.

=--


+-- {: .un_remark }
###### Remark

Due to the $k$-splitness assumption there is an isomorphism of $k$-modules $E \simeq R \oplus N$ and this is equipped with a $k$-algebra structure such that the product on the $R$ [[direct sum]]mand is that of $R$. From this we find that the product on $E$ is of the form

$$
  (r_1, n_1) \cdot (r_2, n_2) =
  (r_1 r_2 , r_1 n_2 + r_2 n_1 + f(r_1, r_2))
  \,,
$$

where $f : R \otimes_k R \to N$ is some $k$-linear map. Since the product on $E$ is (by definition) associative, it follows that for $f$ that this satisfies for all $r_0, r_1, r_2 \in R$ the _cocycle equation_

$$
  r_0 f(r_1, r_2) - f(r_0 r_1, r_2) + f(r_0 , r_1 r_2) - f(r_0, r_1) r_2 = 0
$$

as an equation in $N$. This says that $f$ must be a Hochschild cocycle

$$
  f \in HH^2(R,N)
  \,.
$$ 

=--


Conversely, every such cocycle yields a $k$-split extension of $R$ by $N$ this way:



+-- {: .un_theorem }
###### Theorem

For $R$ a $k$-algebra and $N$ an $R$-[[bimodule]], equivalence
classes of Hochschild extensions of $R$ by $N$ are in bijection with
degree 2 Hochschild cohomology $HH^2(R,N)$.

=--

See for instance [[An Introduction to Homological Algebra|Weibel, theorem 9.3.1]].


#### Hochschild cohomology and deformations {#Deformations}

As a special case of the above statement about extensions of $R$, we obtain a statement about _deformation_ of $R$.

A standard problem is to deform a $k$-algebra $R$ by introducing a new "parameter" $t$ that squares to 0 -- $t \cdot t = 0$ and a new product

$$
  r_1 \cdot_t r_2 = r_1 r_2 + t f(r_1, r_2)  
  \,.
$$

From the above we see that this is the same as finding an $k$-split extension of $R$ by itself. So in particular such extensions are given by Hochschild cocycles $f \in HH^2(R,R)$.

See for instance [Ginzburg, section 7](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf) and for more see [[deformation quantization]].







 
## References
 
The traditional story of Hochschild (co)homology is exposed for instance

in chapter 9 of

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_
{#Weibel}

or in chapter 4 of
 
* [[Victor Ginzburg]], _Lectures on noncommutative geometry_ ([arXiv:math/0506603](http://arxiv.org/abs/math.AG/0506603))
{#Ginzburg}

An original paper on this is

* Tsygan and Feigin,  _Additive K-theory_ 1980-s (LNM 1289, editor Manin, pp 67-209, seminar 1984-1986 in Moscow)

 
The $(\infty,1)$-categorical picture of [[derived stack|derived]] [[free loop space object]]s and their [[geometric ∞-function theory]] is discussed in

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Langlands Parameters_ ([arXiv:0706.0322](http://arxiv.org/abs/0706.0322))

* [[Bertrand Toen]] [[Gabriele Vezzosi]], _$S^1$-Equivariant simplicial algebras and de Rham theory_ ([arXiv:0904.3256](http://arxiv.org/abs/0904.3256))


* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], 
  _[[geometric infinity-function theory|Integral transforms and Drinfeld centers in derived algebraic geometry]]_ ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))
{#Ben-ZviFrancisNadler}
 
The definition of higher order Hochschild complex as (implicitly) the tensoring of an algebra with a simplicial set is due to 

* [[Teimuraz Pirashvili]], _Hodge decomposition for higher order Hochschild homology_ Annales Scientifiques de l'&#201;cole Normale Sup&#233;rieure Volume 33, Issue 2, March 2000, Pages 151-179 ([ps](http://www.mathematik.uni-bielefeld.de/sfb343/preprints/pr98058.ps.gz))
{#Pirashvili}

A survey of higher order Hochschild (co)homology and further developments and results are described in

* [[Grégory Ginot]], _Higher order Hochschild cohomology ([pdf](http://www.institut.math.jussieu.fr/~ginot/papers/Higher-Order-Hochschild-Long.pdf))

Jones's theorem is due to

* J. D. S. Jones, _Cyclic homology and equivariant homology_ , Invent. Math. 87
(1987), no. 2, 403{423.
{#Jones}

The BV-algebra structure on Hochschild cohomology of singular cochain algebras is discussed in

* Y. F&eacute;lix, J.-C. Thomas, M. Vigu&eacute;-Poirrier, _The Hochschild cohomology of a closed manifold_ Publ. Math. IH&Eacute;S Sci. (2004) no 99, 235-252
{#FelixThomasVigue-Poirrier}

* Luc Menichi, _Batalin-Vilkovisky algebra structures on Hochschild cohomology_ ([pdf](http://math.univ-angers.fr/perso/lmenichi/BV_Hochschild.pdf))

The abstract differential caclulus on $(HH^\bullet(A,A), HH_\bullet(A,A))$ is discussed for instance in

* [[Dmitry Tamarkin]], [[Boris Tsygan]], _Cyclic Formality and Index Theorems_ ,  Letters in Mathematical Physics
Volume 56, Number 2, 85-97 ([journal](http://www.springerlink.com/content/u33hv13g0669h414/))
{#TamarkinTsygan}

For references on [[topological chiral homology]] see there.

Interesting wishlists for treatments of Hochschild cohomology are in [this](http://mathoverflow.net/questions/28472/book-on-hochschild-cohomology) MO discussion.



[[!redirects Hochschild homology]]

[[!redirects Hochschild complex]]
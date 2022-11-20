
\tableofcontents

## Idea

In [[quantum information theory]] a *bit flip code* is a [[quantum error correcting code]] to correct for [[quatum noise]] caused by [[bit flip channels]].

## Details

### 3-qbit flip code

The following basic example of a bit flip code encodes single [[logical qbits]] in [[triples]] of [[physical qbits]]. Here the [[Hilbert space]] 

$$
  LogicalQBit
  \;\coloneqq\;
  QBit \otimes QBit \otimes QBit
$$ 

of a single logical qbit has [[complex number|complex]] [[dimension of a vector space|dimension]] $2^2 \,=\, 8$. Inside this is the space of undisturbed logical qbits

\[
  \label{PureLogicalQBit}
  \begin{array}{ccccc}
    QBit
    \xrightarrow[\sim]{encode}
    DisturbedQBit_{0}
    &\overset{\phantom{---}}{\hookrightarrow}&
    LogicalQBit
    &\xrightarrow{
      P_{s = 0}
      \;\coloneqq\;
      \left\vert 0,0,0 \right\rangle
      \left\langle 0,0,0 \right\vert
      +
      \left\vert 1,1,1 \right\rangle
      \left\langle 1,1,1 \right\vert
    }&
    DisturbedQBit_0
    \\
    q_0 \left\vert 0 \right\rangle
    +
    q_1 \left\vert 1 \right\rangle
      &\mapsto&
    q_0 \left\vert 0, 0, 0 \right\rangle
    +
    q_1 \left\vert 1, 1, 1 \right\rangle    
  \end{array}
\]

as well as three further orthogonal subspaces which are the images of this one under one of the three *single* bit flips, respectively:

$$
  \begin{array}{ccc}
    DisturbedQBit_{1}
    &\overset{\phantom{---}}{\hookrightarrow}&
    LogicalQBit
    &\xrightarrow{
      P_{s=1}
      \;\coloneqq\;
      \left\vert 1,0,0 \right\rangle
      \left\langle 1,0,0 \right\vert
      +
      \left\vert 0,1,1 \right\rangle
      \left\langle 0,1,1 \right\vert
    }&
    DisturbedQBit_1
    \\
    q_0 \left\vert 0 \right\rangle
    +
    q_1 \left\vert 1 \right\rangle
    &\mapsto&
    q_0 \left\vert 1, 0, 0 \right\rangle
    +
    q_1 \left\vert 0, 1, 1 \right\rangle   
    \\
    {\phantom{A}}
    \\ 
    DisturbedQBit_{2}
    &\overset{\phantom{---}}{\hookrightarrow}&
    LogicalQBit
    &\xrightarrow{
      P_{s=2}
      \;\coloneqq\;
      \left\vert 0,1,0 \right\rangle
      \left\langle 0,1,0 \right\vert
      +
      \left\vert 1,0,1 \right\rangle
      \left\langle 1,0,1 \right\vert
    }&
    DisturbedQBit_2
    \\
    q_0 \left\vert 0 \right\rangle
    +
    q_1 \left\vert 1 \right\rangle
    &\mapsto&
    q_0 \left\vert 0, 1, 0 \right\rangle
    +
    q_1 \left\vert 1, 0, 1 \right\rangle   
    \\
    {\phantom{A}}
    \\ 
    DisturbedQBit_{3}
    &\overset{\phantom{---}}{\hookrightarrow}&
    LogicalQBit
    &\xrightarrow{
      P_{s=3}
      \;\coloneqq\;
      \left\vert 0,0,1 \right\rangle
      \left\langle 0,0,1 \right\vert
      +
      \left\vert 1,1,0 \right\rangle
      \left\langle 1,1,0 \right\vert
    }&
    DisturbedQBit_3
    \\
    q_0 \left\vert 0 \right\rangle
    +
    q_1 \left\vert 1 \right\rangle
    &\mapsto&
    q_0 \left\vert 0, 0, 1 \right\rangle
    +
    q_1 \left\vert 1, 1, 0 \right\rangle   
  \end{array}
$$

The 4 labels of these three subspaces are called the "error syndrome", which we collect in the 4-element set

$$
  Synd \;\coloneqq\; \{0,1,2,3\}
$$

to express the logical q-bit space alternatively in this linear basis:

$$
  QBit
  \xhookrightarrow{ encode }
  \underset{
    LogicalQBit
  }{
    \underbrace{
      QBit \otimes QBit \otimes QBit
    }
  }
  \xrightarrow[\sim]{
    (P_s)_{s \colon Synd}
  }
  \underset{  
    s \colon Synd
  }{\bigoplus}
  DisturbedQBit_{s}
$$

Beware that there is no room to record the further possible errors of 2 qbits flipping at once. Instead, this error process takes pure qbits to one of the subspaces reserved for single bit flips. Similarly, if all three bits flip at once, the initial pure state remains in the subspace reserved for pure states, but now with its phases mixed up. Therefore, the following error correction code fails on flips of more than one of the 3-qbits and will reduce the overall error probability only if single bit flips are sufficiently more likely than double and triple spin flips.

The error correction now proceeds by:

1. Performing a [[quantum measurement]] of the above error syndrome $s$ on the logical Qbit space. While this measurement [[quantum state collapse|collapses]] the quantum state onto the subspace $DisturbedQBit_s$ the particular logical qbit states of the pure form (eq:PureLogicalQBit) lose no information under this collapse, in that there is a [[unitary operator]] on $DistrubedQBit_s$ which turns any such collapse state back into the original qbit state. 

1. applying this correcting unitary $X_s$, which is evidently the "[[Pauli matrix|Pauli X]]-" (or "[[NOT]]-")[[quantum gate]] $X \,\colon\, QBit \to QBit$ acting on the $s$-th qbit:

   $$
     \begin{array}{cccc}
       X_0 &\coloneqq& id \otimes id \otimes id
       \\
       X_1 &\coloneqq& X \otimes id \otimes id   
       \\
       X_2 &\coloneqq& id \otimes X \otimes id   
       \\
       X_3 &\coloneqq& id \otimes id \otimes X
     \end{array} 
     \;\;\;\colon\;\;\;
     \underset{
       LogicalQBit
     }{
       \underbrace{
         QBit \otimes QBit \otimes QBit
       }
     }
     \multimap
     \underset{
       LogicalQBit
     }{
       \underbrace{
         QBit \otimes QBit \otimes QBit
       }
     }
   $$

1. re-preparing a logical QBit from the recovered Qbit.

$$
  LogicalQBit
  \xrightarrow{ measure_{Synd} }
  \bigcirc_{ s \colon Synd }
  QBit
  \xrightarrow{ (X_s)_{s \colon Synd} }
  \bigcirc_{ s \colon Synd }
  QBit
  \xrightarrow{ (encode)_{s \colon Synd} }
  \bigcirc_{ s \colon Synd }
  LogicalQBit
$$

In the notation from *[[quantum channels via dependent linear types]]*, this is, in summary, the following operation:

$$
  correct
  \;\colon\;
  LogicalQBit
  \xrightarrow{ measure_{Synd} }
  \bigcirc_{ s \colon Synd }
  QBit
  \xrightarrow{ (X_s)_{s \colon Synd} }
  \bigcirc_{ s \colon Synd }
  QBit
  \xrightarrow{ (encode)_{s \colon Synd} }
  \bigcirc_{ s \colon Synd }
  LogicalQBit
$$

and the verification of the protocol is the statement that

$$
  verify
  \;\colon\;
  \underset{s}{prod}
  \;\;
  \Big(
  encode
  \text{>}
  X_s
  \text{>} 
  correct
  \;\;\;
  =
  \;\;\;
  `always` \; encode
  \Big)
$$


***

$$
  \begin{array}{cc}
    x & c
    \\
    a & b
  \end{array}
$$

## Idea

In [[quantum information theory]], by the *bit flip channel* one means the [[quantum channel]] on a [[quantum system]] represented by a single [[q-bit]] whose effect is to "flip" the [[linear basis|basis]] [[q-bit]]  [[quantum states]] $\vert 0 \rangle \leftrightarrow \vert 1 \rangle$ with some [[probability]] $p$ and else leave the system unchanged with probability $1 - p$.

The [[tensor product]] of $N$ bit flip channels model the analogous process on $N$ [[q-bits]], where every single one of them may flip with probability $p$, independently of all the others. In this form, the spin flip channel serves as a simple but important model for [[quantum noise]]. Basic examples of [[quantum error correction codes]] may be used to provide partial correction of such spin flip errors.

## Definition

Fix a [[real number]] $p \in [0,1]$ serving as a measure of the [[probability]] for a spin flip to occur when data is sent through the channel.

Write 

* $QBit \,\simeq\, \mathbb{C}\cdot \vert 0 \rangle \,\oplus\, \mathbb{C} \cdot \vert 1 \rangle$ for the [[space of quantum states]] of a [[q-bit]], regarded as a [[Hilbert space]] ([[Hermitian inner product space]]) with $\big\{\left\vert 0 \right\rangle, \left\vert 1 \right\rangle \big\}$ being an [[orthonormal linear basis]].

* $States(QBit) \subset Herm(QBit)$ for the space of [[density matrices]] on this Hilbert space, hence the subspace of [[positive semi-definite bilinear form|positive semi-definite]] [[Hermitian operators]] $QBit \multimap QBit$ of unit [[trace]]:

* $X \;\colon\; QBit \multimap QBit$ for the "[[Pauli matrix|Pauli X]]" ("[[NOT]]") [[quantum logic gate]] given by $X \left\vert 0 \right\rangle \,=\, \left\vert 1 \right\rangle$, and $X \left\vert 1 \right\rangle \,=\, \left\vert 0 \right\rangle$.


Now, a common way to define the spin flip channel is by the following expression (e.g. [Chuang (2011), p. 296](#Chuang11)):

$$
  \array{
    flip
    &\colon\;
    States(QBit)
    \longrightarrow
    States(QBit)
    \\
    flip(\rho) 
    &\defeq\;
    (1-p) \cdot \rho \,+\, p \cdot (X \rho X)
  }
$$

One readily checks that on the [[q-bit]]-basis [[pure states]] this acts as:

$$
  \array{
    States(QBit)
    &\longrightarrow&
    States(QBit)
    \\
    \vert 0 \rangle \langle 0 \rangle
      &\mapsto&
    \mathrlap{
      (1-p) \cdot 
      \left\vert 0 \right\rangle 
      \left\langle 0 \right\vert
      \;+\;
      p \cdot
      \left\vert 1 \right\rangle 
      \left\langle 1 \right\vert
    }
    \\
    \vert 1 \rangle \langle 1 \rangle
      &\mapsto&
    \mathrlap{
      p \cdot 
      \left\vert 0 \right\rangle 
      \left\langle 0 \right\vert
      \;+\;
      (1-p) \cdot
      \left\vert 1 \right\rangle 
      \left\langle 1 \right\vert
    }
  }
$$

Alternatively, one finds that the [[Kraus decomposition]] of this operator is

$$
  flip 
  \;\colon\;
  \rho
  \;\mapsto\;
  P_0 U_{flip} \rho U_{flip} P_0
  \,+\,
  P_1 U_{flip} \rho U_{flip} P_1
  \,,
$$

where the [[unitary operator]] $U_{flip}$ is:

$$
  U_{flip}
  \;=\;
  \left[
  \array{
    + \sqrt{1-p} & \sqrt{p}
    \\
    \sqrt{p} & - \sqrt{1-p}
  } 
  \right]
  \;\colon\;
  QBit \multimap QBit
$$


## References


* {#Chuang11} [[Isaac L. Chuang]], *Quantum error correction*, Chapter 7 in: *Quantum Machines: Measurement and Control of Engineered Quantum Systems* Lecture Notes of the Les Houches Summer School **96** (2011) 273–320  &lbrack;[doi:10.1093/acprof:oso/9780199681181.003.0007](https://doi.org/10.1093/acprof:oso/9780199681181.003.0007)&rbrack;


***


$\in$

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

A _symmetric monoidal category_ is a category with a product operation -- a [[monoidal category]] -- for which the product is _as commutative as possible_.

The point is that there are different degrees to which higher categorical products may be commutative. While a bare [[monoid]] is either commutative or not, a [[monoidal category]] may be a [[braided monoidal category]] -- which already means that the order of products may be reversed up to some [[isomorphism]] -- without being _symmetric_ monoidal -- which means that changing the order of a product twice, from $a \otimes b$ to $b \otimes a$ back to $a \otimes b$, indeed does yield a result [[equality|equal]] to the original.

For higher monoidal categories there are accordingly ever more shades of the notion of "commutativity" of the monoidal product. This is described in detail at [[k-tuply monoidal n-category]]. 

In general, the term _symmetric monoidal_ is used for the maximally commutative case. See for instance [[symmetric monoidal (∞,1)-category]]. Notably, a symmetric monoidal [[∞-groupoid]] is, under the [[homotopy hypothesis]], the same as a [[spectrum|connective spectrum]].

A symmetric monoidal category is a special case of the notion of [[symmetric pseudomonoid]] in a [[sylleptic monoidal 2-category]].

## Definition

+-- {: .num_defn} 
###### Definition


A **symmetric monoidal category** is a [[braided monoidal category]] for which the [[braiding]] 

$$ 
   B_{x,y} \colon x \otimes y \to y \otimes x 
$$

satisfies the condition:

$$ 
  B_{y,x} \circ B_{x,y} = 1_{x \otimes y}  
$$

for all objects $x, y$

=--

Intuitively this says that switching things twice _in the same direction_ has no effect.

Expanding this out a bit: a  **symmetric monoidal category** is, to begin with a [[category]] $M$ equipped with a [[functor]]
$$ \otimes : M \times M \to M $$
called the **tensor product**, an object
$$ 1 \in M $$
called the **unit object**, a natural isomorphism
$$ a_{x,y,z} : (x \otimes y) \otimes z \to x \otimes (y \otimes z) $$
called the **associator**, a natural isomorphism
$$ \lambda_x : 1 \otimes x \to x $$
called the **left unitor**, a natural isomorphism 
$$  \rho_x : x \otimes 1 \to x $$
called the **right unitor**, and a natural isomorphism
$$ B_{x,y} : x \otimes y \to y \otimes x $$
called the **braiding**.  We then demand that the associator obey the **pentagon identity**, which says this diagram commutes:

+--{: style="text-align:center"}
[[!include monoidal category > pentagon]]
=--


We demand that the associator and unitors  obey the **triangle identity**, which says this diagram commutes:

$$
  \array{
     & (x \otimes 1) \otimes y &\stackrel{a_{x,1,y}}{\longrightarrow} & x \otimes (1 \otimes y)
      \\
      
      & {}_{\rho_x \otimes 1_y}\searrow
       
       && \swarrow_{1_x \otimes \lambda_y}
      & 
     \\
     &&
     x \otimes y
     &&
     
  }
$$

We demand that the braiding and associator obey the first **hexagon identity**:

$$
  \array{
   (x \otimes y) \otimes z 
   &\stackrel{a_{x,y,z}}{\to}&
   x \otimes (y \otimes z)
   &\stackrel{B_{x,y \otimes z}}{\to}&
   (y \otimes z) \otimes x
   \\
   \downarrow^{B_{x,y}\otimes 1_z}
   &&&&
   \downarrow^{a_{y,z,x}}
   \\
   (y \otimes x) \otimes z
   &\stackrel{a_{y,x,z}}{\to}&
   y \otimes (x \otimes z)
   &\stackrel{1_y \otimes B_{x,z}}{\to}&
   y \otimes (z \otimes x)
  }
$$

And lastly, we demand that
$$ B_{y,x} B_{x,y} = 1_{x \otimes y} . $$
(The definition of [[braided monoidal category]] has _two_ hexagon identities, but either one implies the other given this equation.)


## Properties

### The 2-category of symmetric monoidal categories

There is a [[strict 2-category]] $SymmMonCat$ with:

* symmetric monoidal categories as objects,
* [[symmetric monoidal functor]]s as morphisms, 
* [[symmetric monoidal natural transformation]]s as 2-morphisms.

This 2-category has (weak) 2-[[biproducts]] given by the cartesian product of underlying categories (analogously to how [[Ab]] has biproducts given by the cartesian product of underlying sets).  For a proof, see [Fong-Spivak, Theorem 2.3](#FongSpivak), or for a more abstract version involving [[pseudomonoids]] [Schaeppi, Appendix A](#Schaeppi).

### As models for connective spectra
  {#ModelsForConnectiveSpectra}

The [[group completion]] of the [[nerve]] of a symmetric monoidal category is always an  [[infinite loop space]], hence the degree-0-space of a [[connective spectrum]]. One calls this also the [[K-theory]] spectrum of the symmetric monoidal category:

$$
  \array{
     &&&& Spectra
     \\
      && {}^{\mathllap{K}}\nearrow && \downarrow
    \\
    SymmMonCat &\to& Cat &\underset{N}{\to}& sSet
  }
  \,.
$$

This construction extended to an [[equivalence of categories]] 

$$
  K :  Ho(SymmMonCat)
   \stackrel{\simeq}{\to}
  Ho(Spectra)_{\geq 0}
  \hookrightarrow
  Ho(Spectra)
$$ 

between the [[full subcategory]] of the [[stable homotopy category]] $Ho(Spectra)$ on the [[connective spectra]] and the [[homotopy category]] of $SymmMonCat$, regarded with the [[transferred model structure|transferred structure]] of a [[category with weak equivalences]].

This is due to ([Thomason, 95](#Thomason)). Further discussion is in ([Mandell, 2010](#Mandell)).

Notice that this is _almost_ the complete analog in [[stable homotopy theory]] of the [[Quillen equivalence]] between the [[Thomason model structure]] on [[Cat]] and the standard [[model structure on simplicial sets]]. Only that $SymmMonCat$ cannot carry a [[model category]] structure because it does not have all [[colimit]]s. In some sense the "colimit completion" of $SymmMonCat$ is the category of [[multicategories]]. Once expects that this carries a model structure that refines the above equivalence of homotopy categories to a [[Quillen equivalence]].

(This is currently being investigated by Elmendorf, Nikolaus and maybe others.)

However, a subcategory of $SymmMonCat$ whose objects are Permutative categories and maps are strict symmetric monoidal functors, denoted by $Perm$  has a model category structure  which is transferred from the natural model category structure on $Cat$, see [Sharma](#Sharma). This model category structure is combinatorial, left-proper and a $Cat$-model category structure. It is referred to as the natural model category structure on $Perm$. The [[coherence theorem]] for symmetric monoidal categories states that each symmetric monoidal category is equivalent to a [[permutative category]].

### Relation to $\Gamma$-categories

The aforementioned natural model category of permutative categories is NOT a symmetric monoidal closed model category. This shortcoming was overcome in [Sharma] by constructing a Quillen equivalent [[model category]] which is symmetric monoidal closed.
A (unnormalized) $\Gamma$-category is a functor from $\Gamma^{op}$ to $Cat$, where $\Gamma^{op}$ is a skeletal category of finite based sets and based maps.
The category of $\Gamma$-categories and natural transformations, denoted by $\Gamma$$Cat$, is a symmetric monoidal closed category under the [[Day convolution]] product. The aforementioned symmetric monoidal closed model category is constructed in [Sharma](#Sharma) as a left-Bousfield localization of the projective model category structure on $\Gamma$$Cat$. A $\Gamma$-category is fibrant in this model category if it satisfies the Segal's condition in which case it is referred to as a coherently commutative monoidal category. The main result of [Sharma](#Sharma) is that an unnormalized version of the classical Segal's nerve functor is the right [[Quillen functor]] of a [[Quillen equivalence]] between the natural model category of permutative categories and the symmetric monoidal closed model category of coherently commutative monoidal categories.


### As algebras over the little $k$-cubes operad

A symmetric monoidal category is equivalently a category that is equipped with the structure of an [[algebra over an operad|algebra over]] the [[little cubes operad|little k-cubes operad]] for $k \geq 3$

Details are in examples 1.2.3 and 1.2.4 of

* [[Jacob Lurie]], $\mathbb{E}[k]$-[[Ek-Algebras|Algebras]]

### Tannaka duality

[[!include structure on algebras and their module categories - table]]

### Grothendieck ring

The [[Grothendieck group]] of a [[monoidal category]] naturally has the structure of a [[monoid]], of an [[abelian category|abelian]] monoidal category that of a [[ring]], of an abelian [[braided monoidal category]] that of a [[commutative ring]] and, finally, of an abelian symmetric monoidal category that of a _[[Lambda-ring]]_. See there for more.

### Internal logic

The [[internal logic]] of ([[closed monoidal category|closed]]) symmetric monoidal categories is called _[[linear logic]]_. This notably contains [[quantum logic]].

### Permutations

For every $n \ge 2$ and $\sigma \in \mathfrak{S}_{n}$, there is a [[natural transformation]] 
$$\sigma: A_{1} \otimes ... \otimes A_{n} \rightarrow A_{\sigma^{-1}(1)} \otimes ... \otimes A_{\sigma^{-1}(n)}$$
that is defined by the decomposition of a [[permutation]] in a product of adjacent [[transpositions]] and generalizes the [[braiding]] 
$$
B:A_{1} \otimes A_{2} \rightarrow A_{2} \otimes A_{1}
$$

We recall that an adjacent transposition $[1,n] \rightarrow [1,n]$ where $n \ge 2$ is a permutation $t:[1,n] \rightarrow [1,n]$ such that there exists a $1 \le i \le n-1$ such that: 
$$
t(1)=1,..., t(i-1)=i-1, t(i) = i+1, t(i+1) = i, t(i+2)=i+1,.... ,t(n)=n
$$
This $i$ is then unique, and for every $1 \le i \le n-1$, we note $t_{i}$ the associated adjacent transposition.

For $n \ge 2$, every permutation $\sigma \in \mathfrak{S}_{n}$ admits at least a decomposition under the form $\sigma = t_{i_{1}}; ...;t_{i_{q}}$
where $q \ge 0$, and $1 \le i_{1},....,i_{q} \le n-1$. 

In every symmetric monoidal category, for $n \ge 2$ and $1 \le i \le n-1$, we have a natural transformation 
$$t_{i}:A_{1} \otimes .... \otimes A_{n} \rightarrow A_{1} \otimes ... \otimes A_{i-1} \otimes A_{i+1} \otimes A_{i} \otimes A_{i+2} \otimes .... \otimes A_{n}$$ 
defined by: 
$$t_{i} = A_{1} \otimes ... \otimes A_{i-1} \otimes \B_{A_{i},A_{i+1}} \otimes A_{i+2} \otimes ... \otimes A_{n}$$

Given a $\sigma \in \mathfrak{S}_{n}$, the associated natural transformation is then defined as $t_{i_{1}};....;t_{i_{q}}$ for any such decomposition of $\sigma$. The fact that the result doesn't depend on the particular decomposition is a consequence of the [[coherence theorem for symmetric monoidal categories]].
 
## Examples 

* Every [[cartesian monoidal category]] is necessarily symmetric monoidal, due to the essential uniqueness of the categorical [[product]]. This includes cases such as [[Set]], [[Cat]].

* For $k$ some [[field]], the category [[Vect]] of $k$-vector spaces carries the standard structure of a [[monoidal category]] coming from the [[tensor product]], over $k$, of vector spaces. The standard braiding that identifies $V \otimes W$ with $W \otimes V$ by mapping homogeneous elements $v \otimes w$ to $w \otimes v$ obviously makes [[Vect]] into a symmetric monoidal category.

* The category of $\mathbb{Z}_2$-[[graded vector space]]s, on the other hand, has two different symmetric monoidal extensions of the standard [[tensor product]] monoidal structure. One is the trivial one from above, the other is the one that induces a a sign when two odd-graded vectors $v$ and $w$ are passed past each other : $v \otimes w \mapsto - w \otimes v$. This non-trivial symmetric monoidal structure on $Vect[\mathbb{Z}_2]$ defines the symmetric monoidal category of [[super vector spaces]].

* The monoidal category of [[graded modules]] over a [[commutative ring]] (with the usual [[tensor product of modules|tensor product of graded modules]]) can be made into a braided monoidal category with the braiding 

$$
  \array{
    V \otimes W &\longrightarrow& W \otimes V
    \\
    x \otimes y &\mapsto& y \otimes x
  }
  \,.
$$

The braiding $x \otimes y \mapsto (-1)^{|x| |y|} y \otimes x$ (where $|x|$ and $|y|$ denote the degrees) is also commonly used.

  More generally, for any invertible element $u$ of the base ring, there is the [[braided monoidal category|braiding]] $x \otimes y \mapsto u^{|x| |y|} y \otimes x$, and these braidings are the only possible. The resulting [[braided monoidal category]] is symmetric if and only if $u^2 = 1$.



## Related concepts

* [[monoidal category]], [[monoidal (∞,1)-category]]

* **symmetric monoidal category**, [[symmetric monoidal (∞,1)-category]], [[symmetric monoidal (∞,n)-category]] 

  * [[permutative category]], [[bipermutative category]]

  * [[symmetric monoidal dagger category]]

* [[closed monoidal category]] ,  [[closed monoidal (∞,1)-category]]

* [[equivariant symmetric monoidal category]]

* [[symmetric bicategory]]

* [[symmetric monoidal groupoid]]

  * [[symmetric 2-group]], [[abelian ∞-group]]

## References

Original references:

* {#MacLane} [[Saunders Mac Lane]], _Natural Associativity and Commutativity_ , Rice University Studies **49** (1963) pp.28-46. 

* [[Jean Bénabou]], _Algèbre élémentaire dans les catégories_ (1964), C. R. Acad. Sci. Paris **258** (1964) pp.771-774, [gallica](https://gallica.bnf.fr/ark:/12148/bpt6k40102/f817)

Textbook accounts:

* {#Borceux94} [[Francis Borceux]], Section 6.1 of: *Handbook of Categorical Algebra* Vol. 2: *Categories and Structures* $[$[doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865)$]$, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994)


* {#EGNO15} [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], *Tensor Categories*, AMS Mathematical Surveys and Monographs **205** (2015) $[$[ISBN:978-1-4704-3441-0](https://bookstore.ams.org/surv-205), [pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf)$]$

  > (focused on [[tensor categories]])

Exposition of basics of [[monoidal categories]] and [[categorical algebra]]:

* _[[geometry of physics -- categories and toposes]]_, Section 2: _[Basic notions of categorical algebra](geometry+of+physics+--+categories+and+toposes#BasicNotionsOfCategoricalAlgebra)_


A survey of definitions of symmetric monoidal categories, [[symmetric monoidal functor]]s and [[symmetric monoidal natural transformation]]s, is also in

* [[John Baez]], _[Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf)_

For an elementary introduction to symmetric monoidal categories using string diagrams, see:

* [[John Baez]] and [[Mike Stay]], [Physics, topology, logic and computation: a Rosetta Stone](http://math.ucr.edu/home/baez/rosetta.pdf).

The theorem that symmetric monoidal categories model all connective spectra is due to 

* R. Thomason, _Symmetric monoidal categories model all connective spectra_ , Theory and applications of Categories, Vol. 1, No. 5, (1995) pp. 78-118
 {#Thomason}

More discussion is in 

* [[Michael Mandell]], _An Inverse K-Theory Functor_ ([arXiv:1002.3622](http://arxiv.org/abs/1002.3622))
 {#Mandell}

* {#FongSpivak} Brendan Fong and David I, Spivak, *Supplying bells and whistles in symmetric monoidal categories*, [arxiv](https://arxiv.org/abs/1908.02633), 2019

* {#Schaeppi} Daniel Schäppi, *Ind-abelian categories and quasi-coherent sheaves*, [arxiv](https://arxiv.org/abs/1211.3678), 2014

* Amit Sharma, _Symmetric monoidal categories and $\Gamma$-categories_
Theory and applications of Categories, Vol. 35, No. 14, (2020) pp. 417-512
 {#Sharma}

[[!redirects symmetric monoidal categories]]
[[!redirects symmetric monoidal structure]]
[[!redirects symmetric monoidal structures]]

[[!redirects symmetric monoidal]]

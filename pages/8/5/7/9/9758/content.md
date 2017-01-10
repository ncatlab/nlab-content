

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What are called _Fierz identities_ in [[physics]] are the relations that hold between [[multilinear map|multilinear]]  expression in [[spinors]]. For example for all [[Majorana spinors]] $\psi$ in Lorentzian spacetime dimension 4,5,7,11, then the following identity holds (example \ref{TheM2andM5CocyclesAsFierzIdentities} below):

$$
  \left(\overline{\psi} \wedge \Gamma_{a b} \psi\right)
  \wedge
  \left(\overline{\psi} \wedge \Gamma^b \psi\right)
  \;=\;
  0  
  \,.
$$

(Here $\overline{(-)}$ denotes the Majorana conjugate, $\Gamma_a$ are a Clifford representations, the "$\wedge$"-signs denotes symmetrization in the spinor components and summation over repeated indices is understood. The details of this are discussed [below](#BilinearFierzIdentities).)

In [D'Auria-Fr&#233;-Maina-Regge 82](#DAuriaFreMainaRegge82) it was pointed out that all Fierz identities may be understood as expressing the product operation in the [[representation ring]] of the [[spin group]] (in some given dimension): for $\{S_i\}_{i \in I}$ denoting [[isomorphism classes]] of [[irreducible representations|irreducible]] [[spin representations]], then, by definition of [[irreps]], their [[tensor product of representations]] decomposes again as a [[direct sum]] of [[irreducible representations]]

$$
  S_i \otimes S_j  = \underset{k}{\oplus} C_{i j}{}^k S_k
$$

with "[[Clebsch-Gordan coefficients]]" $C_{i j}{}^k$. These coefficients are effectively the Fierz identities.

For example for Lorentzian dimension 11 with $(\tfrac{1}{2})^5$ denoting the unique irreducible [[Majorana spinor]] representation, then one finds ([D'Auria-Fr&#233; 82b, section 3](#DAuriaFre82b)) that the symmetric part in the quadruple tensor product of this representation with itself decomposes as a direct sum of irreps as follows

$$
  \left\{
    (\tfrac{1}{2})^5 
      \otimes
    (\tfrac{1}{2})^5 
      \otimes
    (\tfrac{1}{2})^5 
      \otimes
    (\tfrac{1}{2})^5 
  \right\}_{sym}
   \;\simeq\;
  (0)^5
    \;\oplus\;
  (1)^3 (0)^2
    \;\oplus\;
  (1)^4 (0)
    \;\oplus\;
  (1)^5 
    \;\oplus\;
  (2) (0)^4
    \;\oplus\;
  (2)(1)(0)^3
    \;\oplus\;
  (2)^2 (0)^3
    \;\oplus\;
  (2)^2 (1)^3
    \;\oplus\;
  (2)^5
$$

where the symbols refer to [[Young diagrams]] canonically labeling representations (details are in example \ref{11dQuadrilinearCGCoefficients} below). 

The point is that the expression $ \left(\overline{\psi} \wedge \Gamma_{a b} \psi\right) \wedge \left(\overline{\psi} \wedge \Gamma^b \psi\right)$ from above is a spinor quadrilinear which transforms in the vector representation $(1)(0)^4$ (due to its one free spacetime index). But that vector representation $(1)(0)^4$ is missing from the [[direct sum]] above, meaning that the spinor quadrilinear has vanishing components in this vector representation, hence that this expression vanishes identically.


## In terms of cochains on super-Minkowski spacetimes

We discuss Fierz identities as identities among multispinorial elements of the [[Chevalley-Eilenberg algebra]] $CE(\mathbb{R}^{d-1,1\vert N})$ of [[super-Minkowski spacetime]] $\mathbb{R}^{d-1,1\vert N}$, regarded as the super-translation [[supersymmetry]] [[super Lie algebra]]. In this form Fierz identities encode [[cocycles]] in the [[supersymmetry]] super-[[Lie algebra cohomology]], such as those which serve as [[higher WZW terms]] characterizing [[super p-branes]]. We follow [Castellani-D'Auria-Fr&#233; 82, section II.8](#CDF).


### Bilinear Fierz identities
  {#BilinearFierzIdentities}

Given a fixed [[real spin representation]] $N$, then the
odd [[coordinates]] $\{\theta^\alpha\}_{\alpha = 1}^{dim_{\mathbb{R}}(N) }$ of the [[super Minkowski spacetime]] [[supermanifold]]
$\mathbb{R}^{d-1,1\vert N}$ span, by construction, precisely that representation space, and hence so do the
spinorial components of the [[super vielbein]] form

$$
  \psi^\alpha = \mathbf{d}\theta^\alpha
   \;\;\;
   \in \Omega^{\bullet}_{li}(\mathbb{R}^{d-1,1\vert N})
   \simeq
    CE(\mathbb{R}^{d-1,1\vert N})
  \,,
$$

since in the construction of [[super differential forms]] on $\mathbb{R}^{d-1,1\vert N}$, the de Rham operator
$\mathbf{d}$ acts on the odd coordinates just formally, by sending the generator $\theta^\alpha$ to the new generator
named $\mathbf{d} \theta^\alpha$.

Therefore we may identify the [[spin representation]] $N$ with the [[linear span]] (over $\mathbb{R}$) of these elements

$$
  N  \simeq \langle \mathbf{d}\theta^\alpha \rangle_{\alpha = 1}^{dim_{\mathbb{R}}(N) }
  \,,
$$

were the [[spin group]] acts on the elements on the right in the defining way (see at _[[geometry of physics -- supersymmetry]]_): a spinorial rotation in a plane $\omega = \{\omega^{a b}\}$ by an angle $\alpha$ acts by

$$
  R_\omega(\psi) \coloneqq \exp(\tfrac{\alpha}{4} \omega^{a b} \Gamma_{a b} ) \psi
  \,.
$$

We may build new [[spin representations]] from this one by forming multilinear expressions in the [[super vielbein]]. For example the elements in $CE(\mathbb{R}^{d-1,1\vert N})$ of the form

$$
  \begin{aligned}
    \overline{\psi} \wedge \Gamma_a \psi
    &=
    \left(C_{\alpha \alpha'} \Gamma_a{}^{\alpha'}_{\beta}\right) \, \psi^\alpha \wedge \psi^{\beta}
    \\
    & =
    \left(C_{\alpha \alpha'} \Gamma_a{}^{\alpha'}_{\beta}\right) \, \mathbf{d}\theta^\alpha \wedge \mathbf{d}\theta^\beta
  \end{aligned}
$$

span, as the spacetime index $a$ ranges in $\{0, 1, \cdots, d-1\}$, a $d$-dimensional [[real vector space]]

$$
  \left\langle
     \,\overline{\psi} \wedge \Gamma_a \psi\,
  \right\rangle_{a = 0}^{d-1}
$$

which still carries a linear [[action]] of the [[spin group]], induced from the spin action on the $\psi$-s:

$$
  \begin{aligned}
    R_\omega(\overline{\psi} \wedge \Gamma_a \psi)
    & =
    \overline{\left( \exp(\tfrac{\alpha}{4}\omega^{a b}\Gamma_{a b} ) \psi \right)}
      \wedge \Gamma_a
    \left( \exp(\tfrac{\alpha}{4}\omega^{a b}\Gamma_{a b} \psi ) \right)
    \\
    & =
    \overline{\psi} \wedge \exp(-\tfrac{\alpha}{4} \omega^{a b} \Gamma_{a b}) \Gamma_a \exp(\tfrac{\alpha}{2}\omega^{a b} \Gamma_{a b})
     \psi
    \\
    & =
    \overline{\psi}
      \wedge
      (R_\omega(\Gamma_a))
    \psi
    \end{aligned}
  \,.
$$

Of course similarly we obtain elements

$$
  \overline{\psi} \Gamma_{a_1 \cdots a_p} \psi
$$

which, if they are non-vanishing at all, span the representation

$$
  \wedge^p \mathbb{R}^d
$$

Now observe that we may say all this more abstractly as follows:

1. the elements $(\psi \wedge \overline{\psi})^{\alpha \beta}$ span the symmetrized [[tensor product of representations]]

   $$
     \{N \otimes N\}_{sym}
       \;\simeq\;
     \langle 
       \,  (\psi \wedge \overline{\psi})^\alpha{}_\beta \,
     \rangle_{\alpha,\beta = 1}^{dim_{\mathbb{R}}(N)}
   $$

1. for given $p \in \mathbb{N}$, then the elements of the form $\overline{\psi} \wedge \Gamma_{a_1 \cdots a_p} \psi$ form a [[subrepresentation]] thereof, equivalent to the vector representation $\wedge^p\mathbb{R}^{d}$

1. hence there is a [[direct sum]] decomposition

   $$
     \left\{N \otimes N\right\}_{sym}
       \;\simeq\;
      \underset{p \in \mathbb{N}}{\bigoplus}
      c_p \left(\wedge^p \mathbb{R}^d\right)
   $$

   in the [[category of representations]] of the [[spin group]], which expresses the (symmetrized) [[tensor product of representations]] of the [[Majorana spinor]] representation as a [[direct sum]] of skew-symmetrized tensor products of the vector representation.

Indeed this direct sum decomposition is exhaustive:

+-- {: .num_prop #BilinearFierzDecomposition}
###### Proposition

For $d \in \mathbb{N}$ and $N$ a [[Majorana spinor]] representation of $Spin(d-1,1)$, then the following identity holds:

$$
  (\psi \wedge \overline{\psi})^\alpha{}_\beta
   \;=\;
  \tfrac{1}{dim_{\mathbb{R}}(N)}
  \left(
     \left(
       \overline{\psi}\psi
     \right)
     +
     \left(
       \overline{\psi} \Gamma_a \psi
     \right)
     (\Gamma^a)^\alpha{}_\beta
     + 
     \tfrac{1}{2!}
     \left(
       \overline{\psi} \Gamma_{a_1 a_2} \psi
     \right)
     (\Gamma^{a_1 a_2})^\alpha{}_\beta
      + 
     \cdots
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion there, the [[Majorana spinor]] representation is a real sub-representation of a complex _Dirac representation_ $\mathbb{C}^{(2^\nu)}$. The latter has the special property that

1. the [[Clifford algebra]] contains the full [[matrix algebra]];

1. for $p \geq 1$ the Clifford elements $\Gamma_{a_1 \cdots a_p}$ have vanishing [[trace]].

The first point implies that there exists coefficients $X^{a_1 \cdots a_p} \in \mathbb{C}$ for $p \in \mathbb{N}$ such that

$$
  \psi \wedge \overline{\psi}
    =
  \tfrac{1}{dim_{\mathbb{R}}(N)}
  \left(
    X
    +
    X^a \Gamma_a 
    +
    X^{a b} \Gamma_{a b} 
    +
    \cdots
  \right)
  \,.
$$

The second condition then implies that multiplying this expression with $\Gamma^{a_1 \cdots a_p}$ and taking the trace projects out the coefficient $X^{a_1 \cdots a_p}$:

$$
  \begin{aligned}
    X^{a_1 \cdots a_p}
      & = 
    \frac{1}{p! dim_{\mathbb{R}}(N)}
    tr_N
    \left(
      \left(
        X
        +
        X^a \Gamma_a 
        +
        X^{a b} \Gamma_{a b} 
        +
        \cdots
      \right)
      \Gamma^{a_1 \cdots a_p}
   \right)
   \\
   & = 
   \tfrac{1}{p!}
   tr_N
   \left(
     \psi \wedge \overline{\psi} \, \Gamma^{a_1 \cdots a_p}
   \right)
   \\
   & = 
   \tfrac{1}{p!}
   \left(
     \overline \psi \wedge \Gamma^{a_1 \cdots a_p} \psi
   \right)
  \end{aligned}
  \,.
$$

Notice that it is the last step, identifying the trace over $\psi \wedge \overline{\psi} \Gamma^{a_1 \cdots a_p}$ with the $\psi$-$\psi$ component of the matrix $\Gamma^{a_1 \cdots a_p}$, where we use the _symmetrization_ of the spinor tensor product, namely the identity $\psi^\alpha \wedge \overline{\psi}_\beta = \overline{\psi}_\beta \wedge \psi^\alpha$.  

=--


Some of the coefficients in prop. \ref{BilinearFierzDecomposition} may vanish identically. These are the _bilinear Fierz identities_, of the form

$$
  \overline{\psi} \Gamma_{a_1 \cdots a_p} \psi = 0
  \,.
$$

+-- {: .num_example}
###### Example

Let $d = 11$. Write $\mathbf{32}$ or $(\tfrac{1}{2})^5$ for the [[Majorana spinor]] representation of $Spin(d-1,1)$. Then 

$$
  \left\{
    (\tfrac{1}{2})^5
      \otimes
    (\tfrac{1}{2})^5
  \right\}_{sym}
     \;\simeq\;
  \underset{\simeq \mathbb{R}^d}{\underbrace{(1)^1 (0)^4}}
    \;\oplus\;
  \underset{\simeq \wedge^2 \mathbb{R}^d}{\underbrace{(1)^2 (0)^3}}
    \;\oplus\;
  \underset{\wedge^5 \mathbb{R}^d}{\underbrace{(1)^5}}
  \,.
$$

=--

([D'Auria-Fr&#233; 82b (3.1)](#DAuriaFre82b))


+-- {: .proof}
###### Proof

Since we know from prop. \ref{BilinearFierzDecomposition} that the right hand side has to be some direct sum of representations of the form $\wedge^p \mathbb{R}^d$, it is sufficient to check that there is only one choice of sum such that [[dimensions]] match on both sides of the equation.

Now the dimension of $\{N \otimes N\}_{sym}$ is that of the space of symmetric $32 \times 32$ matrices:

$$
  dim_{\mathbb{R}} 
  \left(
     \{\mathbf{32} \otimes \mathbf{32}\}_{sym}
  \right)
   \;=\;
  \frac{1}{2}
  \left(
    32 \times 33 
  \right)
   = 
  528
$$

while the dimension of $\wedge^p \mathbb{R}^d$ is the [[binomial coefficient]]

$$
  dim_{\mathbb{R}}(\wedge^p \mathbb{R}^d)
   \;=\;
  \left(
    11 \atop p
  \right)
  \,.
$$


Hence the claim follows from the fact that 

$$
  \begin{aligned}
    528 
     & = 11 + 55 + 462
    \\
    & =
  \left(11 \atop 1\right)
   +
  \left(11 \atop 2\right)
   +
  \left(11 \atop 5\right)
  \end{aligned}
  \,.
$$

=--



### Quadrilinear Fierz identities
  {#QuadraticFierzIdentities}


Now we consider the [[direct sum]] decomposition of the [[tensor product of representations]] of _four_ copies of a [[spin representation]]. This yields the quadrilinear Fierz identities.

+-- {: .num_example #11dQuadrilinearCGCoefficients}
###### Example

The group $Spin(10,1)$ has [[rank of a Lie group|rank]] 5, and hence its [[irreducible representation|irreducible]] vector representations are labeled by [[Young diagrams]] consisting of five rows. For instance

$$
  (2)^2 (1)^2 (0)
$$

denotes the representation whose elements may be identified with tensors of the form

$$
  X_{\array{ a_1 & a_2 \\ a_3 & a_4 \\ a_5 }}
$$

which are

1. skew-symmetric in indices in the same column;

1. symmetric and trace-less in indices in the same row.

Write again $(\tfrac{1}{2})^5$ for the [[Majorana spinor]] representation. Then the following identity holds in the [[representation ring]]:


$$
  \left\{
    (\tfrac{1}{2})^5 
      \otimes
    (\tfrac{1}{2})^5 
      \otimes
    (\tfrac{1}{2})^5 
      \otimes
    (\tfrac{1}{2})^5 
  \right\}_{sym}
   \;\simeq\;
  \left.
    \array{
    (0)^5
    \\
    \oplus
    \\
    (2) (0)^4
    \\
    \oplus
    \\
    (1)^3 (0)^2 \oplus  (2)(1)(0)^3
    \\
    \oplus
    \\
    (1)^4 (0) \oplus (2)^2 (0)^3
    \\
    \oplus
     \\
    (1)^5 
     \\
     \oplus
     \\
    (2)^2 (1)^3
    \\
    \oplus
    \\
    (2)^5
   }
  \right.
$$

=--

([D'Auria-Fr&#233; 82b (3.3) ](#DAuriaFre82b))

+-- {: .proof}
###### Proof

As before, this is supposed to follow already by matching total dimensions on both sides


$$
  \frac{32 \times 33 \times 34 \times 35}{4 \times 3 \times 2}
   \;=\;
  \left.
    \array{
    1
    \\
    + 
    \\
    65
    \\
    +
    \\
    165 +  429
    \\
    +
    \\
    330 + 1144
    \\
    +
     \\
    462
     \\
     +
     \\
    17160
    \\
    +
    \\
    32604
   }
  \right.
$$

=--

More in detail we have the following decompositions, in the notation from [above](#QuadraticFierzIdentities).

\[
  \label{Fierz11dA}
  \left(\overline{\psi} \wedge \Gamma_{a_1} \psi\right) 
   \wedge 
  \left( \overline{\psi} \wedge \Gamma_{a_2} \psi \right)
   \;=\;
  X^{(\mathbf{65})}_{\array{a_1 \\ a_2}}
   + 
  \frac{1}{11} \delta_{\array{a_1 a_2}}X^{(\mathbf{1})}
\]

Here for instance the symbol $X^{(\mathbf{65})}_{\array{a_1 \\ a_2}}$ denotes the projection of the term on the left into the direct summand given by the [[representation]] $(2)(0)^4$ of dimension $65$. Similarly: 

\[
  \label{Fierz11dB}
  \left(\overline{\psi} \wedge \Gamma_{a_1 a_2} \psi\right)
    \wedge 
  \left(\overline{\psi} \wedge \Gamma_{a_3}\right)
    \;=\;
  X^{(\mathbf{429})}_{\array{ a_1 & a_2 \\ a_3}}
   +
  X^{(\mathbf{165})}_{\array{a_1 a_2 a_3}}
\]

\[
  \label{Fierz11dC}
  \left(
    \overline{\psi}\Gamma_{a_1 a_2} \psi
  \right)
  \left(
    \overline{\psi} \Gamma_{a_3 a_4}
  \right)
   \;=\;
  X^{(\mathbf{1144})}_{\array{a_1 a_2 \\ a_3 a_4}}
   + 
  X^{(\mathbf{330})}_{\array{a_1 a_2 a_3 a_4}}
   +
  \tfrac{4}{9}\delta_{\array{ [a_1 \\ [a_3} } X^{(\mathbf{65})}_{\array{a_2] \\ a_4] } }
  -
  \tfrac{2}{11} \delta_{\array{a_1 & a_2 \\ a_3 & a_4}} X^{(\mathbf{1})}
\]

\[
  \label{Fierz11dD}
  \left(
    \overline{\psi}
      \wedge
      \Gamma_{a_1 \cdots a_5}
    \psi
  \right)
  \wedge
  \left(
    \overline{\psi}
      \wedge
    \Gamma_{a_6}
   \psi
  \right)
  \;=\;
  \epsilon_{a_1 \cdots a_6}{}^{b_1 \cdots b_5}
  X^{(\mathbf{462})}_{b_1 \cdots b_5}
  + 
  X^{(\mathbf{4290})}_{\array{a_1 & \cdots & a_5 \\ a_6}}
  +
  \frac{15}{7}
  \delta_{a_6 [ a_1} X^{(\mathbf{330})}_{\array{a_2 & \cdots & a_5}}
\]

and some more. 

([D'Auria-Fr&#233; 82b table 2 ](#DAuriaFre82b))



As a corollary:

+-- {: .num_example #TheM2andM5CocyclesAsFierzIdentities}
###### Example

For $d = 11$ then 

1. the following Fierz identity holds:

   $$
     \left(
       \overline{\psi} \wedge \Gamma_{a b} \psi  
     \right) 
     \wedge
     \left(
        \overline{\psi} \wedge \Gamma^b \psi
     \right)
     \;= \; 0
     \,.
   $$

   (this is the cocycle condition for the [[higher WZW term]] of the [[M2-brane]] ([Bergshoeff-Sezgin-Townsend 87](#BergshoeffSezginTownsend87)), [AETW 87](#AETW87)) 

1. the following Fierz identity holds:

   $$
     \left(
       \overline{\psi}
         \wedge
         \Gamma_{a_1 \cdots a_4 b}
       \psi
     \right)
     \wedge
     \left(
       \overline{\psi}
        \wedge
        \Gamma^{b}
        \psi
     \right)
     \;=\;
     3
     \left(
     \overline{\psi}
        \Gamma_{[a_1 a_2}
     \psi
     \right)
     \wedge
     \left(
       \overline{\psi}
          \Gamma_{a_3 a_4]}
       \psi
     \right) 
   $$

   (this is the cocycle condition for the [[higher WZW term]] of the [[M5-brane]] ([BLNPST 97](#BLNPST97), [FSS 15](#FSS15))).

=--

([D'Auria-Fr&#233; 82b (3.13) and (3.28) ](#DAuriaFre82b))

+-- {: .proof}
###### Proof

The first identity is the result of equation (eq:Fierz11dB) after tracing over the indices $a_2$ and $a_3$. Under this trace both summands on the right of (eq:Fierz11dB) vanish: $X^{(\mathbf{429})}_{\array{ a_1 & a_2 \\ a_3}}$ because it is trace-free in indices in a column, and $X^{(\mathbf{165})}_{\array{a_1 a_2 a_3}}$ because it is skew-symmetric in all indices.

The second identity follows from taking the trace over the indices $a_5 and a_6$ in (eq:Fierz11dD) and of skew-symmetrizing over all indices in (eq:Fierz11dC). By the symmetry properties of the tensors on the right of both equations, in both cases all tensors vanish except, in both cases, the contribution proportional to $X^{(\mathbf{330})}_{[a_1 \cdots a_3]}$, which both identities share. So it only remains to check that the proportionality factor is 3, as claimed. By writing out the skew-symmetrization in the last term in (eq:Fierz11dD) one finds:

{#ComputationOfRelativeCoefficientInM5Cocycle}
$$
  \begin{aligned}
    \frac{15}{7}
    \delta^{a_1 a_6}
    \delta_{a_6 [a_1}
    X^{(\mathbf{330})}_{a_2 \cdots a_5]}
    & =
    \frac{15}{7}  
    \delta^{a_1}{}_{[a_1} X^{(\mathbf{330})}_{a_2 \cdots a_5]}
    \\
    & =
    \frac{15}{7}
    \frac{1}{5!}
    \sum_{ \left\{\sigma \atop { {\text{permutation of}} \atop {\{1,\cdots , 5\}} } \right\}}
    (-1)^{\vert \sigma\vert }
    \delta^{a_1}{}_{a_{\sigma(1)}}
    X_{a_{\sigma(2)} \cdots a_{(\sigma(5))}}
    \\
    & =
    \frac{15}{7}
    \frac{1}{5!}
    \sum_{\left\{\sigma \atop { {\text{permutation of}} \atop {\{1,\cdots , 4\}} } \right\} }
    (-1)^{\vert \sigma\vert } 
    \left(  
      \underset{= 11}{\underbrace{\delta^{a_1}_{a_1}}}
      X^{(\mathbf{330})}_{a_{\sigma(1)}\cdots a_{\sigma(4)}}
      -
      4
      \delta^{a_1}{}_{a_{\sigma(1)}}
      X_{a_1 a_{\sigma(2)} \cdots a_{\sigma(4)}}
    \right) 
   \\
   & =
    \frac{15}{7}
    (11-4)
    \frac{1}{5}
    \;
    \underset{X^{(\mathbf{330})}_{a_1\cdots a_4}}{
    \underbrace{
    \frac{1}{4!}
    \sum_{ \left\{ \sigma \atop { {\text{permutation of}} \atop {\{1,\cdots , 4\}} } \right\} }
    (-1)^{\vert \sigma\vert}
    X^{(\mathbf{330})}_{a_{\sigma(1)}\cdots a_{\sigma(4)}}
    }
    }
    \\
    & =
    3 \; X^{(\mathbf{330})}_{a_{\sigma(1)} \cdots a_{\sigma(4)}}
  \end{aligned}
$$

where we used that $X^{(\mathbf{330})}_{a_1 \cdots a_4}$ is already skew-symmetric in all indices.

=--

## Related concepts

* [[Clebsch-Gordan coefficient]]

## References

Named after [[Markus Fierz]].

The interpretation of Fierz identities as relations satisfied by [[Clebsch-Gordan coefficients]] in the [[representation ring]] of the [[spin group]] originates in

* {#DAuriaFreMainaRegge82} [[Riccardo D'Auria]], [[Pietro Fré]],  E. Maina, [[Tullio Regge]]  _A New Group Theoretical Technique for the Analysis of Bianchi Identities and Its Application to the Auxiliary Field Problem of $D=5$ Supergravity_, Annals Phys. 139 (1982) 93 ([doi:10.1016/0003-4916(82)90007-0](http://dx.doi.org/10.1016/0003-4916(82)90007-0), [spire](http://inspirehep.net/record/167640/))

where it was applied to $Spin(4,1)$ (relevant in [[5-dimensional supergravity]]).

By this method the Fierz identities for $Spin(9,1)$ (relevant in [[heterotic supergravity]] and [[type II supergravity]]) are discussed in

* {#DAuriaFre82a} [[Riccardo D'Auria]], [[Pietro Fré]], _Geometric Structure of $N=1, D=10$ and $N=4, D=4$ Super Yang-Mills Theory_, Nucl. Phys. B196 (1982) 205 ([spire](http://inspirehep.net/record/167639))
  
see also appendix C of 

* [[José Figueroa-O'Farrill]], Emily Hackett-Jones, George Moutsopoulos, _The Killing superalgebra of ten-dimensional supergravity backgrounds_, Class.Quant.Grav.24:3291-3308,2007 ([arXiv:hep-th/0703192](http://arxiv.org/abs/hep-th/0703192))

and the Fierz identities for $Spin(10,1)$ (relevant in [[11-dimensional supergravity]]) were tabulated in 

* {#DAuriaFre82b} [[Riccardo D'Auria]], [[Pietro Fré]], pages 12, 13 of _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) ([[GeometricSupergravityErrata.pdf:file]]) 
 
see also

* S. Naito, K. Osada, T. Fukui, _Fierz Identities and Invariance of Eleven-dimensional Supergravity Action_, Phys.Rev. D34 (1986) 536-552 ([spire](http://inspirehep.net/record/236376/?ln=de))

A textbook account of the representation ring method and summary of these results is in

* {#CDF} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], chapter II.8 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

See also

* C. C. Nishi, _Simple derivation of general Fierz-type identities_,  	Am. J. Phys. 73 (2005) 1160-1163 ([arXiv:hep-ph/0412245](http://arxiv.org/abs/hep-ph/0412245))

From the point of view of [[division algebras and supersymmetry]]
the Fierz identities that give the vanishing of trilinear and of quadratic terms in spinors in certain dimensions are discussed in

* [[John Huerta]], section 2.4 _Division Algebras, Supersymmetry and Higher Gauge Theory_ ([arXiv:1106.3385](http://arxiv.org/abs/1106.3385))

The recognition of some Fierz identities as cocycle conditions defining the [[higher WZW terms]] of the [[super p-branes]] is due to

* {#HenneauxMezincescu85} [[Marc Henneaux]], Luca Mezincescu, _A Sigma Model Interpretation of Green-Schwarz Covariant Superstring Action_, Phys.Lett. B152 (1985) 340 ([web](http://inspirehep.net/record/15922?ln=en))

* {#BergshoeffSezginTownsend87}  [[Eric Bergshoeff]], [[Ergin Sezgin]], [[Paul Townsend]], _Supermembranes and eleven dimensional supergravity_, Phys.Lett. B189 (1987) 75-78, In [[Mike Duff]],  (ed.), _[[The World in Eleven Dimensions]]_ 69-72 ([pdf](http://streaming.ictp.trieste.it/preprints/P/87/010.pdf), [spire](http://inspirehep.net/record/248230?ln=en))

* {#AETW87} Anna Ach&#250;carro, [[Jonathan Evans]], [[Paul Townsend]], [[David Wiltshire]], _Super $p$-Branes_, Phys. Lett. B **198** (1987) 441 ([spire](http://inspirehep.net/record/22286?ln=en))

* {#BLNPST97} [[Igor Bandos]], [[Kurt Lechner]], Alexei Nurmagambetov, [[Paolo Pasti]], [[Dmitri Sorokin]], Mario Tonin, _Covariant Action for the Super-Five-Brane of M-Theory_, Phys. Rev. Lett. 78 (1997) 4332-4334 ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))

* {#FSS15} [[nLab:Domenico Fiorenza]], [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[schreiber:The WZW term of the M5-brane|The WZW term of the M5-brane and differential cohomotopy]]_, J. Math. Phys. 56, 102301 (2015) ([arXiv:1506.07557](https://arxiv.org/abs/1506.07557))


[[!redirects Fierz identities]]
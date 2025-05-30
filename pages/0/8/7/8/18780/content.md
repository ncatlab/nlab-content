
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[category]] of [[finite dimensional vector spaces]] and [[linear functions]] between them.

A [[compact closed monoidal category]]

## Properties
 {#Properties}

### Splitting lemma
 {#SplittingLemma}

The [[splitting lemma]] says that every [[short exact sequence]] of [[vector spaces]] [[split exact sequence|splits]]
so that (in [[categorification]] of the [[rank-nullity theorem]]) every linear map $f \,\colon\, D \to C$ is equivalent to 

$$
  f 
  \;\colon\;
  ker(f) \oplus im(f)
  \xrightarrow{
     (0 , \iota_{im(f)})
  }
  C
  \,,
$$

where 

* $ker(f) \xrightarrow{\iota_{ker(f)}} D$ is the [[kernel]]

* $im(f) \xrightarrow{\iota_{im(f)}} C$ is the [[image]]

of $f$.

### Fiber (co)products
 {#FiberCoProducts}

The [[cartesian product]] in $FinDimVect$ is a [[biproduct]] given by [[direct sum of vector spaces]].

More generally, the [[fiber product]] of a [[pair]] of [[linear maps]] is given by the [[direct sum]] of their [[kernels]] and of the [[intersection]] of their [[images]]:

\begin{tikzcd}[
  sep=20pt
]
  & &&
  \def\arraystretch{.9}
  \begin{array}{c}
  \mathrm{ker}(f_1) \oplus \mathrm{ker}(f_2)
  \\
  \oplus 
  \\
  \mathrm{im}(f_1) \cap_{_B} \mathrm{im}(f_2)
  \end{array}
  \ar[
    d,
    phantom,
    "\simeq"{rotate=-90}
  ]
  \\[-10pt]
  &
  && 
  V_1 \times_{{}_B} V_2
  \ar[dll]
  \ar[drr]
  \ar[
    dd, 
    phantom, 
    "\scalebox{.6}{(pb)}"{description, pos=.2}]
  \\
  \mathrm{ker}(f_1)
  \oplus
  \mathrm{im}(f_1)
  \ar[r, phantom, "{\simeq}"]
  \ar[drr, "{ (0,\mathrm{id}) }"{description}]
  &[-10pt]
  V_1
  \ar[
    drr,
    end anchor={[yshift=+3pt]},
    "{ f_1 }"{description}
  ]
  &&
  &&
  V_2
  \ar[
    dll,
    end anchor={[yshift=+3pt]},
    "{ f_2 }"{description}
  ]
  &[-10pt]
  \ar[l, phantom, "{\simeq}"]
  \mathrm{im}(f_2) \oplus \mathrm{ker}(f_2)
  \ar[dll, "{ (\mathrm{id}, 0) }"{description}]
  \\
  &
  &
  \mathrm{im}(f_1)
  \ar[r, hook]
  & 
  B
  &
  \mathrm{im}(f_2)
  \ar[l, hook']
\end{tikzcd}

The [[coproduct]] in the [[slice category]] $FinDimVect_{/B}$ is given (by [general facts](over+category#LimitsAndColimits)) as the [[coproducts]], hence the [[direct sum]], of the domains, equipped with the induced maps to the base.

Applying [[(-1)-truncation]] to this fiber-wise coproduct of a [[pair]] of linear [[monomorphisms]] yields the [[linear span]] in $B$ of the two subspaces:

\begin{tikzcd}[sep=20pt]
  V_1 
  \ar[ddr, hook]
  \ar[r, hook]
  &
  V_1 \oplus V_2
  \ar[d, ->>]
  & 
  V_2
  \ar[ddl, hook']
  \ar[l, hook']
  \\[-10pt]
  &
  \mathrm{Span}_B(V_1, V_2)
  \ar[d, hook]
  \\[+10pt]
  & 
  B
\end{tikzcd}

In summary this means that the [[internal logic]] of [[slice category|slices]] of $FinDimVect$ is a [Birkhoff-vonNeumann quantum logic](quantum+logic#BirkhoffVonNeumannQuantumLogic).
 

## Related concepts

* [[Vect]]

* [[sFinVect]]

* [[quantum information theory]]$\;$[[quantum information theory in terms of dagger-compact categories|in terms of dagger-compact categories]]

* [[linear logic]]

## References

Discussion of [[linear algebra]] in $FinDimVect$ as [[categorical semantics]] for [[linear logic]]:

* {#Murfet14} [[Daniel Murfet]], *Logic and linear algebra: an introduction* &lbrack;[arXiv:1407.2650](http://arxiv.org/abs/1407.2650)&rbrack;


[[!redirects FinDimVec]]

[[!redirects FinVect]]
[[!redirects FinVec]]



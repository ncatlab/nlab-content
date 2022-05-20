
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
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

In [[persistent homology]] a *persistence diagram* or *barcode* is a way to encode the [[isomorphism class]] of a [[persistence module]] in terms of a [[multiset]] of [[pairs]] of [[numbers]] $a \leq b$ which stand for "features" reflected in the module which "appear" at stage $a$, "persist" until stage $b$ and then "disappear".

Concretely, [[Gabriel's theorem]] for [[ADE classification|A-type]] [[quivers]] (and analogously its generalizations to infinite linear diagrams and/or infinite-dimensional modules) says that every ([[zigzag persistence|zig-zag]]) [[persistence module]] (over some [[ground field]] $\mathbb{K}$), such as

\begin{tikzcd}
  V_1
  \ar[r, "{f_1}"]
  &
  V_2
  \ar[from=r, "{f_2}"{swap}]
  &
  V_3
  \ar[r, "{f_3}"]
  &
  \cdots
  \ar[r, "f_{n-1}"]
  &
  V_n
\end{tikzcd}

is [[generalized the|the]] [[direct sum]] (in the [[category]] of [[quiver representations]]) of *interval* modules $I_{a,b}$ of the form:

\begin{tikzcd}[column sep = small, row sep=small]
  1
  \ar[r,-]
  &
  \cdots
  \ar[r,-]
  &
  (a-1)
  \ar[r,-]
  &
  a
  \ar[r,-]
  &
  \cdots
  \ar[r,-]
  &
  b
  \ar[r,-]
  &
  (b+1)
  \ar[r,-]
  &
  \cdots
  \ar[r,-]
  &
  n
  \\
  \mathbb{K}^0
  \ar[r, -, "{0}"]
  &
  \cdots
  \ar[r, -, "{0}"]
  &
  0
  \ar[r,-, "{0}"]
  &
  \mathbb{K}^1
  \ar[r,-, "{\mathrm{id}}"]
  &
  \cdots
  \ar[r,-, "{\mathrm{id}}"]
  &
  \mathbb{K}^1
  \ar[r,-,"{0}"]
  &
  \mathbb{K}^0
  \ar[r,-,"{0}"]
  &
  \cdots
  \ar[r,-,"{0}"]
  &
  \mathbb{K}^0
  \mathrlap{\,.}
\end{tikzcd}

Hence the [[multiset]] of [[pairs]] $(a,b)$ labeling its inverval [[direct sum|summands]] completely characterizes the given persistence module, up to [[isomorphism]].

Regarding these pairs as [[intervals]], the collection they form is naturally envisioned as a collection of "bars" and then known as the *barcode* of the persitence module.

Regarding these pairs instead as points in the [[plane]], $(a,b) \in \mathbb{R}^2$, the [[multiset|multi]]-[[subset]] which they form is called the *persistence diagram* of the persistence module.

## Properties

* [[stability of persistence diagrams]]

## References

See also the references at *[[persistent homology]]*.

Introduction and survey:

* [[Robert Ghrist]], _Barcodes: The Persistent Topology of Data_, Bull. Amer. Math. Soc. 45 (2008), 61-75 ([doi:10.1090/S0273-0979-07-01191-3](https://doi.org/10.1090/S0273-0979-07-01191-3), [pdf](https://www.math.upenn.edu/~ghrist/preprints/barcodes.pdf))

* [[Steve Y. Oudot]], *Persistence Theory: From Quiver Representations to Data Analysis*, Mathematical Surveys and Monographs **209** AMS (2015) $[$[pdf](https://geometrica.saclay.inria.fr/team/Steve.Oudot/books/o-pt-fqrtda-15/surv-209.pdf), [ISBN:978-1-4704-3443-4](https://bookstore.ams.org/surv-209/)$]$

[[!redirects persistence diagrams]]

[[!redirects barcode]]
[[!redirects barcodes]]


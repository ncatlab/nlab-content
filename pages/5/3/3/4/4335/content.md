
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A __pseudonatural transformation__ is a kind of [[homomorphism]] between [[parallel morphisms|parallel]] [[2-functors]]: a a [[lax natural transformation]] whose [[2-morphism]] components are all [[equivalence|invertible]].  


## Definition

\begin{definition}
Given 

* a [[pair]] $\mathcal{X}, \mathcal{Y}$ of [[2-categories]]  

* a [[pair]] $F,G \colon \mathcal{X} \longrightarrow \mathcal{Y}$ of [[2-functors]],

a *pseudonatural transformation* 

$$
 \eta \colon F \Rightarrow G
$$ 
is a [[function]] from [[1-morphisms]] of $\mathcal{X}$ to [[vertical composition|vertically]] [[invertible morphism|invertible]] [[2-morphisms]] of $\mathcal{Y}$, of the form

\begin{tikzcd}
    X_1
    \ar[
      dd,
      "{ f }"{description}
    ]
    &
    F(x_1)
    \ar[
      dd,
      "F(f)"{description}
    ]
    \ar[
      rr,
      "{ \eta(x_1) }"{description}
    ]
    &&
    G(x_1)
    \ar[
      dd,
      "{ G(f) }"{description}
    ]
    \ar[
      ddll,
      shorten=15pt,
      Rightarrow,
      "{ \eta(f) }"{description}
    ]
    \\
    {}
    \ar[
      r,
      |->,
      shorten=15pt
    ]
    & {}
    \\
    x_2
    &
    F(x_2)
    \ar[
      rr,
      "{ \eta(x_2) }"{description}
    ]
    &&
    G(x_2)
\end{tikzcd}  

such that all the following [[equations]] hold among [[2-morphisms]] in $\mathcal{Y}$:

**(pseudo-naturality)**

for all [[2-morphisms]] in $\mathcal{X}$ 

\begin{tikzcd}
    x_1
    \ar[
      dd,
      bend left=50,
      "{ f }"{description, pos=.4, name=s}
    ]
    \ar[
      dd,
      bend right=50,
      "{ g }"{description, pos=.6, name=t}
    ]
    \ar[
      from=s, to=t,
      Rightarrow,
      "{ \alpha }"{description}
    ]
    \\
    \\
    x_2
\end{tikzcd}

we have

\begin{tikzcd}
    F(x_1)
    \ar[
      dd,
      bend left=50,
      "{ F(f) }"{description, pos=.4, name=s}
    ]
    \ar[
      dd,
      bend right=50,
      "{ F(g) }"{description, pos=.6, name=t}
    ]
    \ar[
      from=s, to=t,
      Rightarrow,
      "{ F(\alpha) }"{pos=1}
    ]
    \ar[
      rr,
      "{ \eta(x_1) }"{description}
    ]
    &&
    G(x_1)
    \ar[
      dd,
      bend left=50,
      "{ G(f) }"{description}
    ]
    \ar[
      ddll,
      Rightarrow,
      shorten=15pt,
      shift right=5pt,
      bend left=20,
      "{ \eta(f) }"{description}
    ]
    \\
    \\
    F(x_2)
    \ar[
      rr,
      "{ \eta(x_2) }"{description}
    ]
    &&
    G(x_2)
\end{tikzcd}
$$=$$
\begin{tikzcd}
    F(x_1)
    \ar[
      dd,
      bend right=50,
      "{ F(g) }"{description, pos=.6, name=t}
    ]
    \ar[
      rr,
      "{ \eta(x_1) }"{description}
    ]
    &&
    G(x_1)
    \ar[
      dd,
      bend left=50,
      "{ G(f) }"{description, pos=.4, name=s}
    ]
    \ar[
      dd,
      bend right=50,
      "{ G(g) }"{description, pos=.6, name=t}
    ]
    \ar[
      from=s, to=t,
      Rightarrow,
      "{ G(\alpha) }"{pos=1}
    ]
    \ar[
      ddll,
      Rightarrow,
      shorten=15pt,
      shift left=5pt,
      bend right=20,
      "{ \eta(g) }"{description}
    ]
    \\
    \\
    F(x_2)
    \ar[
      rr,
      "{ \eta(x_2) }"{description}
    ]
    &&
    G(x_2)
\end{tikzcd}


**(unitality)**

for all [[objects]] $x \in \mathcal{X}$ we have

  \begin{tikzcd}
    F(x)
    \ar[
      dd,
      bend left=50,
      "{ \mathrm{id}_{F(x)} }"{description, pos=.4, name=s}
    ]
    \ar[
      dd,
      bend right=50,
      "{ F(\mathrm{id}_x) }"{description, pos=.6, name=t}
    ]
    \ar[
      from=s, to=t,
      Rightarrow,
      "{ F_{\!\mathrm{e}}\!(x) }"{pos=.8}
    ]
    \ar[
      rr,
      "{ \eta(x) }"{description}
    ]
    \ar[
      ddrr,
      bend left=20,
      "{ \eta(x) }"{description, name=mid}
    ]
    &&
    G(x)
    \ar[
      dd,
      bend left=50,
      "{ \mathrm{id}_{G(x)} }"{description}
    ]
    \ar[
      from=mid,
      to=3-1,
      shorten=10pt,
      Rightarrow,
      bend left=20,
      shift right=3pt,
      "{
        \ell^{-1}
      }"
    ]
    \ar[
      from=1-3,
      to=mid,
      shorten=0pt,
      Rightarrow,
      bend left=20,
      shift right=-3pt,
      "{
        r
      }"
    ]
    \\
    & 
    \\
    F(x)
    \ar[
      rr,
      "{ \eta(x) }"{description}
    ]
    &&
    G(x)
  \end{tikzcd}
$$=$$
  \begin{tikzcd}
    F(x)
    \ar[
      dd,
      bend right=50,
      "{ F(\mathrm{id}_x) }"{description, pos=.6, name=t}
    ]
    \ar[
      rr,
      "{ \eta(x_1) }"{description}
    ]
    &&
    G(x)
    \ar[
      dd,
      bend left=50,
      "{ \mathrm{id}_{G(x)} }"{description, pos=.4, name=s}
    ]
    \ar[
      dd,
      bend right=50,
      "{ G(\mathrm{id}_x) }"{description, pos=.6, name=t}
    ]
    \ar[
      from=s, to=t,
      Rightarrow,
      "{ G_{\!\mathrm{e}}\!(x) }"{pos=.8}
    ]
    \ar[
      ddll,
      Rightarrow,
      shorten=15pt,
      shift left=5pt,
      bend right=20,
      "{ \eta(\mathrm{id}_x) }"{description}
    ]
    \\
    \\
    F(x)
    \ar[
      rr,
      "{ \eta(x_2) }"{description}
    ]
    &&
    G(x)
  \end{tikzcd}

**(associativity)**

for all pairs of composable [[1-morphisms]] $x_1 \xrightarrow{f} x_2 \xrightarrow{g} x_3$ in $\mathcal{X}$, we have

  \begin{tikzcd}[
    column sep=30pt
  ]
    F(x_1)
    \ar[
      dr,
      "{ F(f) }"{description}
    ]
    \ar[
      dd,
      "{ F(g \circ f) }"{sloped, swap}
    ]
    \ar[
      rr,
      "{ \eta(x_1) }"{description}
    ]
    &&[-23pt]
    G(x_1)
    \ar[
      dl,
      Rightarrow,
      shorten=8,
      "{ \eta(f) }"
    ]
    \ar[
      dr,
      "{ G(f) }"{description}
    ]
    \\
    {}
    & 
    F(x_2)
    \ar[
      dl,
      "{ F(g) }"{description}
    ]
    \ar[
      l,
      Rightarrow,
      "{ F(f,g) }"{description, pos=.45}
    ]
    \ar[
      rr,
      "{ \eta(x_2) }"{description}
    ]
    &&
    G(x_2)
    \ar[
      dlll,
      Rightarrow,
      shorten=65,
      "{ \eta(g) }"{pos=.52}
    ]
    \ar[
      dl,
      "{ G(g) }"{description}
    ]
    \\
    F(x_3)
    \ar[
      rr,
      "{ \eta(x_3) }"{description}
    ]
    &&
    G(X_3)
  \end{tikzcd}
$$=$$
  \begin{tikzcd}[
    column sep=30pt
  ]
    F(x_1)
    \ar[
      dd,
      "{ F(g \circ f) }"{sloped, swap}
    ]
    \ar[
      rr,
      "{ \eta(x_1) }"{description}
    ]
    &[+10pt]&
    G(x_1)
    \ar[
      ddll,
      Rightarrow,
      shorten=34pt,
      "{ \eta(g \circ f) }"
    ]
    \ar[
      dr,
      "{ G(f) }"{description}
    ]
    \ar[
      dd,
      "{ G(g \circ f) }"{description,sloped}
    ]
    \\
    & 
    &
    {}
    &
    G(x_2)
    \ar[
      dl,
      "{ G(g) }"{description}
    ]
    \ar[
      l,
      Rightarrow,
      "{ G(f,g) }"{description}
    ]
    \\
    F(x_3)
    \ar[
      rr,
      "{ \eta(x_3) }"{description}
    ]
    &&
    G(X_3)
  \end{tikzcd}

\end{definition}

Such a pseudonatural transformation is called a **pseudonatural equivalence** if each component $\eta(x)$ is an [[equivalence]] in the 2-category $C$.  This is equivalent to $\phi$ itself being an equivalence in the [[2-functor 2-category]] $[\mathcal{X},\mathcal{Y}]$ of [[2-functors]], pseudonatural transformations between these, and [[modifications]] between those.

## Related concepts

* [[homotopy]]

* [[transfor]]

  * [[natural transformation]]

    * [[dinatural transformation]], [[extranatural transformation]]

  * **pseudonatural transformation**

  * [[lax natural transformation]]

## References

* [[John W. Gray]], section I.4 of: _[[Adjointness for 2-Categories|Formal category theory: Adjointness for 2-categories]]_, Lecture Notes in Mathematics **391**, Springer (1974) &lbrack;[doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280)&rbrack; 

For review see most references at *[[2-category]]*, such as

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], §4.2 in: *2-Dimensional Categories*, Oxford University Press (2021) &lbrack;[arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378)&rbrack;

A generalization to [[extranatural transformations]]:

* Alexander S. Corner: _A universal characterisation of codescent objects_, Theory and Applications of Categories **34** 24 (2019) 684-713 &lbrack;[tac:34-24](http://tac.mta.ca/tac/volumes/34/24/34-24abs.html)&rbrack;

See also:

* [[Camell Kachour]]: *Définition algébrique des cellules non-strictes*, [[Cahiers]] de Topologie et de Géométrie Différentielle Catégorique **1** (2008) 1-68 &lbrack;[numdam:CTGDC_2008__49_1_1_0](https://www.numdam.org/item/?id=CTGDC_2008__49_1_1_0), [pdf](https://www.numdam.org/article/CTGDC_2008__49_1_1_0.pdf)&rbrack;

* [[Camell Kachour]]: *Steps toward the weak higher category of the weak higher categories in the globular setting*, Categories and General Algebraic Structures with Applications **4** 1 (2016) 9-42 &lbrack;[cgasa:11180](https://cgasa.sbu.ac.ir/article_11180.html), [pdf](https://cgasa.sbu.ac.ir/article_11180_b13cacfd9afe5780932141c269d0add6.pdf)&rbrack;

[[!redirects pseudonatural transformation]]
[[!redirects pseudonatural transformations]]
[[!redirects pseudo-natural transformation]]
[[!redirects pseudo-natural transformations]]
[[!redirects pseudo natural transformation]]
[[!redirects pseudo natural transformations]]
[[!redirects pseudonatural equivalence]]
[[!redirects pseudonatural equivalences]]
[[!redirects pseudo-natural equivalence]]
[[!redirects pseudo-natural equivalences]]
[[!redirects pseudo natural equivalence]]
[[!redirects pseudo natural equivalences]]
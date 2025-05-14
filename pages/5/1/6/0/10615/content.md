
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For all $n \in \{-2, -1, 0,1,2,3, \cdots\}$, [[truncated object in an (infinity,1)-category|$n$-truncation]] is a [[modality]] (in [[homotopy type theory]]).

## Definition

The following applies to [[dependent type theory]] with [[suspension types]] and [[localizations]], such as to standard [[homotopy type theory]].

Recall: 


\begin{definition}\label{SphereTypes}
**([[sphere type|$n$-sphere type]] $S^n$)**

* $S^{-1}$ is the [[empty type]],

* $S^0$ (the [[0-sphere]]) is the [[type of booleans]] [type](boolean+domain#InTypeTheory)

* $S^{n+1} \,\coloneqq\, \Sigma S^n$ is the [[suspension type]] of the sphere type of dimension lower.

\end{definition}

### As nullification of the $n+1$-sphere

The $n$-truncation modality may also be defined to be the [[localization of a type at a family of functions|localization at the unique function]] from the $(n + 1)$-dimensional sphere type (Def. \ref{SphereTypes}) to the [[unit type]] $S^{n + 1} \to \mathbb{1}$

$$\left[A\right]_n \coloneqq L_{S^{n + 1}}(A)$$

By definition, the type of functions $(\mathbb{1} \to \left[A\right]_n) \to (S^{n + 1} \to \left[A\right]_n)$ is an [[equivalence of types]]. 


### Explicit inference rules
 {#ExplicitInferenceRules}

The following are the [[inference rules]] for the $n$-truncation $[X]_n$ of a given $X \,\colon\, Type$ regarded as a [[higher inductive type]] according to [UFP13, §7.3, p. 223](#UFP13) (the [[diagram]] indicates the [[categorical semantics]], for orientation):


\begin{tikzcd}
  X
  \ar[
    d,
    "{ \eta }"
  ]
  \ar[
    rr,
    equals
  ]
  &[-130pt]
  &[-10pt]
  X
  \ar[
    d,
    "{ \eta_D }"
  ]
  &[-130pt]
  \\
  {
    [X]_n
  }
  \ar[ddd, equals]
  \ar[
    rr, 
    dashed,
    shift left=2pt,
    "{ 
       \mathrm{ind}_{
         (D,\, \eta_D,\, \mathrm{hub}_D,\, \mathrm{hmt}_D)
    } }"{description}
  ]
  &[-70pt]
  &[-10pt]
  D
  \ar[dddll]
  \\
  &[-70pt]
  &[-10pt]
  &[-70pt]
  \mathrm{Map}\big({S^{n+1}},\,{D}\big)
  \ar[
    ul,
    "{ \mathrm{hub}_D}"{sloped},
    "{\ }"{name=t2}
  ]
  &[+70pt]
  \\[+10pt]
  &&
  \mathrm{Map}\big({S^{n+1}},\,{D}\big) \times S^{n+1}
  \ar[
    ur,
    "{ \mathrm{pr}_1 }"{description}
  ]
  \ar[dddll]
  \ar[
    uu,
    bend left=50,
    gray,
    "{ \mathrm{ev} }"{pos=.6},
    "{\ }"{pos=.7, swap, name=s2}
  ]
  \\[-80pt]
  {
    [X]_n
  }
  \\
  & 
  \mathrm{Map}\big({S^{n+1}},\,{[X]_n}\big)
  \ar[
    ul,
    "{ \mathrm{hub}}"{sloped},
    "{\ }"{name=t}
  ]
  \ar[
    from=uuurr,
    shorten <=-6pt,
    crossing over
  ]
  \\[+10pt]
  \mathrm{Map}\big({S^{n+1}},\,{[X]_n}\big) \times S^{n+1}
  \ar[
    ur,
    "{ \mathrm{pr}_1 }"{description}
  ]
  \ar[
    uu,
    bend left=40,
    "{ \mathrm{ev} }"{pos=.6},
    "{\ }"{pos=.7, swap, name=s}
  ]
  \ar[
    from=s,
    to=t,
    Rightarrow,
    "{ \mathrm{hmt} }"{yshift=1pt,sloped},
  ]
  \ar[
    from=s2,
    to=t2,
    Rightarrow,
    gray,
    "{ \mathrm{hmt}_D }"{yshift=1pt,sloped},
  ]
\end{tikzcd}


\linebreak

**[[type formation rule]]:**

$$
  \frac{
     X \,\colon\, Type
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    [X]_n \,\colon\, Type
  }
$$

\linebreak


**[[term introduction rule]]:**

$$
  \frac{
    x \,\colon\, X
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    \eta_X(x) \,\colon\, [X]_n
  }
  \;\;\;\;\;\;\;\;\;
  \frac{
    \phi \,\colon\, S^{n+1} \to [X]_n
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    hub_X^{\phi} \,\colon\, [X]_n
  }
  \;\;\;\;\;\;\;\;\;
  \frac{
    \phi \,\colon\, S^{n+1} \to [X]_n  
    \;;
    \;\;\;
    s \,\colon\, S^{n+1}
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    hmt_X^{\phi}(s) 
     \,\colon\, 
    Id_{[X]_n}\big(
      \phi(s)
      ,\,
      hub_X^{\phi}
    \big)
  }
$$

\linebreak

{#TermElimination} **[[term elimination rules]]:**

$$
  \frac{
    \begin{array}{l}
      \overline{x} \,\colon\, [X]_n
      \;\vdash\;
      D(\overline{x}) \,\colon\, Type \;;
      \\
      x \,\colon\, X
      \;\vdash\;
      \eta_D(x) \,\colon\, D\big( \eta_X(x) \big)
      \;;
      \\
      \phi \,\colon\, S^{n+1} \to [X]_n
      \,,
      \;
      \phi_D 
        \,\colon\, 
      \underset{s \,\colon\,S^{n+1}}{\prod}
      \,
      D\big( \phi(s) \big)
      \;\;\vdash\;\;
      hub^{\phi_D}_D 
       \,\colon\,
      D\big( hub_X^\phi \big)
      \;;
      \\
      \phi \,\colon\, S^{n+1} \to [X]_n
      \,,
      \;
      \phi_D 
        \,\colon\, 
      \underset{s \,\colon\,S^{n+1}}{\prod}
      \,
      D\big( \phi(s) \big)
      \,,
      \;
      s \,\colon\, S^{n+1}
      \;\;\vdash\;\;
      hmt_D^{\phi_D}(s)
        \,\colon\, 
      Id_{D\big(hub_X^{\phi}\big)}\Big(
        \big(hmt^{\phi}_X(s)\big)_\ast
        \phi_D(s)
        ,\,
        hub_D^{\phi_D}
      \Big)
      \mathclap{\phantom{\vert^{\vert^{\vert}}}}
    \end{array}
  }{
    \mathclap{\phantom{\vert^{\vert_{\vert}}}}
    ind_{\big(D,\,\eta_D,\, hub_D,\, hmt_D \big)}
    \,\colon\,
    \underset{\overline{x}\colon [X]_n}{\prod}
    \,
    D(\overline{x})
  }
$$

\linebreak

**[[computation rule]]:**

$$
  ind_{\big(D,\,\eta_D,\, hub_D,\, hmt_D \big)}
  \big(
    \eta(x)
  \big)
  \;=\;
  \eta_D(x)
$$

\linebreak




## Properties

### In low degree

$(-2)$-truncation is the [[unit type]] modality ([[constant map|constant]] on the unit type).

$(-1)$-truncation is given by forming _[[bracket types]]_, turning types into genuine [[propositions]]. 

[[classical logic|Classically]], this is the same as the [[double negation modality]]; in general, the bracket type ${\|A\|_{-1}}$ only entails the double negation $\neg(\neg{A})$:
there is a canonical [[function]]

$$
  {\|A\|_{-1}} \longrightarrow \neg(\neg{A})
$$

and this is a [[1-epimorphism]] precisely if the [[law of excluded middle]] holds.


## Related concepts

* [[decategorification]], [[core]]

* [[cone type]], [[bracket type]], [[set truncation]]

[[!include homotopy n-types - table]]


## References
 {#References}

Construction of $n$-truncation as a one-step [[higher inductive type]] in [[homotopy type theory]]:

* {#UFP13} [[Univalent Foundations Project]], §6.9 & §7.3 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

Alternative construction of $n$-truncation as an iterated [[pushout type]] is (somewhat implicit) in:

* {#Rijke19b} [[Egbert Rijke]], Section 7.2 (culminating in Thm. 7.2.10) of: _Classifying Types_ &lbrack;[arXiv:1906.09435](https://arxiv.org/abs/1906.09435)&rbrack;


Discussion of $n$-truncation as a [[modality]]:

* {#RSS20} [[Egbert Rijke]], [[Mike Shulman]], [[Bas Spitters]], Exp. 1.6 in: *Modalities in homotopy type theory*,  Logical Methods in Computer Science, **16** 1 (2020)  &lbrack;[arXiv:1706.07526](https://arxiv.org/abs/1706.07526), <a href="https://doi.org/10.23638/LMCS-16(1:2)2020">doi:10.23638/LMCS-16(1:2)2020</a>&rbrack;

and in addition via [[lifting properties]] against [[n-spheres]]:

* [[Felix Cherubini]], [[Egbert Rijke]], Thm. 3.10 in: *Modal Descent*, Mathematical Structures in Computer Science **31** 4 (2021) 363-391  &lbrack;[arXiv:2003.09713](https://arxiv.org/abs/2003.09713), [doi:10.1017/S0960129520000201](https://doi.org/10.1017/S0960129520000201)&rbrack;

Earlier discussion (and in view of [[homotopy levels]]):

* [[Nicolai Kraus]], Def. 2.3.8 in: *Truncation levels in Homotopy Type Theory*, Nottingham (2015) &lbrack;[pdf](https://eprints.nottingham.ac.uk/28986/1/thesis.pdf), [eprints:28986](https://eprints.nottingham.ac.uk/28986)&rbrack;

Precursor discussion of the material that became [UFP (2013, §7.3)](#UFP13):

* [[Peter LeFanu Lumsdaine]], *Reducing all HIT's to 1-HIT's* (May 2012) &lbrack;[blog posy](https://homotopytypetheory.org/2012/05/07/reducing-all-hits-to-1-hits/)&rbrack;

* [[Guillaume Brunerie]], *Truncations and higher inductive types* (September 2012) &lbrack;[blog post](http://homotopytypetheory.org/2012/09/16/truncations-and-truncated-higher-inductive-types/)&rbrack; 

and precursur discussion of the material that became [RSS (2020)](#RSS20):

* {#Shulman12} [[Mike Shulman]], _Higher modalities_, talk at [[UF-IAS-2012]] (October 2012)  &lbrack;[pdf](https://ncatlab.org/ufias2012/files/modalitt.pdf)&rbrack;

* [[Mike Shulman]], *All modalities are Higher Inductive Types* (November 2012) &lbrack;[blog post](http://homotopytypetheory.org/2012/11/19/all-modalities-are-hits/)&rbrack; 

Considering the combination of $n$-truncation modality and [[shape modality]]:

* [[David Jaz Myers]], Def. 3.0.1 in: *Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory* ([arXiv:2205.15887](https://arxiv.org/abs/2205.15887))


[[!redirects n-truncation modality]]
[[!redirects n-truncation modalities]]

[[!redirects truncation modality]]
[[!redirects truncation modalities]]

[[!redirects n-truncated type]]
[[!redirects n-truncated types]]




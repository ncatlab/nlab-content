
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[morphism]] is said to have the *homotopy extension property* if [[homotopies]] out of its [[domain]] [[extension|extend]] to [[homotopies]] out of its [[codomain]].

More in detail, given a [[category]] with a concept of [[path space object]] and hence of [[right homotopy]], then a [[morphism]] $i \colon A \longrightarrow B$ is said to have the _right homotopy extension property_ with respect to an [[object]] $X$ if it has the [[left lifting property]] against one of the two path endpoint evaluation maps $p_0 \colon Path(X) \longrightarrow X$, i.e. if in every [[commuting square]] as below, a diagonal lift exists:

$$
  \array{
    A &\longrightarrow& Path(X)
    \\
    {}^{\mathllap{i}}\downarrow &{}^{\mathllap{\exists}}\nearrow& \downarrow^{\mathrlap{p_0}}
    \\
    B &\longrightarrow& X
  }
  \,.
$$

Here the top morphism exhibits a [[right homotopy]] between two morphisms $A\to X$, and the diagonal filler is an [[extension]] of the top morphism along $i$ and exhibiting a compatible right homotopy between morphisms $B\to X$, whence the terminology.

The concept of homotopy extension property is the [[Eckmann-Hilton duality|Eckmann-Hilton dual]] of that of (left) _[[homotopy lifting property]]_, where instead one considers the presence of a [[cylinder object]], hence a notion of [[left homotopy]], and lifting in diagrams of the form

$$
  \array{
    A &\longrightarrow& X
    \\
    {}^{\iota_0}\downarrow &{}^{\mathllap{\exists}}\nearrow& \downarrow^{f}
    \\
    Cyl(A) &\longrightarrow& Y
  }
  \,.
$$

In situations where both [[path space objects]] as well as [[cylinder objects]] exist and are compatible, so that the concepts of left and right homotopy coincide, one may equivalently rephrase right homotopy extension in terms of left homotopy (and left homotopy lifting in terms of right homotopy). 

The resulting definition is necessarily less transparent (def. \ref{LeftHomotopyExtensionPropertyInTop} below), but it happens to be more commonly used in the literature.
Specifically in the archetypical case that the ambient category is that of [[topological spaces]] and cylinders and path space objects are induced from the standard topological [[interval object]], a _[[Hurewicz cofibration]]_ (often just called _cofibration_ ) is a [[continuous function]] that satisfies the left homotopy extension property with respect to all topological spaces.


## Definition

### In topological spaces

\begin{definition}\label{LeftHomotopyExtensionPropertyInTop}
**(homotopy extension property for left homotopies in topological spaces)**
\linebreak
A [[continuous function]] $i \colon A \xrightarrow{\;} X$ of [[topological spaces]] is said to satisfy the (left) **homotopy extension property** (HEP) with respect to a space $Y$ if 

* for any map $f \colon X \longrightarrow Y$ and any [[left homotopy]] $\eta \,\colon\,  A \times [0,1] \longrightarrow Y$ such that $\eta(-,0) = f \circ i$, there exists a [[left homotopy]] $\widehat{\eta} \,\colon\,  X \times [0,1] \longrightarrow Y$ such that $\widehat{\eta} \circ (i \times id) = \eta$;

equivalently:

* given a [[commuting diagram]] in [[Top|TopSp]] of solid arrows as shown below, there exists a dashed arrow $\widehat \eta$ making all sub-diagrams commute:

\begin{tikzcd}[column sep={between origins, 40pt}]
    A
    \ar[
      dd,
      "{i}"{left}
    ]
    \ar[
      rr,
      "{(\mathrm{id},\, 0)}"
    ]
    &&
    A \times [0,1]
    \ar[
      dd,
      "{ i \times \mathrm{id} }"{right}
    ]
    \ar[
      dl,
      "{\eta}"{left, yshift=3pt}
    ]
    \\
    &
    Y
    \\
    X
    \ar[
      rr,
      "{ (\mathrm{id},\, 0) }"{below}
    ]
    \ar[
      ur,
      "{f}"
    ]
    &&
    X \times [0,1]
    \ar[
      ul,
      dashed,
      "{ \widehat \eta }"{description}
    ]
\end{tikzcd}
 

The map $f$ is sometimes said to be the _initial condition_ of a _homotopy extension problem_ and $\widehat{\eta}$ is called the [[extension]] of the homotopy $\eta$ subject to that initial condition. 

The map $i$ is called a **[[Hurewicz cofibration]]** if it satisfies this homotopy extension property with respect to all spaces $Y$.
\end{definition}

\begin{remark}
**(re-formulation in terms of right homotopies)**
\linebreak
In a [[convenient category of topological spaces|convenient]] [[cartesian closed category]] $TopSp$ of [[topological spaces]] (such as that of [[compactly generated topological spaces]]) the [[product]] $\dashv$ [[internal hom]]-[[adjunction]]

$$
  TopSp
    \underoverset
    {\underset{ (-)^{[0,1]} }{\longrightarrow}}
    {\overset{ (-) \times [0,1]  }{\longleftarrow}}
    {\;\;\;\;\;\bot\;\;\;\;\;}
  TopSp
$$

allows to pass to [[adjunct]] morphisms in Def. \ref{LeftHomotopyExtensionPropertyInTop} 

$$
  \array{
    TopSp
    \big(
      A \times [0,1]
      ,\,
      Y
    \big)
    &\simeq&
    TopSp
    \big(
      A
      ,\,
      Y^{[0,1]}
    \big)
    \\
    \eta &\leftrightarrow& \eta'
  }
$$

and equivalently express the above diagram of [[left homotopies]] as the following (somewhat more transparent) diagram of [[right homotopies]], where $ev_0 \,\colon\, Y^{[0,1]}\to Y$ denotes [[evaluation]] at 0 $\gamma \mapsto \gamma(0)$:


\begin{tikzcd}
    A
    \ar[
      d,
      "{i}"{left}
    ]
    \ar[
      r,
      "{ \eta' }"{above}
    ]
    &
    Y^{[0,1]}
    \ar[
      d,
      "\mathrm{ev}_0"
    ]
    \\
    X
    \ar[
      r,
      "{f}"{below}
    ]
    \ar[
      ur,
      dashed,
      "\widehat \eta'"{description}
    ]
    &
    Y
\end{tikzcd}



In this equivalent formulation, the homotopy extension property is simply the [[right lifting property]] against the [[evaluation]] map $ev_0 \;\colon\; Y^{[0,1]} \xrightarrow{\;} Y$ out of the [[path space]] of $Y$.
\end{remark}

(e.g. [May 1999, p. 43](#May99))


## Properties

### Closure

+-- {: .num_prop}
###### Proposition

If a map $i\colon A\to X$ has the homotopy extension property with respect to a space $Y$, then for any map $g \colon A\to Z$, the [[pushout]] $g_*(i)=i\amalg_A Z :Z\to X\amalg_A Z$ has the homotopy extension property with respect to the space $Y$. 

=--

This is a general statement about classes of morphisms defined by a [[left lifting property]], see at _[injective and projective morphisms -- closure properties](injective+or+projective+morphism#ClosureProperties)_

+-- {: .proof}
###### Proof

We would like to find $\tilde{F}$ to complete the commutative diagram 

$$
  \array{
    A &\stackrel{g}\to&Z&\stackrel{f}\to& Y^I
    \\
    \downarrow^{i}&&\downarrow^{g_*(i)} &\nearrow {\tilde{F}}&  \downarrow^{ev_0}
    \\
    X&\stackrel{i_*(g)}\to&X\amalg_A Z&\stackrel{F}{\to}& Y
  }
  \,.
$$

Consider the external square obtained by composing the horizontal arrows:

$$
  \array{
    A &\stackrel{f\circ g}\to& Y^I
    \\
    \downarrow^{i} &\nearrow {\exists\tilde{G}}&  \downarrow^{ev_0}
    \\
    X&\stackrel{F\circ i_*(g)}{\to}& Y
  }
  \,.
$$

By the assumption on $i$, there is a $\tilde{G}$ as in the diagram, such that both triangles commute, i.e. $ev_0\circ\tilde{G}=F\circ i_*(g)$ and $\tilde{G}\circ i = \tilde{F}\circ g$.

If $i:A\to X$ is satisfying the HEP with respect to $Y$ then there is a diagonal in that external square which is some map $\tilde{G}:X\to Y^I$. This map together with $f:Z\to Y^I$, by the universal property of pushout, determines a unique map $\tilde{F}:X\amalg_A Z\to Y^I$ such that $\tilde{F}\circ i_*(g)=\tilde{G}$ and $\tilde{F}\circ g_*(i)=f$. We need to show only that 
$ev_0\circ\tilde{F}=F$ as $\tilde{F}\circ g_*(i)=f$ holds by the construction of $\tilde{F}$ as stated.

By the definition of $\tilde{G}$ and the commutativity of the original double square diagram, $ev_0\circ \tilde{F}\circ i_*(g)=ev_0\circ\tilde{G}=F\circ i_*(g)$ and $ev_0\circ \tilde{F}\circ g_*(i)=ev_0\circ f=F\circ g_*(i)$. This is almost what we wanted except that we precompose the wanted identity with both maps into the pushout. Thus by the uniqueness part of the universal property of pushout it follows that $ev_0\circ\tilde{F}=F$.
=--


## Literature

Textbook accounts:

* {#May99} [[Peter May]], Section 6.1 of: *[[A concise course in algebraic topology]]*, University of Chicago Press 1999 ([ISBN: 9780226511832](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

* {#Hatcher02} [[Allen Hatcher]], p. 14-17 in: *Algebraic Topology*, Cambridge University Press 2002 ([ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html))


See also:

* Wikipedia, *[Homotopy extension property](https://en.wikipedia.org/wiki/Homotopy_extension_property)*

[[!redirects h-cofibration]]
[[!redirects h-cofibrations]]


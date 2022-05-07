
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
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

In [[algebraic topology]] and [[homotopy theory]],
*Hurewicz cofibrations* are a kind of [[cofibration]] of [[topological spaces]], hence a kind of [[continuous function]] satisfying certain [[extension]] properties. 

Specifically, a [[continuous function]] is a _Hurewicz cofibration_ if it satisfies the [[homotopy extension property]] for all target spaces and with respect to the standard notion of [[left homotopy]] of topological spaces given by the standard topological [[interval object]]/[[cylinder object]].


In [[point-set topology]] Hurewicz cofibrations are often just called _cofibrations_,for short. If their [[image]] is a [[closed subspace]] they are called _[[closed cofibrations]]_. 

Beware that there are other relevant classes of cofibrations between topological spaces, notably the *[[Serre cofibrations]]*, and (in [[homotopy theory]] and [[model category]]-theory, at least) also often just called "cofibrations". But "closed cofibration" always refers to closed Hurewicz cofibrations.

In fact, the notion of [[homotopy extension property]] makes sense in any [[category]] with a chosen [[cylinder object]]; and in this generality one also speaks of *[[h-cofibrations]]*.


## Definition
 {#Definition}




\begin{definition}\label{HurewiczCofibration}
**(Hurewicz cofibration)**
\linebreak
A map ([[continuous function]]) $i \colon A \xrightarrow{\;} X$ betwee [[topological spaces]] is a *Hurewicz cofibration* if it satisfies the [[homotopy extension property]] for all spaces, hence if

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

allows to pass to [[adjunct]] morphisms in Def. \ref{HurewiczCofibration} 

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

(e.g. [May 1999, p. 43 (51 of 251)](#May99))

\begin{definition}\label{ClosedHurewiczCofibration}
**(closed cofibrations)**
\linebreak
A Hurewicz cofibration $i \colon A\to X$ (Def. \ref{HurewiczCofibration}) is called a _[[closed cofibration]]_ if the [[image]] $i(A)$ is a [[closed subspace]] in $X$. In this case the pair $(A,X)$ is also called an *[[NDR-pair]]*.
\end{definition}



## Properties

### Subspace inclusions
 {#Inclusions}


\begin{proposition}\label{CharacterizationViaRetractionOfPushoutProduct}
  A [[closed subset|closed]] [[topological subspace]]-inclusion $A \xhookrightarrow{\;} X$ is a Hurewicz cofibration precisely if its [[pushout product]] with the endpoint inclusion $\{0\} \xhookrightarrow{\;} [0,1]$ into the [[topological interval]]
\[
  \label{PushoutProductMap}
  X \times \{0\}
  \cup
  A \times [0,1]
  \xrightarrow{\;\;}
  X \times [0,1]
\]
admits a [[retraction]].
\end{proposition}
(e.g. [May 1999, Sec. 6.4, p. 45 (53 of 251)](#May99); [Gutiérrez, Prop. 8.3](#Gutierrez))


\begin{example}\label{KifiedProductsOfCofibrationsWithCompactlyGeneratedSpaces}
  Let $A \xhookrightarrow{i} X$ be a [[closed subset|closed]] [[topological subspace]]-inclusion of [[compactly generated topological spaces]] which is a Hurewicz cofibration. Then for $Y$ any [[compactly generated topological space]], the [[k-ification|k-ified]] [[product space]]-construction $Y \times A \xhookrightarrow{ id_Y \times i  } Y \times X$ is itself a Hurewicz cofibration.
\end{example}
\begin{proof}
  Since [[compactly generated spaces]] with the k-ified product space construction form a [[cartesian closed category]], the operation $Y \times (-)$ is a [[left adjoint]] and [[left adjoints preserve colimits|hence]] [[preserved colimit|preserves]] the [[pushout]] in (eq:PushoutProductMap). It follows that the retract which exhibits, according to Prop. \ref{CharacterizationViaRetractionOfPushoutProduct}, the cofibration property of $i$, may be extended as a [[constant function]] in $Y$ to yield a retract that exhibits the cofibration property of $Y \times i$.
\end{proof}

+-- {: .num_cor}
###### Corollary

A subcomplex inclusion into a [[CW-complex]] is a closed Hurewicz cofibration.

=--

By Prop. \ref{CharacterizationViaRetractionOfPushoutProduct}, see e.g. Bredon _Topology and Geometry_, p. 431.


More generally, every [[retract]] of a [[relative cell complex]] inclusion is a closed Hurewicz cofibration. 

This is part of the statement of the [[Quillen adjunction]] between then [[classical model structure on topological spaces]] and the [[Strøm model structure]] (see [below](#StromModelStructure))

### Closedness
 {#Closedness}


\begin{prop}
Every Hurewicz cofibration $i$ is [[injective function|injective]] and a [[homeomorphism]] onto its image.
\end{prop}

([Homotopietheorie](#Homotopietheorie) (1.17)). 

\begin{prop}\label{HurewiczCofibrationsInCGWHSpacesAreClosed}
In the category of [[weakly Hausdorff space|weakly Hausdorff]] [[compactly generated spaces]], the image $i(A)$ of a Hurewicz cofibration is always closed.
The same holds in the category of all [[Hausdorff spaces]].
\end{prop}

(e.g. [May 1999, Sec. 6.2, p. 44 (52 of 251)](#May99))

But in the plain category [[Top]] of all topological spaces there are pathological counterexamples. 

The simplest example (see [Homotopietheorie](#Homotopietheorie)) is the following: let $A =\{a\}$ and $X=\{a,b\}$ be the one and two element sets, both with the [[codiscrete topology]] (only $X$ and $\emptyset$ are open in $X$), and $i:A\hookrightarrow X$ is the inclusion $a\mapsto a$. Then $i$ is a non-closed cofibration (useful exercise!). 



### Str&#248;m's model structure
 {#StromModelStructure}

The collections

* [[Hurewicz fibrations]],

* closed Hurewicz cofibrations (def. \ref{HurewiczCofibration}, def. \ref{ClosedHurewiczCofibration}),

* and [[homotopy equivalences]] 

make one of the standard Quillen [[model category]] structures on the category [[Top]] of all topological spaces _[[Strøm's model category]]. 

The identity functor $id \colon Top \to Top$ is [[Quillen adjunction|left Quillen]] from the [[classical model structure on topological spaces]] (or the mixed model structure) to the Str&#248;m model structure, and of course right Quillen in the other direction.  

$$
  Top_{Strom}
    \stackrel{\overset{id}{\longleftarrow}}{\underset{id}{\longrightarrow}}
  Top_{Quillen}
  \,.
$$

This means in particular that any  [[retract]] of a  [[relative cell complex]] inclusion is a closed Hurewicz cofibration.


### Interaction with pullbacks
 {#InteractionWithPullbacks}

+-- {: .num_theorem}
###### Theorem

Let

$$
  \array{
     X_0 &\hookrightarrow & X
     \\
     {}^{\mathllap{p_0}}\downarrow && \downarrow^{\mathrlap{p}}
     \\ 
     B_0 &\hookrightarrow& B
     \\
     \uparrow && \uparrow
     \\
     E_0 &\hookrightarrow& E
  }
$$

be a [[commuting diagram]] of [[topological space]]s such that

* the horizontal morphisms are closed cofibrations;

* the morphisms $p_0$ and $p$ are [[Hurewicz fibration]]s.

Then the induced morphism on [[pullback]]s is also a closed cofibration

$$
  X_0 \times_{B_0} E_0 \hookrightarrow X \times_B E
  \,.
$$ 

=--

This is stated and proven in ([Kieboom](#Kieboom)).

+-- {: .num_cor}
###### Corollary

The [[product]] of two closed cofibrations is a closed cofibration.

=--

## References

Named after *[[Witold Hurewicz]]*.

Original articles:

* [[Dieter Puppe]], _Bemerkungen &#252;ber die Erweiterung von Homotopien_, Arch. Math. (Basel) 18 1967 81--88; MR0206954 (34 #6770) [doi](http://dx.doi.org/10.1007/BF01899475)

* [[Arne Strøm]], _Note on cofibrations_,  Math. Scand.  19  1966 11--14 [file](http://www.mscand.dk/article.php?id=1782) MR0211403 (35 #2284); _Note on cofibrations II_,  Math. Scand.  22  1968 130--142 (1969) [file](http://www.mscand.dk/article.php?id=1867) MR0243525 (39 #4846) 

Textbook accounts:

* {#Homotopietheorie} [[Tammo tom Dieck]], [[Klaus Heiner Kamps]], [[Dieter Puppe]], *Homotopietheorie* Lecture Notes in Mathematics **157** Springer 1970 ([doi:10.1007/BFb0059721](https://link.springer.com/book/10.1007/BFb0059721))

* {#May99} [[Peter May]], Chapter 6 of: *[[A concise course in algebraic topology]]*, University of Chicago Press 1999 ([ISBN: 9780226511832](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

Lecture notes:

* {#Gutierrez} [[Javier Gutiérrez]], *Cofibrations*, ([pdf](https://www.math.ru.nl/~gutierrez/files/Lecture08.pdf), [[Gutierrez_Cofibrations.pdf:file]])

The fact that morphisms of fibrant pullback diagrams along closed cofibrations induce closed cofibrations is in

* {#Kieboom} [[Rudger Kieboom]], _A pullback theorem for cofibrations_, Manuscripta Math **58** (1987) pp 381–384, doi:[10.1007/BF01165895](https://doi.org/10.1007/BF01165895)


[[!redirects Hurewicz cofibrations]]

[[!redirects closed cofibration]]
[[!redirects closed cofibrations]]

[[!redirects closed Hurewicz cofibration]]
[[!redirects closed Hurewicz cofibrations]]

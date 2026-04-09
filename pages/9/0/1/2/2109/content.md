+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--




\tableofcontents


## Idea

A **2-category equipped with proarrows**, also called a *proarrow equipment* or simply an *equipment*, is a [[2-category]] equipped with a notion of "proarrows" which enable one to reproduce more [[category theory]] inside it (cf. *[[formal category theory]]*) than is possible in a general [[2-category]]. The ur-example is [[Cat]] equipped with [[profunctors]].

See also at *[[framed bicategory]]*.


## Motivation

Just as ordinary [[category theory]] provides a framework in which one can do "formal mathematics," one of the (many) purposes of [[higher category theory]] is to provide a framework in which one can do [[formal category theory]]. In particular, many concepts in ordinary category theory can be interpreted internally in a [[2-category]], in a way which specializes to the original concept in [[Cat]].  Examples of such concepts include [[adjunctions]], [[monads]], [[Grothendieck fibrations]], [[Kan extensions]], and [[fully faithful morphisms]].

However, these internalizations are not always "correct" in every 2-category. For instance, in the 2-category $V Cat$ of [[enriched categories|categories enriched]] in a [[monoidal category]] $V$, internal adjunctions and monads give the correct notion of a $V$-adjunction and a $V$-monad, but internal fully-faithfulness for a $V$-functor is weaker than the "correct" notion of $V$-fully-faithfulness. More technically, in many cases the naive notion of a Kan extension is not sufficient and one needs "pointwise" Kan extensions; with some more work, these can also be defined in a 2-category, but the resulting notion (though correct in $Cat$) is not always correct in $V Cat$.

Furthermore, some concepts of category theory are difficult to interpret at all in a 2-category. The notion of a [[limit]] in ordinary category theory can be interpreted in a 2-category by identifying the limit of a functor $D\to C$ as its Kan extension along the unique functor $D\to *$.  However, in enriched category theory, the more important notion is that of a [[weighted limit]], and there is no straightforward way to interpret this in $V Cat$.

What is missing is that the 2-category $V Cat$ doesn't natively supply any information about the $V$-valued hom-functors in a 2-category. (In $Cat$ these hom-functors can be recovered by looking at [[comma categories]], which can be interpreted internally as [[comma objects]]---in some sense this is what all the above internalizations are secretly doing.) Thus, all of these problems can be remedied by equipping a 2-category with extra structure which describes these hom-functors, or more generally describes a notion of a [[profunctor]].

There are several not-quite-equivalent ways to describe this extra structure. One due to Street and Walters, called a [[Yoneda structure]], involves assigning to each object $A$ a "presheaf object" $P A$ and a "Yoneda arrow" $A\to P A$; a profunctor $A\to B$ is then identified with an arrow $B \to P A$. The notion of a *proarrow equipment*, due to Wood, instead postulates an additional bicategory of "proarrows" and specifies their relationship to the ordinary arrows. One can then define fully faithful morphisms, pointwise Kan extensions, weighted limits, etc. relative to this structure, in a way which specializes to the correct notions in $V Cat$.

## Definitions 
 {#Definitions}

We give several equivalent definitions of proarrow equipments:

1. [as 2-functors](#DefinitionAsA2Functor) which are bijective on objects, locally fully faithful, and map every 1-morphism to one having a right adjoint,

1. [as double categories](#DefinitionAsDoubleCategory) in which 

   1. [every vertical arrow has a companion and a conjoint](#CharacterizationViaCompanionsAndConjoints),

   1. [every niche has a cartesian filler](#CharacterizationViaCartesianNicheFillers),

1. [as categories internal to $Cat$](#AsInternalCategories).

Here, the first definition is perhaps the simplest or most immediate.  

But for some purposes the second definition is preferable: For instance, the definition of the [[3-category]] of "2-categories equipped with proarrows" is much more naturally defined by viewing them as double categories (cf. [Verity 2011](#Verity2011) and [Shulman 2008](#Shulman2008)). The perspective of double categories also generalizes better to situations in which not all proarrows have composites; see on *[[virtual equipments]]* [below](#VirtualEquipments).


### As 2-functors
 {#DefinitionAsA2Functor}
 
\begin{definition}
  \label{TheDefinitionAsA2Functor}
Let $K$ be a [[2-category]].  The following structure is said to **equip $K$ with proarrows**.

* A [[2-category]] $M$, whose [[1-morphisms]] are called *proarrows*.

* A [[2-functor]] $K\to M$ which is [[bijective-on-objects functor|bijective on objects]] and [[locally fully faithful 2-functor|locally fully faithful]].  If $f\colon A\to B$ is a 1-morphism in $K$, we write its image in $M$ as $B(1,f)\colon A\nrightarrow B$.

* For each [[1-morphism]] $f\colon A\to B$ in $K$, the proarrow $B(1,f)\colon A\to B$ has a [[right adjoint]] in $M$, which we write as $B(f,1)$.

\end{definition}

> As usual on the nLab, here by *[[2-categories]]* we mean *weak 2-categories (aka *[[bicategories]]*) and by *[[2-functors]]* we mean weak 2-functors (aka *[[pseudofunctors]]*).  However, in many or most examples, $K$ is in fact a [[strict 2-category]].

For a proarrow $H\colon B\to D$ and ordinary arrows $f\colon A\to B$ and $g\colon C\to D$, we write $H(g,f)$ for the composite 
\[ 
  A 
    \xrightarrow{B(1, f)} 
  B 
    \xrightarrow{H} 
  D 
    \xrightarrow{D(g, 1)} 
  C
  \mathrlap{\,.} 
\]
We also write $U_A$, $A(1,1)$, or simply $A$ for the identity proarrow $A\nrightarrow A$.  

\begin{remark}
In the case where proarrows are [[profunctors]], $H(g, f)$ is not the action on a set of [[heteromorphisms]] by pre- and post- composing with morphisms; instead it is the functor $f$, followed by the profunctor $H$, followed by taking the preimage under the functor $g$, resulting in a profunctor from $A$ to $C$.
\end{remark}



\begin{remark}
**(terminology)**

We refer to the entire structure defined above as a **2-category equipped with proarrows** or a **2-category proarrow equipment**.  Those working in the field often use the term **proarrow equipment** or simply **equipment** for the entire structure.  We prefer "2-category equipped with proarrows" (or, equivalently, "pro-morphisms") for the following reasons:

* It conveys that we are talking about extra stuff added to a 2-category.  (Actually, it is "eka-stuff" or "2-stuff" in the sense of [stuff, structure, property](http://ncatlab.org/nlab/show/stuff,+structure,+property).)
* It includes the word "proarrow" which tells people what the extra stuff consists of, namely a generalization of [[profunctors]].
* It includes the word "equipment" which signals what is meant to readers who are familiar with that term.

We do sometimes avail ourselves of the shorter terminology "proarrow equipment," however, once we are clear what is under discussion.
\end{remark}


\begin{example}
For $V$ is a [[Bénabou cosmos]], the [[2-category]] [[V Cat|$K= V Cat$]] of $V$-[[enriched categories]] is equipped with proarrows by the 2-category $M=V Mod$ of $V$-[[enriched profunctors]], where $B(1,f)$ and $B(f,1)$ are the two ways of regarding a $V$-functor $f \colon A\to B$ as a profunctor, namely $B(-,f-)$ and $B(f-,-)$ (hence the notation in the general case).  Composition of $V$-profunctors is by [[tensor product]], i.e. by [[coends]] (note that we require $V$ to be [[cocomplete category|cocomplete]] with colimits preserved by $\otimes$ on both sides in order to form such associative tensor products).  In [[V Cat|$V Cat$]], $H(g,f)$ is the result of [[precomposition|precomposing]] the profunctor $H:D^{op}\otimes B \to V$ with $g^{op}\otimes f$.
\end{example}

\begin{example}
The other most common sorts of generalized category, such as [[internal categories]] in some category with [[pullbacks]], and [[fibered categories]] over some base, are also naturally equipped with proarrows.  For [[internal categories]] in $S$, we require $S$ to have [[finite limits]] and [[coequalizers]] [[preserved limit|preserved]] by [[pullback]] in order for the bicategory of [[internal profunctors]] to have [[associativity|associative]] [[compositions]].  (See on *[[virtual equipments]]* [below](#VirtualEquipments), for a context which avoids some of these restrictions on $V$ and $S$.)
\end{example}




### As double categories
  {#DefinitionAsDoubleCategory}

We discuss now how a 2-category with proarrow equipment is equivalently a [[double category]] with [[extra structure]]. 

\begin{definition}\label{TheAssociatedDoubleCategory}
Given a [[2-category]] $K$ equipped with proarrows according to Def. \ref{TheDefinitionAsA2Functor}, we can construct a [[double category]] having the same [[objects]] as $K$, whose [[vertical 1-cells]] are the arrows, whose [[horizontal 1-cells]] are the proarrows, and whose squares
\begin{tikzcd}
  A
  \arrow[r,  "H", ""{name=U, below}]
  \arrow[d, "f"']
  & C
  \arrow[d, "g"]
  \\
  B
  \arrow[r, "J"', ""{name=D, above}]
  & D
  \arrow[Rightarrow, from=U, to=D, "\alpha"]
\end{tikzcd}
are the [[2-cells]] $H \to J(g,f)$.  
\end{definition}

\begin{remark}

Dually, the 2-cells can be also represented as [[string diagram|string diagrams]] ([Myers 2016](#Myers16)).

\begin{tikzpicture}[scale=2, >=latex]
  \usetikzlibrary{decorations.markings}
\tikzset{mid->/.style={
  decoration={markings, mark=at position 0.6 with {\arrow[scale=1.5]{>}}},
  postaction={decorate}
}}

  % Quadrant fills (centered at origin)
  \fill[blue!15]   (-1,0) rectangle (0,1);
  \fill[teal!20]   (0,0) rectangle (1,1);
  \fill[orange!20] (-1,-1) rectangle (0,0);
  \fill[violet!15] (0,-1) rectangle (1,0);

  % Border
  \draw[gray] (-1,-1) rectangle (1,1);

  % Central node
  \node[circle,draw,fill=white,inner sep=1.5pt] at (0,0) (alpha) {$\alpha$};

  % Arrows
  \draw[line width=0.6pt] (-1,0) -- (alpha);
  \draw[line width=0.6pt] (alpha) -- (1,0);
  \draw[mid->, line width=0.6pt] (alpha) -- (0,-1);
  \draw[mid->, line width=0.6pt] (0,1) -- (alpha);

  % Labels
  \node[left]  at (-1,0) {$H$};
  \node[right] at (1,0)  {$J$};
  \node[above] at (0,1)  {$f$};
  \node[below] at (0,-1) {$g$};
  \node at (-0.5, 0.5) {$A$};
  \node at ( 0.5, 0.5) {$B$};
  \node at (-0.5,-0.5) {$C$};
  \node at ( 0.5,-0.5) {$D$};
\end{tikzpicture}
\end{remark}
\begin{remark}
If $K$ is a [[strict 2-category]], then this is a [[pseudo double category]] (vertically strict and horizontally weak) while if $K$ and $M$ are both weak 2-categories, this double category is weak in both directions (like a [[double bicategory]]).
\end{remark}

\begin{example}
In [[V Cat|$V Cat$]], the squares of the above form (Def. \ref{TheAssociatedDoubleCategory}) are transformations $H(b,a) \to J(g b,f a)$ natural in $a$ and $b$.  
Arguably, this double category is a more fundamental and natural object than the 2-functor $V Cat \to V Prof$.  
\end{example}

#### Via companions and conjoints
 {#CharacterizationViaCompanionsAndConjoints}

More generally, if $K$ is any 2-category equipped with proarrows, we can reconstruct $K$ and its proarrow equipment from the double category of Def. \ref{TheAssociatedDoubleCategory}, and we can characterize the double categories that arise in this way.

One way to state this characterization is that they are those in which every vertical 1-cell $f\colon A\to B$ has both a [[companion]] (namely $B(1,f)$) and a [[conjoint]] (namely $B(f,1)$).

This can be illustrated using string diagrams. The companion and conjoint of $f$ are the horizontal arrows

<table>
<tr>
<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (W) at (-1, 0);
  \coordinate (E) at ( 1, 0);
  % fills
  \fill[colorA] (-1,0) rectangle (1,1);
  \fill[colorB] (-1,0) rectangle (1,-1);
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrow points W
  \draw[mid->] (E) -- (W);
  % area labels
  \node at (0,  0.5) {$A$};
  \node at (0, -0.5) {$B$};
  % edge label
  \node[left] at (W) {$B(1, f)$};
\end{tikzpicture}
</td>
<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{orange!20}
  \colorlet{colorB}{teal!20}
  \coordinate (W) at (-1, 0);
  \coordinate (E) at ( 1, 0);
  % fills
  \fill[colorA] (-1,0) rectangle (1,1);
  \fill[colorB] (-1,0) rectangle (1,-1);
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrow points E
  \draw[mid->] (W) -- (E);
  % area labels
  \node at (0,  0.5) {$B$};
  \node at (0, -0.5) {$A$};
  % edge label
  \node[right] at (E) {$B(f, 1)$};
\end{tikzpicture}
</td>
</tr>
</table>

equipped with 2-cells

<table>
<tr>
<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (SE) at ( 1, -1);
  \coordinate (S)  at ( 0, -1);
  \coordinate (E)  at ( 1,  0);
  \coordinate (C)  at ( 0,  0);
  % fills
  \fill[colorA] (-1,-1) rectangle (1,1);
  \fill[colorB] (SE) -- (S) -- (C) -- (E) -- cycle;
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrows
  \draw[mid<-] (S) -- (C);
  \draw[mid->] (E) -- (C);
  % central node
  \node[circle, draw, fill=white, inner sep=1.5pt] at (C) {$\eta_p$};
  % area labels
  \node at (-0.5, 0.5) {$A$};
  \node at ( 0.5,-0.5) {$B$};
  % real edge labels
  \node[below] at (S) {$f$};
  \node[right] at (E) {$B(1,f)$};
  % phantom edge labels for alignment
  \node[above, opacity=0] at (0, 1) {$f$};
  \node[left,  opacity=0] at (-1, 0) {$B(1,f)$};
\end{tikzpicture}
</td>

<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (NW) at (-1,  1);
  \coordinate (N)  at ( 0,  1);
  \coordinate (W)  at (-1,  0);
  \coordinate (C)  at ( 0,  0);
  % fills
  \fill[colorB] (-1,-1) rectangle (1,1);
  \fill[colorA] (NW) -- (N) -- (C) -- (W) -- cycle;
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrows
  \draw[mid->] (N) -- (C);
  \draw[mid<-] (W) -- (C);
  % central node
  \node[circle, draw, fill=white, inner sep=1.5pt] at (C) {$\epsilon_p$};
  % area labels
  \node at (-0.5, 0.5) {$A$};
  \node at ( 0.5,-0.5) {$B$};
  % real edge labels
  \node[above] at (N) {$f$};
  \node[left]  at (W) {$B(1,f)$};
  % phantom edge labels for alignment
  \node[below, opacity=0] at (0, -1) {$f$};
  \node[right, opacity=0] at (1,  0) {$B(1,f)$};
\end{tikzpicture}
</td>

<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (NE) at ( 1,  1);
  \coordinate (N)  at ( 0,  1);
  \coordinate (E)  at ( 1,  0);
  \coordinate (C)  at ( 0,  0);
  % fills
  \fill[colorA] (-1,-1) rectangle (1,1);
  \fill[colorB] (NE) -- (N) -- (C) -- (E) -- cycle;
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrows
  \draw[mid->] (N) -- (C);
  \draw[mid<-] (E) -- (C);
  % central node
  \node[circle, draw, fill=white, inner sep=1.5pt] at (C) {$\eta_j$};
  % area labels
  \node at (-0.5,-0.5) {$A$};
  \node at ( 0.5, 0.5) {$B$};
  % real edge labels
  \node[above] at (N) {$f$};
  \node[right] at (E) {$B(f,1)$};
  % phantom edge labels for alignment
  \node[below, opacity=0] at (0, -1) {$f$};
  \node[left,  opacity=0] at (-1, 0) {$B(1,f)$};
\end{tikzpicture}
</td>

<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (SW) at (-1, -1);
  \coordinate (S)  at ( 0, -1);
  \coordinate (W)  at (-1,  0);
  \coordinate (C)  at ( 0,  0);
  % fills
  \fill[colorB] (-1,-1) rectangle (1,1);
  \fill[colorA] (SW) -- (S) -- (C) -- (W) -- cycle;
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrows
  \draw[mid<-] (S) -- (C);
  \draw[mid->] (W) -- (C);
  % central node
  \node[circle, draw, fill=white, inner sep=1.5pt] at (C) {$\epsilon_j$};
  % area labels
  \node at (-0.5,-0.5) {$A$};
  \node at ( 0.5, 0.5) {$B$};
  % real edge labels
  \node[below] at (S) {$f$};
  \node[left]  at (W) {$B(f,1)$};
  % phantom edge labels for alignment
  \node[above, opacity=0] at (0,  1) {$f$};
\end{tikzpicture}
</td>
</tr>
</table>

whose compositions satisfy the following laws: $\eta_p \epsilon_p = id_f$, $\epsilon_p \odot \eta_p = id_{B(1, f)}$, and $\eta_j \epsilon_j = id_f$, $\eta_j \odot \epsilon_j = id_{B(f, 1)}$


One can then recover $K$ and $M$ as the [[vertical 2-category|vertical and horizontal 2-categories]], respectively, and the 2-functor $K\to M$ as the functor taking every vertical arrow to its companion.  Whenever a vertical arrow has both a companion $B(1,f)$ and a conjoint $B(f,1)$, we automatically have an adjunction $B(1,f)\dashv B(f,1)$, so this defines a proarrow equipment in the first sense.


#### Via cartesian niche fillers
 {#CharacterizationViaCartesianNicheFillers}

Another, perhaps even more natural, way to characterize these double categories (Def. \ref{TheAssociatedDoubleCategory}) is as those with the following property: given any "niche"
\begin{tikzcd}
  A
   \arrow[d, "f"']
  & C
  \arrow[d, "g"]
  \\
  B
  \arrow[r, "J"', ""{name=D, above}]
  & D
\end{tikzcd}
there exists a "universal" or "cartesian" filler square
\begin{tikzcd}
  A
  \arrow[r,  "{J(g, f)}", ""{name=U, below}]
  \arrow[d, "f"']
  & C
  \arrow[d, "g"]
  \\
  B
  \arrow[r, "J"', ""{name=D, above}]
  & D \mathrlap{\,,}
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
namely with the property that any other square 
\begin{tikzcd}
  X
  \arrow[r,  "", ""{name=U, below}]
  \arrow[d, "h"']
  & Y
  \arrow[d, "k"]
  \\
  A
  \arrow[d, "f"']
  &C
  \arrow[d, "g"]
  \\
  B
  \arrow[r, "J"', ""{name=D, above}]
  & D
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
factors through the universal one uniquely:
\begin{tikzcd}
 X
 \arrow[d, "h"']
  \arrow[r, ""', ""{name=T, below}]
 &Y
 \arrow[d, "k"]
 \\
  A
  \arrow[
    r,  
    "{J(g, f)}"{description}, 
    ""{name=U, below}, 
    ""{name=U1, above, yshift=5pt}
  ]
  \arrow[d, "f"']
  & C
  \arrow[d, "g"]
  \\
  B
  \arrow[r, "J"', ""{name=D, above}]
  & D
  \arrow[Rightarrow, from=U, to=D]
  \arrow[Rightarrow, from=T, to=U1, "\exists !"']
\end{tikzcd}

The profunctor $J(g,f)$ will, of course, turn out to be the same one we gave that name to earlier.  The proarrows $B(1,f)=U_B(id_B,f)$ and $B(f,1) = U_B(f,id_B)$ are then a special case of this construction.  

We show that they are a [[companion]] and [[conjoint]] of $f$, respectively, as follows.

By factoring the identity square
\begin{tikzcd}
  A
  \arrow[r,  "U_A", ""{name=U, below}]
  \arrow[d, "f"']
  & A
  \arrow[d, "f"]
  \\
  B
  \arrow[r, "U_B"', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=U, to=D, "U_f"']
\end{tikzcd}
through the universal fillers
<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
  A
  \arrow[r,  "{B(1, f)}", ""{name=U, below}]
  \arrow[d, "f"']
  & B
  \arrow[d, "id"]
  \\
  B
  \arrow[r, "U_B"', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
<td style="border: none;">
\begin{tikzcd}
  B
  \arrow[r,  "{B(f, 1)}", ""{name=U, below}]
  \arrow[d, "id"']
  & A
  \arrow[d, "f"]
  \\
  B
  \arrow[r, "U_B"', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
</tr>
</table>
that define $B(1,f)$ and $B(f,1)$, we obtain additional squares
<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
  A
  \arrow[r,  "U_A", ""{name=U, below}]
  \arrow[d, "f"']
  & A
  \arrow[d, "id"]
  \\
  B
  \arrow[r, "{B(f, 1)}"', ""{name=D, above}]
  & A
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
<td style="border: none;">
\begin{tikzcd}
  A
  \arrow[r,  "U_A", ""{name=U, below}]
  \arrow[d, "id"']
  & A
  \arrow[d, "f"]
  \\
  A
  \arrow[r, "{B(1,f)}"', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
</tr>
</table>
such that the vertical composites
<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
  A
  \arrow[r,  "U_A", ""{name=T, below}]
  \arrow[d, "f"']
  & A
  \arrow[d, "id"]
  \\
  B
  \arrow[
    r, 
    "{B(f, 1)}"{description}, 
    ""{name=U, below}, 
    ""{name=U1, above, yshift=5pt}
  ]
  \arrow[d, "id"']
  & A
 \arrow[d, "f"]
  \\
  B
  \arrow[r, "U_B"', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=T, to=U1]
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
<td style="border: none;">
\begin{tikzcd}
   A
  \arrow[r,  "U_A", ""{name=T, below}]
  \arrow[d, "id"']
  & A
  \arrow[d, "f"]
  \\
  B
  \arrow[
    r, 
    "{B(1, f)}"{description}, 
    ""{name=U, below}, 
    ""{name=U1, above, yshift=5pt}
  ]
   \arrow[d, "f"']
  & A
 \arrow[d, "id"]
  \\
  B
  \arrow[r, "U_B"', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=T, to=U1]
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
</tr>
</table>
are both equal to $U_f$.  

Using the uniqueness of factorization through the universal squares, we can conclude moreover that the [[horizontal composition|horizontal composites]]
<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
 A
   \arrow[r,  "U_A", ""{name=U1, below}]
   \arrow[d, "id"']
& A
  \arrow[r,  "{B(1, f)}", ""{name=U2, below}]
  \arrow[d, "f"]
 & B
  \arrow[d, "id"]
 \\
 A
   \arrow[r,  "{B(1,f)}"', ""{name=D1, above}]
 & B
   \arrow[r,  "U_B"', ""{name=D2, above}]
 & B
  \arrow[Rightarrow, from=U1, to=D1]
  \arrow[Rightarrow, from=U2, to=D2]
\end{tikzcd}
</td>
<td style="border: none;">
\begin{tikzcd}
 B
   \arrow[r,  "{B(f, 1)}", ""{name=U1, below}]
   \arrow[d, "id"']
& A
  \arrow[r,  "U_A", ""{name=U2, below}]
  \arrow[d, "f"]
 & A
  \arrow[d, "id"]
 \\
 B
   \arrow[r,  "U_B"', ""{name=D1, above}]
 & B
   \arrow[r,  "{B(f, 1)}"', ""{name=D2, above}]
 & A
  \arrow[Rightarrow, from=U1, to=D1]
  \arrow[Rightarrow, from=U2, to=D2]
\end{tikzcd}
</td>
</tr>
</table>
are equal to the identity squares of $B(1,f)$ and $B(f,1)$ respectively. Together these are the defining equations of a [[companion]] and a [[conjoint]].

The [[unit of an adjunction|unit]] and [[counit of an adjunction|counit]] of the adjunction $B(1, f) \dashv B(f, 1)$ are given by the horizontal composites:
<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
 A
   \arrow[r,  "U_A", ""{name=U1, below}]
   \arrow[d, "id"']
& A
  \arrow[r,  "U_A", ""{name=U2, below}]
  \arrow[d, "f"]
 & A
  \arrow[d, "id"]
 \\
 A
   \arrow[r,  "{B(1,f)}"', ""{name=D1, above}]
 & B
   \arrow[r,  "{B(f, 1)}"', ""{name=D2, above}]
 & B
  \arrow[Rightarrow, from=U1, to=D1]
  \arrow[Rightarrow, from=U2, to=D2]
\end{tikzcd}
</td>
<td style="border: none;">
\begin{tikzcd}
 B
   \arrow[r,  "{B(f, 1)}", ""{name=U1, below}]
   \arrow[d, "id"']
& A
  \arrow[r,  "{B(1, f)}", ""{name=U2, below}]
  \arrow[d, "f"]
 & B
  \arrow[d, "id"]
 \\
 B
   \arrow[r,  "U_B"', ""{name=D1, above}]
 & B
   \arrow[r,  "U_B"', ""{name=D2, above}]
 & B
  \arrow[Rightarrow, from=U1, to=D1]
  \arrow[Rightarrow, from=U2, to=D2]
\end{tikzcd}
</td>
</tr>
</table>


#### The Central Lemma

Finally, we record the following **central lemma**.

\begin{lemma}\label{CentralLemma}
There is a [[natural bijection]] between squares of the form

<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
  A_0
  \arrow[r,  "H", ""{name=U, below, yshift=-10pt}]
  \arrow[d, "f_1"']
  & B_0
  \arrow[d, "g_1"]
  \\
  A_1
  \arrow[d, "f_2"']
  & B_1
  \arrow[d, "g_2"]
  \\
  A_2
  \arrow[d, "f_3"']
   & B_2
 \arrow[d, "g_3"]
  \\
  A_3
 \arrow[r, "J"', ""{name=D, above, yshift=10pt}]
  & B_3
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
<td style="border: none;">
≅
</td>
<td style="border: none;">
\begin{tikzcd}
  A_1
  \arrow[r, "{A_1(f_1, 1)}"]
  \arrow[d, "f_2"']
  & A_0
  \arrow[r,  "H", ""{name=U, below}]
  & B_0
  \arrow[r, "{B_1(1, g_1)}"]
  & B_1
  \arrow[d, "g_2"]
  \\
  A_2
  \arrow[r, "{A_3(1, f_3)}"']
  & A_3
 \arrow[r, "J"', ""{name=D, above}]
  & B_3
  \arrow[r, "{B_3(g_3, 1)}"']
  & B_2
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
</tr>
</table>

\end{lemma}

\begin{remark}
\label{SpiderLemmaStringDiagram}
Illustrated in terms of [[string diagram|string diagrams]], the Central Lemma \ref{CentralLemma} is also called the *Spider Lemma* ([Myers 2016 Lemma 1.2.3](#Myers16)):

\begin{tikzpicture}[scale=2.5]
  \usetikzlibrary{decorations.markings, arrows.meta, calc}
  \tikzset{
    >=Latex,
    mid->/.style={
      decoration={markings, mark=at position 0.55 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.55 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }

  \colorlet{colorA0}{red!20}
  \colorlet{colorA1}{orange!30}
  \colorlet{colorA2}{yellow!40}
  \colorlet{colorA3}{green!25}
  \colorlet{colorB0}{cyan!25}
  \colorlet{colorB1}{violet!20}
  \colorlet{colorB2}{red!10}
  \colorlet{colorB3}{green!15}

  % --- LEFT SQUARE ---
  \coordinate (NW)  at (-1,  1);
  \coordinate (NE)  at ( 1,  1);
  \coordinate (SW)  at (-1, -1);
  \coordinate (SE)  at ( 1, -1);
  \coordinate (W)   at (-1,  0);
  \coordinate (E)   at ( 1,  0);
  \coordinate (C)   at ( 0,  0);
  \coordinate (NNW) at (-0.6,  1);
  \coordinate (N)   at ( 0,    1);
  \coordinate (NNE) at ( 0.6,  1);
  \coordinate (SSW) at (-0.6, -1);
  \coordinate (S)   at ( 0,   -1);
  \coordinate (SSE) at ( 0.6, -1);

  % fills
  \fill[colorA0] (NW)  -- (NNW) to[out=270, in=130] (C) to[out=180, in=0] (W)   -- cycle;
  \fill[colorA1] (NNW) to[out=270, in=130] (C) to[out=90,  in=270] (N)   -- cycle;
  \fill[colorA2] (N)   to[out=270, in=90]  (C) to[out=50,  in=270] (NNE) -- cycle;
  \fill[colorA3] (NNE) to[out=270, in=50]  (C) to[out=0,   in=180] (E)   -- (NE) -- cycle;
  \fill[colorB0] (SW)  -- (W)   to[out=0,   in=180] (C) to[out=230, in=90]  (SSW) -- cycle;
  \fill[colorB1] (SSW) to[out=90,  in=230] (C) to[out=270, in=90]  (S)   -- cycle;
  \fill[colorB2] (S)   to[out=90,  in=270] (C) to[out=310, in=90]  (SSE) -- cycle;
  \fill[colorB3] (SSE) to[out=90,  in=310] (C) to[out=0,   in=180] (E)   -- (SE) -- cycle;

  % border
  \draw[gray] (SW) rectangle (NE);

  % arrows
  \draw[mid->] (NNW) to[out=270, in=130] (C);
  \draw[mid->] (N)   to[out=270, in=90]  (C);
  \draw[mid->] (NNE) to[out=270, in=50]  (C);
  \draw[mid->] (C) to[out=230, in=90] (SSW);
  \draw[mid->] (C) to[out=270, in=90] (S);
  \draw[mid->] (C) to[out=310, in=90] (SSE);
  \draw (W) -- (C);
  \draw (C) -- (E);

  % central node
  \node[circle, draw, fill=white, inner sep=3pt] at (C) {};

  % edge labels
  \node[above] at (NNW) {$f_1$};
  \node[above] at (N)   {$f_2$};
  \node[above] at (NNE) {$f_3$};
  \node[below] at (SSW) {$g_1$};
  \node[below] at (S)   {$g_2$};
  \node[below] at (SSE) {$g_3$};
  \node[left]  at (W)   {$H$};
  \node[right] at (E)   {$J$};

  % area labels
  \node at ($(NW)!0.5!(NNW)+(0,-0.25)$) {$A_0$};
  \node at ($(NNW)!0.5!(N) +(0,-0.25)$) {$A_1$};
  \node at ($(N)!0.5!(NNE) +(0,-0.25)$) {$A_2$};
  \node at ($(NNE)!0.5!(NE)+(0,-0.25)$) {$A_3$};
  \node at ($(SW)!0.5!(SSW)+(0, 0.25)$) {$B_0$};
  \node at ($(SSW)!0.5!(S) +(0, 0.25)$) {$B_1$};
  \node at ($(S)!0.5!(SSE) +(0, 0.25)$) {$B_2$};
  \node at ($(SSE)!0.5!(SE)+(0, 0.25)$) {$B_3$};

  % isomorphism symbol
  \node at (1.7, 0) {$\cong$};

  % --- RIGHT SQUARE ---
  \begin{scope}[xshift=4cm]

    \coordinate (NW)  at (-1,  1);
    \coordinate (NE)  at ( 1,  1);
    \coordinate (SW)  at (-1, -1);
    \coordinate (SE)  at ( 1, -1);
    \coordinate (W)   at (-1,  0);
    \coordinate (E)   at ( 1,  0);
    \coordinate (C)   at ( 0,  0);
    \coordinate (N)   at ( 0,  1);
    \coordinate (S)   at ( 0, -1);
    \coordinate (WNW) at (-1,  0.6);
    \coordinate (WSW) at (-1, -0.6);
    \coordinate (ENE) at ( 1,  0.6);
    \coordinate (ESE) at ( 1, -0.6);

    % fills
    \fill[colorA1] (NW)  -- (N)   to[out=270, in=90]  (C) to[out=140, in=0] (WNW) -- cycle;
    \fill[colorA0] (W)   -- (WNW) to[out=0,   in=140] (C) to[out=180, in=0] (W)   -- cycle;
    \fill[colorA2] (N)   -- (NE)  -- (ENE) to[out=180, in=40]  (C) to[out=90,  in=270] (N)   -- cycle;
    \fill[colorA3] (C) to[out=40,  in=180] (ENE) -- (E)   to[out=180, in=0]   (C) -- cycle;
    \fill[colorB0] (W)   to[out=0,   in=180] (C) to[out=220, in=0]   (WSW) -- cycle;
    \fill[colorB1] (SW)  -- (S)   to[out=90,  in=270] (C) to[out=220, in=0]   (WSW) -- cycle;
    \fill[colorB3] (C) to[out=320, in=180] (ESE) -- (E)   to[out=180, in=0]   (C) -- cycle;
    \fill[colorB2] (S)   -- (SE)  -- (ESE) to[out=180, in=320] (C) to[out=270, in=90]  (S)   -- cycle;

    % border
    \draw[gray] (SW) rectangle (NE);

    % arrows
    \draw[mid->] (N)   to[out=270, in=90]  (C);
    \draw[mid->] (C)   to[out=270, in=90]  (S);
    \draw[mid->] (WNW) to[out=0,   in=140] (C);
    \draw        (W)   to[out=0,   in=180]  (C);
    \draw[mid<-] (WSW) to[out=0,   in=220] (C);
    \draw[mid<-] (C) to[out=40,  in=180] (ENE);
    \draw        (C) to[out=0,   in=180]  (E);
    \draw[mid->] (C) to[out=320, in=180] (ESE);

    % central node
    \node[circle, draw, fill=white, inner sep=3pt] at (C) {};

    % edge labels
    \node[above] at (N)   {$f_2$};
    \node[below] at (S)   {$g_2$};
    \node[left]  at (WNW) {$A_1(f_1, 1)$};
    \node[left]  at (W)   {$H$};
    \node[left]  at (WSW) {$B_1(1, g_1)$};
    \node[right] at (ENE) {$A_3(1, f_3)$};
    \node[right] at (E)   {$J$};
    \node[right] at (ESE) {$B_3(g_3, 1)$};

    % area labels
    \node at ($(NW)!0.5!(WNW)+(0.3, 0)$)  {$A_1$};
    \node at ($(W)!0.5!(WNW) +(0.3, 0)$)  {$A_0$};
    \node at ($(NE)!0.5!(ENE)+(-0.3,0)$)  {$A_2$};
    \node at ($(E)!0.5!(ENE) +(-0.3,0)$)  {$A_3$};
    \node at ($(W)!0.5!(WSW) +(0.3, 0)$)  {$B_0$};
    \node at ($(SW)!0.5!(WSW)+(0.3, 0)$)  {$B_1$};
    \node at ($(E)!0.5!(ESE) +(-0.3,0)$)  {$B_3$};
    \node at ($(SE)!0.5!(ESE)+(-0.3,0)$)  {$B_2$};

  \end{scope}

\end{tikzpicture}
\end{remark}


\begin{remark}
One way to think of this Lemma \ref{CentralLemma} is as saying that vertical arrows can be "slid around corners" to become horizontal arrows, turning them into the "representable proarrows" $B(1,f)$ or $B(f,1)$ (depending on whether you slid them "backwards" or "forwards" to get around the corner).  The bijection is just given by composing with the four special squares in the definition of companions and conjoints.  In particular, by a Yoneda argument, for any $f\colon A\to C$, $g\colon B\to D$, and $J\colon C\nrightarrow D$ we have
\[
  \label{coyon}
  J(g,f) 
    \cong 
  C(1,f) 
    \odot 
  J 
    \odot 
  D(g,1)
  \mathrlap{\,,} 
\]
which was what we took as the the definition of $J(g,f)$ with the original Def. \ref{TheDefinitionAsA2Functor} of proarrow equipment.  Thus, the companions and conjoints determine the rest of the cartesian squares.  Note that this is an equipment-version of [[Yoneda reduction]]
\end{remark}

We also write $U_A$, $A(1,1)$, or simply $A$ for the identity proarrow $A\nrightarrow A$.  

\begin{remark}
In the case where proarrows are profunctors, $H(g, f)$ is not the action on a set of [[heteromorphisms]] by pre- and post- composing with morphisms; instead it is the functor $f$, followed by the profunctor $H$, followed by taking the preimage under the functor $g$, resulting in a profunctor from $A$ to $C$.
\end{remark}


\begin{remark}
**(terminology)**
We refer to the entire structure defined above as a **2-category equipped with proarrows** or a **2-category proarrow equipment**.  Those working in the field often use the term **proarrow equipment** or simply **equipment** for the entire structure.  We prefer "2-category equipped with proarrows" (or, equivalently, "pro-morphisms") for the following reasons:

* It conveys that we are talking about extra stuff added to a 2-category.  (Actually, it is "eka-stuff" or "2-stuff" in the sense of [stuff, structure, property](http://ncatlab.org/nlab/show/stuff,+structure,+property).)
* It includes the word "proarrow" which tells people what the extra stuff consists of, namely a generalization of [[profunctors]].
* It includes the word "equipment" which signals what is meant to readers who are familiar with that term.

We do sometimes avail ourselves of the shorter terminology "proarrow equipment," however, once we are clear what is under discussion.
\end{remark}


### As categories internal to $Cat$
 {#AsInternalCategories}

We discuss how 2-categories with proarrow equipment are equivalently [[internal categories]] in the [[(2,1)-category]] [[Cat]], in the sense of the theory of _[[internal (∞,1)-categories]]_. 

(...)


For the time being see at _[Segal space -- Examples -- In 1Grpd](Segal+space#ExamplesInIGrpd)_.



## Category theory in proarrow equipments

We now give a few examples of how to do [[formal category theory]] internal to proarrow equipments.


### Homset definition of adjunctions 
  {#HomsetAdjn}

We start with this: two (vertical) arrows $f\colon A\to B$ and $g\colon B\to A$ are adjoint (in $\mathcal{V}(\underline{X})$) if and only if we have an isomorphism $B(f,1)\cong A(1,g)$.  Why?  Well, an adjunction $f\dashv g$ comes with a unit and a counit, which (expressed in $\underline{X}$) are of the form
<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
  A
  \arrow[r,  "U_A"]
  \arrow[d, "f"']
  \arrow[dd, "", ""{name=L, right}, phantom]
  & A
  \arrow[dd, "id", ""{name=R, left}]
  \\
  B
    \arrow[d, "g"']
  \\
  A
  \arrow[r, "U_A"']
  & A
    \arrow[Rightarrow, from=R, to=L, "\eta"']
\end{tikzcd}
</td>
<td style="border: none;">
\begin{tikzcd}
  B
  \arrow[r,  "U_B"]
  \arrow[dd, "id"',  ""{name=L, right}]
  & B
  \arrow[d, "g"]
  \arrow[dd, "", ""{name=R, left}, phantom]
  \\
  & A
    \arrow[d, "f"]
  \\
  B
  \arrow[r, "U_B"']
  & B
   \arrow[Rightarrow, from=R, to=L, "\varepsilon"']
\end{tikzcd}
</td>
</tr>
</table>
Applying the bijection of the Central Lemma (\ref{CentralLemma}), we see that $\eta$ corresponds to a map $B(f,1) \to A(1,g)$, and likewise $\varepsilon$ corresponds to a map $A(1,g)\to B(f,1)$.  The triangle identities for $\eta$ and $\varepsilon$ are then equivalent to saying that these two maps are inverse isomorphisms.  So we've recovered the classical equivalence between the "diagrammatic" and isomorphism-of-hom-sets definitions of [[adjunctions]], in a purely formal way.



### Fully faithful arrows

An arrow $f:A\to B$ in a 2-category equipped with proarrows is said to be **fully faithful** if the canonical morphism $U_A\to B(f,f)$ is an isomorphism of proarrows $A\to A$.  In $V Cat$ this recaptures the correct notion of $V$-fully-faithful $V$-functor.

It is not hard to see, using the fact that $K\to M$ is locally fully faithful, that any fully-faithful arrow $f\colon A\to B$ is, in fact, internally fully-faithful in $K$ in the sense that $K(X,A)\to K(X,B)$ is fully faithful for all $X\in K$.  However, the converse fails in general.  But it is not hard to show that the two are equivalent if $f\colon A\to B$ has a left or right adjoint, using the above characterization of adjunctions.


### Limits

The notion of limit we end up in a 2-category equipped with proarrows with is actually more general than what you're probably used to, but this extra generality turns out to be useful.  Let $d\colon D\to C$ be an arrow and let $J\colon D\nrightarrow A$ be a proarrow; we're going to define what it means for an arrow $\ell\colon A\to C$ to be the *$J$-weighted limit* of $d$.  In the proarrow-equipped 2-category $V Cat$ of $V$-enriched categories, if $A$ is the [unit](http://ncatlab.org/nlab/show/unit+enriched+category) $V$-category $I$, then this will recover the usual notion of [weighted limit](http://ncatlab.org/nlab/show/weighted+limit).  Of course, in a general proarrow equipment we may not have a "unit object," so that extra generality is unavoidable; it's like using generalized elements in ordinary category theory.

To make things easier, let's assume that our proarrow equipment is *closed*, in the sense that composition of proarrows has adjoints in each variable
$$ \mathcal{H}(\underline{X})(H\odot K,L) \cong \mathcal{H}(\underline{X})(H,K\rhd L) \cong \mathcal{H}(\underline{X})(K,L\lhd H).$$
The Central Lemma implies that analogously to \eqref{coyon}, we have
\[K(g,f) \cong D(1,g)\rhd K \lhd C(f,1). \label{yon} \]
In $V\text{-}Prof$, the adjoints are given by the [ends](http://ncatlab.org/nlab/show/end)
$$ (K\rhd L)(b,a) = \int_{c\in C} [K(c,b), L(c,a)] $$
and
$$ (L \lhd H)(c,b) = \int_{a\in A} [H(b,a), L(c,a)]. $$
Therefore, \eqref{yon} is an abstract form of the Yoneda lemma, just as \eqref{coyon} is an abstract form of Yoneda reduction.

Now recall that for $V$-categories $D$ and $C$, an object $\ell\in C$ is a $J$-weighted limit of $d\colon D\to C$ if we have a natural isomorphism
$$
\begin{aligned}
C(c,\ell) &\cong [D,V](J, C(c,d(-)))\\
&= \int_{x\in D} [J(x), C(c,d(x))].
\end{aligned}
$$
Thus it makes sense to define, in a closed proarrow equipment, an arrow $\ell\colon A\to C$ to be the $J$-weighted limit of $d$ if we have an isomorphism
$$ C(1,\ell) \cong C(1,d) \lhd J. $$
(If our proarrow equipment is not closed, we simply assert that $C(1,\ell)$ has the universal property that $C(1,d) \lhd J$ would have if it existed.  In other terminology, we assert that $C(1,\ell)$ is a *right lifting* of $C(1,d)$ along $J$ in the 2-category of proarrows.)  In particular, when $A$ is the unit $V$-category, this recovers the classical notion.  But even in $V Cat$ there are interesting examples for other values of $A$.  If we take $J = D(j,1)$ for some functor $j\colon A\to D$, then \eqref{coyon} and \eqref{yon} imply that
$$
\begin{aligned}
C(1,d) \lhd J &= C(1,d) \lhd D(j,1)\\
& \cong j^* C(1,d)\\
& \cong D(1,j) \odot C(1,d)\\
& \cong C(1,d j) 
\end{aligned}
$$
so that $\ell = d j$ is the $J$-weighted limit of $d$.  That is, $D(j,1)$-weighted limits are just given by composition with $j$.

More interestingly, one can show that if $J = D(1,k)$ for some $k\colon D\to A$, then $J$-weighted limits specialize to *pointwise* right Kan extensions along $k$.  That is, the extra data of a proarrow equipment lets us define the good notion of Kan extension (even in the enriched case) as a special case of a general notion of limit.  Thus, in a general 2-category equipped with proarrows, we *define* a "pointwise right Kan extension" along an arrow $k\colon D\to A$ to be a $D(1,k)$-weighted limit.  It is easy to show that any pointwise Kan extension is, in particular, an internal Kan extension in $K$, but as we have seen the converse fails in $V Cat$.


### Right adjoints preserve limits

Suppose that $\ell\colon A\to C$ is a $J$-weighted limit of $d\colon D\to C$ in the above sense, and let $g\colon C\to B$ be an arrow with a left adjoint $f\colon B\to C$.  We want to show that $g\ell$ is a $J$-weighted limit of $g d$.  But we have
$$
\begin{aligned}
B(1,g\ell) &\cong C(1,\ell) \odot B(1,g)\\
&\cong \big(C(1,d) \lhd J\big) \odot C(f,1)\\
&\cong C(1,f) \rhd \big(C(1,d) \lhd J\big)\\
&\cong \big(C(1,f) \rhd C(1,d)\big) \lhd J\\
&\cong \big(C(1,d) \odot C(f,1)\big) \lhd J\\
&\cong \big(C(1,d) \odot B(1,g)\big) \lhd J\\
&\cong B(1,g d) \lhd J.
\end{aligned}
$$
which is what we want.


### Graphs and cographs

As noted above, in the case of ordinary categories, the profunctors can in fact be recovered from the 2-category $Cat$.  Specifically, profunctors $A\to B$ can be identified with two-sided discrete fibrations from $B$ to $A$ (that is, spans $B \leftarrow C \to A$ such that $C \to B$ is a [[Grothendieck fibration|(Grothendieck) fibration]], $C\to A$ is an opfibration, the two structures are compatible, and each fiber of $C\to B\times A$ is discrete).  The two-sided fibration corresponding to a profunctor is also called its [[graph of a profunctor|graph]].  The same is true for internal categories, but not for enriched categories.

However the $V$-profunctors $A\to B$ *can* be recovered from the 2-category $V Cat$ in a different, and in fact dual, way: they are the two-sided [[codiscrete cofibrations]] from $B$ to $A$, i.e. two-sided discrete fibrations in $(V Cat)^{op}$.  The two-sided cofibration corresponding to a profunctor is, unsurprisingly, its [[cograph of a profunctor|cograph]], and also its [[collage]].  This was first noticed by Street and subsequently expanded on by other authors.  In particular, one can write down axioms on a 2-category guaranteeing that its codiscrete cofibrations can be used to equip it with proarrows, and axioms on a proarrow equipment guaranteeing that it arises from codiscrete cofibrations.

### Virtual equipments
 {#VirtualEquipments}

One can formulate a generalized notion of equipment which includes $V Cat$ for _any_ monoidal category $V$ (and in fact, any [[multicategory]]), and $Cat(S)$ for any category $S$ with pullbacks.  The precise definition is complicated, but the basic idea is not: we start from the double-category definition, and instead of composites of the horizontal (pro)arrows, we allow the squares to have domains that are arbitrary composable strings, like so:
$$\array{ & \to \to \dots \to &\\
  \downarrow & \Downarrow & \downarrow\\
  & \underset{}{\to}& .}$$
So far this is analogous to the generalization from monoidal categories to multicategories, and gives the notion of [[virtual double category]].  We then impose a condition analogous to the existence of companions and conjoints to obtain the notion of *[[virtual equipments]]*.  Most of category theory can be done in a virtual equipment just as well as in an equipment.


## Related concepts

Variant concepts:

* [[virtual proarrow equipment]]

* [[1-category proarrow equipment]]

* [[(1,2)-category proarrow equipment]]

Related concepts:

* [[cartesian bicategory]]

* [[bicategory of relations]]

* [[allegory]]


## References

* {#Wood82} [[Richard J. Wood]]: *Abstract Proarrows I*, Cahiers de topologie et géométrie différentielle **23** 3 (1982) 279-290 &lbrack;[numdam:CTGDC_1982__23_3_279_0](http://www.numdam.org/item/CTGDC_1982__23_3_279_0)&rbrack;

* {#Wood85} [[Richard J. Wood]], *Proarrows II*, Cahiers de Topologie et Géométrie Différentielle Catégoriques **26** 2 (1985) 135-168 &lbrack;[numdam:CTGDC_1985__26_2_135_0](http://www.numdam.org/item/CTGDC_1985__26_2_135_0)&rbrack; 

* [[Ross Street]]: *Fibrations in bicategories*, [[Cahiers de Topologie et Géométrie Différentielle Catégoriques]], **21** 2 (1980) 111--160 &lbrack;[numdam:CTGDC_1980__21_2_111_0](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1980__21_2_111_0)&rbrack;
  > (construction of $V Mod$ from $V Cat$)

* [[Aurelio Carboni]], [[Scott Johnson]], [[Ross Street]], [[Dominic Verity]]: *Modulated bicategories*, Journal of Pure and Applied Algebra **94** 3 (1994) 229-282 &lbrack;<a href="https://doi.org/10.1016/0022-4049(94)90009-4">doi:10.1016/0022-4049(94)90009-4</a>, [MR:1285544](http://www.ams.org/mathscinet-getitem?mr=1285544)&rbrack;
 > (improved construction of $V Mod$ from $V Cat$)

* {#Verity2011} [[Dominic Verity]]: _Enriched categories, internal categories and change of base_, PhD. thesis, Cambridge University (1992), reprinted as: Reprints in Theory and Applications of Categories **20** (2011) 1-266 &lbrack;[tac:tr20](http://www.tac.mta.ca/tac/reprints/articles/20/tr20abs.html)&rbrack;

* {#Shulman2008} [[Mike Shulman]]: *Framed bicategories and monoidal fibrations*, Theory and Applications of Categories **20** 18 (2008) 650-738 &lbrack;[tac:20-18](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html)&rbrack;
  > (The equivalence with certain double categories, there called *framed bicategories*, and a general way to construct equipments such as $Ab(S)$.)

* {#CruttwellShulman10} [[Geoff Cruttwell]], [[Mike Shulman]]: *A unified framework for generalized multicategories*, Theory Appl. Categ. **24** 21 (2010) 580-655 &lbrack;[arxiv/0907.2460](http://arxiv.org/abs/0907.2460), [TAC:24-21](http://www.tac.mta.ca/tac/volumes/24/21/24-21abs.html)&rbrack;
  > (currently the only reference for [[virtual equipments]])

* Renato Betti, [[Aurelio Carboni]], [[Ross Street]], [[Robert Walters]]: *Variation through enrichment*, Journal of Pure and Applied Algebra **29** 2 (1983) 109-127 &lbrack;<a href="https://doi.org/10.1016/0022-4049(83)90100-7">doi:10.1016/0022-4049(83)90100-7</a>&rbrack;
  > (locally small fibrations as $Span$-enriched categories)

A blog post surveying ideas of proarrow equipments, much of which has been copied over to this page:

* [[Mike Shulman]], _Equipments_ ([blog](http://golem.ph.utexas.edu/category/2009/11/equipments.html))

On a [[string diagram]]-calculus for ([[virtual double category|virtual]]) [[double categories]] with ([[virtual equipment|virtual]]) [[2-category equipped with proarrows|pro-arrow equipments]]:

* {#Myers16} [[David Jaz Myers]]: _String Diagrams For Double Categories and (Virtual) Equipments_ &lbrack;[arXiv:1612.02762](https://arxiv.org/abs/1612.02762)&rbrack;

* [[David Jaz Myers]], *String Diagrams for (Virtual) Proarrow Equipments* (2017) &lbrack;slides: [pdf](http://www.mat.uc.pt/~ct2017/slides/myers_d.pdf), [[Myers-StringDiagrams2017.pdf:file]]&rbrack;

An [[(∞,1)-category theory|(∞,1)-category theoretic]] version of proarrow equipments is in

* Jaco Ruit, _Formal category theory in ∞-equipments I_ ([arXiv:2308.03583](https://arxiv.org/abs/2308.03583))







[[!redirects 2-category equipped with proarrows]]
[[!redirects 2-categories equipped with proarrows]]
[[!redirects 2-category equipped with pro-arrows]]
[[!redirects 2-categories equipped with pro-arrows]]
[[!redirects 2-category with proarrow equipment]]
[[!redirects 2-categories with proarrow equipment]]
[[!redirects 2-category with pro-arrow equipment]]
[[!redirects 2-categories with pro-arrow equipment]]
[[!redirects 2-category equipment]]
[[!redirects 2-category equipments]]
[[!redirects equipment]]
[[!redirects equipments]]
[[!redirects proarrow equipment]]
[[!redirects proarrow equipments]]
[[!redirects pro-arrow equipment]]
[[!redirects pro-arrow equipments]]

[[!redirects proarrow]]
[[!redirects proarrows]]

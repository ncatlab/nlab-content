
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

A _path space object_ in [[homotopy theory]] is an [[object]] in a [[homotopical category]] that behaves for many purposes as the [[topology|topological]] [[path space]] does in [[topological homotopy theory]].


## Definition
 {#Definition}

\begin{definition}\label{PathSpaceObject}
**(path space object)**
\linebreak
For $\mathcal{C}$ a [[category with weak equivalences]] and with [[binary products]], a **path space object of/for an [[object]] $X$** of $\mathcal{C}$ is a factorization of the [[diagonal]] morphism $X \stackrel{(Id, Id)}{\to} X \times X$ into the [[product]] as

$$
  X 
    \xrightarrow{\;\;\; s \;\;\;} 
  Paths_X
    \xrightarrow{\;\;\; (d_0, d_1) \;\;\;}
  X \times X
$$

such that $s$ is a [[weak equivalence]] ([Quillen 1967, §I.1](#Quillen67)).  

Moreover ([Dwyer & Spalinski 1995, §4.12](#DwyerSpalinski95)):

If $\mathcal{C}$ in addition has the structure of a [[fibration category]] then one speaks, furthermore, of a **good path space object** if $(d_0,d_1)$ is a [[fibration]].

If $\mathcal{C}$ furthermore has the structure of a [[model category]] then one speaks of a **very good path space object** if $(d_0,d_1)$ is a [[fibration]] and $s$ is a [[cofibration]] (hence an [[acyclic cofibration]]).
\end{definition}

\begin{remark}
In Def. \ref{PathSpaceObject} one interprets 

1. a ([[generalised element|generalised]]) [[global element|element]] of $X^I$ as a [[path]] in $X$;

1. $d_0, d_1$ as the maps that send a path to its start- or endpoint, respectively

1. $s$ as the map that sends a point to the path [[constant function|constant]] on that point.

\end{remark}

\begin{remark}\label{InModelCategories}
**(in model categories)**
  In any [[model category]], the [[factorization system|factorization axioms]] applied to the [[diagonal maps]] immediately imply that every object has a path space object, and in fact a "very good" one. (See [below](#InModelCategories).)

The very good path space objects in [[locally cartesian closed model categories]] serve as [[categorical semantics]] for the [[identity types]] in [[dependent type theory]] ([[homotopy type theory]]).
\end{remark}

\begin{remark}
In the presence of a (good, very good) [[interval object]] 

$$
  \ast \sqcup \ast \to I \to \ast
  \,,
$$

the [[exponential objects]] of the form $X^I$ are (good, very good) path space objects (at least for the evident corresponding definition of "interval object").

In particular, in a [[convenient category of topological spaces]], with $I = [0,1]$ the standard [[closed interval]], the [[compact-open topology|mapping space]] $X^{[0,1]}$ is the standard [[path space]] and is a path object in the general sense of Def. \ref{PathSpaceObject}.
\end{remark}


## Examples

### In model categories
 {#InModelCategories}

If $C$ is a [[model category]] then the factorization axiom ensures that for every object $X \in C$ there is a factorization of the diagonal 

$$
  X \stackrel{\simeq}{\to} X^I \stackrel{(d_0, d_1)}{\to} X \times X
$$

with the additional property that $X^I \to X \times X$ is a fibration.

If $X$ itself is fibrant, then the projections $X \times X \to X$ are fibrations and moreover by 2-out-of-3 applied to the diagram

$$
  \array{
    && X^I
    \\
    & {}^{\mathllap{s}}\nearrow && \searrow^{\mathrlap{d_i}}
    \\
    X &&\stackrel{Id}{\to}&& X
  }
$$

are themselves weak equivalences $X^I \stackrel{\simeq}{\to} X$. This is a key property that implies the [[category of fibrant objects|factorization lemma]].

If moreover the [[small object argument]] applies in the model category $C$, then such factorizations, and hence path objects, may be chosen functorially: such that for each morphism $X \to Y$ the factorizations fit into a [[commuting diagram]]

$$
  \array{
     X &\stackrel{\simeq}{\to} &X^I &\to & X \times X  
    \\
    \downarrow && \downarrow && \downarrow
    \\
    Y & \stackrel{\simeq}{\to} & Y^I &\to & Y \times Y  
  }
$$


### In simplicial model categories

If $C$ is a [[simplicial model category]], then the [[power]]ing over [[sSet]] can be used to explicitly construct functorial path objects for fibrant objects $X$: define $X \to X^I \to X \times X$ to be the [[power|powering]] of $X$ by the morphisms

$$
  \Delta[0] \coprod \Delta[0]
  \stackrel{d_0, d_1}{\hookrightarrow} \Delta[1]
  \stackrel{\simeq}{\to} 
  \Delta[0]
$$

in $sSet_{Quillen}$. Notice that the first morphism is a cofibration and the second a weak equivalence in the standard [[model structure on simplicial sets]] and that all objects are cofibrant.

Since by the axioms of an [[enriched model category]] the [[power|powering functor]]

$$
  (-)^{(-)} : sSet^{op} \times C \to C
$$

sends cofibrations and acyclic cofibrations in the first argument to fibrations and acyclic fibrations inif the second argument is fibrant, and since this implies by the [[category of fibrant objects|factorization lemma]] that it then also preserves weak equivalences between cofibrant objects, it follows that $X^{\Delta[1]}$ is indeed a path object with the extra property that also the two morphisms $X^{\Delta[1]} \to X$ are acyclic fibrations.

## Related notions

### Right homotopies

Path objects are used to define a notion of [[right homotopy]] between morphisms in a category. Thus they capture aspects of [[higher category theory]] in a $1$-categorical context.


### Loop space objects 

From a path space object may be derived [[loop space object]]s.

## References

The general definition in [[model categories]] is due to:

* {#Quillen67} [[Daniel Quillen]], § I.1, Def. 4, p. 9 (15 of 165) in: _Axiomatic homotopy theory_ in: _[[Homotopical Algebra]]_, Lecture Notes in Mathematics 43, Springer 1967 ([doi:10.1007/BFb0097438](https://doi.org/10.1007/BFb0097438))

The terminology of "good" and "very good" path space objects appears in:

* {#DwyerSpalinski95} [[William Dwyer]], [[Jan Spalinski]], §4.12 in: *[[Homotopy theories and model categories]]* ([[DwyerSpalinski_HomotopyTheories.pdf:file]]) 

  in: [[Ioan Mackenzie James|I. M. James]], *[[Handbook of Algebraic Topology]]*, North Holland 1995 ([ISBN:9780080532981](https://www.elsevier.com/books/handbook-of-algebraic-topology/james/978-0-444-81779-2), [doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))


Lecture notes:

* *[[Introduction to Homotopy Theory]]*, around [this Def.](Introduction+to+Homotopy+Theory#PathAndCylinderObjectsInAModelCategory)


[[!redirects path object]]
[[!redirects path objects]]
[[!redirects path space object]]
[[!redirects path space objects]]

[[!redirects good path space object]]
[[!redirects good path space objects]]

[[!redirects very good path space object]]
[[!redirects very good path space objects]]

[[!redirects stable path object]]
[[!redirects stable path objects]]

[[!redirects cocylinder object]]
[[!redirects cocylinder objects]]

[[!redirects path fibration]]
[[!redirects path fibrations]]

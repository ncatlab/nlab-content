
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The notion of a _comma object_ or a _comma square_ is a generalization of the notion of a [[pullback]] or a _pullback square_ from [[category theory]] to [[2-category|2-category theory]]. It is a special kind of _[[2-limit]]_ (and, in particular, a [[PIE-limit]]).

Where a [[pullback]] involves a [[commuting diagram|commuting square]], for a comma object this square is filled by a [[2-morphism]].


## Definition

\begin{definition}\label{CommaObject}
**(comma object)**
\linebreak
A *comma object* of a pair of [[1-morphisms]] $f \colon A\to C$ and $g \colon B\to C$ in a [[2-category]] is an [[object]] $(f/g)$ equipped with [[projections]] $p \colon (f/g)\to A$ and $q \colon (f/g)\to B$ and a [[2-morphism]] of this form:

$$
\array{
  (f/g) 
  & 
    \overset{p}{\longrightarrow} 
  & 
  A 
  \\
  \mathllap{\scriptsize{q}} \big\downarrow 
  & 
  \swArrow \alpha 
  & 
  \big\downarrow   \mathrlap{\scriptsize{f}} 
  \\
  B 
  & 
  \underset{g}{\longrightarrow} 
  & 
  C
}
$$

which is [[universal property|universal]] in the sense of a [[2-limit]].  
\end{definition}
\begin{remark}\label{RelationToLaxLimits}
**(terminology)**
\linebreak
Comma objects are also sometimes called **lax pullbacks**, but this term more properly refers to a [[lax limit]] of a [[cospan]], which is a slightly different notion.
\end{remark}

\begin{remark}
**(in components)** More concretely: 

Part of Def. \ref{CommaObject} is the statement that, for any object $D$, 1-morphisms $p' \colon D\to A$, $q' \colon D\to B$, and 2-morphism $\sigma \colon f p'\Rightarrow g q'$, there is a 1-morphism $u \colon D\to(f/g)$ and isomorphisms $p u\cong p'$, $q u\cong q'$ such that, modulo these isomorphisms, we have $\sigma=\alpha u$.  

In addition, there is the "2-dimensional universality" saying that, given 1-morphisms $u \colon D\to (f/g)$ and $v \colon D\to (f/g)$ and 2-morphisms $\mu \colon p u \to p v$ and $\nu \colon q u \to q v$ such that $\alpha v. f \mu = g\nu . \alpha u$, there exists a unique 2-morphism $\beta \colon u\to v$ such that $p\beta = \mu$ and $q \beta = \nu$.

Notice that the 2-dimensional property implies that in the 1-dimensional property, [[generalized the|the]] 1-morphism $u$ is unique up to unique isomorphism. A square containing a 2-cell with this property is sometimes called a **comma square**.
\end{remark}

\begin{remark}\label{IsoCommaObjects}
By an **iso-comma object** one means the analogous notion as in Def. \ref{CommaObject}, now subject to the requirement that the [[2-morphism]] is a [[2-isomorphism]] and subject to the relevant universal property.

For more on this case see at *[[2-pullback]]*.
\end{remark}

\begin{remark}
The notion of a  **strict comma object** is analogous to that of Def. \ref{CommaObject}, but has the [[universal property]] of a [[strict 2-limit]]. This means that, given $p'$, $q'$, and $\sigma$ as above, there exists a _unique_ $u:D\to (f/g)$ such that $p u = p'$, $q u = q'$, and $\alpha u = \sigma$. Note that any strict comma object is a comma object, but the converse is not generally true.

When combining this with the constraint in Rem. \ref{IsoCommaObjects}, one also has the notion of *strict iso-comma objects*.
\end{remark}



## Properties

### Construction

The comma object $f/g$ can be constructed by means of [[pullbacks]] and [[powers]]:
$$
\array{
f/g & \to & P & \to & A \\
\downarrow & & \downarrow & & \downarrow \mathrlap{\scriptsize{f}} \\
Q & \to & C^{\mathbf{2}} & \underset{dom}{\to} & C \\
\downarrow & & \downarrow \mathrlap{\scriptsize{cod}} \\
B & \underset{g}{\to} & C
}
$$
where $C^{\mathbf{2}}$ is the power of $C$ with the arrow category $\mathbf{2} = \bullet \to \bullet$.


### Pasting lemma

Suppose we are given a diagram
$$
\array{
  P & \to & Q & \to & A \\
  \downarrow & & \mathllap{\scriptsize{p}} \downarrow & \swArrow & \downarrow   \mathrlap{\scriptsize{f}} \\
  D & \underset{h}{\to} & C & \underset{g}{\to} & B
}
$$
where the right-hand square is a comma square. Then the following are equivalent:

* The whole diagram is a comma square.
* The left-hand square is a (2-)pullback square.

The proof is analogous to that at [[pullback]].


## Examples

* In [[Cat]], a [[comma category]] is a comma object (in fact a strict one, as normally defined); these give their name to the general notion.

* In the 2-category of [[virtual double categories]], a comma object is a [[comma double category]]. If the virtual double categories are (pseudo) [[double categories]] and the domain functor $f$ in $f/g$ is strong (while $g$ might be only lax), then the comma object is also a pseudo double category and the comma object lives in the 2-category of pseudo double categories and lax functors.

## Related pages

* [[oplax/lax comma object]]

* [[representable 2-category]]

[[!include notions of pullback -- contents]]



[[!redirects comma object]]
[[!redirects comma objects]]
[[!redirects comma square]]
[[!redirects comma squares]]
[[!redirects lax pullback]]
[[!redirects lax pullbacks]]

[[!redirects strict comma object]]
[[!redirects strict comma objects]]

[[!redirects iso-comma object]]
[[!redirects iso-comma objects]]

[[!redirects isocomma object]]
[[!redirects isocomma objects]]

[[!redirects iso-comma-object]]
[[!redirects iso-comma-objects]]


[[!redirects strict iso-comma object]]
[[!redirects strict iso-comma objects]]

[[!redirects strict isocomma object]]
[[!redirects strict isocomma objects]]

[[!redirects strict iso-comma-object]]
[[!redirects strict iso-comma-objects]]


[[!redirects bi-iso-comma object]]
[[!redirects bi-iso-comma objects]]

[[!redirects bi-iso-comma-object]]
[[!redirects bi-iso-comma-objects]]





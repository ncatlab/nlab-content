
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


\tableofcontents

## Definition

In evident variation of the notion of *[[pointed objects]]*, a **bi-pointed object** in a [[category]] $V$ with [[terminal object]] $pt$ is a [[co-span]] from $pt$ to itself, i.e. a [[diagram]] of this form:

$$
  \array{
    && S
    \\
    & {}^{\sigma_S}\nearrow && \nwarrow^{\tau_S}
    \\
    pt &&&& pt
  }
  \,.
$$

Similarly, a [[pointed object]] in a category with [[initial object]] $\varnothing$ and terminal object $pt$ may be regarded as a co-span from $\varnothing$ to $pt$. 

If $V$ has in addition binary [[coproducts]] then a bi-pointed object in $V$ is the same as a [[co-span]] from $\varnothing$  to the [[coproduct]] $pt \sqcup pt$.

### In more general monoidal categories

One can consider [[generalised elements]] out of an object $I$, where we do not require $I$ to be the [[terminal object]], a **bi-pointed object** is a [[co-span]] from $I$ to itself, i.e. a [[diagram]] of this form:

$$
  \array{
    && S
    \\
    & {}^{\sigma_S}\nearrow && \nwarrow^{\tau_S}
    \\
    I &&&& I
  }
  \,.
$$

In many cases, $I$ would be a [[tensor unit]] of a [[monoidal category]], in which case the pointed objects are [[pointed objects in a monoidal category]]. 

## Examples

* The [[subobject classifier]] $\Omega$ and the [[Sierpinski space]] $\mathbb{S}$ in the category of [[choice object|choice sets]] are bi-pointed objects. 

* In general, any non-degenerate subobject classifier in a topos or pretopos is a bi-pointed object.

* Any [[interval object]] is a bi-pointed object with a [[2-morphism]] connecting the two global elements. 

* The [[boolean domain]] is the [[initial object|initial]] bi-pointed object in [[Set]].

## Closed structure

From the [[bicategory]] structure on [[co-span]]s in $V$ bi-pointed objects in $V$ naturally inherit the structure of a monoidal category

$$
  BiPointed(V) = End_{CoSpan(V)}(pt)
  \,.
$$

Assume that the terminal object $pt$ is the tensor unit in $V$.

Then moreover, following the construction of the $V$-internal hom of [[pointed object]]s and being a special case of that of [[co-span]]s in $V$, there is an internal [[hom-object]]
${}_{pt}[X,Y]_{pt} \in Obj(V)$
of bipointed objects $X$ and $Y$ defined as the pullback

$$
\array{ 
  {}_{pt}[X,Y]_{pt} 
   & \longrightarrow & 
  pt \sqcup pt
  \\
  \Big\downarrow 
    && 
  \Big\downarrow\mathrlap{{}^{\sigma_Y \sqcup \tau_Y}}
  \\
  [X,Y] 
  & 
  \underset
    {\sigma_X^* \times \tau_X^*}
    {\longrightarrow} 
  & 
  [pt \sqcup pt,Y].}
$$

Here the [[map]] 
$pt \sqcup pt \stackrel{\sigma_Y \sqcup \tau_Y}{\to} 
[pt \sqcup pt,Y]$ 
is [[adjunct]] to 
$\pt \otimes (pt \sqcup pt) \to pt \sqcup pt 
\stackrel{\sigma_Y \sqcup \tau_Y}{\to} Y$.  

This $V$-object ${}_{pt}[X,Y]_{pt}$ is itself naturally bi-pointed with the bi-point $pt \sqcup pt \to {}_pt[X,Y]_{pt}$ given by the morphism induced from the above pullback diagram by the commuting diagram

$$
  \array{
     pt \sqcup pt 
     &
       \overset{Id}{\longrightarrow}& 
     pt \sqcup pt
     \\
     \Big\downarrow\mathrlap{{}^{\sigma_X \sqcup \sigma_X}}
     && 
     \Big\downarrow\mathrlap{{}^{\sigma_Y \sqcup \tau_Y}}
     \\
     [X,Y]
     &
     \underset
       {\sigma_X^* \times \sigma_Y^*}
       {\longrightarrow}
     &
     [pt \sqcup pt, Y],
  }
  
$$

where the morphism 
$pt \sqcup pt \stackrel{\sigma_X \sqcup \sigma_X}{\to}
[X,Y]
$ is [[adjunct]] to 
$
  X \otimes (pt \sqcup pt)
  \to
  pt \otimes (pt \sqcup pt)
  \simeq pt \sqcup pt
  \stackrel{\sigma_Y \sqcup \tau_Y}{\to}
  Y
$. 

## See also

* [[pointed object]]

* [[boolean domain object]]

* [[bi-pointed type]]

* [[bi-pointed set]]

[[!redirects bipointed object]]
[[!redirects bipointed objects]]

[[!redirects bi-pointed object]]
[[!redirects bi-pointed objects]]
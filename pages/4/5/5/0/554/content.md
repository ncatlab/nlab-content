#Definition#

A **bi-pointed object** in a category $V$ with terminal object $pt$ is a [[co-span]] from $pt$ to itself, i.e. a diagram

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

Similarly, a [[pointed object]] in a category with initial object $\emptyset$ and terminal object $pt$ is a co-span from $\emptyset$ to $pt$, and if $V$ has in addition binary [[coproduct]]s then a bi-pointed object in $V$ is the same as a [[co-span]] from $\emptyset$ to $pt \sqcup pt$.

#Examples#

* The [[subobject classifier]] $\Omega$ and the [[Sierpinski space]] $\mathbb{S}$ in the category of [[axiom of choice|choice sets]] are bi-pointed objects. 

* In general, any non-degenerate subobject classifier in a topos or pretopos is a bi-pointed object.

* Any [[interval object]] is a bi-pointed object with a [[2-morphism]] connecting the two global elements. 

* A [[two-valued object]] is an [[initial object|initial]] bi-pointed object.

#Closed structure#

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
   & \rightarrow & pt \sqcup pt\\
  \downarrow && \downarrow^{\sigma_Y \sqcup \tau_Y}
  \\
  [X,Y] & 
  \stackrel{\sigma_X^* \times \tau_X^*}
  {\rightarrow} & [pt \sqcup pt,Y]}
  \,.
$$

Here the map 
$pt \sqcup pt \stackrel{\sigma_Y \sqcup \tau_Y}{\to} 
[pt \sqcup pt,Y]$ 
is [[adjunct]] to 
$\pt \otimes (pt \sqcup pt) \to pt \sqcup pt 
\stackrel{\sigma_Y \sqcup \tau_Y}{\to} Y$.  

This $V$-object ${}_{pt}[X,Y]_{pt}$ is itself naturally bi-pointed with the bi-point $pt \sqcup pt \to {}_pt[X,Y]_{pt}$ given by the morphism induced from the above pullback diagram by the commuting diagram

$$
  \array{
     pt \sqcup pt &\stackrel{Id}{\to}& pt \sqcup pt
     \\
     \downarrow^{\sigma_X \sqcup \sigma_X} 
     && \downarrow^{\sigma_Y \sqcup \tau_Y}
     \\
     [X,Y]
     &\stackrel{\sigma_X^* \times \sigma_Y^*}{\to}&
     [pt \sqcup pt, Y]
  }
  \,,
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
$

## See also

* [[two-valued object]]

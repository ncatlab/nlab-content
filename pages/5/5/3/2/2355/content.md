
#Idea#

The notion of adjunction between two [[(∞,1)-functor]]s generalizes the notion of [[adjoint functor]]s from [[category theory]] to [[(infinity,1)-category|(∞,1)-category theory]].

There are many equivalent definitions of the ordinary notion of [[adjoint functor]]. Some of them have more ovvious generalizations to [[higher category theory]] than others. A useful one is the characterization of adjoint functors  in terms of their [[cograph of a functor|cograph]]s. Recall from the discussion at [[cograph of a functor]] that two functors $L : C \to D$ and $R : D \to C$ are [[adjoint functor]]s precisely if the cograph of $L$ coincides with the cograph of $R$ up to the obvious reversal of arrows

$$
  (L \vdash R) \Leftrightarrow
  (cograph(L) \simeq cograph(R^{op})^{op})
  \,.
$$

Since the notion of cograph has a rather straightforward generalization to the context of [[(infinity,1)-category|(∞,1)-categories]] this immediately leads to a definition of adjoint [[(infinity,1)-functor|(∞,1)-functors]].


# Definition #

Let $C$ and $D$ be [[(infinity,1)-category|(∞,1)-categories]]. An **adjunction** between $C$ and $D$ is 

* an [[(∞,1)-functor]] $K \to I$ to the [[interval category]] $I = \{0 \to 1\}$ which is a [[Cartesian fibration]] and a [[coCartesian fibration]]

* together with equivalences $C \stackrel{\simeq}{\to} K_{\{0\}}$ and $D \stackrel{\simeq}{\to} K_{\{1\}}$.

Two [[(∞,1)-functor]]s $L : C \to D$ and $R : D \to C$ are called **adjoint** -- with $L$ _left adjoint_ ro $R$ and $R$ _right adjoint_ to $L$ if

* there exists an adjunction $K \to I$ in the above sense

* and $K$ is the [[cograph of a functor|cograph]] of $L$ and the opposite of the cograph of $R^{op}$.

#References#

This is definition 5.2.2.1 in 

* [[Jacob Lurie]], [[Higher Topos Theory]] .

There the statement "$K$ is the cograph of $L$" is phrased as "$L$ is associated to $K$". See the discussion at [[cograph of a functor]] for details on this.

[[!redirects adjoint (∞,1)-functor]]
[[!redirects adjoint (infinity,1)-functors]]
[[!redirects adjoint (∞,1)-functors]]
[[!redirects characteristic functions]]
[[!redirects characteristic morphism]]
[[!redirects indicator functions]]
[[!redirects indicator function]]

The __characteristic function__ of a [[subset]] $U$ of some [[set]] $X$ is a [[function]] from $X$ to the set $TV$ of [[truth values]] (which classically is $TV = \{\bot,\top\}$) that takes $a$ in $X$ to the truth value of the statement that $a \in U$.  That is,
$$ \chi_U(a) \;\Leftrightarrow\; a \in U ,$$
where $\chi_U$ (also often $1_U$) is the characteristic function of $U$.

More generally, the __characteristic morphism__ of a [[subobject]] $U$ of some objects $X$ in a category with a [[subobject classifier]] $\Omega$ is the morphism from $X$ to $\Omega$ that classifies $U$; we have that
$$ \array {
  U          & \hookrightarrow    & X \\
  \downarrow &                    & \downarrow & \chi_U \\
  1          & \underset{\top}\to & \Omega
} $$
is a [[pullback]] square.

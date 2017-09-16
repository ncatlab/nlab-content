#Definition#

Let $B$ be a  [[bicategory]] with a class $W$ of 1-[[morphism|cells]]. $W$ is said to **admit a right calculus of fractions** if it satisfies the following conditions

* [2CF1.] $W$ contains all equivalences
* [2CF2.]
   * a) $W$ is closed under composition
   * b) If $a\in W$ and a iso-2-cell $a \stackrel{\sim}{\Rightarrow} b$ then $b\in W$
* [2CF3.] For all $w: A' \to A$, $f: C \to A$ with $w\in W$ there exists a 2-commutative square
$$
\begin{matrix}
  P& \stackrel{g}{\to} & A' \\
  v \downarrow&\Rightarrow &\, \downarrow w\\
  C &\underset{f}{\to} & A
\end{matrix}
$$
with $v\in W$.
* [2CF4.] If $\alpha: w \circ f \Rightarrow w \circ g$ is a 2-cell and $w\in W$ there is a 1-cell $v \in W$ and a 2-cell $\beta: f\circ v \Rightarrow g \circ v$ such that $\alpha\circ v = w \circ \beta$. Moreover: when $\alpha$ is an iso-2-cell, we require $\beta$ to be an isomorphism too; when $v'$ and $\beta'$ form another such pair, there exist 1-cells $u,\,u'$ such that $v\circ u$ and $v'\circ u'$ are in $W$, and an iso-2-cell $\epsilon: v\circ u \Rightarrow v' \circ u'$ such that the following diagram commutes:
$$
\begin{matrix}
f \circ v \circ u & \stackrel{\beta\circ u}{\Rightarrow} & g\circ v \circ u \\
f\circ \epsilon \Downarrow \simeq && 
\simeq \Downarrow g\circ \epsilon \\
\\
f\circ v' \circ u' &\underset{\beta'\circ u'}{\Rightarrow}& g\circ v' \circ u'
\end{matrix}
$$

If $B$ is a category, then these axioms reduce to the ones of Gabriel and Zisman for a [[category of fractions]].


Given such a setup, in the article _Etendues and stacks as bicategories of fractions_, Pronk constructs the [[localization]] of $B$ at $W$.



#Example#

Let $S$ be a category with binary products and pullbacks together with a class of [[davidroberts:class of admissible maps|admissible maps]] $E$.

+-- {: .un_theorem}
######Theorem: 
The 2-catgeories $Cat(S)$ and $Gpd(S)$ of categories and groupoids internal to $S$ admit [[bicategory of fractions|bicategories of fractions]] for the class of $E$-[[davidroberts:weak equivalence|equivalences]].
=--

The resulting localization is equivalent to the bicategory of [[anafunctor|anafunctors]] in $S$. For details, see [[davidroberts:anafunctors.pdf:file]] 
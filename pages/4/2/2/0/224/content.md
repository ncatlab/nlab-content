Given a set $G$, an _$G$-graded vector space_ is a map $V$
assigning to each element $g \in G$ a vector space $V_g$.  Given $G$-graded vector spaces $V$ and $W$, a morphism $f : V \to W$ assigns to each element $g \in G$ a linear operator $f_g : V_g \to W_g$.

In other words, a $G$-graded vector space is a functor $V: G \to Vect$, where the set $G$ is treated as a [[discrete category]], and [[Vect]] is the category of vector spaces. Similarly, a morphism of $G$-graded vector spaces is a natural transformation between such functors.  In short, the category of $G$-graded vector spaces is the [[functor category]] $Vect^G$.  

People are usually interested in $G$-graded vector spaces when the set $G$ is equipped with extra structure.  If the set $M$ is a [[monoid]], $Vect^G$ is a [[monoidal category]].  If $G$ is a commutative monoid, $Vect^G$ is a [[symmetric monoidal category]].  If $G$ is a group, every finite-dimensional $G$-graded vector space has a [[left dual object|left dual]] and a [[right dual object|right dual]].  And if $G$ is an abelian group, these duals coincide.

By far the most widely-used examples are $G = \mathbb{Z}$ and $G = \mathbb{N}$.  Indeed, the term _graded vector space_ is often used to mean a $G$-graded vector space with one of these choices of $G$.  The case $G = \mathbb{Z}/2$ is also important: a $\mathbb{Z}/2$-graded vector space is also called a [[super vector space]].

It is also interesting to consider $G$-graded objects in other categories.  A _$G$-graded object_ in the category $C$ is a functor $F :G \to C$, and the category of $G$-graded objects in $C$ is the [[functor category]] $C^G$.

#Remarks#

For the case that $G$ is a group,
this means that the category of $G$-graded vector spaces is a [[vertical categorification|categorification]] of the [[category algebra|group algebra]] of $G$, where numbers are replaced by vector spaces. Recalling from the remark in [[category algebra]] that the group algebra of a group can be identified with the monoid of spans of the form
$$
  \array{
     && G
     \\
     & \swarrow && \searrow
     \\
     pt &&\Rightarrow&& pt
     \\ 
     & \searrow && \swarrow
     \\
     &&
     Vect
  }
\,,
$$
where $pt \to Vect$ goes to the ground field $k$,
the monoidal category of $G$-graded vector spaces can be identified with the monoid of spans of the form
$$
  \array{
     && G
     \\
     & \swarrow && \searrow
     \\
     pt &&\Rightarrow&& pt
     \\ 
     & \searrow && \swarrow
     \\
     &&
     2Vect
  }
  \,.
$$
Here $2Vect$ denotes some version of the category of 2-vector spaces with the property that the category $Vect$ is one of its objects and such that $End_{2Vect}(Vect) \simeq Vect$ (in analogy to how $End_{Vect}(k) \simeq k$) and $pt \to 2Vect$ maps to $Vect$. Possible choices for $2Vect$ is the 2-category of [[Kapranov-Voevodsky 2-vector space]]s or the bigger bicategory of [[bicategory of algebras and bimodules|algebras and bimodules]].
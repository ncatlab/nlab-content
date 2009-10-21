#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Quillen equivalence is the right notion of [[equivalence]] for [[model category|model categories]].  Most importantly, it is weaker than [[equivalence of categories]].  The work of Dwyer--Kan, Bergner and others has shown that Quillen equivalent model categories [[presentable (infinity,1)-category|present]] equivalent [[(infinity,1)-category|(infinity,1)-categories]].

#Definition#

Let $C$ and $D$ be [[model category|model categories]] and let

$$
  D \stackrel{G}{\to} C
$$
$$
  D \stackrel{F}{\leftarrow} C
$$
be a [[Quillen adjunction]] with $F$ [[left adjoint]] to $G$.

Write $h C$ and $h D$ for the corresponding [[homotopy category|homotopy categories]].

Notice that

* $h C$ may be regarded as obtained by first passing to the full [[subcategory]] on cofibrant objects and then inverting weak equivalences

* $F$ (being a left Quillen adjoint) preserves weak equivalences between cofibrant objects

* so that it induces a functor $L F : h C \to h D$ between the [[homotopy category|homotopy categories]]: its total left [[derived functor]].

* Similarly (but dually) for $G$ and its right total derived functor $R G : h D \to h C$.

The Quillen adjunction $(F,G)$ is a **Quillen equivalence** if the following equivalent conditions are satisfied

* the total left [[derived functor]] $L F : h C \to h D$ is an [[equivalence of categories]];

* the total right [[derived functor]] $R G : h D \to h C$ is an [[equivalence of categories]];

* for every cofibrant object $c \in C$ and every fibrant object $d \in D$ a morphism $c \to G(d)$ is a weak equivalence in $C$ precisely is the [[adjunct]] morphism $F(c) \to d$ is a weak equivalence in $D$.

[[!redirects Quillen equivalences]]
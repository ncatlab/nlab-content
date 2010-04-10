
#Contents#
* automatic table of contents goes here
{:toc}

## Triangulation

A **triangulation** of a [[topological space]] $Y$ is a [[simplicial set]] $X$ together with a [[homeomorphism]] $h: R X \to Y$, where $R$ denotes the [[geometric realization]] [[functor]]. 

(Often $Y$ here is taken to be a [[simplicial complex]], but the difference does not really matter here.)

Explicitly, $R X$ is given by a [[coend]] formula 

$$\int^{n \in \Delta} X(n) \cdot \sigma(n)$$ 

where $\sigma: \Delta \to Top$ is the standard affine [[simplex]] functor.

## Cubulation

Similarly, a **cubulation** of a [[topological space]] $Y$ is a [[cubical set]] $C$ together with a [[homeomorphism]] $h: R_{cub}C \to Y$ where $R_{cub}$ denotes the realization functor for [[cubical set]]s $Set^{\Box^{op}}$. Explicitly, $R_{cub}C$ is given by a [[coend]] formula 

$$R_{cub}C = \int^{m \in Cube} C(m) \cdot \Box(m)$$ 

where $\Box: Cube \to Top$ is the standard geometric cube functor.

## Relation between triangulation and cubulation

There is a "cubulation" functor for standard simplices, $\Sigma: \Delta \to Set^{\Box^{op}}$, such that the affine simplex functor $\sigma: \Delta \to Top$ is naturally isomorphic to the composite 

$$\Delta \stackrel{\Sigma}{\to} Set^{\Box^{op}} \stackrel{R_{cub}}{\to} Top$$ 

Given a triangulation $(X, h: R X \to Y)$ of a space $Y$, we have [[isomorphism]]s 

$$\array{
Y & \cong & \int^n X(n) \cdot \sigma(n) \\
 & \cong & \int^n X(n) \cdot (\int^m \Sigma_n(m) \cdot \Box(m)) \\
 & \cong & \int^m (\int^n X(n) \cdot \Sigma_n(m)) \cdot \Box(m) 
}$$ 

where in the last line we used the [[coend Fubini theorem]] for interchange of coends. Thus, defining the cubical set $C$ by 

$$C(m) = \int^n X(n) \cdot \Sigma_n(m)$$ 

we have a homeomorphism $Y \cong \int^m C(m) \cdot \Box(m) = R_{cub} C$, i.e., we obtain a cubulation of $Y$. 


The functor $\Sigma$ effectively regards an $n$-simplex as an iterated [[join of simplicial sets]] and then produces the analogous join in the category of cubical sets. This for instance regards the 2-simplex as a square with one degenerate edge.

For that recall that one way of defining the affine simplex functor $\sigma: \Delta \to Top$ is by taking advantage of the fact that the augmented $\Delta$ (containing the object $[-1]$) is the walking [[monoid]], so all we need to do is cook up an appropriate monoidal structure on $Top$ and a monoid therein, and the walking monoid property takes care of the rest: we get an induced monoidal functor $\sigma: \Delta: \to Top$. So: take the monoidal product on $Top$ to be "topological simplicial join": the join $X \star Y$ of two spaces $X$, $Y$ may be defined for our purposes by pushout of the diagram 

$$X \stackrel{\pi_1}{\leftarrow} X \times Y \stackrel{1_X \times \{0\} \times 1_Y}{\to} X \times I \times Y \stackrel{1_X \times \{1\} \times 1_Y}{\leftarrow} X \times Y \stackrel{\pi_2}{\to} Y$$ 

and now take the monoid in $Top$ to be the 1-point space with its unique monoid structure. 

Now mimic this construction for cubical sets in the following way: there is a promonoidal structure on the site $Cube$ where, if $X$, $Y$ are objects of $Cube$, we define $X \star Y$ to be the pushout (in cubical sets) of the same diagram as above (but replacing $\times$ by the monoidal product $\otimes$ of $Cube$). Note that even though $\otimes$ is not cartesian product in $Cube$ (because $Cube$ lacks diagonals), the monoidal unit $1$ of Cube is terminal, so we do have "projection maps" to work with to produce the analogous diagram in $Cube$ (the $I$ is the monoidal generator of $Cube$). This promonoidal product on $Cube$ induces a monoidal product on cubical sets which I'll call "cubical simplicial join". As before, the terminal cubical set is a monoid with respect to this monoidal product, so by the walking monoid property we obtain a monoidal functor 

$$\Sigma: \Delta \to Set^{Cube^{op}}$$ 

which plays a role analogous to the affine simplex functor into $Top$. 

The crucial observation is that geometric realization $R_{cub}: Set^{Cube^{op}} \to Top$ takes cubical simplicial joins to topological simplicial joins, when restricted to the full subcategory given by the essential image of $\Sigma$. By definition, $R_{cub}$ takes $\otimes$ on representable objects to cartesian products of geometric cubes, and preserves colimits and in particular pushouts. So it takes cubical simplicial joins of *representable* cubical sets to topological simplicial joins. It is not unfortunately not generally true that 

$$R_{cub}(X \star Y) \cong R_{cub}(X) \star R_{cub} Y \qquad (1)$$ 

for general cubical sets $X$, $Y$; for example, if $X = 0$ is initial, then the left side is initial but the right side is isomorphic to $R_{cub}(Y)$. Basically, the problem is that topological simplicial join $\star$ does not preserve all colimits in each of its separate arguments. It does however preserve *connected* colimits in each of its separate arguments. Therefore, the isomorphism (1) obtains if $X$ and $Y$ are connected colimits of representables, and in particular applies when $X$ and $Y$ belong to the essential image of $\Sigma$.  

We conclude that $\sigma: \Delta \to Top$ and $R_{cub} \circ \Sigma: \Delta \to Top$ take monoidal products in $\Delta$ to topological simplicial joins, and both take the walking monoid of $\Delta$ to the one-point space. By the universal property of $\Delta$, it follows that these functors are naturally isomorphic (as monoidal functors, even), which is what we wanted to show.






[[!redirects cubulation]]
[[!redirects triangulations]]
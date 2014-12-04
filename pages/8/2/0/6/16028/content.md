

This entry is going to become an exposition to the topics of 

1. [[Cartan geometry]];

1. higher dimensional [[supergravity]];

1. the [[brane scan]].

and an indication of how these all naturally flow out of a common source when considered in [[higher differential geometry|higher differential]] [[supergeometry]].

> However, for the time being this entry is under construction and mostly non-existent.  Nothing to be seen here yet, please move to another entry.


[[manifolds]], such as [[spacetimes]], are modeled on the [[real line]] and its [[products]], the [[Cartesian spaces]] $\mathbb{R}^n$. (see also at _[[geometry of physics -- coordinate systems]]_).

It is clear that here it is crucial that $\mathbb{R}^n$ is regarded with its [[smooth structure]].

But $\mathbb{R}^n$ also has ([[smooth group|smooth]]) _[[group]]_ structure. As such it is the [[translation group]]. In [[Newtonian mechanics]] this group structure plays a key role, as it allows for instance to say what in means that a [[particle]] propagates along a straight [[trajectory]].

With the dawn of [[general relativity]] and its "[[general covariance]]" it was finally understood that this is a bit too naive: [[free field|free]] [[particles]] propagate on straight lines in $\mathbb{R}^n$ only [[infinitesimal object|infinitesimally]]. After every infinitesimal translation, the notion of "straight" needs to be adjusted.

This has a straightforward visualization in 2-dimensions: visualize a bumpy [[surface]] $X$ [[embedding|embedded]] in $\mathbb{R}^3$ (for instance a [[2-sphere]]). Pick a point $x \in X$ and visualize the [[tangent]] [[plane]] to that point, which is an $\mathbb{R}^2$. Now given a [[curve]] in $X$ that emanates from $x$, then one may visualize the plane to be "rolling without sliding" on $X$ such that the point where it touches $X$ follows the curve.

Under this map from curves in the plane to curves in the $X$, straight lines in $\mathbb{R}^2$ now map to [[geodesics]] in $X$. These are the actual paths that free particles in $X$ follow.

The most popular way to formalize this is the modern concept of the [[Levi-Civita connection]] of the [[Riemannian metric]] on $X$ (which in the above example is induced from the canonical one on the embedding space $\mathbb{R}^3$).

But [[Élie Cartan]]'s original way of speaking about [[affine connections]] much closer resembles this picture of a "local model space with group structure" doing "rolling without slipping" over [[spacetime]]. This is now mostly called a _[[Cartan connection]]_.

Here one regards the [[Euclidean group]] $Iso(n)$ of all [[isometries]] of $\mathbb{R}^n$. Inside this is the [[rotation group]] $SO(n) \hookrightarrow Iso(n)$. The [[quotient group]] is [[Cartesian space]]

$$
  \mathbb{R}^n \simeq Iso(n)/SO(n)
  \,.
$$

The structure of "rolling without sliding" is then formalized by saying 

1. **rolling** -- there is an $Iso(n)$-[[principal connection]] on $X$ (the group $Iso(n)$, via its [[action]]  on $\mathbb{R}^n$, rolls and slides the Cartesian space around);

1. **without sliding** -- such that there is a [[reduction of the structure group]] to $SO(n)$ (this makes the original $Iso(n)$-bundle be have [[associated bundle|associated]] to it the actual $\mathbb{R}^n$-[[fiber bundle]]);

  and such that under this reduction the connection at each point infinitesimally identifies the [[tangent space]] of $X$ with the abstract copy of $\mathbb{R}^n \simeq Iso(n)/SO(n)$.

This has an evident heneralization where we conisder any inclusion $H \hookrightarrow G$ of [[Lie groups]]. If one considers instead of [[Cartesian space]] $\mathbb{R}^n$ the [[Minkowski space]] $\mathbb{R}^{n-1,1}$, then $Iso(n-1,1)$ is the [[Poincaré group]]. and $SO(n-1,1)$ is the [[Lorentz group]]. Now the [[geodesics]] via [[parallel transport]] along a $(SO(n-1,1)\hookrightarrow Iso(n-1,1))$-[[Cartan connection]] reflect the [[force]] of [[gravity]] in the [[theory (physics)|theory]] of [[general relativity]].

Many other combinations $(H \hookrightarrow G)$ may be considered. For instance


* the [[Cartan geometry]] induced by the orthochonous [[Lorentz group]] with the [[stabilizer subgroup]] of a [[lighlike]] ray is _[[conforam connections]]_;

* the [[Cartan geometry]] induced by [[parabolic subgroup]] inclusions gives _[[parabolic geometry]]._

In the contemporary [[physics]] literature this concept of [[Cartan connection]] may seem to play an orphaned role, at least if one compares the number of occurences of this term in the physics literature over that of "[[Levi-Civita connection]]",and certainly when compared to the number of contemporary articles that speak of [[geodesics]] with any concept of [[connection]] made explicit.

However, this is partly an illusion. Examination of the literature shows that at least as soon as authors consider _[[supergravity]]_, then everything is really secretly formulated in terms of [[Cartan geometry]], as only in this formulation is the incorporation of [[fermions]] and  of [[supersymmetry]] really natural.




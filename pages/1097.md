#Definition#

Given a [[topological space]] $X$, the **category of open subsets** $Op(X)$ of $X$ is the [[category]] whose

* [[object]]s are the open subsets $U \hookrightarrow X$ of $X$;

* [[morphism]]s are the inclusions 
$
  \array{
     V &&\hookrightarrow && U
     \\
     & \searrow && \swarrow
     \\
     && X
  }
$ of open subsets into each other.

#Remarks#

* The category $Op(X)$ is a [[poset]].

* The category $Op(X)$ is naturally equipped with the
structure of a [[site]], where a collection $\{U_i \to U\}_i$ of morphisms is a cover precisely if their [[union]] in $X$ equals $U$:
$$ \bigcup_i U_i = U .$$
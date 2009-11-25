#Idea#

The _join_ of two categories $C$ and $C'$ is obtained from the [[disjoint union]] of $C$ with $C'$ by throwing in a unique morphism from every object of $C$ to every object of $C'$.

#Definition#

The **join** of [[category|categories]] $C$ and $C'$ is the category with

* objects $Obj(C \star C') := Obj(C) \amalg Obj(C')$;

* morphisms given by
$$
  Mor_{C \star C'}(a,b) :=
  \left\lbrace
    \array{
      Mor_C(a,b) & if a,b \in C
      \\
      Mor_{C'}(a,b) & if a,b \in C'
      \\
      \emptyset & if a \in C', b \in C;
      \\
      \mathrm{pt} & if a \in C, b \in C';
    }
  \right.
$$

#Examples#

* The **cone** below a category $C$ is the join $C \star \mathrm{pt}$. The cone above $C$ is the join $\mathrm{pt} \star C$. 

#References#

See [p. 42](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=42) of 

* J. Lurie, _Higher topos theory_ ([arXiv](http://arxiv.org/abs/math.CT/0608040))
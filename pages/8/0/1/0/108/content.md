
 ... general discussion goes here ...


##(Co)descent as homotopy (co)limit ##

**In weak $\infty$-categories**

Fundamentally the $\infty$-category of descent data associated to a simplicial hypercover $Y^\bullet$ of $Spaces$ and a (pseudo)preshaf $A : Spaces^\op \to \infty Cat$ should be the _weak limit_ or _homotopy limit_ 
$$
  Desc(Y^\bullet,\mathbf{A}) := lim_{[n \in \Delta]} \mathbf{A}(Y^n)
  \,.
$$

Similarly the $\infty$-category of codescent data should be a _weak colimit_ or _homotopy colimit_.

In a suitable context of weak $\infty$-categories this weak limit can be realized intrincsically. See for instance

* Bertran To&#235;en, _Higher and derived stcks: a global overview_ ([page 12](http://arxiv.org/PS_cache/math/pdf/0604/0604504v3.pdf#page=12))

**In strict $\infty$-categories**

But there is also a way to realize this naturally in the [[semi-strict|more strict]] context of [[omega category|omega categories]] using [[oriental]]s and other cosimplicial $\omega$-categories. This was introduced in

* Ross Street, _The algebra of oriented simplices_

and reviewed and expanded on

* Ross Street, _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math.CT/0303175)).

Using language of [[enriched category theory]] Street's construction of the $\omega$-category of descent data is given by the [[end]]

$$
  Desc(Y^\bullet, \mathbf{A}) := 
   \int_{[n]\in \Delta}
   hom(O(\Delta^n), \mathbf{A}(Y^n)) 
  \,.
$$

(Dominic Verity kindly provided help in obtaining this coend-reformulation).

For the moment, more details about this [[omega-category|omega categorical]] notion of descent and codescent is relegated to [[schreiber:Differential Nonabelian Cohomology]].
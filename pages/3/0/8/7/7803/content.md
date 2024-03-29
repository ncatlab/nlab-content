
Funcoids were first named and studied by [[Victor Porton]], an independent researcher, as an approach to [[general topology]], in particular as a massive generalisation of [[proximity spaces]], [[pretopological spaces]], etc. -- somewhat along the same lines described at [[syntopogenous space]] where nearness notions are taken to be primitive. 

Let $\mathfrak{F}(A)$ and $\mathfrak{F}(B)$ be the [[reverse lattices of filters]] for the [[sets]] $A$ and $B$.

Then a __funcoid__ from $A$ to $B$ consists of [[functions]] $\alpha\colon \mathfrak{F}(A) \to \mathfrak{F}(B)$ and $\beta\colon \mathfrak{F}(B) \to \mathfrak{F}(A)$ such that
$$\forall\mathcal{X}\in\mathfrak{F}(A),\mathcal{Y}\in\mathfrak{F}(B): (\mathcal{Y}\sqcap\alpha \mathcal{X} \ne 0^{\mathfrak{F}(A)} \Leftrightarrow \mathcal{X}\sqcap\beta \mathcal{Y} \ne 0^{\mathfrak{F}(B)}).$$
That is, for every [[filter]] $\mathcal{X}$ on $A$ and every filter $\mathcal{Y}$ on $B$, the filter (on $B$) generated by the [[union]] of $\mathcal{Y}$ and $\alpha(\mathcal{X})$ is not the entire [[power set]] $\mathcal{P}(B)$ iff the filter (on $A$) generated by the union of $\mathcal{X}$ and $\beta(\mathcal{Y})$ is not the entire power set $\mathcal{P}(A)$.

The above formulation is due to [[Victor Porton]]. A slight reformulation is that funcoids can be seen as morphisms between certain types of [[Chu spaces]]. [[Todd Trimble]] has written some notes on funcoids from this point of view [here](http://ncatlab.org/toddtrimble/published/topogeny), where they are also shown to be equivalent to [[topogenous relations]] provided that the reflexivity condition of the latter is dropped (which is reasonable from an abstract perspective). The category of endofuncoids and continuous functions, and the full subcategory of reflexive endofuncoids, are each [[topological functor|topological]] over $Set$. 

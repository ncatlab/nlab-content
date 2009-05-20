## Statement 

The **Tychonoff theorem** is a theorem of topology, which says that a [[product]] of [[topological space|spaces]] indexed over a set is [[compact space|compact]] if each of the spaces is compact. 

The Tychonoff theorem is one of many theorems which in Zermelo [[set theory]] is equivalent to the [[axiom of choice]]. 

## Proof via ultrafilter convergence 

One method of proof uses ultrafilter convergence. Let $\{X_\alpha\}_{\alpha \in A}$ be a collection of compact spaces. 

* Every ultrafilter $U_\alpha$ on the underlying set of $X_\alpha$ converges to some point $x_\alpha$. (If not, then $U_\alpha$ contains a closed set $C_x$ in the complement of each point $x$. The intersection of all the $C_x$ is empty. Thus some finite subcollection of the $C_x$ is empty, by compactness. But then $U_\alpha$, being closed under finite intersections, contains the empty set, contradiction.) 

* Let $U$ be an ultrafilter on $\prod_\alpha X_\alpha$. Since the set-of-ultrafilters construction $X \mapsto \beta X$ is functorial, we have a push-forward ultrafilter $U_\alpha = \beta(\pi_\alpha)(U)$ on each $X_\alpha$. Choose a point $x_\alpha$ to which $U_\alpha$ converges. Then it is easily checked that $U$ converges to the point $\langle x_\alpha \rangle$ in the product space. 

* Since every ultrafilter $U$ on $\prod_\alpha X_\alpha$ converges to a point, the product is compact. (If it were not, then we could find a collection of nonempty closed sets whose intersection is empty, but closed under finite intersections. This collection generates a filter which is contained in some ultrafilter $U$, by the [[ultrafilter theorem]]. Since every ultrafilter $U$ converges to some $x$, it cannot contain any closed set in the complement of $x$, hence cannot contain some closed set in the original collection, contradiction.) 

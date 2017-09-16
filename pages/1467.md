## Idea

A compact space is a [[topological space]] in which every [[net]] has a convergent subnet. It is a kind of ultimate topological expression of the general idea of a space being "bounded" in extent: every net must accumulate somewhere in the space (must frequently get close to some point $x$). 

## Definitions 

There are many ways to characterize compactness. The first is perhaps the most common: 

* $X$ is **compact** if for every collection of open sets whose union is $X$ (which _covers_ $X$), there is a finite subcollection which also covers $X$. 

This is easily equivalent to: 

* $X$ is compact if, for any collection of closed sets of $X$ whose intersection is empty, some finite subcollection also has empty intersection. 

If the axiom of choice is assumed, compactness can be characterized in terms of [[ultrafilter|filter]] convergence: 

* $X$ is compact if every ultrafilter $\cal{U}$ on $X$ converges to some point $x \in X$, meaning that $\cal{U}$ contains the neighborhood filter of $x$. 

Similarly (but without assuming AC), 

* $X$ is compact if every filter on $X$ has a convergent refinement. 

This is similar in tone to the characterization given above: 

* $X$ is compact if every net in $X$ has a convergent subnet. 

Assuming the axiom of choice, compactness can also be characterized in terms of universal closure: 

* $X$ is compact iff for any space $Y$, the projection map $X \times Y \to Y$ is closed. 

## Standard Results


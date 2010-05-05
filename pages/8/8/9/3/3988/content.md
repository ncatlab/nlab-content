
#Contents#
* automatic table of contents goes here
{:toc}

##Idea##


The **K-topology** is a topology on the [[real number|reals]] $\mathbb{R}$ which is finer than the usual [[topology]], but such that the new open sets are 'piled up' on the positive side of 0 (and actually are all contained in $[0,1)$) and have lots of 'holes'. It is useful for constructing topological counterexamples.


##Definition ##

**Definition** Define the subset $K \subset \mathbb{R}$ as $K = \{1/n  | n \ge 1 \}$. Generate a topology on $\mathbb{R}$ by taking as [[basis for a topology|basis]] all open intervals $(a, b)$ (these are the usual basic open sets) and all sets of the form $(a,b)-K$. Clearly only those open intervals that contain $(0,\frac{1}{2})$ need to be included in this latter collection. This topology is the K-topology on $\mathbb{R}$ and denote the corresponding topological space as $\mathbb{R}_K$ ([[David Roberts|DR]]: this is not standard, but I need a symbol for it).

##Application##

The set of [[rational numbers]], with the subspace topology inherited from the inclusion $\mathbb{Q} \hookrightarrow \mathbb{R}_K$, is an example of a non-[[regular space|regular]], [[path-connected space|totally path-disconnected]] [[Hausdorff space|Hausdorff]] space. This space can be used to construct a [[quasitopological groupoid]] which isn't a [[internal groupoid|topological groupoid]].
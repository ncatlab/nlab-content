[[!redirects Structural Complexity Of Proofs]]
_Structural Complexity of Proofs_ (1974) is the title of a Ph.D. thesis by [[Richard Statman]], who was a student of [[Georg Kreisel]] at Stanford University.  Among other contributions, the thesis is notable for defining a notion of "genus of a proof", as a global measure of complexity more interesting than (but analogous to) number of inferences, depth of the proof tree, etc.

#Contents#
* table of contents
{:toc}

## Genus of a proof

Any proof $\pi$ in [[natural deduction]] induces a [[rooted tree]], by representing the judgments $B$ occurring in the proof as nodes $x_B$ (note that different occurrences of the same judgment are represented as distinct nodes), and drawing a directed edge 

$$x_B \to x_C$$

just in case $B$ occurs as a premise of the inference rule with conclusion $C$.  This rooted tree can then be turned into a directed [[graph]] $G(\pi)$ by adding more edges

$$x_A \to x_C$$

just in case the assumption $A$ is _discharged_ by the inference rule with conclusion $C$ (see [[natural deduction#hypothetical_reasoning|natural deduction: hypothetical reasoning]]).

The **genus** of the proof $\pi$ is then defined to be the graph genus of $G(\pi)$, i.e., the minimal [[genus of a surface]] in which $G(\pi)$ embeds without crossing edges.

## Chapters

### 1: The Effect of the Elimination of Explicit Definitions on the Complexity of Proofs

### 2: The Effect of the Choice of Recursion Equations and Rules on the Lengths of Equational Proofs

### 3: Strong Normalization of Classical Analysis with Some Applications to the Length of Proofs 

## References

* Richard Statman. _Structural Complexity of Proofs_, Ph.D. Thesis (1974), Stanford University.

* Alessandra Carbone. _Logical structures and the genus of proofs_, APAL 161:2, 2009. ([doi](http://dx.doi.org/10.1016/j.apal.2009.05.007))

## Related pages

* [[proof net]]
* [[natural deduction]]
* [[lambda calculus]]
* [[proof theory]]

[[!redirects Structural Complexity Of Proofs]]

category:reference
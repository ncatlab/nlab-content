
#Contents#
* automatic table of conmtents goes here
{:toc}

## Young diagram 

A **Young diagram** $F^\lambda$ also called **Ferrers diagram** is a graphical representation of an unordered integer partition $\lambda = (\lambda_1\ge\lambda_2\ge\ldots\ge\lambda_l$). If $\lambda\vdash n$ is a partition of $n$ then the Young
diagram has $n$ boxes. A partition can be addressed as a multiset over $\mathbb{N}$.

There are two widely used such representations. The _English_ one using matrix
like indices, and the _French_ one using Cartesian (coordinate) like indices
for the boxes $x_{i,j}$ in the diagram $F^\lambda$.

In the English representation the boxes are adjusted to the north-west in the 4th quadrant of a 2-dimensional Cartesian coordinate system, with the 'y'-axis being
downward oriented. (Representing boxes as stars, ugly is there \youngtab available? BF.) The partition $(5,4,4,2,1,1)$ of $17$ is given as:

` * * * * *`<br>
` * * * *`<br>
` * * * *`       = $F^{(5,4,4,2,1,1)}$<br>
` * *`<br>
` *`<br>
` *`

Let $\mathbb{Y}$ be the set of Young diagrams. Important functions on Young 
diagrams include:

* **conjugation**: denoted by a prime $\prime : \mathbb{Y} \rightarrow \mathbb{Y}$
  reflects the Young diagram along its main diagonal (north-west to south-east). 
  In the above example the conjugated partition would be $\lambda^\prime=(6,4,3,3,1)$.
* **weight**: $wt \colon \mathbb{Y} \rightarrow \mathbb{N}$ provides the number 
  of boxes.
* **length**: $\ell \colon \mathbb{Y} \rightarrow \mathbb{N}$ provides the number
  of rows or equivalently the number of positive parts of the partition $\lambda$.
  The length of the conjugated diagram gives the number of columns. 
* **plus**: $+ \colon \mathbb{Y}\times \mathbb{Y} \rightarrow \mathbb{Y} :: 
  (\mu,\nu) \mapsto \mu + \nu = (\mu_1+\nu_1,\ldots,\mu_l+\nu_l)$
* **times**: $\times \colon \mathbb{Y}\times \mathbb{Y} \rightarrow \mathbb{Y} ::
 (\mu,\nu) \mapsto (\mu \cup \nu)_{\ge}$ the unordered union of the multisets. It
  follows that $\mu\times \nu =(\mu^\prime + \nu^\prime)^\prime$.

## Skew Young diagram

A generalisation of a Young diagram is a skew Young diagram. Let $\mu,\nu$ be two
partitions, and let $\nu \le \mu$ be defined as $\forall i : \nu_i\le \mu_i$ (possibly adding trailing zeros). The skew Young diagram $F^{\mu/\nu}$ is given by the Young diagram $F^\mu$ with all boxes belonging to $F^\nu$ when superimposed removed. If $mu=(5,4,4,2,1,1)$ and $\nu=(3,3,2,1)$ then $F^{\mu/\nu}$ looks like:

` _ _ _ * *`<br>
` _ _ _ *`<br>
` _ _ * *`<br>
` _ *`<br>
` *`<br>
` *`

* A skew diagram is called connected if all boxes share an edge.
* A skew diagram is called a horizontal strip if every column contains at most one box.
* A skew diagram is called vertical strip if every row contains at most one box.
* conjugation, weight, length extend to skew diagrams accordingly.

A **filling** of a Young diagram with elements from a set $S$ is called a [[Young tableau]].


See also [[Schur functor]]. 

#Contents#
* automatic table of contents goes here
{:toc}

## Young diagram 

A **Young diagram** $F^\lambda$ also called **Ferrers diagram** is a graphical representation of an unordered integer partition $\lambda = (\lambda_1\ge\lambda_2\ge\ldots\ge\lambda_l$). If $\lambda\vdash n$ is a partition of $n$ then the Young
diagram has $n$ boxes. A partition can be addressed as a multiset over $\mathbb{N}$.

There are two widely used such representations. The _English_ one using matrix
like indices, and the _French_ one using Cartesian (coordinate) like indices
for the boxes $x_{i,j}$ in the diagram $F^\lambda$.

In the English representation the boxes are adjusted to the north-west in the 4th quadrant of a 2-dimensional Cartesian coordinate system, with the 'y'-axis being
downward oriented. For instance the diagram $F^{(5,4,4,2,1,1)}$ representing the partition $(5,4,4,2,1,1)$ of $17$ is given in the English representation as:

<svg width="480" height="160" xmlns="http://www.w3.org/2000/svg" se:nonce="13138" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <g>
  <title>Layer 1</title>
  <line x1="200" y1="20" x2="200" y2="140" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="199" y1="20" x2="301" y2="20" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="220" y1="20" x2="220" y2="140" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="240" y1="20" x2="240" y2="100" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="260" y1="20" x2="260" y2="80" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="280" y1="20" x2="280" y2="80" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="300" y1="20" x2="300" y2="40" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="200" y1="40" x2="301" y2="40" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="200" y1="60" x2="280" y2="60" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="200" y1="80" x2="281" y2="80" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="200" y1="100" x2="241" y2="100" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="200" y1="120" x2="220" y2="120" stroke="#000000" stroke-width="2" fill="none"/>
  <line x1="199" y1="140" x2="221" y2="140" stroke="#000000" stroke-width="2" fill="none"/>
 </g>
</svg>

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
partitions, and let $\nu \le \mu$ be defined as $\forall i : \nu_i\le \mu_i$ (possibly adding trailing zeros). The skew Young diagram $F^{\mu/\nu}$ is given by the Young diagram $F^\mu$ with all boxes belonging to $F^\nu$ when superimposed removed. If $\mu=(5,4,4,2,1,1)$ and $\nu=(3,3,2,1)$ then $F^{\mu/\nu}$ looks like:

<svg width="480" height="160" xmlns="http://www.w3.org/2000/svg" se:nonce="13138" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:se="http://svg-edit.googlecode.com">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <g>
  <title>Layer 1</title>
  <line fill="none" stroke-width="2" stroke="#000000" y2="140" x2="200" y1="100" x1="200"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="20" x2="301" y1="20" x1="259"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="140" x2="220" y1="80" x1="220"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="100" x2="240" y1="60" x1="240"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="80" x2="260" y1="20" x1="260"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="80" x2="280" y1="20" x1="280"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="40" x2="300" y1="20" x1="300"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="40" x2="301" y1="40" x1="259"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="60" x2="280" y1="60" x1="239"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="80" x2="281" y1="80" x1="219"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="100" x2="241" y1="100" x1="199"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="120" x2="220" y1="120" x1="199"/>
  <line fill="none" stroke-width="2" stroke="#000000" y2="140" x2="221" y1="140" x1="199"/>
 </g>
</svg>

* A skew diagram is called connected if all boxes share an edge.
* A skew diagram is called a horizontal strip if every column contains at most one box.
* A skew diagram is called vertical strip if every row contains at most one box.
* conjugation, weight, length extend to skew diagrams accordingly.

A **filling** of a Young diagram with elements from a set $S$ is called a [[Young tableau]].


See also [[Schur functor]]. 
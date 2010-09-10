
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

* [[connection on a bundle]]

* [[connection on a 2-bundle]] / [[connection on a gerbe]] / **connection on a bundle gerbe**

* [[connection on a 3-bundle]] / [[connection on a bundle 2-gerbe]]

* [[connection on an ∞-bundle]]

***

#Contents#
* table of contents
{:toc}

## Idea

A _connection on a [[bundle gerbe]]_ is a slight variant of a [[Cech cohomology|Cech]]-realization of a degree 3 [[Deligne cohomology]] cocycle.

> old content, needs to be polished

Like a [[connection on a bundle|connection]] on a locally trivialized bundle is encoded in a  Lie algebra-valued connection $1$-form on $Y$, the connection on a bundle gerbe 
gives rise to a Lie-algebra valued $2$-form on $Y$ (this shift in degree
is directly related to the step from second to third integral cohomology). This $2$-form
is sometimes addressed as the _curving $2$-form_ of a bundle gerbe.

But there is more data necessary to describe a connection on a bundle gerbe.
The details of the definition -- which is evident for line bundle gerbes but more
involved for principal bundle gerbes -- can be naturally derived from a functorial
concept of parallel surface transport, just like connection $1$-forms on bundles
can be derived from parallel line transport.

###Definitions###



####for line bundle gerbes####

A connection (also known as "connection and curving") on a line bundle gerbe
$$
  B \stackrel{p}{\to} Y^{[2]} \stackrel{\to}{\to} Y \stackrel{\pi}{\to} X
$$ 
is

* a 2-form on $Y$
    $$
      B \in \Omega^2(Y)
    $$

* a connection $\nabla$ on the line bundle $B \to Y^{[2]}$

* such that
   $$
      \pi_1^*B \; -\;  p_2^*B \;=\; F_\nabla
   $$

* together with an extension of the bundle gerbe product $\mu$ to an isomorphism
    $$
        \mu_\nabla \;:\; p_{12}^* (B,\nabla) \;\; \otimes p_{23}^* (B,\nabla) \;\to\; p_{13}^* (B,\nabla)
    $$
    of line bundles with connection.



Notice that this condition ensures that $d B$ is a $3$-form on $Y$ which agrees on
double intersections
$$
  p_1^* d B \;\; = \;\; p_2^* d B
  \,.
$$
This means that $d B$ actually descends to a 3-form on $X$.

The __curvature__ associated with the connection on a line bundle gerbe 
is the unique 3-form on $X$
$$
  H \in \Omega^3(X)
$$
such that
$$
  \pi^* H = d B
  \,.
$$

The deRham class $[H]$ of this 3-form is the image in real cohomology of the class in integral coholomology classifying the bundle gerbe.

#### for principal bundle gerbes ####

A connection on a $G$-principal bundle gerbe is

* a $\mathrm{Lie}(G)$-valued 2-form on $Y$
    $$
       B \in \Omega^2(Y,\mathrm{Lie}(G))
    $$

* together with a $\mathrm{Lie}(\mathrm{Aut}(G))$-valued 1-form on $Y$
    $$
       A \in \Omega^1(Y,\mathrm{Lie}(\mathrm{Aut}(G)))
    $$

* and a certain twisted notion of connection on the $G$-bundle $B$


* satisfying a couple of conditions that reduce to those described above in the case $G = U(1)$.

For the case that $F_{A} + \mathrm{ad} B = 0$, these conditions are nothing but
a tetrahedron law on a 2-functor from 2-paths in $Y$ to the category 
$\Sigma(G\mathrm{BiTor})$. This is discussed in
[math.DG/0511710](http://arxiv.org/abs/math.DG/0511710).

For the more general case a choice for these conditions that harmonizes with the
conditions found for (proper) gerbes with connection by Breen & Messing in
[math.AG/0106083](http://arxiv.org/abs/math.AG/0106083) has
been given by Aschieri, Cantini & Jur&#269;o in  
[hep-th/0312154](http://arxiv.org/abs/hep-th/0312154).

###Surface transport###

From a line bundle gerbe with connection one obtains a notion of [[parallel transport]] along surfaces in a way that generalizes the procedure for locally trivialized fiber bundles with connection.

Recall that in the case of fiber bundles, the holonomy associated to a based loop $\gamma$ is obtained by

* choosing a triangulation of the loop (i.e., a decomposition into intervals) such that each vertex sits in a double intersection $U_{ij}$ and such that each edge sits in a patch $U_i$ 

* choosing for each edge a lift into $Y = \sqcup_i U_i$

* choosing for each vertex a lift into $Y^{[2]} = \sqcup_{ij} U_i\cap U_j$

* assigning to each edge lifted to $U_i$ the transport computed from the connection 
    1-form $a_i$

* assigning to each vertex  lifted to $U_i \cap U_j$ the value of the transition function
    $g_{ij}$ at that point

* multiplying these data in the order given by $\gamma$ .

For bundle gerbes this generalizes to a procedure that assigns a triangulation to a closed surface, that lifts faces, edges, and vertices to single, double and triple intersections,
respectively, and which assigns the exponentiated integrals of the 2-form over faces, of the connection 1-form over edges, and assigns the isomorphism $\mu_{ijk}$ to vertices.

For the abelian case (line bundle gerbes) this procedure has been first described in

* K. Gawedzki & N. Reis, _WZW branes and Gerbes_
([arXiv](http://arxiv.org/abs/hep-th/0205233))

based on

* O. Alvarez, _Topological quantization and cohomology_
Commun. Math. Phys. 100 (1985), 279-309.

Further discussion can be found in 

* A. Carey, S. Johnson & M. Murray, _Holonomy on D-branes_, ([arXiv](http://arxiv.org/abs/hep-th/0204199))

Gawedzki and Reis showed this way that the Wess-Zumino term in the WZW-model is nothing but the surface holonomy of a (line bundle) gerbe.

In terms of string physics this means that the string (the $2$-particle) couples to the Kalb-Ramond field -- which hence has to be interpreted as the connection ("and curving") of a gerbe -- in a way that categorifies the coupling of the electromagnetically charged ($1$-)particle to a line bundle.

The necessity to interpret the Kalb--Ramond field as a connection on a gerbe was originally discussed in

* D. Freed and E. Witten
_Anomalies in string theory with D-branes_, Asian J. Math. 3 (1999), 819-851 ([arXiv](http://arxiv.org/abs/hep-th/9907189))


Underlying the Gawedzki--Reis formula is a general mechanism of transition of transport $2$-functors, described in

* U. Schreiber, K. Waldorf, _Connections on non-abelian gerbes and their holonomy_ ([arXiv](http://arxiv.org/abs/0808.1923))

and similarly in 

* Joao Faria Martins, Roger Picken, _A Cubical Set Approach to 2-Bundles with Connection and Wilson Surfaces_ ([arXiv](http://arxiv.org/abs/0808.3964))


 This applies to more general situations than ordinary line bundle gerbes with connection.

The generalization to unoriented surfaces (hence to type I strings) was given in

* K. Waldorf, C. Schweigert & U. S., _Unoriented WZW Models and Holonomy of Bundle Gerbes_ ([arXiv](http://arxiv.org/abs/hep-th/0512283))



## References

(...)
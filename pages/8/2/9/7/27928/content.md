
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### QFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



\tableofcontents

Under *Maxwell-Chern-Simons theories* one understands [[Lagrangian field theories]] whose [[field (physics)|field]] content is a single [[circle group|$\mathrm{U}(1)$]] [[gauge field]] (locally on [[spacetime]] given by a [[differential 1-form]] $A$ with [[flux density]] $F = \mathrm{d}A$) and whose [[Lagrangian density]] is a [[sum]] of that of (vacuum) [[Maxwell theory]] with that of an [[abelian Chern-Simons theory]].

Over a [[spacetime]] of [[dimension of a manifold|dimension]]  $D = 3$ this means that the Lagrangian density is proportional to.

$$
  L_{MCS}^{3D}(A)
  \;\propto\;
  \tfrac{1}{2}
  F \wedge \star F
  \;-\;
  \tfrac{c}{2} A \wedge F
  \,.
$$

The corresponding [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] are (where we include the [[Bianchi identity]] in the first line in order to highlight the comparison to [[Maxwell's equations]]):

$$
  \begin{aligned}
    \mathrm{d} F & = 0
    \\
    \mathrm{d} \star F & = c \,F
    \,.
  \end{aligned}
$$

Similarly, there are higher dimensional versions. For instance over a [[spacetime]] of [[dimension of a manifold|dimension]] $D =5$ and using the Lagrangian density of abelian [[D=5 Chern-Simons theory]] one has
 
$$
  L_{MCS}^{5D}(A)
  \;\propto\;
  \tfrac{1}{2}
  F \wedge \star F
  \;-\;
  \tfrac{c}{3} A \wedge F \wedge F
$$

with [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] 

$$
  \begin{aligned}
    \mathrm{d} F & = 0
    \\
    \mathrm{d} \star F & = c \,F \wedge F
    \,.
  \end{aligned}
$$

This appears notably in the [[bosonic field|bosonic]] sector of [[D=5 supergravity]] (which is an [[Einstein-Maxwell theory|Einstein-Maxwell]]-[[D=5 Chern-Simons theory]]).


## Related entries

* [[Chern-Simons theory]], [[abelian Chern-Simons theory]]

* [[Einstein-Maxwell theory]]

* [[Einstein-Yang-Mills theory]]


## References

### In 3D 

Review:

* [[Gerald V. Dunne]]: section 2.2 in: *Aspects of Chern-Simons Theory*, in: *Topological aspects of low dimensional systems*, Les Houches -- École d'Été de Physique Théorique **69**, Springer (1999) &lbrack;[doi:10.1007/3-540-46637-1_3](https://doi.org/10.1007/3-540-46637-1_3), [arXiv:hep-th/9902115](https://arxiv.org/abs/hep-th/9902115)&rbrack;

* S. I. Kruglov: *Maxwell–Chern–Simons Topologically Massive Gauge Fields in the First-Order Formalism*, Int J Theor Phys **51** (2012) 1–13 &lbrack;[doi:10.1007/s10773-011-0872-1](https://doi.org/10.1007/s10773-011-0872-1), [arXiv:1010.4728](https://arxiv.org/abs/1010.4728)&rbrack;

As an [[effective field theory|effective]] description of [[superconductivity]]:

* [[M. Cristina Diamantini]], P. Sodano, [[Carlo A. Trugenberger]]: *Gauge Theories of Josephson Junction Arrays*, Nucl. Phys. B **474** (1996) 641-677 \[<a href="https://doi.org/10.1016/0550-3213(96)00309-4">doi:10.1016/0550-3213(96)00309-4</a>, [arXiv:hep-th/9511168](https://arxiv.org/abs/hep-th/9511168)\]



### In 5d

In the context of [[quantum electrodynamics]] in 5d:

* [[Christopher T. Hill]]: *Anomalies, Chern-Simons Terms and Chiral Delocalization in Extra Dimensions*, Phys. Rev. D **73** (2006) 085001 &lbrack;[arXiv:hep-th/0601154](https://arxiv.org/abs/hep-th/0601154), [doi:10.1103/PhysRevD.73.085001](https://doi.org/10.1103/PhysRevD.73.085001)&rbrack;

* [[Christopher T. Hill]]: _Physics of $D = 5$ Chern-Simons term_ (2006) &lbrack;[pdf](https://particle.physics.ucdavis.edu/seminars/lib/exe/fetch.php?media=2006:oct:hill.pdf), [[Hill-5dCS.pdf:file]]&rbrack;


[[!redirects Maxwell-Chern-Simons theories]]

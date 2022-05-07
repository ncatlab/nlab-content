


This is an entry on the notion of **complex of groups** introduced by [[André Haefliger]] and [[Jon Corson]] as a higher dimensional generalisation of the Bass-Serre theory of [[graphs of groups]]. (It does _not_ refer to the idea of chain complexes of groups, i.e., [[chain complexes]] in the (more or less) usual sense.) 

#Contents#
* table of contents
{:toc}


##Idea

A _complex of groups_ is a [[diagram]] of [[groups]], [[homomorphisms]] and [[conjugations]], corresponding, abstractly, to the system of inclusions of the [[stabiliser]] subgroups of an [[action]] of a group on a [[simplicial cell complex]] or equivalently on a [[small category without loops]]. If the complex is 1-dimensional one obtains a [[graph of groups]] - note however, the category of 1-complexes of groups is not equivalent as a category to the category of graphs of groups (see [[A. Thomas]] Proposition 2.1).

##Definition

We will initially give the definition in its 'bare hands' form. Here $K$ is a [[simplicial complex]]

 A _complex of groups_, $G(K)$, on $K$ is specified by the data, $(\{G_\sigma\}, \{\psi_a\}, \{g_{a, b}\})$
given by

* a group, $G_{\sigma}$, for each simplex, $\sigma$, of $K$; 

* an injective homomorphism,

$$\psi_a :G_{i (a)} \rightarrow G_{t(a)},$$

for each edge, $a \in E_K$, of the barycentric subdivision of $K$;

* for each pair of composable edges, $a$ and $b$, in $E_K$, an element
  $g_{a, b} \in G_{t(a)}$ is given such that

$$g^{- 1}_{a, b} \psi_{ba} (_-) g_{a, b} = \psi_a \psi_b$$

and such that the   'cocycle condition'

$$g_{a, cb} \psi_a (g_{b, c}) = g_{ab, c} g_{a, b}$$

holds.


###Developability and the universal cover

(to come later)

###The universal group and fundamental group

(to come later)


##Examples

(to come later)



## Complexes of groups as pseudofunctors.

see paper by [[Tom Fiore]] et al (below)



##References

* [[M. Bridson]] and [[A. Haefliger]], 1999, _Metric Spaces of Non-Positive Curvature_, number 31 in 
Grundlehren der Math. Wiss, Springer.

* [[A. Haefliger]], 1991, _Complexes of Groups and Orbihedra_, in Group Theory from a Geometric 
viewpoint , 504 &#8211; 540, ICTP, Trieste, 26 March- 6 April 1990, World Scientific.

* [[J. M. Corson]], _Complexes of Groups_, Proc. London Math. Soc., 65, (1992), 199&#8211;224.

* [[A. Thomas]], 2006 _Lattices acting on right-angled buildings_, Alg. Geom. Top., 6, 1215-1238.

See also:

* [[Thomas M. Fiore]], Wolfgang L&#252;ck, and Roman Sauer, _Euler Characteristics of Categories and Homotopy Colimits_, ([arXiv: 1007.3868](http://arxiv.org/abs/1007.3868))

[[!redirects complexes of groups]]

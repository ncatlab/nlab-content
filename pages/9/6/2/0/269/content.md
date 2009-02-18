#Definition#

A **cubical set** is a [[presheaf]] on the [[cube category]] $\Box$. 

##Remarks##

* The definition is to be understood from the point of view of [[space and quantity]]: a _cubical set_ is a space characterized by the fact that and how it may be _probed_ by mapping standard cubes into it: the set $S_n$ assigned by a cubical set to the standard $n$-cube $[n]$ is the set of $n$-cubes in this space, hence the way of mapping a standard $n$-cube into this spaces.

#Geometric realization#

If $X$ is a cubical set, the _geometric realization_ $|X|$ may be defined as the weighted colimit (a [[end|coend]]) in [[Top]] 

$$X \otimes_{\Box} I^{\bullet} = \int^{n \in \Box} X(n) \cdot I^n$$ 

where $I^{\bullet}: (\Box, \otimes, I) \to (\Top, \times, 1)$ is the unique (up to isomorphism) monoidal functor mapping the generating object $int$ to $[0, 1]$, and for $k = 0, 1$, mapping $i_k$ to the inclusion $\{k\} \hookrightarrow [0, 1]$. This is parallel to one way of defining the geometric realization of a [[simplicial set]]. 
Geometric realization is a functor [[left adjoint]] to the functor 
$$cub: Top \to Set^{\Box^{op}}$$ 
which takes a space $S$ to the functor $\hom_{Top}(I^{\bullet}-, S)$. 


# Background# 

The notion of cubical set and of homology theory and homotopy theory based on singular cubes goes way back in the literature. Serre's work on spectral sequences and fibre spaces was based on cubes. Kan's early work on combinatorial homotopy was based on cubes. However the category of cubical sets was found to have a major disadvantage compared with simplicial sets, in that the cartesian product in this category failed to have the correct homotopy type. 

Nonetheless cubical sets continued to have a kind of underground existence. 

Brown and Higgins introduced the extra structure of [[connection]]s $\Gamma^\pm_i$ on cubical sets, and included this structure into their cubical  [[omega-groupoid]]s. All this structure was essential for the equivalence with [[crossed complex]]es and for the applications to homotopy theory. For example these omega-groupoids have a canonical structure of [[thin]] elements, defined as any composition of elements of the form $\pm \epsilon_j x, \pm \Gamma^\pm_i$. Such elements have "commuting boundary". 

The geometric realisation of cubical sets with connections, and the relation with cartesian products, has not yet been analysed. 

Nonetheless, the advantages of cubes are:

1. Easy notions of multiple compositions (compared with the globular pasting schemes); 

1. Good notions of tensor product, because of the rule $I^m \times I^n \cong I^{m+n}$, and hence easy conceptual handling of homotopies.  

For the first of these, we refer to [[compositions in cubical sets]]. 

#References#

* Grandis, M. and Mauri, L. Cubical sets and their site, _Theory Applic. Categories_ {11} (2003) 185--201.

This discusses variations on the cubical set theme and normal forms in several cases. 


* Brown, R. and Higgins, P.~J., Tensor products and homotopies for $\omega$-groupoids and crossed complexes.
 _J. Pure Appl. Algebra_ 47 (1987) 1--33.

* Massey, W.~S.,   _Singular homology theory_, _Graduate Texts in
  Mathematics_, Volume~70. Springer-Verlag, New York (1980).


Section 2 of

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega-Cat$_ ([web](http://crans.fol.nl/papers/thten.html), [ps](http://crans.fol.nl/papers/thten.ps.gz), [[thten.pdf|pdf:file]])

gives a general discussion of the cube category and of cubical sets. 
The **cubical identities** satisfied by a cubical set are given in proposition 2.8 on p. 9.

Cubical sets are what Brown and Higgins based their long series of articles on [[strict omega-groupoid|strict omega-groupoids]] on. For instance

* Brown, Higgins, _The equivalence of $\omega$-groupoids and cubical $T$-complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 349-370  ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1981__22_4/CTGDC_1981__22_4_349_0/CTGDC_1981__22_4_349_0.pdf)).

and generally

* Ronald Brown, Philip J. Higgins and Rafael Sivera, _Nonabelian algebraic topology_ ([web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html)).
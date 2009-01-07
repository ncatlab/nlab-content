#Definition#

A **cubical set** is a [[presheaf]] on the [[cube category]] $\Box$. 

If $X$ is a cubical set, the _geometric realization_ $|X|$ may be defined as the weighted colimit in [[Top]] 

$$X \otimes_{\Box} I^{\bullet} = \int^{n \in \Box} X(n) \cdot I^n$$ 

where $I^{\bullet}: (\Box, \otimes, I) \to (\Top, \times, 1)$ is the unique (up to isomorphism) monoidal functor mapping the generating object $int$ to $[0, 1]$, and for $k = 0, 1$, mapping $i_k$ to the inclusion $\{k\} \hookrightarrow [0, 1]$. This is parallel to one way of defining the geometric realization of a simplicial set. 
Geometric realization is a functor left adjoint to the functor 
$$cub: Top \to Set^{\Box^{op}}$$ 
which takes a space $S$ to the functor $\hom_{Top}(I^{\bullet}-, S)$. 

##Remarks##

* The definition is to be understood from the point of view of [[space and quantity]]: a _cubical set_ is a space characterized by the fact that and how it may be _probed_ by mapping standard cubes into it: the set $S_n$ assigned by a cubical set to the standard $n$-cube $[n]$ is the set of $n$-cubes in this space, hence the way of mapping a standard $n$-cube into this spaces.


#References#

Section 2 of

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega-Cat$_ ([web](http://crans.fol.nl/papers/thten.html), [ps](http://crans.fol.nl/papers/thten.ps.gz), [[thten.pdf|pdf:file]])

gives a general discussion of the cube category and of cubical sets. 
The **cubical identities** satisfied by a cubical set are given in proposition 2.8 on p. 9.

Cubical sets are what Brown and Higgins based their long series of articles on [[strict omega-groupoid|strict omega-groupoids]] on. For instance

* Brown, Higgins, _The equivalence of $\omega$-groupoids and cubical $T$-complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 349-370  ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1981__22_4/CTGDC_1981__22_4_349_0/CTGDC_1981__22_4_349_0.pdf)).

and generally

* Ronald Brown, Philip J. Higgins and Rafael Sivera, _Nonabelian algebraic topology_ ([web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html)).
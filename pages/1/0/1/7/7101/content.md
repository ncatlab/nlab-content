
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[topological group]] there is a notion of $G$-[[principal bundles]] $P \to X$ over any [[topological space]] $X$. Under [[continuous maps]] $f : X \to Y$ there is a notion of [[pullback]] of principal bundles $f^* : G Bund(Y) \to G Bund(X)$.

A **universal $G$-principal bundle** is a $G$-principal bundle, which is usually written $E G \to B G$, such that for every [[CW-complex]] $X$ the map

$$
  [X, B G] \to G Bund(X)/_\sim
$$

from [[homotopy]] classes of [[continuous functions]] $X \to B G$ given by $[f] \mapsto f^* E G$, is an [[isomorphism]].

In this case one calls $B G$ a [[classifying space]] for $G$-principal bundles.

The universal principal bundle is characterized, up to equivalence, by its total space $E G$ being [[contractible]].

More generally, we can ask for a universal bundle for _numerable_ bundles, that is principal bundles which admit a trivialisation over a [[numerable]] [[open cover]]. Such a bundle exists, and classifies numerable bundles over _all_ topological spaces, not just [[paracompact]] spaces or CW-complexes.

## Details

See at _[[classifying space]]_.

## Related concepts

* [[classifying space]]

* [[Milnor construction]]

* [[universal vector bundle]], [[universal complex line bundle]]

* [[universal principal infinity-bundle]].


## References

### General

Among the earliest references that consider the notion of universal bundles is

* [[Shiing-shen Chern]], Sun, ... (1949)

A review is for instance in

* Stephen Mitchell, _Universal principal bundles and classifying spaces_ ([pdf](http://www-math.mit.edu/~mbehrens/18.906/prin.pdf))

For more see the references at _[[classifying space]]_.


### For equivariant bundles
 {#ReferencesForEquivariantBundles}

Discussion of universal [[equivariant principal bundles]]:


* {#tomDieck69} [[Tammo tom Dieck]], _Faserb&uuml;ndel mit Gruppenoperation_, Arch. Math 20, 136–143 (1969) ([doi:10.1007/BF01899003](https://doi.org/10.1007/BF01899003))

* {#Lashof82} [[Richard Lashof]], _Equivariant bundles_, Illinois J. Math. 26(2): 257-271, 1982 ([doi:10.1215/ijm/1256046796.full](https://projecteuclid.org/journals/illinois-journal-of-mathematics/volume-26/issue-2/Equivariant-bundles/10.1215/ijm/1256046796.full))
 
* {#May90} [[Peter May]], _Some remarks on equivariant bundles and classifying spaces_, Théorie de l'homotopie, Astérisque, no. 191 (1990), 15 p. ([numdam:AST_1990__191__239_0](http://www.numdam.org/item/?id=AST_1990__191__239_0))

* {#MurayamaShimakawa95} [[Mitutaka Murayama]], [[Kazuhisa Shimakawa]], _Universal equivariant bundles_, Proc. Amer. Math. Soc. 123 (1995), 1289-1295 ([doi:10.1090/S0002-9939-1995-1231040-9](https://doi.org/10.1090/S0002-9939-1995-1231040-9))

* {#UribeLueck14} [[Bernardo Uribe]], [[Wolfgang Lück]], _Equivariant principal bundles and their classifying spaces_, Algebr. Geom. Topol. 14 (2014) 1925-1995 ([arXiv:1304.4862](https://arxiv.org/abs/1304.4862), [doi:10.2140/agt.2014.14.1925](http://dx.doi.org/10.2140/agt.2014.14.1925))

* {#GuillouMayMerling17} [[Bertrand Guillou]], [[Peter May]], [[Mona Merling]] _Categorical models for equivariant classifying spaces_, Algebr. Geom. Topol. 17 (2017) 2565-2602 ([arXiv:1201.5178](https://arxiv.org/abs/1201.5178), [doi:10.2140/agt.2017.17.2565](https://doi.org/10.2140/agt.2017.17.2565)) 


[[!redirects universal principal bundles]]

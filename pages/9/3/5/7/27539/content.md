
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--



\tableofcontents


## Idea

Where an ordinary [[braid group]] $Br_n(\Sigma)$ is a group of [[isotopy]]-classes of plain braids under concatenation, and where the closure of such a braid is a plain [[link]], so a *framed braid group* consists of isotopy classes of *framed braids* (ribbon braids closing to *[[framed links]]*), whose strands, in addition to braiding around each other, may also twist in themselves.

Concretely, the plain braid group $Br_n(\Sigma)$ has a [[surjective map|surjective]] [[group homomorphism]] onto the [[symmetric group]] $Sym_n$ and the framed braid group $FBr_n(\Sigma)$ is the [[wreath product group]], relative to this [[permutation group]]-[[structure]], with the additive group [[integers|$\mathbb{Z}$]] ("counting the twists" of a strand):

$$
  FBr_n(\Sigma)
  \;\;
  \simeq
  \;\;
  \mathbb{Z} \wr Br_n(\Sigma)
  \;\;
  \simeq
  \;\;
  \mathbb{Z}^n \rtimes Br_n(\Sigma)
  \,,
$$

hence equivalently the [[semidirect product group]] of the [[direct product group]] $\mathbb{Z}^n$ via the [[group action]] of $Br_n(\Sigma) \to Sym_n$ given by [[permutation|permuting]] the $\mathbb{Z}$-factors.


## References

### General

* Ki Hyoung Ko, Lawrence Smolinsky: *The framed braid group and 3-manifolds*, Proc. Amer. Math. Soc. **115** (1992) 541-551 &lbrack;[doi:10.1090/S0002-9939-1992-1126197-1](https://doi.org/10.1090/S0002-9939-1992-1126197-1), [pdf](https://www.ams.org/journals/proc/1992-115-02/S0002-9939-1992-1126197-1/S0002-9939-1992-1126197-1.pdf)&rbrack;

* Ki Hyoung Ko, Lawrence Smolinsky: *The framed braid group and representations*, in: *Knots 90*, Proceedings in Mathematics, De Gruyter (1992) 289-297 &lbrack;[doi:10.1515/9783110875911](https://doi.org/10.1515/9783110875911), [[KoSmolinsky-FramedBraidsAndReps.pdf:file]]&rbrack;

* R. Krasauskas: *Crossed simplicial groups of framed braids and mapping class groups of surfaces*, Lith Math J **36**  (1996) 263–281 &lbrack;[doi:10.1007/BF02986853](https://doi.org/10.1007/BF02986853)&rbrack;

* [Bellingeri & Gervais 2012](#BellingeriGervais12)

* Akishi Ikeda: *Homological and Monodromy Representations of Framed Braid Groups*, Commun. Math. Phys. **359** (2018) 1091–1121  &lbrack;[doi:10.1007/s00220-017-3036-1](https://doi.org/10.1007/s00220-017-3036-1), [arXiv:1702.03918](https://arxiv.org/abs/1702.03918)&rbrack;

* [[Lukas Woike]]: *The Cyclic and Modular Microcosm Principle in Quantum Topology* &lbrack;[arXiv:2408.02644](https://arxiv.org/abs/2408.02644)&rbrack;
  > (in relation to the framed [[little disk operad]])

* Anastasios Kokkinakis: *Framed Braid Equivalences* &lbrack;[arXiv:2503.05342](https://arxiv.org/abs/2503.05342)&rbrack;


### As a mapping class group

In the context of [[Reshetikhin-Turaev TQFT]]:

* Marco De Renzi, Azat M. Gainutdinov, Nathan Geer, Bertrand Patureau-Mirand, [[Ingo Runkel]], §3.1 in: *Mapping Class Group Representations From Non-Semisimple TQFTs*, Commun. Contemp. Math. (2021) 2150091 &lbrack;[arXiv:2010.14852](https://arxiv.org/abs/2010.14852), [doi:10.1142/S0219199721500917](https://doi.org/10.1142/S0219199721500917)&rbrack;

* Iordanis Romaidis, pp 37 in: *Mapping class group actions and their applications to 3D gravity*, PhD thesis, Hamburg (2022) &lbrack;[ediss:9945](https://ediss.sub.uni-hamburg.de/handle/ediss/9945)&rbrack;
 
* Iordanis Romaidis, [[Ingo Runkel]], p. 8 of: *CFT correlators and mapping class group averages* &lbrack;[arXiv:2309.14000](https://arxiv.org/abs/2309.14000)&rbrack;
 

In the context of the [[Crane-Yetter model]]:


* [[Ying Hong Tham]]: §3.2.1 in: *On the Category of Boundary Values in the Extended Crane-Yetter TQFT*, PhD thesis, Stony Brook (2021) &lbrack;[arXiv:2108.13467](https://arxiv.org/abs/2108.13467)&rbrack;


[[!redirects framed braid groups]]

[[!redirects framed braid]]
[[!redirects framed braids]]



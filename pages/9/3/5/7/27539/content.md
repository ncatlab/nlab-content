
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

Where an ordinary [[braid group]] $Br_n(\Sigma)$ is a group of [[isotopy]]-classes of plain braids under concatenation, and where the closure of such a braid is a plain [[link]], so a *framed braid group* (also "ribbon braid group") consists of isotopy classes of *framed braids* (ribbon braids closing to *[[framed links]]*), whose strands, in addition to braiding around each other, may also twist in themselves.

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


## Related concepts

* [[framed little disk operad]]

* [[framed link]], [[plat closure]]

## References

### General

Original articles:

* [[Paul Melvin]], N. B. Tufillaro: *Templates and framed braids*, Phys. Rev. A **44** (1991) R3419(R) \[<a href="https://doi.org/10.1103/PhysRevA.44.R3419">doi:10.1103/PhysRevA.44.R3419</a>, [pdf](https://repository.brynmawr.edu/cgi/viewcontent.cgi?article=1007&context=math_pubs)\]

* Ki Hyoung Ko, Lawrence Smolinsky: *The framed braid group and 3-manifolds*, Proc. Amer. Math. Soc. **115** (1992) 541-551 &lbrack;[doi:10.1090/S0002-9939-1992-1126197-1](https://doi.org/10.1090/S0002-9939-1992-1126197-1), [pdf](https://www.ams.org/journals/proc/1992-115-02/S0002-9939-1992-1126197-1/S0002-9939-1992-1126197-1.pdf)&rbrack;

* Ki Hyoung Ko, Lawrence Smolinsky: *The framed braid group and representations*, in: *Knots 90*, Proceedings in Mathematics, De Gruyter (1992) 289-297 &lbrack;[doi:10.1515/9783110875911](https://doi.org/10.1515/9783110875911), [[KoSmolinsky-FramedBraidsAndReps.pdf:file]]&rbrack;

Further discussion (some in the context of the [[framed little disk operad]]):

* Hans Wenzel, p. 4 of: *Braids and invariants of 3-manifolds*, Invent Math **114** (1993) 235–275 &lbrack;[doi:10.1007/BF01232670](https://doi.org/10.1007/BF01232670), [eudml:144148](https://eudml.org/doc/144148)&rbrack;

* R. Krasauskas: *Crossed simplicial groups of framed braids and mapping class groups of surfaces*, Lith Math J **36**  (1996) 263–281 &lbrack;[doi:10.1007/BF02986853](https://doi.org/10.1007/BF02986853)&rbrack;

* [[Nathalie Wahl]], p. 25 of: *Ribbon braids and related operads*, PhD thesis, University of Oxford (2001) &lbrack;[pdf](https://ora.ox.ac.uk/objects/uuid:4ae9f906-be3e-4cba-bf3c-a626337d1cf9/files/m1ffea5bebdaee4287e6cca831c6568b5)&rbrack;

* [[Ralph Cohen]], [[Alexander Voronov]]: _Notes on string topology_, in: _String topology and cyclic homology_, Advanced courses in mathematics CRM Barcelona, Birkhäuser (2006) &lbrack;[math.GT/05036259](http://arxiv.org/abs/math/0503625), [doi:10.1007/3-7643-7388-1](https://doi.org/10.1007/3-7643-7388-1), [pdf](http://gen.lib.rus.ec/get?md5=adde9464705ede0fea6b435edb58fbe7)&rbrack;
  > (in the context of [[string topology]])


* [[Ralph Cohen]] (notes by Eric Malm), p 20 of: *MATH 283: Topological Field Theories* (2008) &lbrack;[pdf](https://ericmalm.net/ac/projects/math283-w08/math283-w08-n.pdf), [[RCohen-TQFT.pdf:file]]&rbrack;

* {#BellingeriGervais12} Paolo Bellingeri, Sylvain Gervais: *Surface framed braids*, Geom Dedicata **159** (2012) 51–69 &lbrack;[doi:10.1007/s10711-011-9645-5](https://doi.org/10.1007/s10711-011-9645-5), [arXiv:1001.4471](https://arxiv.org/abs/1001.4471)&rbrack;

* Akishi Ikeda: *Homological and Monodromy Representations of Framed Braid Groups*, Commun. Math. Phys. **359** (2018) 1091–1121  &lbrack;[doi:10.1007/s00220-017-3036-1](https://doi.org/10.1007/s00220-017-3036-1), [arXiv:1702.03918](https://arxiv.org/abs/1702.03918)&rbrack;

* [[Christoph Schweigert]], [[Lukas Woike]]: *The differential graded Verlinde Formula and the Deligne Conjecture*, Proc. Lond. Math. Society **126** 6 (2023) 1811-1841 &lbrack;[arXiv:2105.01596](https://arxiv.org/abs/2105.01596)&rbrack;

* Francesca Aicardi, Jesús Juyumaya, Paolo Papi: *Framization and Deframization* &lbrack[arXiv:2405.10809](https://arxiv.org/abs/2405.10809)&rbrack;

* [[Lukas Woike]]: *The Cyclic and Modular Microcosm Principle in Quantum Topology* &lbrack;[arXiv:2408.02644](https://arxiv.org/abs/2408.02644)&rbrack;

* Anastasios Kokkinakis: *Framed Braid Equivalences* &lbrack;[arXiv:2503.05342](https://arxiv.org/abs/2503.05342)&rbrack;


### As a mapping class group

As the [[mapping class group]] of [[surfaces]] with framed [[punctures]], and in the context of [[Reshetikhin-Turaev TQFT]]:

* Jens Kristian Egsgaard, Søren Fuglede Jørgensen §1.3 in: *The homological content of the Jones representations at $q = -1$*,  Journal of Knot Theory and Its Ramifications **25** 11 (2016) 1650062 &lbrack;[arXiv:1402.6059](https://arxiv.org/abs/1402.6059), [doi:10.1142/S0218216516500620](https://doi.org/10.1142/S0218216516500620)&rbrack;

* Marco De Renzi, Azat M. Gainutdinov, Nathan Geer, Bertrand Patureau-Mirand, [[Ingo Runkel]], §3.1 in: *Mapping Class Group Representations From Non-Semisimple TQFTs*, Commun. Contemp. Math. (2021) 2150091 &lbrack;[arXiv:2010.14852](https://arxiv.org/abs/2010.14852), [doi:10.1142/S0219199721500917](https://doi.org/10.1142/S0219199721500917)&rbrack;


* Rachel Skipper, Xiaolei Wu, Def. 2.1 in: *Homological stability for the ribbon Higman--Thompson groups* &lbrack;[arXiv:2106.08751](https://arxiv.org/abs/2106.08751)&rbrack;


* Iordanis Romaidis, pp 37 in: *Mapping class group actions and their applications to 3D gravity*, PhD thesis, Hamburg (2022) &lbrack;[ediss:9945](https://ediss.sub.uni-hamburg.de/handle/ediss/9945)&rbrack;
 
* Iordanis Romaidis, [[Ingo Runkel]], p. 8 of: *CFT correlators and mapping class group averages*, Commun. Math. Phys. **405** 247 (2024) &lbrack;[arXiv:2309.14000](https://arxiv.org/abs/2309.14000), [doi:10.1007/s00220-024-05111-6](https://doi.org/10.1007/s00220-024-05111-6)&rbrack;
 

In the context of the [[Crane-Yetter model]]:

* [[Ying Hong Tham]]: §3.2.1 in: *On the Category of Boundary Values in the Extended Crane-Yetter TQFT*, PhD thesis, Stony Brook (2021) &lbrack;[arXiv:2108.13467](https://arxiv.org/abs/2108.13467)&rbrack;


[[!redirects framed braid groups]]

[[!redirects framed braid]]
[[!redirects framed braids]]

[[!redirects ribbon braid group]]
[[!redirects ribbon braid groups]]

[[!redirects ribbon braid]]
[[!redirects ribbon braids]]




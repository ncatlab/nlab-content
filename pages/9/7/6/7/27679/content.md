
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}


## Definition ## 

Let $\mathcal{C}$ be a [[fusion category]]. The [[vector space]]

$$
  Tube (\mathcal{C}) 
  \coloneqq 
  \bigoplus_{a,b,c \in \mathcal{I}} \mathcal{C}(c \otimes a, b \otimes c),
$$

for $\mathcal{I}$ the set of [[simple object|simple objects]] of $\mathcal{C}$, has an [[associative unital algebra|algebra]] structure. This is called the **Tube** (or [[Adrian Ocneanu|Ocneanu]]) **algebra**. For $\epsilon \in \mathcal{C}(x \otimes a, a \otimes y)$, $\epsilon' \in \mathcal{C}(x' \otimes a', a' \otimes y')$, their product is given by

$$
\epsilon \cdot \epsilon' = \delta_{y,x'} \sum_{b,\alpha} (\alpha \otimes \text{id}_{y'}) \circ (\text{id}_a \otimes \epsilon') \circ (\epsilon \otimes \text{id}_{a'}) \circ (\text{id}_x \otimes \alpha^* ),
$$

for $\alpha \in \text{Hom}(a \otimes a', b)$ ([Ocneanu 94](#Ocneanu94)). Note that implicit in this definition are several [[associator|associators]], in-between compositions.

The tube algebra is furthermore a [[C-star-algebra]] ([Ocneanu 01](#Ocneanu01)), and even a [[weak bialgebra|weak]] [[Hopf algebra]] ([Müger 03](#Muger03), [Jia et al 24](#JTK24)).

## Properties

### Relation to the Drinfeld center

The [[category of representations]] of the tube algebra $Tube(\mathcal{C})$ of $\mathcal{C}$ is equivalent to the [[Drinfeld center]] $\mathcal{Z}(\mathcal{C})$ of $\mathcal{C}$ ([Müger 03](#Muger03)). 

### Relation to action on Hilbert spaces

In the context of a [[conformal field theory|2d CFT]], twist fields are thought of as elements of a twist [[Hilbert space]] $\mathcal{H}_a$ for $a \in \mathcal{I}$. The [[action]] of $b\in \mathcal{I}$ (essentially by [[conjugation action|conjugation]]) is described by an element $x\in \mathcal{C}( b\otimes a, c \otimes b)$. Thus, the tube algebra $Tube(\mathcal{C})$ [[action|acts]] on the total [[Hilbert space]] $\mathcal{H} = \bigoplus_{a\in \mathcal{I}} \mathcal{H}_a$, meaning the latter is a [[representation]] of the tube algebra, and by the equivalence above is identified with an object in the [[Drinfeld center]] $\mathcal{Z}(\mathcal{C})$ of $\mathcal{C}$. See e.g. ([Lin et al. 23](#Linetal23)).

## References

General:

* {#Ocneanu94} [[Adrian Ocneanu]]. *Chirality for operator algebras.* Subfactors (Kyuzeso, 1993) 39 (1994). ([pdf](https://www.ms.u-tokyo.ac.jp/~yasuyuki/chiral.pdf)).

* {#Ocneanu01} [[Adrian Ocneanu]]. *Operator algebras, topology and subgroups of quantum symmetry–construction of subgroups of quantum groups–.* Taniguchi Conference on Mathematics Nara'98. Vol. 31. Mathematical Society of Japan, 2001. ([doi](http://doi.org/10.2969/aspm/03110235)).

* {#Muger03} [[Michael Müger]]. *From subfactors to categories and topology II: The quantum double of tensor categories and subfactors.* Journal of Pure and Applied Algebra 180.1-2 (2003): 159-219. ([doi](https://doi.org/10.1016/S0022-4049(02)00248-7)).

* Dietmar Bisch, Paramita Das, Shamindra Kumar Ghosh, Narayan Rakshit. *Tube algebra of group-type subfactors* (2017). ([arXiv:1701.00097](https://arxiv.org/abs/1701.00097)).

On its structure

* {#JTK24} Zhian Jia, Sheng Tan, and Dagomir Kaszlikowski. *Weak Hopf symmetry and tube algebra of the generalized multifusion string-net model.* Journal of High Energy Physics 2024.7 (2024): 1-63. ([doi](https://doi.org/10.1007/JHEP07(2024)207)).

As encoding actions on Hilbert spaces

* {#Linetal23} Ying-Hsuan Lin, Masaki Okada, Sahand Seifnashri, and Yuji Tachikawa. *Asymptotic density of states in 2d CFTs with non-invertible symmetries.* Journal of High Energy Physics 2023, no. 3 (2023): 1-43. ([doi](https://doi.org/10.1007/JHEP03(2023)094)).

* Yichul Choi, Brandon C. Rayhaun, Yunqin Zheng. *Generalized Tube Algebras, Symmetry-Resolved Partition Functions, and Twisted Boundary States* (2024). ([arXiv:2409.02159](https://arxiv.org/abs/2409.02159)).

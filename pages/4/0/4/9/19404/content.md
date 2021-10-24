
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _spherical space form_ is a [[quotient space]] $S^n/G$ of a [[round sphere|round]] [[Riemannian manifold|Riemannian]] [[n-sphere]] ($n \geq 2$) by a [[subgroup]] $G$ of its [[isometry group]], which [[action|acts]] [[free action|freely]] and [[properly discontinuous action|properly discontinuously]]. 

Equivalently, a spherical space form is a [[Riemannian manifold]] of [[constant function|constant]] [[positive number|positive]] [[sectional curvature]] (an [[elliptic geometry]]) which is [[connected topological space|connected]] and [[geodesically complete Riemannian manifold|geodesically complete]] (see e.g. [Gadhia 07, Lemma 5](#Gadhia07)).

The spherical space forms are one of three classical examples of _[[Clifford-Klein space forms]]_.

Their classification was raised as an open problem by [Killing 1891](#Killing1891) and a complete solution was finally compiled by ([Wolf 74](#Wolf74)) (reviewed in [Gadhia 07, section 2.2](#Gadhia07)). A re-proof of the classification is claimed in ([Allock 15](#Allock15)). 


For more on this see at _[[group actions on n-spheres]]_.


## Examples

### 7-dim spherical space forms with $Spin$-structure
 {#7DSphericalSpaceFormsWithSpinStructure}

For $n =7$ all the groups $G$ in [Wolf's classification](#Wolf74) [[action|act]] as [[subgroups]] of [[special orthogonal group|SO(8)]], the latter equipped with its defining action on $\mathbequib{R}^8$ restricted to the action on $S^7 = S(\mathbb{R}^8) \subset \mathbb{R}^8$.

Therefore one may consider the [[lift]] $\widehat{G}$ of these [[subgroups]] to subgroups of the [[spin group]] $Spin(8) \to SO(8)$ through the [[double cover]]-projection. Such a lift corresponds to a choice of [[spin structure]] on the [[spherical space form]] $S^7/G$.  These Spin-lifts $\widehat{G}$, have been classified in ([Gadhia 07](#Gadhia07)).

Given any such lift $\widehat{G} \subset Spin(8)$, one may consider its [[action|action]] on the two [[irreducible representation|irreducible]] [[real spin representations]] $\mathbf{8}_\pm$ of $Spin(8)$. Write

$$
  N_\pm \;\coloneqq\; dim_{\mathbb{R}}\left( \left(\mathbf{8}_{\pm}\right)^{\widehat{G}} \right)
$$

for the [[dimension]] of the subspace of [[spinors]] that are [[fixed point|fixed]] by the action of $\widehat{G}$. For $\widehat{G}$ non-[[trivial group|trivial]], we have 

$$
  (N_+, N_-) = (N,0)
  \phantom{AA} \text{or} \phantom{AA} 
  (N_+, N_-) = (0,N)
$$

and hence up to a choice of [[orientation]] there is a unique 

$$
  N \in \{0,1,\cdots, 8\}
$$

associated with each 7-dimensional [[spherical space form]] equipped with [[spin structure]].

Hence this allows to stratify [Wolf's classification](#Wolf74) of 7-dimensional spherical space forms, first into the cases that do and that do not admit any [[spin structure]], and then the former further into the dimension $N$ of the space of [[Killing spinors]] that they carry.

In the case  $N \geq 4$
It turns out that the resulting sub-classification demands $\widehat{G}$ to be a [[finite subgroup of SU(2)]]; hence this is an [[ADE classification]] ([MFFGME 09, Sections 3-7](#MFFGME09)):

* $N = 8$: here $\widehat{G} = \mathbb{Z}/2$, the [[cyclic group of order 2]];

* $N = 7$: does not occur;

* $N = 6$: here $\widehat{G} = \mathbb{Z}/k$ (for $k \gt 2)$, a [[cyclic group]];

* $N = 5$: here $\widehat{G} = $ a non-[[cyclic group|cyclic]] [[finite subgroup of SU(2)]], hence a [[binary dihedral group]] or the [[binary tetrahedral group]] or [[binary octahedral group]] or [[binary icosahedral group]], [[diagonal action|acting diagonally]] on $\mathbb{R}^8 \simeq \mathbb{H} \oplus \mathbb{H}$;

* $N = 4$: here $\widehat{G} = $ any [[finite subgroup of SU(2)]] _except_ the [[binary tetrahedral groups]], but acting via the [[diagonal action]] composed with a suitable non-trivial [[outer automorphism]] of $\widehat{G}$ on one of the two sides.

(In the last case, while there is one nontrivial outer automorphism of the binary tetrahedral group, its twisted action yields $N =5$, hence is equivalent to one of the previous cases ([MFFGME 09, section 7.3](#MFFGME09)).)


[[!include 7d spherical space forms -- table]]


This analysis applies to the classification of the [[near horizon geometry]] of smooth (i.e. non-[[orbifold]]) $\geq \tfrac{1}{2}$ [[BPS state|BPS]] [[black brane|black]] [[M2-brane]]-solutions of the [[equations of motion]] of [[11-dimensional supergravity]]:

These are the [[Cartesian product]] $AdS_4 \times (S^7/G)$ of 4-[[dimension|dimensional]] [[anti de Sitter spacetime]] with a 7-[[dimension|dimensional]] [[spherical space form]] $S^7/G$ with [[spin structure]] and $N \geq 4$, as above ([MFFGME 09](#MFFGME09)).

## Properties

### Higher gerbes on spherical space forms

Let $G \,\in\, Grp(FinSet) \xhookrightarrow{\;} Grp(TopSp)$ be a [[finite group]] equipped with a [[continuous function|continuous]] [[free action]] on the [[n-sphere]] $S^{n+2}$ for some $n \in \mathbb{N}$. We write

\[
  \label{CoprojectionInDiscussionOfGerbesOnSphericalSpaceForms}
  S^{n+2}
  \overset{\; q \;}{\twoheadrightarrow}
  S^{n+2}/G
  \;\;\;
  \in
  \;
  TopSp
\]

for the [[quotient space]] [[coprojection]] onto the corresponding [[spherical space form]].

Moreover, let $\Gamma \,\in\, Grp(TopSp)$ be a [[topological group]] whose [[underlying]] [[homotopy type]] is a [[homotopy n-type]], hence [[n-truncated object of an (infinity,1)-category|n-truncated]].

$$
  \tau_n Shp(\Gamma) \,\simeq\, Shp(\Gamma)
  \;\;\;
  \in
  \;
  Grp_\infty
  \,.
$$

This implies that its [[classifying space]] $B \Gamma \,\simeq\, Shp( \left\vert \Gamma \rightrightarrows \ast \right\vert  )$ is an $(n+1)$-type

$$
  \tau_{n+1} Shp(\Gamma) \,\simeq\, Shp(\Gamma)
  \;\;\;
  \in
  \;
  Grp_\infty
$$

and hence that every $\Gamma$-principal bundle on $S^n$ is [[isomorphism|isomorphic]] to the [[trivial bundle]]:

\[
  \label{UniqueGerbesOnNSphere}
  \tau_0 \Gamma PrnBdl(TopSp)_X
  \;\;
  \simeq
  \;\;
  Maps
  \big(
    Shp(S^n) 
    ,\,
    B \Gamma
  \big)
  \;\;
  \simeq
  \;\;
  \ast
  \,.
\]

Here we write 

$$
  \array{
    Grp(TopSp)
    &
    \xrightarrow{\; Dtoplg \;}
    &
    Grp(DiffSp)  
    &
    \xrightarrow{\;}
    &
    Grpd(SmthGrp_{\infty})
    &
    \xrightarrow{\;}
    &
    SmthGrp_\infty
    \\
    \Gamma \rightrightarrows \ast
    &&
    &\mapsto&
    &&
    \mathbf{B}\Gamma
  }
$$

for 

1. the [[delooping groupoid]] of $\Gamma$, regarded as a [[topological groupoid]] $\Gamma \rightrightarrows \ast$, 

1. its associated [[D-topological space|D-]][[topological stack]] $\mathbf{B}\Gamma$.


According to (eq:UniqueGerbesOnNSphere), every $\Gamma$-[[principal bundle]] on the spherical space form $S^n/G$ trivializes when [[pullback bundle|pulled back]] along the coprojection $q$ (eq:CoprojectionInDiscussionOfGerbesOnSphericalSpaceForms). The corresponding [[Cech cohomology|Cech cocycle]] is a [[topological functor]]

$$
  \big(
    S^{n+2} \times G \rightrightarrows S^{n+2}
  \big)
  \xrightarrow{\;\; 
    c_1 \rightrightarrows \ast 
  \;\;}
  \big(
    \Gamma \rightrightarrows \ast
  \big)
$$

out of the [[action groupoid]] $S^{n+2} \times G \rightrightarros X$ of $G$ acting on $S^n$ into the [[delooping groupoid]] $\Gamma \rightrightarrows \ast$:

\begin{tikzcd}
    {}
    \ar[d,-, dotted]
    &&
    {}
    \ar[d,-, dotted]
    \\
    S^{n+2} \times  G \times G 
    \ar[rr, "{c_2}"{above}]
    \ar[d, shift left=12pt]
    \ar[d]
    \ar[d, shift right=12pt]
    &&
    \Gamma \times \Gamma
    \ar[d, shift left=12pt]
    \ar[d]
    \ar[d, shift right=12pt]
    \\
    S^{n+2} \times G 
    \ar[rr, "c_1"{above}]
    \ar[d, shift left=6pt]
    \ar[d, shift right=6pt]
    \ar[u, shift right=6pt]
    \ar[u, shift left=6pt]
    &&
    \Gamma
    \ar[d, shift left=6pt]
    \ar[d, shift right=6pt]
    \ar[u, shift right=6pt]
    \ar[u, shift left=6pt]
    \\
    S^{n+2}
    \ar[rr, "{ }"{below, name=s, pos=.4}]
    \ar[d, ->>, "{ }"{right, name=t, pos=.7 }]
    \ar[u]
    &&
    \ast
    \ar[u]
    \ar[d, ->>]
    \\
    S^{n+2}/G
    \ar[rr, "c"{below}]
    &&
    \mathbf{B}\Gamma
    %
    \ar[
      from=s,
      to=t,
      Rightarrow,
      "\sim"{sloped, below}
    ]
\end{tikzcd}

(...)


## Literature

Historical articles

* {#Killing1891} [[Wilhelm Killing]], _Ueber die Clifford-Klein’schen Raumformen_, Math. Ann. 39 (1891), 257–278 ([doi:10.1007/BF01206655](https://doi.org/10.1007/BF01206655))

Solution of the classification problem:

* {#Wolf74} [[Joseph Wolf]], _Spaces of constant curvature_, Publish or Perish, Boston, Third ed., 1974

Review:

* Ian Hambleton, _Topological spherical space forms_, Handbook of Group Actions (Vol. II), ALM 32 (2014), 151-172. International Press, Beijing-Boston ([arXivL:1412.8187](https://arxiv.org/abs/1412.8187))


Discussion for the [[7-sphere]] with application to [[near horizon geometries]] of [[M2-brane]]:

* {#MFFGME09} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], [[Sunil Gadhia]], [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))

* {#Gadhia07} [[Sunil Gadhia]], _Supersymmetric quotients of M-theory and supergravity backgrounds_, PhD thesis, School of Mathematics, University of Edinburgh, 2007 ([spire:1393845](http://inspirehep.net/record/1393845/))



* {#Allock15} Daniel Allcock, _Spherical space forms revisited_ ([arXiv:1509.00906](https://arxiv.org/abs/1509.00906))



[[!redirects spherical space forms]]
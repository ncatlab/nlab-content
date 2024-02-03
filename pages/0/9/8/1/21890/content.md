
#Contents#
* table of contents
{:toc}

## Idea

The notion of [[projective space]] $\mathbb{O}P^n$ over the [[octonions]] $\mathbb{O}$ makes sense for $n \,\in\, \{ 0,1,2 \}$ (but not beyond, see e.g. [Voelkel 16, Sec. 1.3](#Voelkel16)).
The [[octonionic projective plane]] $\mathbb{O}P^2$ is also called the *Cayley projective plane*.


## Properties

### Octonionic projective line and the 8-Sphere

+-- {: .num_prop} 
###### Proposition

We have a [[homeomorphism]]

$$
  \mathbb{O}P^1 \,\simeq\, S^8
$$

between the [[octonionic projective line]] and the [[8-sphere]].

=--

### Cell structure on octonionic projective plane

+-- {: .num_prop} 
###### Proposition

There is a [[homeomorphism]]

$$
  \mathbb{O}P^2 \,\simeq\, D^{16} \underset{h_{\mathbb{O}}}{\cup} \mathbb{O}P^1
$$

between the [[octonionic projective plane]] and the [[attaching space]] obtained from the [[octonionic projective line]] along the [[octonionic Hopf fibration]].

=--

([Lackmann 19, Lemma 3.4.](#Lackmann19))

([Mimura 67, page 166](#Mimura67))

See also at _[[cell structure of projective spaces]]_.

### Homotopy groups

+-- {: .num_prop #HomotopyGroupsOfOctonionicProjectivePlane}
###### Proposition

The [[homotopy groups]] of octonionic projective plane are
\[
  \label{ListOfHomotopyGroupsOfOctonionicProjectivePlane}
    \pi_k
    \big(
      \mathbb{O}P^2
    \big)
    \;=\;
    \left\{
    \array{
      1 &\vert& k \leq 7
      \\
      \pi_k
      \big(
        S^8
      \big)
      &\vert&
      8 \leq k \leq 14
    }
    \right.
\]
Further homotopy groups are
$$\pi_{15}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_{120}$$
$$\pi_{16}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_2^3$$
$$\pi_{17}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_2^4$$
$$\pi_{18}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_{24}\times\mathbb{Z}_2$$
$$\pi_{19}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_{504}\times\mathbb{Z}_2$$
$$\pi_{20}\big(\mathbb{O}P^2\big)
\cong 1$$
$$\pi_{21}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_6$$
$$\pi_{22}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_4$$
$$\pi_{23}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}\times\mathbb{Z}_{120}\times\mathbb{Z}_2^2\,.$$
(While $\pi_{15}\big(S^8\big)
\cong\mathbb{Z}\times\mathbb{Z}_{120}$, which includes the [[homotopy class]] of the [[octonionic Hopf fibration]].)

=--

([Lackmann 19, page 7](#Lackmann19))

([Mimura 67, Theorem 7.2.](#Mimura67))

### Cohomology

+-- {: .num_prop #OrdinaryCohomologyOfOctonionicProjectivePlane}
###### Proposition

For $A \in $ [[Ab]] any [[abelian group]], then the [[ordinary cohomology]] [[cohomology groups|groups]] of octionionic projective plane $\mathbb{O}P^2$ with [[coefficients]] in $A$ are

$$
  H^k(\mathbb{O}P^2,A)
   \simeq
  \left\{
    \array{
       A & for \; k=0,8,16
       \\
       0 & otherwise
    }
  \right.
  \,.
$$

=--

([Lackmann 19, Corollary 4.1.](#Lackmann19))

## References

* {#Lackmann19} [[Malte Lackmann]], _The octonionic projective plane_, in MATRIX Book Series **4**, Springer (2021) &lbrack;[doi:10.1007/978-3-030-62497-2_6](https://doi.org/10.1007/978-3-030-62497-2_6), [arXiv:1909.07047](https://arxiv.org/abs/1909.07047)&rbrack;

* {#Voelkel16} [[Konrad Voelkel]], _Motivic cell structures for projective spaces over split quaternions_, 2016 &lbrack;[freidok:11448](https://freidok.uni-freiburg.de/data/11448), [pdf](https://freidok.uni-freiburg.de/fedora/objects/freidok:11448/datastreams/FILE1/content)&rbrack;

* Rowena Held, Iva Stavrov, Brian VanKoten, _(Semi-)Riemannian geometry of (para-)octonionic projective planes_, Diff. Geom. & its Appl. __27__ 4 (2009) 464-481 &lbrack;[doi:/10.1016/j.difgeo.2009.01.007](https://doi.org/10.1016/j.difgeo.2009.01.007)&rbrack;

* {#Mimura67} Mamoru Mimura, _The Homotopy groups of Lie groups of low rank_, J. Math. Kyoto Univ. **6** 2 (1967) 131-176 &lbrack;[doi:10.1215/kjm/1250524375](https://doi.org/10.1215/kjm/1250524375)&rbrack;

[[!redirects octonionic projective spaces]]

[[!redirects octonionic projective line]]
[[!redirects octonionic projective lines]]


[[!redirects octonion projective spaces]]
[[!redirects octonion projective spaces]]

[[!redirects octonion projective line]]
[[!redirects octonion projective lines]]






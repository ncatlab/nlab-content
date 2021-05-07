
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

_Representation theory_ is concerned with the study of [[algebra|algebraic]] [[structures]] via their [[representations]]. This concerns notably [[groups]], directly or in their incarnation as [[group algebras]], [[Hopf algebras]] or [[Lie algebras]], and usually concerns [[linear algebra|linear]] [[representations]], hence [[modules]] of these structures. But more generally representation theory also studies [[representations]]/[[modules]]/[[actions]] of generalizations of such structures, such as [[coalgebras]] via their [[comodules]] etc.

See also at _[[geometric representation theory]]_.

## In homotopy type theory
 {#InHomotopyTypeTheory}

The fundamental concepts of representation theory have a particular natural formulation in  [[homotopy theory]] and in fact in [[homotopy type theory]], which also  refines it from the study of [[representations]] of [[groups]] to that of     [[∞-representations]] of [[∞-groups]]. This includes both [[discrete ∞-groups]] as well as [[geometric homotopy types]] such as [[smooth ∞-groups]], the higher analog of [[Lie groups]].

The key observation to this translation is that 

1. an [[∞-group]] $G$ is equivalently given by its [[delooping]] $\mathbf{B}G$ regarded with its canonical [[pointed object|point]] (see at [[looping and delooping]]), hence the universal $G$-[[principal ∞-bundle]] 

   $$
     \array{
        G &\longrightarrow& \ast
        \\
        && \downarrow
        \\
        && \mathbf{B}G
     }
   $$

1. an [[∞-action]] $\rho$ of $G$ on any [[geometric homotopy type]] $V$ is equivalently given by a [[homotopy fiber sequence]] of the form

   $$
     \array{
        V &\stackrel{}{\longrightarrow}& V//_\rho G
        \\
        && \downarrow
        \\
        && \mathbf{B}G
     }
     \,,
   $$

   hence by a $V$-[[fiber ∞-bundle]] over $\mathbf{B}G$ which is the $\rho$-[[associated ∞-bundle]] to the universal $G$-[[principal ∞-bundle]] (see at _[[∞-action]]_ for more on this).

Under this identification, the representation theory of $G$ is equivalently 

* the [[homotopy theory]] in the [[slice (∞,1)-topos]] over $\mathbf{B}G$;

* the [[homotopy type theory]] in the [[context]] of/[[dependent type theory|dependent on]] $\mathbf{B}G$. 

More in detail, this yields the following identifications:

[[!include homotopy type representation theory -- table]]


## Examples

* [[representation theory of the symmetric group]]

* [[representation theory of the general linear group]]

* [[Schur-Weyl duality]]

## Related entries

* [[representation]], [[action]], [[module]]

  * [[group]], [[group algebra]], [[groupoid]], [[algebraic group]], [[Lie algebra]]

  * [[vector space]],  [[affine space]], [[symplectic vector space]]

  * [[character]]

  * [[action]], [[module]], [[equivariant object]]

  * [[bimodule]], [[Morita equivalence]], [[induced representation]]

  * [[Hilbert space]], [[Banach space]], [[Fourier transform]], [[functional analysis]]
  
  * [[weight (in representation theory)]]

  * [[orbit]], [[coadjoint orbit]], [[Killing form]]

  * [[geometric quantization]], [[coherent state]]

  * [[socle]], [[quiver]]

  * [[module algebra]], [[comodule algebra]], [[Hopf action]], [[measuring]]

* [[representation ring]]

* [[irreducible representation]]

* [[Schur's lemma]]

* [[Young diagram]]

* [[Schur index]]

* [[McKay correspondence]], [[ADE classification]]

* [[geometric representation theory]]
  
  * [[Borel-Weil theorem]], [[Beilinson-Bernstein localization]]
  * [[D-module]], [[perverse sheaf]], [[BBDG decomposition theorem]]
  * [[Kazhdan-Lusztig theory]]
  * [[Dirac induction]]

* [[Verma module]], [[BGG resolution]]

* [[Grothendieck group]], [[lambda-ring]], [[symmetric function]], [[formal group]]

* [[principal bundle]], [[torsor]], [[vector bundle]], [[Atiyah Lie algebroid]]

* [[character sheaf]], [[Harish Chandra transform]]

* [[geometric function theory]], [[groupoidification]]

* [[Eilenberg-Moore category]], [[algebra over an operad]], [[actegory]], [[crossed module]]

* [[reconstruction theorem]]s


## References
 {#References}

Lecture notes include

* {#tomDieck09} [[Tammo tom Dieck]], _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

* {#Teleman05} [[Constantin Teleman]], _Representation theory_, lecture notes 2005 ([pdf](https://math.berkeley.edu/~teleman/math/RepThry.pdf))

* Joel Robbin, _Real, Complex and Quaternionic representations_, 2006 ([pdf](http://www.math.wisc.edu/~robbin/angelic/RCH-G.pdf), [[Robbin08RCHRep.pdf:file]])


Textbooks include

* Charles Curtis, Irving Reiner, _Representation theory of finite groups and associative algebras_, AMS 1962

* {#FultonHarris91} [[William Fulton]], [[Joe Harris]], _Representation Theory: a First Course_, Springer, Berlin, 1991 ([pdf](http://isites.harvard.edu/fs/docs/icb.topic1381051.files/fulton-harris-representation-theory.pdf))


* {#LuxPahlings10} Klaus Lux, Herbert Pahlings, _Representations of groups -- A computational approach_, Cambridge University Press 2010 ([author page](http://www.math.rwth-aachen.de/~RepresentationsOfGroups/), [publisher page](http://www.cambridge.org/catalogue/catalogue.asp?isbn=9780521768078))


A list of texts on representation theory is maintained at

* [[Mikhail Khovanov]], _[Resources](http://www.math.columbia.edu/~khovanov/resources)_.

The relation to [[number theory]] and the [[Langlands program]] is discussed in 

* [[Robert Langlands]], _Representation theory: Its rise and its role in number theory_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.207.3303))

[[!redirects linear representation theory]]


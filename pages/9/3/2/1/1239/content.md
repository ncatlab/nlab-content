
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

* [[representation theory of the special unitary group]]

* [[Schur-Weyl duality]]


## Related entries

* [[representation]], [[action]], [[module]]

  * [[group]], [[group algebra]], [[groupoid]], [[algebraic group]], [[Lie algebra]]

  * [[vector space]],  [[affine space]], [[symplectic vector space]]

  * [[character]]

  * [[action]], [[module]], [[equivariant object]]

  * [[bimodule]], [[Morita equivalence]]

  * [[induced representation]], [[Mackey theory]]

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

* [[asymptotic representation theory]]

* [[geometric representation theory]]
  
  * [[Borel-Weil theorem]], [[Beilinson-Bernstein localization]]

  * [[D-module]], [[perverse sheaf]], [[BBDG decomposition theorem]]

  * [[Kazhdan-Lusztig theory]]

  * [[Dirac induction]]

* [[Verma module]], [[BGG resolution]]

* [[representation stability]]

* [[Grothendieck group]], [[lambda-ring]], [[symmetric function]], [[formal group]]

* [[principal bundle]], [[torsor]], [[vector bundle]], [[Atiyah Lie algebroid]]

* [[character sheaf]], [[Harish Chandra transform]]

* [[geometric function theory]], [[groupoidification]]

* [[Eilenberg-Moore category]], [[algebra over an operad]], [[actegory]], [[crossed module]]

* [[reconstruction theorems]]


## References
 {#References}


Lecture notes:

* [[Pavel Etingof]], Oleg Golberg, Sebastian Hensel, Tiankai Liu, Alex Schwendner, [[Dmitry Vaintrob]], Elena Yudovina:
*Introduction to representation theory*, Student Mathematical Library **59**, AMS (2011) &lbrack;[arXiv:0901.0827](https://arxiv.org/abs/0901.0827), [ams:stml-59](https://bookstore.ams.org/stml-59)&rbrack;

* {#tomDieck09} [[Tammo tom Dieck]], _Representation theory_ (2009) &lbrack;[pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf), [[tomDieckRepresentationTheory.pdf:file]]&rbrack;

* {#Teleman05} [[Constantin Teleman]], _Representation theory_, lecture notes 2005 ([pdf](https://math.berkeley.edu/~teleman/math/RepThry.pdf))

* Joel Robbin, _Real, Complex and Quaternionic representations_, 2006 ([pdf](http://www.math.wisc.edu/~robbin/angelic/RCH-G.pdf), [[Robbin08RCHRep.pdf:file]])

* [[Igor R. Shafarevich]], [[Alexey O. Remizov]]: §14 in: *Linear Algebra and Geometry* (2012) &lbrack;[doi:10.1007/978-3-642-30994-6](https://doi.org/10.1007/978-3-642-30994-6), [MAA-review](https://maa.org/press/maa-reviews/linear-algebra-and-geometry)&rbrack; 

* S. Martin: *Representation Theory*, notes by [[Dexter Chua]] (2016) &lbrack;[web](https://dec41.user.srcf.net/h/II_L/representation_theory)&rbrack;

Textbook accounts 

for [[finite groups]]:

* [[Charles Curtis]], [[Irving Reiner]]: _Representation theory of finite groups and associative algebras_, AMS (1962) &lbrack;[ISBN:978-0-8218-4066-5](https://bookstore.ams.org/chel-356.h)&rbrack;

* [[I. Martin Isaacs]]: *Character theory of finite groups*, Academic Press, New York (1976) &lbrack;[ISBN:978-0-8218-4229-4](https://bookstore.ams.org/view?ProductCode=CHEL/359.H)&rbrack;

* {#Serre77} [[Jean-Pierre Serre]]: *Linear Representations of Finite Groups*, Graduate Texts in Mathematics **42**, Springer (1977) &lbrack;[doi:10.1007/978-1-4684-9458-7](https://doi.org/10.1007/978-1-4684-9458-7), [pdf](https://www.math.tau.ac.il/~borovoi/courses/ReprFG/Hatzagot.pdf)&rbrack;

* [[Charles Curtis]], [[Irving Reiner]]: *Methods of representation theory -- With applications to finite groups and orders -- Vol. I*, Wiley (1981) &lbrack;[ark:/13960/t8gf4wd3x](https://archive.org/details/methodsofreprese00curt/page/n1/mode/2up)&rbrack;

* {#LuxPahlings10} Klaus Lux, Herbert Pahlings, _Representations of groups -- A computational approach_, Cambridge University Press (2010) &lbrack;[author page](http://www.math.rwth-aachen.de/~RepresentationsOfGroups/), [publisher page](http://www.cambridge.org/catalogue/catalogue.asp?isbn=9780521768078)&rbrack;

* {#Steinberg12} [[Benjamin Steinberg]]: *Representation Theory of Finite Groups -- An Introductory Approach*, Springer (2012) &lbrack;[doi:10.1007/978-1-4614-0776-8](https://doi.org/10.1007/978-1-4614-0776-8)&rbrack;

* Caroline Gruson, Vera Serganova, *From Finite Groups to Quivers via Algebras -- A Journey Through Representation Theory*, Springer (2018) &lbrack;[doi:10.1007/978-3-319-98271-7](https://doi.org/10.1007/978-3-319-98271-7)&rbrack;

* [[Gabriel Navarro]]: *Character Theory and the McKay Conjecture*, Cambridge University Press (2018) &lbrack;[doi:10.1017/9781108552790](https://doi.org/10.1017/9781108552790)&rbrack;

and more generally for [[compact Lie groups]]:

* [[Tammo tom Dieck]], [[Theodor Bröcker]], *Representations of compact Lie groups*, Springer (1985) &lbrack;[doi:10.1007/978-3-662-12918-0](https://link.springer.com/book/10.1007/978-3-662-12918-0)&rbrack;

* Asim O. Barut, Ryszard Rączka: *Theory of group representations and applications*, World Scientific (1986) &lbrack;[doi:10.1142/0352](https://doi.org/10.1142/0352), [ark:/13960/s2131r9mqpj](https://archive.org/details/theoryofgrouprep0000baru/page/n9/mode/2up), [pdf](https://github.com/carlosal1015/Books/blob/master/Physics/A.%20O%20Barut%20Theory%20of%20group%20representations%20and%20applications%20part%201.pdf)&rbrack;
  > (advertized as being for [[physics|physicists]])  

* {#FultonHarris91} [[William Fulton]], [[Joe Harris]]: _Representation Theory: a First Course_, Springer (1991) &lbrack;[doi:10.1007/978-1-4612-0979-9](https://link.springer.com/book/10.1007/978-1-4612-0979-9)&rbrack;

* [[Amritanshu Prasad]]: *Representation theory -- A Combinatorial Viewpoint*, Cambridge University Press (2014) &lbrack;[doi:10.1017/CBO9781139976824](https://doi.org/10.1017/CBO9781139976824)&rbrack;


In the context of [[physics]] and specifically [[quantum mechanics]] (cf. *[[Gruppenpest]]*):

* J. F. Cornwell: *Group Theory in Physics -- An Introduction*, Academic Press (1997) \[<a href="https://www.sciencedirect.com/book/9780121898007/group-theory-in-physics">ISBN:9780121898007</a>, [doi:10.1016/B978-0-12-189800-7.X5000-6](https://doi.org/10.1016/B978-0-12-189800-7.X5000-6)\]

* Wu Ki-Tung: *Group Theory in Physics*, World Scientific (1985) \[<a href="https://doi.org/10.1142/0097">doi:10.1142/0097</a>\]

* [[Peter Woit]], *Quantum Theory, Groups and Representations: An Introduction*, Springer 2017 &lbrack;[doi:10.1007/978-3-319-64612-1](https://doi.org/10.1007/978-3-319-64612-1), ISBN:978-3-319-64610-7&rbrack;

Discussion via [[string diagrams]]/[[Penrose notation]]:

* [[Jeffrey Ellis Mandula]], *Diagrammatic techniques in group theory*, Southampton Univ. Phys. Dept. (1981) ([cds:129911](https://cds.cern.ch/record/129911), [pdf](https://cds.cern.ch/record/129911/files/SHEP%2080-81-7.pdf))

* {#Cvitanovic08} [[Predrag Cvitanović]], _Group Theory: Birdtracks, Lie's, and Exceptional Groups_, Princeton University Press July 2008 ([PUP](https://press.princeton.edu/books/paperback/9780691202983/group-theory), [birdtracks.eu](http://birdtracks.eu/), [pdf](http://www.birdtracks.eu/version9.0/GroupTheory.pdf))

  > (aimed at [[Lie theory]] and [[gauge theory]])

Further references:

* [[Mikhail Khovanov]], _[Resources](http://www.math.columbia.edu/~khovanov/resources)_.


The relation to [[number theory]] and the [[Langlands program]] is discussed in 

* [[Robert Langlands]], _Representation theory: Its rise and its role in number theory_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.207.3303))

[[!redirects linear representation theory]]

[[!redirects representation theories]]


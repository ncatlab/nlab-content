
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

**Geometric representation theory** studies [[representation]]s (of various symmetry objects like [[algebraic group|algebraic groups]], [[Hecke algebra]]s, [[quantum groups]], [[quiver]]s etc.) realizing them by [[higher geometry|geometric means]], e.g. by geometrically defined [[actions]] on [[sections]] of various [[bundles]] or [[sheaves]] as in [[geometric quantization]] (see at _[[orbit method]]_), [[D-modules]], [[perverse sheaf|perverse sheaves]], [[deformation quantization]] [[modules]] and so on. 

Typically the underlying spaces for the sheaves involved are [[Grassmannian]]s, [[flag variety|flag varieties]], [[configuration space]]s and the like. Another important tool are cohomological vanishing theorems in appropriate contexts. Some historical landmarks are the [[Borel-Weil theorem]], the [[Borel-Weil-Bott theorem]], [[Kazhdan-Lusztig conjecture]], the [[BBDG decomposition theorem]], the [[Beilinson-Bernstein localization theorem]] and the [[Lusztig conjectures]]. 

Quoting from ([MSRI 14](#MSRI14)):


> Representation theory is the study of the basic symmetries of mathematics and physics. Symmetry groups come in many different flavors: finite groups, Lie groups, p-adic groups, loop groups, adelic groups,.. A striking feature of representation theory is the persistence of fundamental structures and unifying themes throughout this great diversity of settings. One such theme is the Langlands philosophy, a vast nonabelian generalization of the Fourier transform of classical harmonic analysis, which serves as a visionary roadmap for the subject and places it at the heart of number theory.

> The fundamental aims of geometric representation theory are to uncover the deeper geometric and categorical structures underlying the familiar objects of representation theory and harmonic analysis, and to apply the resulting insights to the resolution of classical problems. A groundbreaking example of its success is Beilinson-Bernstein's generalization of the Borel-Weil-Bott theorem, giving a uniform construction of all representations of Lie groups via the geometric study of differential equations on flag varieties.

> The geometric study of representations often reveals deeper layers of structure in the form of categorification. Categorification typically replaces numbers (such as character values) by vector spaces (typically cohomology groups), and vector spaces (such as representation rings) by categories (typically of sheaves). It is a primary explanation for miraculous integrality and positivity properties in algebraic combinatorics. A recent triumph of geometric methods is Ng&#244;'s proof of the Fundamental Lemma, a key technical ingredient in the Langlands program. The proof relies on the cohomological interpretation of orbital integrals, which makes available the deep topological tools of algebraic geometry (such as Hodge theory and the Weil conjectures).

A similar description was given by [[David Ben-Zvi]] in an [MO answer](http://mathoverflow.net/questions/126474/new-geometric-methods-in-number-theory-and-automorphic-forms/126540#126540)

> Representation theory is the study of the basic symmetries of mathematics and physics. The primary aim of the subject is to understand concrete linear models for abstract symmetry groups. A signature triumph of the past century is our understanding of compact Lie groups. At the foundation, there is Cartan's classification of Lie algebras and Borel-Weil-Bott's uniform construction of all representations in the cohomology of line bundles on flag varieties. Thus we have a list of every compact Lie group we could ever encounter and every way in which it could appear concretely as a matrix group. Furthermore, there is a deep combinatorial theory of other key structures such as the tensor product of representations. The ideas and results of this subject are the basic input to diverse areas from number theory to quantum field theory.

> Though mysteries still remain, the theory of compact Lie groups is a representative model for what we would like to achieve with other symmetry groups. Because of their universal importance, symmetry groups come in many different flavors: finite groups, Lie groups, p-adic groups, loop groups, adelic groups,... and the list will only increase with the discovery of new important structures. For the above examples, our understanding is still very coarse though the last decades have witnessed breathtaking advances. The Langlands program along with its geometric spinoffs provide a visionary roadmap for where the subject could go in the coming years. In particular, current developments such as the recent proof of the Fundamental Lemma create great optimism that geometric techniques will have a deep impact.

> Geometric representation theory seeks to understand groups and representations as a consequence of more subtle but fundamental symmetries. A groundbreaking example of its success is Beilinson-Bernstein's uniform construction of all representations of Lie groups via the geometry of D-modules on flag varieties. The result is not difficult to state and prove but has the Borel-Weil-Bott theorem and the Kazhdan-Lusztig multiplicity conjectures as immediate consequences. A reasonable reaction is to wonder what allows one to prove deep results about representations of Lie groups with so little effort. One answer is that the true focus of the Beilinson-Bernstein theory is not representations but rather the symmetries of flag varieties. The geometric notion of D-module allows one to localize symmetries and to apply the sheaf-theoretic techniques of algebraic geometry. In this way, our understanding of representations of Lie groups follows from that of infinitesimal symmetries of algebraic varieties.

> There are now many instances where difficult questions about representations can be translated into more tractable questions about geometry. Other famous examples include the Deligne-Lusztig theory of representations of finite groups of Lie type, the Springer theory of representations of Weyl groups, the Kazhdan-Lusztig theory of modules for Hecke algebras, and Lusztig and Nakajima's theory of representations of Kac-Moody algebras and quantum groups via quiver varieties. In the theory of automorphic forms, one of the fundamental tools is the realization of representations of adelic groups in the cohomology of Shimura varieties (in the case of number fields) and Drinfeld modular varieties (in the case of function fields). The recent proof of the Fundamental Lemma exploits the fact that computing orbital integrals in p-adic groups can be reduced to calculating cohomology of fibers of Hitchin's integrable system.

> The twin modern goals of geometric representation theory are to explore the above dictionaries and to discover new unexpected ones. As an important consequence, the geometric realization of representations often reveals deeper layers of structure in the form of categorification. Categorification typically turns numbers (for example, the coefficients of Kazhdan-Lusztig polynomials) into the dimensions of vector spaces (in this case, the Ext groups of intersection cohomology sheaves). It is a primary explanation for miraculous integrality and positivity properties in algebraic combinatorics. At the center of geometric representation theory is Grothendieck's categorification of functions by &#8467;-adic sheaves. An important example is Lusztig's theory of character sheaves: it provides a uniform geometric source for the characters of all finite groups of Lie type. Another important example is the theory of canonical bases: here categorification replaces representation spaces with linear categories equipped with canonical generating objects. Another broad example is the geometric Langlands program: it provides a categorification of the Langlands program in the setting of function fields, providing new insights into many classical constructions.

> Geometric representation theory has close and profound connections to many fields of mathematics, which we expect to play a significant role in the program. Perhaps the most significant are to number theory, via the theory of automorphic forms, L-functions and modularity. Much current activity in the field is motivated either directly by problems in number theory or by more tractable geometric analogues thereof. Another major influence on the subject comes from physics, in particular gauge theory, integrable systems, and recently topological string theory. There is a significant interaction with the theory of C&#8727;-algebras through the Baum-Connes conjecture, an instance of which provides an organizing principle for representation theory of real and p-adic groups. Finally, geometric representation theory is closely entwined with very active areas in combinatorics such as Schubert calculus, its affine analogue, and the theory of Macdonald polynomials.


## References

* A. Beilinson, J. Bernstein, _Localisations de $\mathfrak{g}$&#8211;modules_, C. R. Acad. Sci. Paris 292 (1981), 15--18.

* N. Chriss, V. Ginzburg, _Representation theory and complex geometry_, book

* K. Vilonen, _Geometric methods of representation theory_, [math.AG/0410032](http://arxiv.org/abs/math/0410032)

* R. Hotta, K. Takeuchi, T. Tanisaki, _D-modules, perverse sheaves, and representation theory_, Progress in Mathematics __236__, Birkh&#228;user 2008

* M. Kashiwara, _Equivariant derived category and representation of real semisimple Lie groups_, in CIME Summer school _Representation Theory and Complex Analysis_, Cowling, Frenkel et al. eds. LNM __1931__ Springer ([pdf](http://www.kurims.kyoto-u.ac.jp/~kenkyubu/kashiwara/sd.pdf)).

* A. Borel et al., _Algebraic D-modules_, Perspectives in Mathematics, Academic Press, 1987.

* M.Kashiwara, W.Schmid, _Quasi-equivariant D-modules, equivariant
derived category, and representations of reductive Lie groups_, Lie Theory
and Geometry, in Honor of Bertram Kostant, Progress in Mathematics,
Birkh&#228;user, 1994, pp. 457--488.

* [[Dennis Gaitsgory]], _Geometric representation theory_, 61 pp. 2005 course notes [cat0.pdf](http://www.math.harvard.edu/~gaitsgde/267y/catO.pdf)
* [[David Kazhdan]], _Algebraic geometry and representation theory_, Proc. ICM 1986, vol. I, 849-852, [djvu:201K](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0849.0852.ocr.djvu), [pdf:399K](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0849.0852.ocr.pdf)
* V. Ginzburg (Paper read by D. Vogan.) _Geometrical aspects of representation theory_, Proc. ICM 1986, vol. I, 840-848, [djvu:487K](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0840.0848.ocr.djvu), [pdf:940K](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0840.0848.ocr.pdf)

* [MSRI program Geometric Representation Theory](http://www.msri.org/web/msri/scientific/programs/show/-/event/Pm8951) (2014)
 {#MSRI14}

* [[David Ben-Zvi]], _[[Loop Groups, Characters and Elliptic Curves]]_, talk (2012)

See also the references at _[[orbit method]]_.
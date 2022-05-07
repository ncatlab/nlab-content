+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


# String diagrams
* table of contents
{: toc}

## Idea
 {#Idea}

_String diagrams_ constitute a graphical calculus for expressing operations in [[monoidal categories]]. 

\begin{imagefromfile}
    "file_name": "HotzFigure2.jpg",
    "float": "right",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 20
    },
    "caption": "From [Hotz 65](#Hotz65)"
\end{imagefromfile}

\begin{imagefromfile}
    "file_name": "PenroseDepictAContraction.jpg",
    "float": "right",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 20
    },
    "caption": "From [Penrose 71a](#Penrose71a)"
\end{imagefromfile}


\begin{imagefromfile}
    "file_name": "PenroseRindlerFigureA1.jpg",
    "float": "right",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 20
    },
    "caption": "From [Penrose-Rindler 84, Append.](#PenroseRindler84)"
\end{imagefromfile}

In the archetypical cases of the [[Cartesian monoidal category]] of [[finite sets]] this is Hotz's notation ([Hotz 65](#Hotz65)) for [[automata]], while for  [[finite-dimensional vector spaces]] with their [[tensor product of vector spaces|usual tensor product]] this is Penrose's notation ([Penrose 71a](#Penrose71a), [Penrose-Rindler 84](#PenroseRindler84)) for [[tensor networks]]; but the same idea immediately applies more generally to any other [[monoidal category]] and yet more generally to [[bicategories]], etc.


The idea is roughly to think of [[objects]] in a monoidal category as "strings" and of [[morphisms]] from one [[tensor product]] to another as a node which the source strings enter and the target strings exit. Further structure on the monoidal category is encoded in geometrical properties on these strings. 

For instance:

* putting strings next to each other denotes the [monoidal product](monoidal+category#eq:TensorProductFunctor), and having no string at all denotes the [[tensor unit]];

* braiding strings over each other corresponds to &#8211; yes, the [[braided monoidal category|monoidal braiding]] (if any);

* bending strings around corresponds to dualities on [[dualizable objects]] (if any).

Many operations in monoidal categories that look  unenlightening in symbols become obvious in string diagram calculus, such as the [[trace]]: an output wire gets bent around and connects to an input.

String diagrams may be seen as dual (in the sense of [[Poincaré duality]]) to [[commutative diagrams]]. For instance, in a [[2-category]], an example of a string diagram for a [[2-morphism]] (shown on the left) is shown on the right here:

\begin{centre}
\begin{tikzpicture}[every node/.style={node distance=1.5cm}]
\usetikzlibrary{calc,automata}

\node (a) {$A$};
\node[above right of=a] (b) {$B$};
\node[right of=b] (c) {$C$};
\node at ($(b) !.5! (c)$) (bc) {};
\node[below right of=c] (d) {$D$};
\node[below of=bc,node distance=1.875cm] (e) {$E$};

\draw[->] (a) edge node[above left] {$f$} (b);
\draw[->] (b) edge node[above] {$g$} (c);
\draw[->] (c) edge node[above right] {$h$} (d);
\draw[->] (a) edge node[below] {$k$} (e);
\draw[->] (e) edge node[below] {$l$} (d);

\node[below of=bc,node distance=0.9cm] (double) {\large $\Downarrow \alpha$};

\node[right of=d] (egal) {\large $\mapsto$};

\tikzstyle{point}=[circle,draw,fill,inner sep=1pt];
\node[right of=egal,node distance=3cm,point] (centre) {};
\draw ($(centre)-(1.5,1.5)$) rectangle ($(centre)+(1.5,1.5)$);

% Points
\tikzstyle{label}=[node distance=0.3cm]
\node[inner sep=0pt] at ($(centre)+(-1,1.52)$) (h) {};
\node[inner sep=0pt] at ($(centre)+(0,1.52)$) (g) {};
\node[inner sep=0pt] at ($(centre)+(1,1.52)$) (f) {};
\node[inner sep=0pt] at ($(centre)+(-0.5,-1.52)$) (l) {};
\node[inner sep=0pt] at ($(centre)+(0.5,-1.52)$) (k) {};
\node[above of=h,label] {$h$};
\node[above of=g,label] {$g$};
\node[above of=f,label] {$f$};
\node[below of=l,label] {$l$};
\node[below of=k,label] {$k$};
\node[right of=centre,label] {$\alpha$};

% Edges
\draw[thick] (f) edge[bend left] (centre);
\draw[thick] (h) edge[bend right] (centre);
\draw[thick] (l) edge[bend left] (centre);
\draw[thick] (k) edge[bend right] (centre);
\draw[thick] (g) -- (centre);

% Regions
\tikzstyle{region}=[node distance=0.9cm]
\node[below of=centre,region] {$E$};
\node[left of=centre,region] {$D$};
\node[right of=centre,region] {$A$};
\node[below left of=f,region] {$B$};
\node[below right of=h,region] {$C$};
\end{tikzpicture}

\end{centre}

String diagrams for monoidal categories can be obtained in the same way, by considering a monoidal category as a 2-category with a single object.

## Variants 

There are many additional [[extra structures]] on monoidal categories, or similar structures, which can usually be represented by encoding further geometric properties of their string diagram calculus For instance:

* in monoidal categories which are _[[ribbon category|ribbon categories]]_ the strings from above behave as if they have a small transversal extension which makes them behave as ribbons. Accordingly, there is a _twist_ operation in the axioms of a ribbon category and graphically it corresponds to twisting the ribbons by 360 degrees.

* in a [[traced monoidal category]], the trace can be represented by bending an output string around to connect to an input, even though if the objects are not dualizable the individual "bends" do not represent anything.

* in monoidal categories which are _[[spherical category|spherical]]_ all strings behave as if drawn on a sphere.

* in a [[hypergraph category]], the string diagrams are labeled [[hypergraphs]].

* string diagrams can be extended to represent [[monoidal functors]] in several ways.  One nice way is described in [these slides](http://web.science.mq.edu.au/~mmccurdy/cms2010talk.pdf), and can also be done with "3D regions" as drawn [here](http://golem.ph.utexas.edu/category/2010/08/the_geometry_of_monoidal_fibra.html#c034428).

* there is also a string diagram calculus for [[bicategories]], which extends that for monoidal categories regarded as one-object bicategories.  Thus, the strings now represent 1-cells and the nodes 2-cells, leaving the two-dimensional planar regions cut out by the strings to represent the 0-cells.  This makes it manifest that in general, string diagram notation is _Poincar&#233; dual_ to the [[globe|globular]] notation: where one uses $d$-dimensional symbols, the other uses $(2-d)$-dimensional symbols.

* string diagrams for bicategories can be generalized to string diagrams for [[double categories]] and [[proarrow equipments]] by distinguishing between "vertical" and "horizontal" strings.

* Similarly, one can [[categorification|categorify]] this to "[[surface diagrams]]" for [[3-categories]] (including [[monoidal bicategories]]) and so on; see for instance [[toddtrimble:Surface diagrams|here]].

* As explained [here](http://sbseminar.wordpress.com/2007/07/12/the-operadic-periodic-table/), in the presence of certain levels of duality it may be better to work with diagrams on cylinders or spheres rather than in boxes. This relates to [[planar algebras]] and [[canopolis|canopolises]]. 

* A string diagram calculus for [[monoidal fibrations]] can be obtained as a generalization of C.S. Peirce's "existential graphs."  The ideas are essentially contained in ([Brady-Trimble 98](#BradyTrimble98)) and developed in ([Ponto-Shulman 12](#PontoShulman12)), and was discussed [here](http://golem.ph.utexas.edu/category/2010/08/the_geometry_of_monoidal_fibra.html).

* String diagrams for [[closed monoidal categories]] (see also at _[[Kelly-Mac Lane graph]]_) are similar to those for [[autonomous categories]], but a bit subtler, involving "boxes" to separate parts of the diagram.  They were used informally by Baez and Stay [here](#BaezQG06) and [here](#Rosetta), but can also be done in essentially the same way as the [[proof nets]] used in [[intuitionistic logic|intuitionistic]] [[linear logic]]; see [Lamarche](#Lamarche08).

* Proof nets for multiplicative [[linear logic]] with negation similarly give string diagrams for [[*-autonomous categories]], or more generally [[linearly distributive categories]]; see [Blute-Cockett-Seely-Trimble](#BCST).

* Proof surfaces for noncommutative multiplicative [[linear logic]] with negation, see [Dunn-Vicary](#DunnVicary17)

* _Sheet diagrams_, string diagrams drawn on a branching surface, may be used for [[rig categories]], see [Comfort-Delpeuch-Hedges](#CDH).

See also [Selinger 09](#Selinger09) for a review of different string diagram formalisms.


## Examples
 {#Examples}

### In linear algebra
 {#InLinearAlgebra}

String diagram calculus in [[linear algebra]]:

* {#PenroseNotation} String diagrams in [[finite-dimensional vector spaces]] with the [[tensor product of vector spaces|usual tensor product]] are *Penrose's notation* ([Penrose 71a](#Penrose71a), [71b](#Penrose71b), [72](#Penrose72), [Penrose-Rindler 84, Append.](#PenroseRindler84)) for working with [[tensors]]. 

* More recently, string diagrams in this category have come to be known as *[[tensor networks]]*, especially so in application to [[condensed matter physics]] and also in [[quantum computation]] and in particular in [[quantum error correction]].

### In quantum computation

* In [[quantum computation]], *[[quantum circuit diagrams]]* are a form of string diagrams in [[finite-dimensional vector spaces|finite-dimensional]] [[Hilbert spaces]].

### In representation theory
 {#InRepresentationTheory}

String diagram calculus in [[representation theory]]:

*  String diagrams for the monoidal category of finite-dimensional [[linear representations]] of the group [[SU(2)]] on complex vector spaces are called [[spin networks]].


### In Lie theory
 {#ExamplesInLieTheory}

For string diagrams calculus in [[Lie theory]] see at:

* _[[Lie algebra object]]_

* _[[metric Lie algebra]]_

* _[[metric Lie representation]]_

* _[[Lie algebra weight system]]_.

* _[[M2-brane 3-algebra]]_


### In perturbative quantum field theory
 {#ExamplesInpQFT}

For applications of string diagram calculus in [[perturbative quantum field theory]], see at 

* [['t Hooft double line notation]]

(...)

## Related concepts

* [[sharing graph]]

* [[surface diagram]]

* [[Kelly-Mac Lane diagram]]

* [[proof net]]

* [[Feynman diagram]]

* [[tensor network]],

* [[neural network]]

* [[Lie algebra weight system]]

* [[linguistics|natural language syntax]]

* [[Petri net]]

## References

### Introduction and survey

Introductions to and surveys of string diagram calculus:

* {#Selinger09} [[Peter Selinger]], _A survey of graphical languages for monoidal categories_, in: [[Bob Coecke]] (ed.) _New Structures for Physics_, Lecture Notes in Physics, vol 813. Springer, Berlin, Heidelberg (2010) ([arXiv:0908.334](http://arxiv.org/abs/0908.3347), [doi:10.1007/978-3-642-12821-9_4](https://doi.org/10.1007/978-3-642-12821-9_4))

* {#Cvitanovic08} [[Predrag Cvitanović]], _Group Theory: Birdtracks, Lie's, and Exceptional Groups_, Princeton University Press July 2008 ([PUP](https://press.princeton.edu/books/paperback/9780691202983/group-theory), [birdtracks.eu](http://birdtracks.eu/), [pdf](http://www.birdtracks.eu/version9.0/GroupTheory.pdf))

  (aimed at [[Lie theory]] and [[gauge theory]])

* [[John Baez]], QG Seminar Fall 2000 ([web](http://math.ucr.edu/home/baez/qg-fall2000/)), Winter 2001 ([web](http://math.ucr.edu/home/baez/qg-winter2001/)), Fall 2006 ([web](http://math.ucr.edu/home/baez/qg-fall2006/index.html#computation)).

* [[John Baez]], [[Mike Stay]], _Physics, Topology, Logic and Computation: A Rosetta Stone_ ([arXiv:0903.0340](http://arxiv.org/abs/0903.0340))

* [[Aleks Kissinger]], _Pictures of Processes: Automated Graph Rewriting for Monoidal Categories and Applications to Quantum Computing_ ([arXiv:1203.0202](https://arxiv.org/abs/1203.0202))
 
* [[Simon Willerton]], _String diagrams_ ([YouTube](http://www.youtube.com/view_play_list?p=50ABC4792BD0A086))

* [[Ross Street]], _Low dimensional topology and higher-order categories_ ([ps](http://www.mta.ca/~cat-dist/CT95Docs/LowDim.ps))

  (about surface diagrams)

* [[Ross Street]], _Categorical structures_, in: M. Hazewinkel (ed.), _Handbook of algebra -- Volume 1_, Elsevier 1996 ([pdf](http://maths.mq.edu.au/~street/45.pdf), [978-0-444-82212-3](https://www.elsevier.com/books/handbook-of-algebra/hazewinkel/978-0-444-82212-3))

  (in the generality of [[bicategories]])

From the point of view of [[finite quantum mechanics in terms of dagger-compact categories]]:

* {#CoeckePicturalism} [[Bob Coecke]], _Quantum Picturalism_ ([arXiv:0908.1787](http://arxiv.org/abs/0908.1787))

* {#CoeckeIntroducing} [[Bob Coecke]], _Introducing categories to the practicing physicist_ ([arXiv:0808.1032](http://arxiv.org/abs/0808.1032))

* {#CoeckePractising} [[Bob Coecke]], _Categories for the practising physicist_ ([arXiv:0905.3010](http://arxiv.org/abs/0905.3010))

* [[Bob Coecke]], [[Ross Duncan]], _Interacting Quantum Observables: Categorical Algebra and Diagrammatics_, New J. Phys. 13 (2011) 043016 ([arXiv:0906.4725](http://arxiv.org/abs/0906.4725))

* {#HeunenVicary12} [[Chris Heunen]], [[Jamie Vicary]], _Lectures on categorical quantum mechanics_, 2012 ([pdf](https://www.cs.ox.ac.uk/files/4551/cqm-notes.pdf))


From the point of view of [[tensor networks]] in [[solid state physics]]:

* [[Jacob Biamonte]], Ville Bergholm, _Tensor Networks in a Nutshell_, Contemporary Physics ([arxiv:1708.00006](https://arxiv.org/abs/1708.00006))

* [[Jacob Biamonte]], _Lectures on Quantum Tensor Networks_ ([arXiv:1912.10049](https://arxiv.org/abs/1912.10049))


Some philosophical discussion is given in  

* [[David Corfield]], Section 10.4 of: _Towards a Philosophy of Real Mathematics_, CUP, 2003.


### Original articles 
 {#OriginalArticles}

The development and use of string diagram calculus pre-dates its graphical appearance in print, due to the difficulty of printing non-text elements at the time.

> Many calculations in earlier works were quite clearly worked out with string diagrams, then painstakingly copied into equations. Sometimes, clearly graphical structures were described in some detail without actually being drawn: e.g. the construction of free compact closed categories in Kelly and Laplazas 1980 "Coherence for compact closed categories".

> ([Pawel Sobocinski, 2 May 2017](http://angg.twu.net/categories-2017may02.html#.1))

> This idea that string diagrams are, due to technical issues, only useful for private calculation, is said explicitly by Penrose. Penrose and Rindler's book "Spinors and Spacetime" (CUP 1984) has an 11-page appendix full of all sorts of beautiful, carefully hand-drawn graphical notation for tensors and various operations on them (e.g. anti-symmetrization and covariant derivative). On the second page, he says the following:

> "The notation has been found very useful in practice as it grealy simplifies the appearance of complicated tensor or spinor equations, the various interrelations expressed being discernable at a glance. Unfortunately the notation seems to be of value mainly for private calculations because it cannot be printed in the normal way."

> ([Alex Kissinger, 2 May 2017](http://angg.twu.net/categories-2017may02.html#.2))



The first formal definition of string diagrams in the literature appears to be in

* {#Hotz65} [[Günter Hotz]], _Eine Algebraisierung des Syntheseproblems von Schaltkreisen_, EIK, Bd. 1, (185-205), Bd, 2, (209-231) 1965 ([part I](https://www.magentacloud.de/lnk/LiPMlYfh), [part II](https://www.magentacloud.de/lnk/YivslUWJ), [[HotzSchaltkreise.pdf:file]])

Application of string diagrams to [[tensor]]-calculus in [[mathematical physics]] (hence for the case that the ambient [[monoidal category]] is that of [[finite dimensional vector spaces]] equipped with the [[tensor product of vector spaces]]) was propagated by [[Roger Penrose]], whence [[physics|physicists]] know string diagrams as _Penrose notation for tensor calculus_:


* {#Penrose71a} [[Roger Penrose]], _Applications of negative dimensional tensors_, Combinatorial Mathematics and its Applications, Academic Press (1971) ([pdf](http://www2.math.uic.edu/~kauffman/Penrose.pdf), [[PenroseNegativeDimensionalTensors.pdf:file]])

* {#Penrose71b} [[Roger Penrose]], _Angular momentum: An approach to combinatorial spacetime_, in Ted Bastin (ed.) _Quantum Theory and Beyond_, Cambridge University Press (1971), pp.151-180 ([[PenroseAngularMomentum71.pdf:file]])

* {#Penrose72} [[Roger Penrose]], _On the nature of quantum geometry_, in: J. Klauder (ed.) _Magic Without Magic_, Freeman, San Francisco, 1972, pp. 333–354 ([spire:74082](http://inspirehep.net/record/74082), [[PenroseQuantumGeometry.pdf:file]])

* {#PenroseRindler84} [[Roger Penrose]], [[Wolfgang Rindler]], appendix (p. 424-434) of: _Spinors and space-time -- Volume 1: Two-spinor calculus and relativistic fields_, Cambridge University Press 1984 ([doi:10.1017/CBO9780511564048](https://doi.org/10.1017/CBO9780511564048))

See also 

* Wikipedia, _[Penrose graphical notation](https://en.wikipedia.org/wiki/Penrose_graphical_notation)_

From the point of view of [[monoidal category|monoidal]] [[category theory]], an early description of string diagram calculus (without actually depicting any string diagrams, see the above comments) is in:

* {#KellyLaplaza80} [[Max Kelly]], M. L. Laplaza, _Coherence for compact closed categories_. Journal of Pure and Applied Algebra, 19:193&#8211;213, 1980 (<a hef="https://doi.org/10.1016/0022-4049(80)90101-2">doi:10.1016/0022-4049(80)90101-2</a>, [pdf](https://core.ac.uk/download/pdf/82696829.pdf))

  (proving the [[coherence theorem for monoidal categories|coherence for compact closed categories]])

following 

* {#Kelly72} [[Max Kelly]], _Many-variable functorial calculus I_, in: [[Max Kelly]], M. Laplaza , [[L. Gaunce Lewis, Jr.]], [[Saunders Mac Lane]] (eds.) _Coherence in Categories_, Lecture Notes in Mathematics, vol 281. Springer, Berlin, Heidelberg 1972 ([doi:10.1007/BFb0059556](https://doi.org/10.1007/BFb0059556))

  (which does include the hand-drawn diagrams that are missing in [Kelly-Laplaza 80](#KellyLaplaza80)!) 

and in

* [[André Joyal]], [[Ross Street]], _The geometry of tensor calculus I_, Advances in Math. 88 (1991) 55-112; MR92d:18011 ([pdf](https://core.ac.uk/download/pdf/82659437.pdf), <a href="https://doi.org/10.1016/0001-8708(91)90003-P">doi:10.1016/0001-8708(91)90003-P</a>)

* [[André Joyal]] and [[Ross Street]], _The geometry of tensor calculus II_  ([pdf](http://www.math.mq.edu.au/~street/GTCII.pdf))


String diagram calculus was apparently popularized by its use in

* [[Louis Kauffman]], _Knots and physics_, Series on _Knots and Everything_, Volume 1,  World Scientific, 1991 ([doi:10.1142/1116](https://doi.org/10.1142/1116))

  (in the context of [[knot theory]])

Probably [[David Yetter]] was the first (at least in public) to write string diagrams  with "coupons" (a term used by [[Nicolai Reshetikhin]] and [[Turaev]] a few months later) to represent maps which are not inherent in the (braided or symmetric compact closed) monoidal structure. 

See also these:

* [[Peter Freyd]], [[David Yetter]], _Braided compact closed categories with applications to low dimensional topology_ Advances in Mathematics, 77:156&#8211;182, 1989.

* [[Peter Freyd]] and [[David Yetter]], _Coherence theorems via knot theory_. Journal of Pure and Applied Algebra, 78:49&#8211;76, 1992.

* [[David Yetter]], _Framed tangles and a theorem of Deligne on braided deformations of tannakian categories_ In M. Gerstenhaber and [[Jim Stasheff]] (eds.) _Deformation Theory and Quantum Groups with Applications to Mathematical Physics_, Contemporary Mathematics 134, pages 325&#8211;349. Americal Mathematical Society,
1992.

For more on the history of the notion see the bibliography in ([Selinger 09](#Selinger09)).


### Details

String diagrams for [[monoidal categories]] are discussed in:

* [Hotz 65](#Hotz65)

* [[Andre Joyal]] and [[Ross Street]], _The geometry of tensor calculus I_, Advances in Math. 88 (1991) 55-112; MR92d:18011.  ([pdf](http://tqft.net/other-papers/Geometry%20of%20Tensor%20Calculus%20-%20Joyal%20&%20Street.pdf))

* [[Andre Joyal]] and [[Ross Street]], _The geometry of tensor calculus II_.  ([pdf](http://www.math.mq.edu.au/~street/GTCII.pdf).

* [[Andre Joyal]] and [[Ross Street]], _Planar diagrams and tensor algebra_, available [here](http://www.math.mq.edu.au/~street/PlanarDiags.pdf).


For [[1-categories]] in 

* [[Dan Marsden]], _Category Theory Using String Diagrams_, ([arXiv:1401.7220](https://arxiv.org/abs/1401.7220)).

  (therein: many explicit calculations, colored illustrations, avoiding the common practice of indicating 0-cells by non-filled circles)

For [[traced monoidal categories]] in

* [[Andre Joyal]], [[Ross Street]] and [[Dominic Verity|Verity]], _Traced monoidal categories_.

*  David I. Spivak, Patrick Schultz, Dylan Rupel, _String diagrams for traced and compact categories are oriented 1-cobordisms_, [arxiv](https://arxiv.org/abs/1508.01069)

For [[closed monoidal categories]] in

* [[John Baez]], Quantum Gravity Seminar - Fall 2006.  &lt;http://math.ucr.edu/home/baez/qg-fall2006/index.html#computation>
 {#BaezQG06}

*  {#Rosetta} [[John Baez]] and [[Mike Stay]], *Physics, Topology, Logic and Computation: A Rosetta Stone*, [arxiv](https://arxiv.org/abs/0903.0340)


* Francois Lamarche, *Proof Nets for Intuitionistic Linear Logic: Essential nets*, 2008 [pdf](http://hal.inria.fr/docs/00/34/73/36/PDF/prfnet1.pdf)
 {#Lamarche08}

* Ralf Hinze, *Kan Extensions for Program Optimisation, Or:
Art and Dan Explain an Old Trick*, [pdf](http://www.cs.ox.ac.uk/ralf.hinze/Kan.pdf)

For [[biclosed monoidal categories]] in

* [[Bob Coecke]], Edward Grefenstette, and [[Mehrnoosh Sadrzadeh]], *Lambek vs. Lambek: Functorial vector space semantics and string diagrams for Lambek calculus*, 2013 [link](https://www.sciencedirect.com/science/article/pii/S0168007213000626)

For [[linearly distributive categories]] in 

* [[Richard Blute]] and [[Robin Cockett]] and [[R.A.G. Seely]] and [[Todd Trimble]], *Natural deduction and coherence for weakly distributive categories.
 {#BCST}

* {#DunnVicary17} Lawrence Dunn, [[Jamie Vicary]], _Surface Proofs for Nonsymmetric Linear Logic_ ([arXiv:1701.04917](http://arxiv.org/abs/1701.04917)) 


For [[indexed monoidal categories]] in

* {#BradyTrimble98} Geraldine Brady, [[Todd Trimble]], _[[A string diagram calculus for predicate logic]]_ (1998)

* {#PontoShulman12} [[Kate Ponto]], [[Michael Shulman]], _Duality and traces for indexed monoidal categories_, Theory and Applications of Categories, Vol. 26, 2012, No. 23, pp 582-659 ([arXiv:1211.1555](http://arxiv.org/abs/1211.1555))

For [[symmetric monoidal category|symmetric]] [[traced monoidal categories]] in 

* George Kaye, _The Graphical Language of Symmetric Traced Monoidal Categories_, ([arXiv:2010.06319](https://arxiv.org/abs/2010.06319))

The generalization of string diagrams to one dimension higher is discussed in

* [[Todd Trimble]], _[Surface diagrams](/toddtrimble/published/Surface+diagrams)_

* [[John Barrett]], [[Catherine Meusburger]], [[Gregor Schaumann]], _Gray categories with duals and their diagrams_, available [here](http://arxiv.org/abs/1211.0529).

The generalization to arbitrary dimension in terms of [[opetope|opetopic]] "zoom complexes" is due to 

* {#KockJoyalBataninMascari07} [[Joachim Kock]], [[André Joyal]], [[Michael Batanin]], [[Jean-François Mascari]], _Polynomial functors and opetopes_ ([arXiv:0706.1033](http://arxiv.org/abs/0706.1033)) 

Discussion for [[double categories]] and [[2-category equipped with proarrows|pro-arrow equipments]] is in 

* {#Myers16} David Jaz Myers, _String Diagrams For Double Categories and (Virtual) Equipments_ ([arXiv:1612.02762](https://arxiv.org/abs/1612.02762))

See also at _[[opetopic type theory]]_.

Discussion of sheet diagrams for [[rig categories]] is in

* {#CDH} Cole Comfort, Antonin Delpeuch, [[Jules Hedges]], _Sheet diagrams for bimonoidal categories_, ([arXiv:2010.13361](https://arxiv.org/abs/2010.13361))


### Software

The higher dimensional string diagrams ("zoom complexes" ([Kock-Joyal-Batanin-Mascari 07](#KockJoyalBataninMascari07))) used for presenting [[opetopes]] in the context of [[opetopic type theory]] are introduced in 

* [[Eric Finster]], _Opetopic Diagrams 1 - Basics_ ([video](http://www.youtube.com/watch?v=OANwLohwJqk))

* [[Eric Finster]], _Opetopic Diagrams 2 - Geometry_ ([video](http://www.youtube.com/watch?v=E7OvuA1jRKM))


* [[Globular]] is a web-based proof assistant for finitely-presented semistrict globular higher categories. It allows one to formalize higher-categorical proofs in finitely-presented n-categories and visualize them as string diagrams. 




[[!redirects string diagrams]]
[[!redirects circuit diagram]]
[[!redirects circuit diagrams]]

[[!redirects graphical calculus]]

[[!redirects Penrose notation]]
[[!redirects Penrose graphical notation]]


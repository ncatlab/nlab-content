
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Constructivism, Retalizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

A profound cross-disciplinary insight has emerged -- starting in the late 1970s, with core refinements in recent years -- observing that 
three superficially different-looking fields of [[mathematics]], 

* [[computation]]/[[programming languages]] 

* [[formal logic]]/[[type theory]]

* [[(∞,1)-category|∞-]][[category theory]]/[[(∞,1)-topos|∞-]][[topos theory]] ([[algebraic topology]])

are but three different perspectives on a single underlying phenomenon at the [[foundations of mathematics]]:

\begin{tikzpicture}
  
  \draw (0,0) circle (1.6);
  \draw (75+0:1.6) node {\colorbox{white}{\Large computation}};
  \draw (75+120:1.6) node {\colorbox{white}{\Large spaces}};
  \draw (75+240:1.6) node {\colorbox{white}{\Large  logic}};

\end{tikzpicture}



### Classical

#### Plain
  {#ClassicalPlain}

Under the identifications

1. [[propositions as types]],

1. [[programs as proofs]],

1. [[relation between type theory and category theory]]

the following notions are equivalent:

| In [[intuitionistic mathematics|intuitionistic]] [[logic]] <br/> and [[type theory]]: | In  [[programming languages]] <br/> and [[computation]]: | In [[category theory]] <br/> and [[topos theory]]: |
|--|--|--|
| A [[proof]] of a [[proposition]], <br/> [[propositions as types|or]] a [[term]] of some [[type]]. | A [[program]]/[[λ-term]] with <br/> output of some [[data type]]. | A [[generalized element]] <br/> of an [[object]]. |

\begin{tikzpicture}

\begin{scope}[rotate=(60), scale=(1.2)]

\draw (0,0) circle (2.4);

\draw
  (45:2)
    node
  {\colorbox{white}{
    \fbox{
    \begin{tabular}{c}
      Computation and
      \\
      Programming Language
    \end{tabular}
    }
  }};

\draw
  (45+120:2.4)
    node
  {\colorbox{white}{
    \fbox{
    \begin{tabular}{c}
      Category and
      \\     
      Topos Theory
    \end{tabular}
    }
  }};

\draw
  (45+240:2.4)
    node
  {\colorbox{white}{
    \fbox{
    \begin{tabular}{c}
      Intuitionistic Logic
      \\
      and Type Theory
    \end{tabular}
    }
  }};

\draw (0,-5) node {\phantom{a}};

\end{scope}

\end{tikzpicture}


Whence these three subjects are but three perspectives on a single underlying phenomenon.

This insight dates from the late 1970s; an early record is [Lambek & Scott 86](#LambekScott86); it is explicitly highlighted as a *trilogy* ([Wikipedia](https://en.wikipedia.org/wiki/Trilogy): "three works of art that are connected and can be seen either as a single work or as three individual works") in [Melliès 06, Sec. 1](#Mellies06):

\begin{imagefromfile}
    "file_name": "MelliesClassicalComputationalTrilogy.jpg",
    "width": 510,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Melliès 06](#Mellies06)"
\end{imagefromfile}

(Notice that [Melliès 06](#Mellies06) on [p.2](https://hal.archives-ouvertes.fr/hal-00154243/document#page=3) does mean to regard [[λ-calculus]] as [[programming language]].)




In [Harper 11](#Harper11) the profoundness of the trilogy inspires the following emphatic prose:

> The central dogma of computational trinitarianism holds that Logic, Languages, and Categories are but three manifestations of one divine notion of computation. There is no preferred route to enlightenment: each aspect provides insights that comprise the experience of computation in our lives.

> Computational trinitarianism entails that any concept arising in one aspect should have meaning from the perspective of the other two. If you arrive at an insight that has importance for logic, languages, and categories, then you may feel sure that you have elucidated an essential concept of computation--you have made an enduring scientific discovery.  

For more detailed review see [Eades 12, Sec. 3](#Eades12).



#### Parametrized
 {#ClassicalParametrized}

More is true: Since

1. computation happens in [[contexts]] and is [[proof relevance|proof relevant]];

1. [[categories]] give rise to their [[codomain fibration|systems of]] [[slice categories]] and are in general [[(∞,1)-categories]];

1. [[types]] may [[dependent type theory|depend]] on other types and are in general [[homotopy type theory|homotopy types]]

the traditional computational trilogy [above](#ClassicalPlain) enhances to read as follows:

| In [[dependent type theory|dependent]] <br/> [[homotopy type theory]]: | In  [[programming languages]] <br/> and [[computation]]: | In [[locally cartesian closed (∞,1)-categories|locally cartesian closed]] <br/> [[(∞,1)-categories]]/[[(∞,1)-toposes]]: |
|--|--|--|
| A [[term]] of some [[type]] <br/> in [[context]]. | A [[program]] outputting some [[data type]] <br/> in [[context]]. | A [[generalized element]] of an [[object]] <br/> in a [[slice (∞,1)-category|slice]].  |

See also [Shulman 18](#Shulman18).

In this deeper form yet another equivalence -- to [[algebraic topology]] ([[schreiber:Proper Orbifold Cohomology|Sati & Schreiber 20]], [p. 5](https://ncatlab.org/schreiber/files/orbi210313.pdf#page=5)) -- opens up, as [[generalized elements]] in an [[(∞,1)-topos]] may equivalently be regarded as [[cocycles]] in ([[non-abelian cohomology|non-abelian]]) [[cohomology]], and in [[twisted cohomology]] if in a [[slice (∞,1)-category]] ([[schreiber:Proper Orbifold Cohomology|Sati & Schreiber 20]] [p. 6](https://arxiv.org/pdf/2008.01101.pdf#page=6), [[schreiber:The Character Map in Twisted Non-Abelian Cohomology|FSS 20]]), whence we have a *computational tetralogy*:

> (from Sati&Schreiber 21, "Topological and Quantum Systems")

| In [[dependent type theory|dependent]] <br/> [[homotopy type theory]]: | In  [[programming languages]] <br/> and [[computation]]: | In [[locally cartesian closed (∞,1)-categories|locally cartesian closed]] <br/> [[(∞,1)-categories|∞-categories]]/[[(∞,1)-toposes|∞-toposes]]: | In [[non-abelian cohomology|non-abelian]] [[cohomology]] <br/> [[parametrized homotopy theory|param. homotopy theory]]:
|--|--|--|--|
| A [[term]] of some [[type]] <br/> in [[context]]. | A [[program]] of some [[data type]] <br/> in [[context]]. | An [[generalized element|element]] of an [[object]] <br/> in a [[slice (∞,1)-category|slice]]. | A [[cocycle]] <br/> in [[twisted cohomology]]. |

\begin{tikzpicture}

\begin{scope}[rotate=(60), scale=(1.2)]

\draw (0,0) circle (2.4);

\draw
  (45:2)
    node
  {\colorbox{white}{
    \fbox{
    \begin{tabular}{c}
      Contextual Computation/
      \\
      Programming Language
    \end{tabular}
    }
  }};

\draw
  (45+120:2.4)
    node
  {\colorbox{white}{
    \fbox{
    \begin{tabular}{c}
      Twisted Non-Abelian
      \\
      Cohomology Theory
    \end{tabular}
    }
  }};

\draw
  (45+240:2.4)
    node
  {\colorbox{white}{
    \fbox{
    \begin{tabular}{c}
      Homotopy
      \\
      Type Theory
    \end{tabular}
    }
  }};

\draw (0,-5) node {\phantom{a}};

\end{scope}

\end{tikzpicture}



### Quantum
 {#Quantum}

#### Plain
  {#QuantumPlain}

An analogous trilogy is seen under passage:

1. from [[logic]]/[[type theory]] to [[linear logic]]/[[linear type theory]];

1. from [[computation]] to [[quantum computation]];

1. from [[cartesian closed categories]] to [[closed monoidal categories|closed]].

This is the main point of [Melliès 06, Sec. 1](#Mellies06), only that where Melliès shows "[[proof nets]]" ([p. 4](https://hal.archives-ouvertes.fr/hal-00154243/document#page=5)) we refer to them as "[[quantum computation]]" for better emphasis, following [Abramsky-Coecke 04](quantum+programming+language#AbramskyCoecke04), [Abramsky & Duncan 05](quantum+programming+language#AbramskyDuncan05), [Duncan 06](quantum+programming+language#Duncan06); going back to [Pratt 92](quantum+programming+language#Pratt92):

\begin{imagefromfile}
    "file_name": "MelliesQuantumComputationalTrilogy.jpg",
    "width": 510,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Melliès 06, p. 4](#Mellies06)"
\end{imagefromfile}

See also [Baez & Stay 09](#BaezStay09).

#### Parametrized
 {#QuantumParametrized}

Combining the [classical parametrized trilogy](#ClassicalParametrized) with the [plain quantum trilogy](#QuantumPlain), as one passes

* from classical [[computation]] to **[classically controlled](quantum+computation#ClassicalControlQuantumData) [[quantum computation]]** on [[linear spaces|linear]] [[spaces of quantum states]] parametrized over classical [[data types]];

* from [[dependent type theory|dependent]] [[intuitionistic type theory|intuitionistic]] [[homotopy type theory]] to **[[dependent linear type theory|dependent]] [[linear type theory]]** of dependent [[stable homotopy types]];

* from [[locally cartesian closed categories]]/[[locally cartesian closed (∞,1)-categories|(∞,1)-categories]] to **[[indexed monoidal categories]]/[[indexed monoidal (∞,1)-categories|(∞,1)-categories]]** of [[parametrized spectra]];

  which in the language of [[algebraic topology]] is the context of **[[twisted generalized cohomology|twisted]] [[generalized cohomology theory]]**.

there appears the "classically controlled quantum computational tetralogy":

> (from Sati & Schreiber 21, "Topological and Quantum Systems")

| In [[dependent linear type theory|dependent linear]] <br/> [[homotopy type theory]]: | In  [classically controlled](quantum+computation#ClassicalControlQuantumData) <br/> [[quantum programming languages]]: | In [[indexed monoidal (∞,1)-categories|indexed monoindal]] <br/> [[parameterized stable homotopy theory|∞-cats of par. spectra]]: | In [[Whitehead generalized cohomology theory|Whitehead-generalized]] <br/> [[twisted cohomology theory]]:
|--|--|--|--|
| A [[term]] of some [[type]] <br/> in [[context]]. | A [[quantum circuit]] <br/> controlled by [[data type|classical data]].  | An [[generalized element|element]] of an [[object]] <br/> in a [[slice (∞,1)-category|slice]]. | A [[cocycle]] <br/> in [[twisted cohomology]]. |


\begin{tikzpicture}

\begin{scope}[rotate=(60), scale=(1.2)]

\draw (0,0) circle (2.4);

\draw
  (45:2)
    node
  {\colorbox{white}{
    \fbox{
    \begin{tabular}{c}
      Classically Controlled
      \\
      Quantum Computation
    \end{tabular}
    }
  }};

\draw
  (45+120:2.4)
    node
  {\colorbox{white}{
    \fbox{
    \begin{tabular}{c}
      Twisted Generalized
      \\
      Cohomology Theory
    \end{tabular}
    }
  }};

\draw
  (45+240:2.4)
    node
  {\colorbox{white}{
    \fbox{
    \begin{tabular}{c}
      Linear Homotopy
      \\
      Type Theory
    \end{tabular}
    }
  }};

\draw (0,-5) node {\phantom{a}};

\end{scope}

\end{tikzpicture}

(along the lines of [[schreiber:Quantization via Linear homotopy types|Schreiber 14]], [[schreiber:master thesis Nuiten|Nuiten 13]],

* with parametrized stable homotopy theory understood as twisted cohomology theory as in [Ando, Blumberg & Gepner 10](twisted+cohomology#ABG10), [Ando, Blumberg, Gepner & Hopkins 14](#twisted+cohomology#ABGHR14), [[schreiber:The Character Map in Twisted Non-Abelian Cohomology|Fiorenza, Sati, & Schreiber 20]];

* with dependent linear homotopy type theory understood as, e.g., in [Riley, Finster & Licata 21](dependent+linear+type+theory#RileyFinsterLicata21) following [[schreiber:differential cohomology in a cohesive topos|Schreiber 13]] [Prop. 4.1.9](https://arxiv.org/pdf/1310.7930v1.pdf#page=446);

* with classically controlled quantum computation seen as dependent linear type theory, as stated fully explicitly in [Fu, Kishida & Selinger 20](quantum+programming+language#FKS20), [Fu, Kishida, Ross & Selinger 20](quantum+programming+language#FKS20) and more tentatively before in [Vakar 14](dependent+linear+type+theory#Vakar14), [Vakar 15](dependent+linear+type+theory#Vakar15), [Vakar 17](dependent+linear+type+theory#Vakar17), following [[schreiber:Quantization via Linear homotopy types|Schreiber 14]])


\linebreak


\begin{imagefromfile}
    "file_name": "ComputationalTrilogyTopologizedQuantized.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From Sati+Schreiber21: 'Topological and Quantum Systems'"
\end{imagefromfile}


\linebreak

## Rosetta stone

The following shows a rosetta stone dictionary with more details:

> (NB. This table shows the computational aspect mostly under "type theory"...)

[[!include types and logic - table]]



## Related concepts

* [[syntax-semantics duality]]

* [[relation between category theory and type theory]]

* [[programs as proofs]], [[propositions as types]]

* [[initiality conjecture]]

## References

In the introduction of 

* {#Mellies06} [[Paul-André Melliès]], _Functorial boxes in string diagrams_, Procceding of _Computer Science Logic 2006_ in Szeged, Hungary. 2006 ([hal:00154243](https://dumas.ccsd.cnrs.fr/PPS/hal-00154243), [pdf](https://hal.archives-ouvertes.fr/hal-00154243/document), [[MelliesFunctorialBoxesInStringDiagrams.pdf:file]])
 
the insight is recalled to have surfaced in the 1970s, with an early appearance in print being the monograph

* {#LambekScott86} [[Joachim Lambek]], [[Phil Scott]], _Introduction to Higher Order Categorical Logic_, Cambridge Studies in Advanced Mathematics Vol. 7. Cambridge University Press, 1986 (ISBN:978-0-521-24665-1)

See also at _[History of categorical semantics of linear type theory](linear+type+theory#HistoryCategoricalSemantics)_ for more on this.

A exposition of the relation between the three concepts is in

* {#Harper11} [[Robert Harper]], _The Holy Trinity_ (2011) ([web](http://existentialtype.wordpress.com/2011/03/27/the-holy-trinity/), [wayback machine snapshot](https://web.archive.org/web/20170921012554/http://existentialtype.wordpress.com/2011/03/27/the-holy-trinity/)) 

* {#Eades12} [[Harley Eades]], Section 3 of: *Type Theory and Applications*, 2012 ([pdf](https://metatheorem.org/includes/pubs/comp.pdf), [[EadesTypeTheoryAndApplications.pdf:file]])
 
* {#Frumin14} Dan Frumin, _Computational trinitarianism_, Feb 2014 ([prezi slides](http://prezi.com/fnz-4wzsygiq/computational-trinitarianism/))

An exposition with emphasis on [[linear logic]]/[[quantum logic]] and the relation to [[physics]] is in

* {#BaezStay09} [[John Baez]], [[Mike Stay]], _Physics, Topology, Logic and Computation: A Rosetta Stone_, Notes in Physics vol. 813, Springer, Berlin, 2011, pp. 95-174 ([arXiv:0903.0340](http://arxiv.org/abs/0903.0340))

Discussion in the context of [[homotopy type theory]]:

* {#Shulman18} [[Mike Shulman]], *Homotopical trinitarianism: A perspective on homotopy type theory*, 2018 ([pdf slides](http://home.sandiego.edu/~shulman/papers/trinity.pdf), [[ShulmanHomotopicalTrinitarianism.pdf:file]])

For further references see at _[[programs as proofs]]_, _[[propositions as types]]_, and _[[relation between category theory and type theory]]_.

Textbooks on the [[foundations of mathematics]] and foundations of [[programming language]] which connect via the common theme of [[type theory]]/[[categorical logic]] include the following:

* [[Paul Taylor]], _[[Practical Foundations of Mathematics]]_ ([web](http://www.paultaylor.eu/~pt/prafm/index.html))

* [[William Lawvere]], [[Robert Rosebrugh]], _[[Sets for Mathematics]]_,  Cambridge UP  2003 ([book homepage](http://www.mta.ca/~rrosebru/setsformath/), [GoogleBooks](http://books.google.de/books?id=h3_7aZz9ZMoC&pg=PP1&dq=sets+for+mathematics), [pdf](http://patryshev.com/books/Sets%20for%20Mathematics.pdf))

* [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_,  Cambridge University Press (2016) ([ISBN:9781107150300](http://www.cambridge.org/us/academic/subjects/computer-science/programming-languages-and-applied-logic/practical-foundations-programming-languages-2nd-edition?format=HB))

See also

* [[Joseph A. Goguen]], _[[A Categorical Manifesto]]_. In _Mathematical Structures in Computer Science_ **1** 1 (1991) 49-67 ([doi:10.1017/S0960129500000050](https://doi.org/10.1017/S0960129500000050), [CiteSeerX](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.13.362).


[[!redirects computational trinitarianism]]
[[!redirects computational trinitarianism]]
[[!redirects computational trinity]]


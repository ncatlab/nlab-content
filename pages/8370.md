
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
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea

### Classical

Under the identifications

1. [[propositions as types]]

1. [[programs as proofs]]

1. [[relation between type theory and category theory]]

the following notions are equivalent:

1. A [[proof]] of a [[proposition]]. (In [[logic]].)

2. A [[program]] with output some [[type]]. (In [[type theory]] and [[computer science]].)

3. A [[generalized element]] of an [[object]]. (In [[category theory]].)

This goes back, at least, to [Lambek & Scott 86](#LambekScott86) and is referred to as "computational trinitarianism" in the exposition of [Harper 11](#Harper11):

> The central dogma of computational trinitarianism holds that Logic, Languages, and Categories are but three manifestations of one divine notion of computation.  There is no preferred route to enlightenment: each aspect provides insights that comprise the experience of computation in our lives.

> Computational trinitarianism entails that any concept arising in one aspect should have meaning from the perspective of the other two.  If you arrive at an insight that has importance for logic, languages, and categories, then you may feel sure that you have elucidated an essential concept of computation--you have made an enduring scientific discovery. ([Harper](#Harper)) 

\linebreak

The following shows a rosetta stone dictionary with more details:

[[!include types and logic - table]]


### Quantum
 {#Quantum}

There is an analogous *Quantum Computational Trinitarianism* as one passes:

* from classical [[computation]] to **[classically controlled](quantum+computation#ClassicalControlQuantumData) [[quantum computation]]** on [[linear spaces|linear]] [[spaces of quantum states]] parametrized over classical [[data types]];

* from [[dependent type theory|dependent]] [[intuitionistic type theory|intuitionistic]] [[homotopy type theory]] to **[[dependent linear type theory|dependent]] [[linear type theory]]** of dependent [[stable homotopy types]];

* from [[locally cartesian closed categories]]/[[locally cartesian closed (∞,1)-categories|(∞,1)-categories]] to **[[indexed monoidal categories]]/[[indexed monoidal (∞,1)-categories|(∞,1)-categories]]** of [[parametrized spectra]];

  which in the language of [[algebraic topology]] is the context of **[[twisted generalized cohomology|twisted]] [[generalized cohomology theory]]**;


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




## Related concepts

* [[syntax-semantics duality]]

* [[relation between category theory and type theory]]

* [[programs as proofs]], [[propositions as types]]

* [[initiality conjecture]]

## References

In the introduction of 

* {#Mellies06} [[Paul-André Melliès]], _Functorial boxes in string diagrams_, Procceding of _Computer Science Logic 2006_ in Szeged, Hungary. 2006 ([article](https://dumas.ccsd.cnrs.fr/PPS/hal-00154243))
 
the insight is recalled to have surfaced in the 1970s, with an early appearance in print being the monograph

* {#LambekScott86} [[Joachim Lambek]], [[Phil Scott]], _Introduction to Higher Order Categorical Logic_, Cambridge Studies in Advanced Mathematics Vol. 7. Cambridge University Press, 1986 (ISBN:978-0-521-24665-1)

See also at _[History of categorical semantics of linear type theory](linear+type+theory#HistoryCategoricalSemantics)_ for more on this.

A exposition of the relation between the three concepts is in

* {#Harper11} [[Robert Harper]], _The Holy Trinity_ (2011) ([web](http://existentialtype.wordpress.com/2011/03/27/the-holy-trinity/), [wayback machine snapshot](https://web.archive.org/web/20170921012554/http://existentialtype.wordpress.com/2011/03/27/the-holy-trinity/)) 

* [[Harley Eades]], Section 3 of: *Type Theory and Applications*, 2012 ([pdf](https://metatheorem.org/includes/pubs/comp.pdf))
 
* {#Frumin14} Dan Frumin, _Computational trinitarianism_, Feb 2014 ([prezi slides](http://prezi.com/fnz-4wzsygiq/computational-trinitarianism/))

An exposition with emphasis on [[linear logic]]/[[quantum logic]] and the relation to [[physics]] is in

* [[John Baez]], [[Mike Stay]], _Physics, Topology, Logic and Computation: A Rosetta Stone_, Notes in Physics vol. 813, Springer, Berlin, 2011, pp. 95-174 ([arXiv:0903.0340](http://arxiv.org/abs/0903.0340))

A discussion in the context of [[homotopy type theory]] is in

* [[Mike Shulman]], *Homotopical trinitarianism*, [talk slides](http://home.sandiego.edu/~shulman/papers/trinity.pdf)

For further references see at _[[programs as proofs]]_, _[[propositions as types]]_, and _[[relation between category theory and type theory]]_.

Textbooks on the [[foundations of mathematics]] and foundations of [[programming language]] which connect via the common theme of [[type theory]]/[[categorical logic]] include the following:

* [[Paul Taylor]], _[[Practical Foundations of Mathematics]]_ ([web](http://www.paultaylor.eu/~pt/prafm/index.html))

* [[William Lawvere]], [[Robert Rosebrugh]], _[[Sets for Mathematics]]_,  Cambridge UP  2003 ([book homepage](http://www.mta.ca/~rrosebru/setsformath/), [GoogleBooks](http://books.google.de/books?id=h3_7aZz9ZMoC&pg=PP1&dq=sets+for+mathematics), [pdf](http://patryshev.com/books/Sets%20for%20Mathematics.pdf))

* [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_,  Cambridge University Press (2016) ([webpage](http://www.cambridge.org/us/academic/subjects/computer-science/programming-languages-and-applied-logic/practical-foundations-programming-languages-2nd-edition?format=HB))

See also

* [[Joseph A. Goguen]], _[[A Categorical Manifesto]]_. In _Mathematical Structures in Computer Science_, Vol. 1, No. 1. (1991), pp. 49-67, doi:[10.1017/S0960129500000050](https://doi.org/10.1017/S0960129500000050), [CiteSeerX](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.13.362).



[[!redirects computational trinitarianism]]
[[!redirects computational trinity]]
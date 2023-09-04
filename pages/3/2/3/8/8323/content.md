
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



# Structural rules
* table of contents
{: toc}

## Idea

\begin{imagefromfile}
    "file_name": "Gentzen-StrukturSchlussfiguren.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [Gentzen 1935](#Gentzen35))"
\end{imagefromfile}


### General

In [[formal logic]] and [[type theory]], by the _structural inference rules_ &lbrack;[Gentzen 1935 §1.2.1](#Gentzen35), [1969, §1.21](#Gentzen69)&rbrack; of a [[deductive system]]  one means those [[inference rules]] which make no reference to [logical operations](formal+logic#LogicalOperations) but only to the unstructured [[premises]] of a [[deduction]].

In standard [[intuitionistic logic]] ([[intuitionistic type theory]]) the structural rules notably include the [[weakening rule]] and the [[contraction rule]] in the [[antecedent]], which exhibit [[context extensions]] $\Gamma \,\mapsto\, \Gamma, P$ as admitting [[natural transformation|natural]] [[diagonal map|diagonal]] and [[projection]] [[maps]], respectively, hence as admitting [[categorical semantics|interpretation]] as *[[cartesian products]]* $\Gamma \times P$ (cf. [Jacobs 1994](structural+rule#Jacobs94)):

\begin{imagefromfile}
    "file_name": "WeakeningContractionRules-230330d.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Discarding these rules leads to [[linear logic]] ([[linear type theory]]). 

Generally, logical systems discarding some structural rules are called *[[substructural logics]]*.


### In dependent type theory
 {#InDependentTypeTheory}

In ([[intuitionistic type theory|intuitionistic]]) [[dependent type theory]] the structural rules include (e.g. [Jacobs (1998), p. 122](#Jacobs98), [UFP13, A.2.2](#UFP13), [Rijke (2018), Sec. 1.4](#Rijke18)):

* the [[variable rule]], 

* the [[weakening rule]], 

* the [[substitution rule]]

shown in the following table together with their [[categorical semantics]] [[categorical semantics of dependent types|of dependent types]]:

<center>
<img src="/nlab/files/DependentTermsSyntaxAndSemantics-230326.jpg" width="650">
</center>

<center>
<img src="/nlab/files/StructuralTypeInferenceRules-230326b.jpg" width="650">
</center>


## Examples

* [[structural rules]]

  * [[identity rule]]

  * [[weakening rule]]

  * [[contraction rule]]

  * [[exchange rule]]

  * [[substitution rule]]

  * [[cut rule]]


## Sub-structural logic

If some of the structural rules are *not* imposed in a [[formal logic]] one speaks of *[[substructural logic]]*.

For instance, if the [[weakening rule]] and [[contraction rule]] are omitted, one speaks of [[linear logic]]/[[linear type theory]] (see [there](linear+logic#AbsenceOfWeakeningAndContraction)), since then the [[logical conjunction]] is no longer consrained to behave like a [[Cartesian product]] but may behave like a non-cartesian [[tensor product]].




## References

The notion of the structural inference rules originates (under the German name *Struktur-Schlußfiguren*) with 

* {#Gentzen35} [[Gerhard Gentzen]], §1.2.1 in: _Untersuchungen &#252;ber das logische Schlie&#223;en. I_, _Mathematische Zeitschrift_ **39** 1 (1935) &lbrack;[doi:10.1007/BF01201353](http://dx.doi.org/10.1007/BF01201353)&rbrack;

* {#Gentzen69} [[Gerhard Gentzen]], §1.21 in: *Investigations into Logical Deduction*, in M. E. Szabo (ed.), *The Collected Papers of Gerhard Gentzen*, Studies in Logic and the Foundations of Mathematics **55**, Springer (1969) 68-131 &lbrack;[ISBN:978-0-444-53419-4](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/55), [pdf](https://logic-teaching.github.io/prop/texts/Gentzen%201969%20-%20Investigations%20into%20Logical%20Deduction.pdf)&rbrack;

Review:

* [[Anne Sjerp Troelstra]], §1.5 in: *Lectures on Linear Logic*, CSLI Lectures notes **29** (1992) &lbrack;[ISBN:0937073776](https://web.stanford.edu/group/cslipublications/cslipublications/site/0937073776.shtml)&rbrack;


Their [[categorical semantics]] is made explicit in:

* {#Jacobs94} [[Bart Jacobs]], *Semantics of weakening and contraction*, Annals of Pure and Applied Logic **69** 1 (1994) 73-106 &lbrack;<a href="https://doi.org/10.1016/0168-0072(94)90020-5">doi:10.1016/0168-0072(94)90020-5</a>&rbrack;

Discussion in [[dependent type theory]]:

* {#Jacobs98} [[Bart Jacobs]], p. 122, 585 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;

  > (emphasis on the [[categorical model of dependent types]])

* {#UFP13} [[Univalent Foundations Project]], §A of *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

  > (in the context of [[homotopy type theory]])


* {#Rijke18} [[Egbert Rijke]], *Dependent type theory* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/dtt.pdf)&rbrack;, Lecture 1 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;

  > (in the context of [[homotopy type theory]])


[[!redirects structural rule]]
[[!redirects structural rules]]

[[!redirects structural inference rule]]
[[!redirects structural inference rules]]

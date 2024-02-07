
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


# Bunched logic
* table of contents
{:toc}

## Idea
 {#Idea}

In [[formal logic]], and more specifically in [[sequent calculus]]/[[natural deduction]]/[[type theory]], a **bunched logic** is a logical [[theory]] in which the [[formulas]] appearing in any [[context]] are not necessarily just a [[list]] but have some additional structure, usually that of [[tree]] whose nodes are then the eponymous "bunches":

Where a classical [[context]] is traditionally presented as a comma-separated [[list]] of [[propositions]] [[propositions as types|and/or]] [[types]], e.g.

$$
  \Gamma 
  ,\;
  X
  ,\;
  Y
  \;\;\;
  ctxt
  \,,
$$

which classically may always be thought of as a ([[dependent pair type|dependent]]) classical [[product type]]

$$
  \Gamma 
  \times
  X
  \times
  Y
  \;\;\;
  ctxt
  \,,
$$

so a context in bunched logic is allowed, more generally, to be a nested list of *[[structural rule|structural]] [[logical connective|connectives]]*, iterating between this comma-denoted conjunction and another connective typically denoted by a semicolon, e.g.:


$$ 
  A,\;
  B,\;
  \big(
    C;\;
    (D,\,E);
    \;
    F
  \big),\;
  (G;\,H) 
  \;\;\;\;
  ctxt
  \,.
$$

The original and common motivation for such "bunched contexts" is the existence of further ([[function types]] and) [[product types]] *in addition* to the classical ones; such as in [[linear type theories]] with their additional ([[linear implication]] $(-)\multimap (-)$ and) [[linear conjunction]] $(-)\otimes (-)$, and more generally in the [[internal logic]] of a [[doubly closed monoidal category]], whence bunched contexts as above may usefully be thought of as types formed consecutively from [[cartesian products]] and another [[tensor product]]: 

$$ 
  A
  \times
  B  
  \times
  \big(
    C
    \otimes
    (D \times E)
    \otimes
    F
  \big)
  \times
  (G \otimes H) 
  \;\;\;\;
  ctxt
  \,.
$$

> (NB: In saying this we are reversing the role of commas and semicolons as compared to the original literature on bunched logic, so that the comma retains it original meaning as the classical connective.)

Accordingly, the bunched context indicates a variation of [[structural rules]]: The classical product $\times$ will admit the [[contraction rule]] and/or the [[weakening rule]], while $\otimes$ may not.


Notice that the general phrase *bunched logic* is not entirely standard, and the word "bunches" has been used with more than one logic of this form. 

The notion (together with its [[categorical semantics]] in [[doubly closed monoidal categories]]) originates with the logic of "bunched implication" (BI) and its "$\alpha \lambda$-calculus" (a bunched variation of the [[lambda-calculus]]) due to &lbrack;[O'Hearn & Pym (1999)](#O'HearnPym99), [Pym (2002)](#Pym2002), see also [O'Hearn (2003)](#O'Hearn03).

{#Unsatisfactory} But aspects of the proposal of [O'Hearn & Pym (1999)](#O'HearnPym99) and [Pym (2002)](#Pym2002) have remained unsatisfactory, see [Pym (2008), Errata to Pym (2002)](#Pym08Errata) and [Riley(2022)](#Riley22Thesis), [pp. 19](https://mvr.hosting.nyu.edu/pubs/thesis.pdf#page=29) and Rem. 1.4.1 ([p. 64](https://mvr.hosting.nyu.edu/pubs/thesis.pdf#page=64)): 

> &lbrack;[Riley 2022, pp. 19](https://mvr.hosting.nyu.edu/pubs/thesis.pdf#page=29)&rbrack;: &lbrack;Since&rbrack; context manipulations are not recorded in the terms, typechecking a term can be difficult. First, it is not always obvious when and how the contraction rule has to be applied, and secondly, it is not always obvious how the context has to be split into two pieces to apply $\multimap$-ELIM. Besides the challenge of typechecking, the combination of the weakening rule and the rules for the monoidal unit also breaks soundness for the intended semantics.

> The various extensions of the αλ-calculus that have since appeared &lbrack;BO06; CPR08; SS04; Atk04&rbrack; do not resolve these issues. It is also not so clear how to add [[dependent types]] to this system and how dependency should behave between bunches.

Further developments had not resolved the fundamental issue:

> {#UnsatisfactorySchöppStark} &lbrack;[Riley 2022, p. 91](https://mvr.hosting.nyu.edu/pubs/thesis.pdf#page=101):&rbrack; Schöpp and Stark’s Bunched Dependent Type Theory &lbrack;[Schöpp & Stark (2004)](#SchöppStark04)&rbrack; &lbrack;admits&rbrack; no dependency across bunches. The corresponding monoidal pair type therefore requires the input types to be closed. &lbrack;...&rbrack; the monoidal unit is the terminal object. This is certainly not the case in &lbrack;linear&rbrack; models of interest.

In reaction to this, [Riley (2022)](#Riley22Thesis) proposes an enhanced form of bunched type theory which is claimed to fix all these problems at least in the case that the second structural connective $\otimes$ is a [[multiplicative conjunction]] in a [[linear type theory]], hence for a form of [[dependent linear type theory]]. The key new ingredients in [Riley (2022)](#Riley22Thesis) to make this work are: 

1. a [[classical modality]] $\natural$ which from any "parameterized linear type" projects out the underlying classical type;

2. a decoration of bunched contexts by "color palettes" which keep explicit track of the bunching/tree structure. 

  (On the other hand, this second point leads to a proliferation of [[inference rules]], but maybe that's what it takes.)



## Examples

### Bunched implications

In **bunched implications** logic ([O'Hearn & Pym (1999)](#O'HearnPym99)), the semicolon allows contraction and weakening while the comma does not.  This allows defining both an [[additive conjunction]] and a [[multiplicative conjunction]], internalizing the semicolon and the comma respectively, such that both [[distributive law|distribute]] over the "" [[additive disjunction]] and moreover both come with a corresponding implication: the "additive" [[implication]] and the [[multiplicative implication]].

### Relevance logic

Some forms of [[relevance logic]] can be presented with a bunched sequent calculus that is similar to BI, but in which the comma also has contraction (though not weakening) and there is no additive implication.  See for instance ([Mints](#Mints)).

### Classical bunched implication

A logic of **classical bunched implication** is like BI but with arbitrary bunches on the right as well as on the left.  On the right, the semicolon represents the [[additive disjunction]] and the comma represents a [[multiplicative disjunction]], and there are both an additive and a multiplicative [[negation]] that move formulas back and forth.  Both negations are "classical" with respect to their corresponding connectives, e.g. we have $\sim\sim A \multimap A$ (where $\sim$ is the multiplicative negation and $\multimap$ the multiplicative implication) and also $\neg\neg A \to A$ (where $\neg$ is the additive negation and $\to$ the additive implication).  See [Pym 2002](#Pym2002) and [this discussion](https://nforum.ncatlab.org/discussion/4004/paraconsistent-logic/?Focus=57557#Comment_57557).

### Dependent versions

Bunched logics are also used to combine linear type theories with [[dependent type theories]].  See some of the references at [[dependent linear type theory]].

## Categorical semantics

Bunched logics naturally have semantics in categories with more than one [[monoidal structure]], so that a bunch such as $(A,(B;C),((D,E);F))$ can be interpreted as $A \otimes (B\boxtimes C) \otimes ((D\otimes E)\boxtimes F)$.  Frequently (e.g. if one kind of bunch admits contraction and weakening) one of the two monoidal structures is a [[cartesian monoidal category|cartesian]] one.  A typical and motivating example of a model for BI is the [[category of presheaves]] $[C^{op},Set]$ over a monoidal category $C$, which comes equipped both with the ordinary [[ccc structure on presheaves]] as well as the closed monoidal structure given by [[Day convolution]].

## Related pages

* [[linear logic]]

* [[doubly closed monoidal category]]

* [[relevance logic]]

* [[separation logic]]

* [[display logic]]

* [[substructural logic]]

* [[monoidal topos]]


## References

Precursors:

* {#Mints} G. E. Mints. *Cut-elimination theorem for relevant logics*, Zap. Nauchn. Sem. LOMI, 1972,	Volume 32, Pages 90&#8211;97. ([math-net.ru](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=znsl&paperid=2569&option_lang=eng)).
An English translation appears in the Journal of Soviet Mathematics 6 (1976) 422-8 &lbrack;[doi:10.1007/BF01084083](http://doi.org/10.1007/BF01084083)&rbrack;

The original articles:

* {#O'HearnPym99} [[Peter O'Hearn]], [[David J. Pym]], *The Logic of Bunched Implications*, The Bulletin of Symbolic Logic **5** 2 (1999) 215-244  &lbrack;[pdf](http://www.lsv.ens-cachan.fr/~demri/OHearnPym99.pdf), [doi:10.2307/421090](https://doi.org/10.2307/421090)&rbrack;
  
* {#Pym2002} [[David Pym]], *The Semantics and Proof Theory of the Logic of Bunched Implications*, Applied Logic Series **26**, Springer (2002) &lbrack;[doi:10.1007/978-94-017-0091-7](https://doi.org/10.1007/978-94-017-0091-7), [GoogleBooks](https://books.google.com/books/about/The_Semantics_and_Proof_Theory_of_the_Lo.html?id=0bAfqhzDuOcC&redir_esc=y)&rbrack;

  {#Pym08Errata} Errata and Remarks for *The Semantics and Proof Theory of the Logic of Bunched Implications* (2008) &lbrack;[pdf](https://www.cantab.net/users/david.pym/BI-monograph-errata.pdf), [[Pym-BI-Errata.pdf:file]]&rbrack;

  > &lbrack;[p. 5](https://ncatlab.org/nlab/files/Pym-BI-Errata.pdf#page=5)&rbrack; "Items 3, 4, and 5 in the errata for Chapter 12 and 4, 5 in Chapter 13, whilst necessary to fix a technical problem, leave us in a conceptually and computationally undesirable situation: we have no clean characterization of a useful notion of well-formedness, leading to obvious computational difficulties in, say, theorem proving. We conclude that such a highly multiplicative system is far too complex, at least in its current formulation, to be of much value. All of the applications of multiplicative quantifiers known to-date require much simpler systems. It is the author's recommendation that readers should not devote very much of their resources to studying the system of predicate BI discussed in these chapters"


* {#O'Hearn03} [[Peter O'Hearn]], *On bunched typing*, Journal of Functional Programming **13** 4 (2003) 747-796 &lbrack;[doi:10.1017/S0956796802004495](https://doi.org/10.1017/S0956796802004495)&rbrack;

Review and further development:

* Bodil Biering, *On the logic of bunched implications -- and its relation to separation logic*, MSc thesis, Copenhagen (2004) &lbrack;[[Biering-BunchedLogic.pdf:file]]&rbrack;
 

* Brotherston and Calcagno, *Classical BI: Its Semantics and Proof Theory*, [arxiv](http://arxiv.org/abs/1005.2340)


Discussion of bunched logic with the [[linear logic]]-part regarded as a [[quantum logic]]:

* [[Li Zhou]], [[Gilles Barthe]], [[Justin Hsu]], [[Mingsheng Ying]], [[Nengkun Yu]], *A Quantum Interpretation of Bunched Logic for Quantum Separation Logic*, LICS '21: Proceedings of the 36th Annual ACM/IEEE Symposium on Logic in Computer Science  75 (2021) 1–14 &lbrack;[arXiv:2102.00329](https://arxiv.org/abs/2102.00329), [doi:10.1109/LICS52264.2021.9470673](https://doi.org/10.1109/LICS52264.2021.9470673)&rbrack;




A bunched [[dependent type theory]], to some extent:

* {#SchöppStark04} [[Ulrich Schöpp]], [[Ian Stark]], *A Dependent Type Theory with Names and Binding*, in *Computer Science Logic. CSL 2004*, Lecture Notes in Computer Science **3210** (2004) 235–249 &lbrack;[doi:10.1007/978-3-540-30124-0_20](https://doi.org/10.1007/978-3-540-30124-0_20), [web](https://homepages.inf.ed.ac.uk/stark/names+binding.html)&rbrack;


Further refinement to *dependent bunches*  for a [[dependent linear types|dependent linear]] [[homotopy type theory|homotopy types]]:    

* {#Riley22Thesis} [[Mitchell Riley]], *A Bunched Homotopy Type Theory for Synthetic Stable Homotopy Theory*, PhD Thesis (2022) &lbrack;[doi:10.14418/wes01.3.139](https://doi.org/10.14418/wes01.3.139), [ir:3269](https://digitalcollections.wesleyan.edu/object/ir%3A3269), [pdf](https://mvr.hosting.nyu.edu/pubs/thesis.pdf)&rbrack;

* {#Riley22} [[Mitchell Riley]], *Linear Homotopy Type Theory*, talk at: [HoTTEST Event for Junior Researchers 2022](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest_junior_2022.html)  (Jan 2022) &lbrack;slides: [pdf](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Riley-2022-01-20-HoTTEST.pdf), video: [YT](https://www.youtube.com/watch?v=o2oWhHabjdM)&rbrack;

* [[Mitchell Riley]], *Dependent Type Theories à la Carte*, talk at *[[CQTS]] Initial Researcher's Meeting* (Sep 2022) &lbrack;[[CQTS-InitialResearcherMeeting-Riley-220913.pdf:file]]&rbrack;


[[!redirects bunched logics]]
[[!redirects bunch]]
[[!redirects bunches]]
[[!redirects bunched implication]]
[[!redirects bunched implications]]
[[!redirects BI]]
[[!redirects structural connective]]
[[!redirects structural connectives]]


[[!redirects bunched type theory]]
[[!redirects bunched type theories]]

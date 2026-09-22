
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--



\tableofcontents


## Idea

A **large cardinal** is a [[cardinal number]] that is larger than can be proven to exist in the ambient [[set theory]], usually [[ZF]] or ZFC.  Large cardinals arrange themselves naturally into a more or less linear order of size and consistency strength, and provide a convenient yardstick to measure the consistency strength of various other assertions that are unprovable from ZFC.

Set theorists often adopt the existence of certain large cardinals as [[axioms]] in the [[foundation of mathematics]].

## List of large cardinal conditions

### Large cardinals with replacement

* [[axiom of infinity]] -- a large cardinal axiom relative to finitist theories, but not relative to ZF

* [[regular cardinal]] - a large cardinal in strongly [[predicative mathematics]] where function sets and power sets do not exist. 

* [[inaccessible cardinal]] -- the smallest sort of large cardinal in ZF, equivalent to the existence of a [[Grothendieck universe]].

* [[hyper-inaccessible cardinal]]

* [[Mahlo cardinal]]

* [[weakly compact cardinal]]

* [[measurable cardinal]] -- the boundary between "small" large cardinals and "large" large cardinals

* [[real-valued-measurable cardinal]], a “solution” to the Banach–Ulam problem.

* [[strongly compact cardinal]], whose existence controls properties images of [[accessible functors]]

* [[elementary embedding]] -- a tool used in the study of large large cardinals. 

* [[supercompact cardinal]]

* [[extendible cardinal]] 

* [[C(n)-extendible cardinal]]

* [[Vopěnka's principle]] -- a large cardinal axiom with important implications for the behavior of [[locally presentable categories]] and [[accessible categories]].

* [[wholeness axiom]]

* [[rank-to-rank axiom]]

* [[Reinhardt cardinal]] -- a large cardinal axiom that inconsistent with [[ZFC]] due to [[Kunen's inconsistency theorem]]; one has to move either to [[ZF]] or [[ZC]]. 

* [[Berkeley cardinal]] -- a large cardinal axiom larger than [[Reinhardt cardinals]] that is also inconsistent with [[ZF]] + [[countable choice]]. It is still consistent with [[ZF]] however. 

* [[club Berkeley cardinal]]

* [[limit club Berkeley cardinal]]

Here is a diagram showing the relation between these:

\begin{imagefromfile}
    "file_name": "LargeCardinalsDiagram.jpg",
    "width": 570,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}


In the context of [[ZFC]], certain axioms are inconsistent with large cardinal axioms:

[[ZFC-large-cardinals-consistency-strength.png:pic]]

### Large cardinals without replacement

The [[axiom of replacement]] is an axiom schemata that states that certain [[families]] of sets or [[diagrams]] in the [[category of sets]], which usually can be proven (for example, in [[Zermelo set theory]] or in a [[well-pointed topos]]) to be [[large sets|large]] or [[proper classes]], are instead [[small set|small]]. 

In the absence of the [[axiom of replacement]], there are certain cardinals which are now large. For example, a [[beth fixed point]] is a cardinal which is small in the presence of the [[axiom of replacement]] and large in the absence of the [[axiom of replacement]]. 

Furthermore [[Reinhardt cardinals]] are now consistent with the [[axiom of choice]] in the absence of the [[axiom of replacement]]. 

[[Vopěnka's principle]] implies the [[axiom of replacement]]. 

### Large cardinals without full separation

In the absence of the [[axiom of full separation]], such as in [[BZC]] or [[Mostowski set theory]], most of the large cardinal axioms mentioned above traditionally stronger than [[Mahlo cardinals]] in [[ZFC]] are instead weaker than [[Mahlo cardinals]]. While the large cardinal axioms imply the existence of [[recursively Mahlo cardinals]]; they are not strong enough to imply the usual [[Mahlo cardinals]]. This spans the entire gamut of large cardinals from weakly compact cardinals to Ramsey cardinals to [[measurable cardinals]] to the [[wholeness axiom]], and the $I_0$ through $I_3$ axioms all the way to [[Reinhardt cardinals]]. 

Furthermore, many large cardinals can be defined in more than one way. In the absence of the [[axiom of full separation]], these definitions no longer coincide with each other. Many large cardinals traditionally between [[Mahlo cardinals]] and [[measurable cardinals]] in [[ZFC]] have this property: they each have a combinatorial definition and a model-theoretic definition, and without full separation, the combinatorial definition of the cardinal does not coincide with the model-theoretic definition of the cardinal. Examples of such cardinals include weakly compact cardinals, subtle cardinals, ineffable cardinals, Erdős cardinals, Silver cardinals, Jónsson cardinals, Rowbottom cardinals, Ramsey cardinals, Magidor cardinals, and [[measurable cardinals]]. In addition, only the model-theoretic definition has sufficient power to prove the existence of recursively [[Mahlo cardinals]], and none of the definitions has sufficient power to prove the existence of the usual [[Mahlo cardinals]]. 

## References

* Wikipedia has a [list of large cardinal properties](http://en.wikipedia.org/wiki/List_of_large_cardinal_properties).

A general axiomatic framework for large cardinal axioms is proposed in 

* Arthur Apter, Carlos Diprisco, James Henle, William Swicker, _Filter spaces: towards a unified theory of large cardinal and embedding axioms_, Annals of Pure and Applied Logic Volume 41, Issue 2, 6 February 1989, Pages 93&#8211;106

* Arthur Apter, Carlos Diprisco, James Henle, William Swicker, _Filter spaces. II. Limit ultraproducts and iterated embeddings_, Acta Cient. Venezolana 40 (1989), no. 5-6, 311&#8211;318.

An overview of large cardinal axioms:

* Rohan Srivastava, *The Landscape of Large Cardinals* &lbrack;[arXiv:2205.01787](https://arxiv.org/abs/2205.01787)&rbrack;

Some discussion on large cardinal axioms in the context of a [[polynomial function]] whose [[Lebesgue measure|Lesbegue measurability]] is independent of [[ZFC]] occurs in:

* [[James E. Hanson]], *Any function I can actually write down is measurable, right?* ([arXiv:2501.02693](https://arxiv.org/abs/2501.02693))

On [[large set axioms]] in [[constructive set theory]]:

* [[Hanul Jeon]], [[Richard Matthews]], *Very large set axioms over constructive set theories*, The Bulletin of Symbolic Logic. 2024;30(4):455-535. &lbrack;[doi:10.1017/bsl.2024.8](https://doi.org/10.1017/bsl.2024.8), [arXiv:2204.05831](https://arxiv.org/abs/2204.05831)&rbrack;

On very [[large cardinal axioms]]:

* [[Joan Bagaria]], [[Peter Koellner]], [[W. Hugh Woodin]]: *Large Cardinals Beyond Choice*, The Bulletin of Symbolic Logic, Vol. 25, No. 3 (September 2019), pp. 283-318 (36 pages) &lbrack;[jstor:stable/26788522](https://www.jstor.org/stable/26788522)&rbrack;

On [[large cardinal axioms]] without the [[axiom of replacement]]:

* *Large cardinals without replacement*, MathOverflow ([web](https://mathoverflow.net/questions/383978/large-cardinals-without-replacement))

On [[large cardinal axioms]] in weak [[set theories]]

* {#Mathias01} [[Adrian Mathias]]: *The strength of Mac Lane set theory*, Annals of Pure and Applied Logic 110 (1-3):107-234 (2001) &lbrack;<a href="https://doi.org/10.1016/S0168-0072(00)00031-2">doi:10.1016/S0168-0072(00)00031-2</a>&rbrack; 

On [[realizability]] models for [[large cardinals]]:

* [[Laura Fontanella]], [[Guillaume Geoffroy]], [[Richard Matthews]]: *Realizability Models for Large Cardinals*, In 32nd EACSL Annual Conference on Computer Science Logic (CSL 2024). Leibniz International Proceedings in Informatics (LIPIcs), Volume 288, pp. 28:1-28:18, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2024) &lbrack;[10.4230/LIPIcs.CSL.2024.28](https://doi.org/10.4230/LIPIcs.CSL.2024.28)&rbrack;

[[!redirects large cardinal]]
[[!redirects large cardinals]]

[[!redirects large cardinal axiom]]
[[!redirects large cardinal axioms]]

[[!redirects large set axiom]]
[[!redirects large set axioms]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--



\tableofcontents


## Idea
 {#Idea}

The notion of *cyclic operads* ([Getzler & Kapranov 1995](#GetzlerKapranov1995)) is a variant of that of *[[symmetric operads]]* in which the distinction between "inputs" and "output" of operations is made to disappear. 

Where a symmetric operad consists of sets (spaces, objects) $P(n)$ of $n$-to-1 operations for all $n$, [[group action|acted]] on by the [[symmetric group]] $Sym(n)$ [[permutation|permuting]] the $n$ inputs (only), for a cyclic operad this is extended to an [[group action|action]] of $Sym(n+1)$, which [[permutation|permutes]] all $n+1$ "ports" (inputs and output) among each other.

This larger [[symmetric group]] $Sym(n+1)$ may be regarded a generated from the smaller $Sym(n)$ together with the [[cyclic group]] $\mathbb{Z}_{/(n+1)}$ which rotates the $n+1$ in/outputs into each other. This [[cyclic group]] [[group action|action]] is essentially what the term *cyclic operad* is alluding to, though the terminology was more concretely motivated by applications to *[[cyclic homology]]*, see [below](#MotivationInCyclicHomology). (Cyclic operads also appear in ([[2D TQFT|2D]]) [[TQFT]], in the further refinement to *[[modular operads]]*.)

Accordingly, where the [[composition]] operations in a symmetric operad are indexed by grafting of [[rooted trees]] (the unique root of one tree to any of the leaves of another), in a cyclic operad the composition operations are indexed by unrooted trees, any of their leaves (external legs) can be attached among each other.

\begin{imagefromfile}
    "file_name": "CyclicOperadComposition.png",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    },
    "caption": "(from [Doherty-Hackney 2025](#DohertyHackney2025))"
\end{imagefromfile}

In fact, in terms of unrooted indexing [[trees]] the notion of cyclic operads may be formulated more intrinsically (cf. the idea of *[[hyperstructure]]*) as certain cyclic *[[dendroidal sets]]*. In this form the definition seamlessly generalizes to cyclic [[(infinity,1)-operad|$(\infty,1)$-operads]] ([Doherty & Hackney 2025](#DohertyHackney2025)).


## Motivation in cyclic homology
 {#MotivationInCyclicHomology}

[[Hochschild homology]] and cohomology have a natural meaning via [[Tor]] and [[Ext]] groups; and they also have an [[(infinity,1)-category theory|$(\infty,1)$-category theoretic]] interpretation. The [[Hochschild complex]] for associative algebras has a remarkable quotient, the [[cyclic complex]]; this construction is not as general as the mentioned construction, and it can not be generalized to algebras over an arbitrary [[operad]]. Instead there is an additional structure on an operad which enables one to produce an analogue of [[cyclic homology]]. However the long exact sequence of Connes which in the classical case involves cyclic homology and Hochschild homology, here involves the cyclic homology for the original cyclic operad but also the one for the [[Koszul dual operad]] and the Hochschild. In the classical, associative case of course the operad and its Koszul dual coincide. 


## Related concepts

* [[modular operad]]


## References

The original article:

* {#GetzlerKapranov1995} [[Ezra Getzler]], [[Mikhail Kapranov]]: *Cyclic operads and cyclic homology*, in: *Geometry, topology and physics*, International Press (1995) 167-201 &lbrack;[pdf](http://sites.northwestern.edu/getzler/files/2019/08/cyclic.pdf), [intlpress:1698885469150470146](https://intlpress.com/BDetail?id=1698885469150470146)&rbrack;

Generalization to cyclic [[(infinity,1)-operads|$(\infty,1)$-operads]] via cyclic [[dendroidal sets]]:

* {#DohertyHackney2025} Brandon Doherty, [[Philip Hackney]]: *Models for cyclic infinity operads* &lbrack;[arXiv:2506.15622](https://arxiv.org/abs/2506.15622)&rbrack;


See also:

* Benjamin C. Ward: _Maurer-Cartan elements and cyclic operads_, J. Noncommut. Geom. __10__ 4 (2016) 1403--1464
&lbrack;[arXiv:1409.5709](https://arxiv.org/abs/1409.5709), [doi:10.4171/JNCG/263](https://doi.org/10.4171/JNCG/263)&rbrack;

* [[Pierre-Louis Curien]], [[Jovana Obradović]]: _A formal language for cyclic operads_, Higher Structures **1** 1 (2017) 22-55 &lbrack;[arXiv:1602.07502](https://arxiv.org/abs/1602.07502), [pdf](https://higher-structures.math.cas.cz/api/files/issues/Vol1Iss1/CurienObradovic)&rbrack;

* [[Jovana Obradović]]: _Monoid-like definitions of cyclic operad_, Theory and Applications of Categories **32** 12 (2017) 396-436 &lbrack;[tac:32-12](http://tac.mta.ca/tac/volumes/32/12/32-12abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/32/12/32-12.pdf)&rbrack;

* [[Pierre-Louis Curien]], [[Jovana Obradović]]: _Categorified cyclic operads_, Appl. Categ. Struct. __28__  (2020) 59--112 &lbrack;[doi:10.1007/s10485-019-09569-7](https://doi.org/10.1007/s10485-019-09569-7)&rbrack;


[[!redirects cyclic operad]]
[[!redirects cyclic operads]]





# Bunched logic

* table of contents
{:toc}

## Idea

In [[logic]], and more specifically in [[sequent calculus]]/[[natural deduction]], a **bunched logic** is a logic in which the formulas in the [[context]] are not just a [[list]] or [[set]] but have some additional, usually [[tree]]-like, structure.

This can be indicated syntactically by the use of two or more punctuation symbols, such as comma and semicolon, along with parentheses for grouping.  Thus for instance a sequent with bunches might be written like

$$ A,B,(C;(D,E);F),(G;H) \vdash K $$

The contexts put together with both commas and semicolons are called *bunches*.  The general phrase *bunched logic* is not entirely standard, although the word "bunches" has been used with more than one logic of this form (the original is "bunched implication (BI)", below).

Each type of punctuation also comes with a nullary version.  The punctuation symbols like comma and semicolon are sometimes called *structural connectives*, since they are part of the judgmental structure (like [[structural rules]]) but are closely related to the [[logical connectives]] such as conjunction and disjunction.

Usually the reason for using a bunched logic is that the different structural connectives obey different [[structural rules]].  For instance, the semicolon might allow the [[contraction rule]] and/or the [[weakening rule]], while the comma does not.

## Examples

### Bunched implications

In **bunched implications** logic ([BI](#BI)), the semicolon allows contraction and weakening while the comma does not.  This allows defining both an [[additive conjunction]] and a [[multiplicative conjunction]], internalizing the semicolon and the comma respectively, such that both [[distributive law|distribute]] over the [[additive disjunction]] and moreover both come with a corresponding implication: the [[additive implication]] and the [[multiplicative implication]].

### Relevance logic

Some forms of [[relevance logic]] can be presented with a bunched sequent calculus that is similar to BI, but in which the comma also has contraction (though not weakening) and there is no additive implication.  See for instance ([Mints](#Mints)).

### Classical bunched implication

A logic of **classical bunched implication** is like BI but with arbitrary bunches on the right as well as on the left.  On the right, the semicolon represents the [[additive disjunction]] and the comma represents a [[multiplicative disjunction]], and there are both an additive and a multiplicative [[negation]] that move formulas back and forth.  Both negations are "classical" with respect to their corresponding connectives, e.g. we have $\sim\sim A \multimap A$ (where $\sim$ is the multiplicative negation and $\multimap$ the multiplicative implication) and also $\neg\neg A \to A$ (where $\neg$ is the additive negation and $\to$ the additive implication).  See [Pym 2002](#Pym2002) and [this discussion](https://nforum.ncatlab.org/discussion/4004/paraconsistent-logic/?Focus=57557#Comment_57557).

## Categorical semantics

Bunched logics naturally have semantics in categories with more than one [[monoidal structure]], so that a bunch such as $(A,(B;C),((D,E);F))$ can be interpreted as $A \otimes (B\boxtimes C) \otimes ((D\otimes E)\boxtimes F)$.  Frequently (e.g. if one kind of bunch admits contraction and weakening) one of the two monoidal structures is a [[cartesian monoidal category|cartesian]] one.  A typical and motivating example of a model for BI is the [[category of presheaves]] $[C^{op},Set]$ over a monoidal category $C$, which comes equipped both with the ordinary [[ccc structure on presheaves]] as well as the closed monoidal structure given by [[Day convolution]].

## Related pages

* [[linear logic]]
* [[relevance logic]]
* [[separation logic]]
* [[display logic]]
* [[substructural logic]]
* [[monoidal topos]]

## References

* Peter W. O'Hearn and David J. Pym, *The Logic of Bunched Implications*.  [PDF](http://www.lsv.ens-cachan.fr/~demri/OHearnPym99.pdf)
 {#BI}

* G. E. Mints. *Cut-elimination theorem for relevant logics*, Zap. Nauchn. Sem. LOMI, 1972,	Volume 32, Pages 90&#8211;97. ([math-net.ru](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=znsl&paperid=2569&option_lang=eng)).
An English translation appears in the Journal of Soviet Mathematics 6 (1976) pp.422-8. ([doi](http://doi.org/10.1007/BF01084083))
 {#Mints}

* Bodil Biering, *On the logic of bunched implications - and its relation to separation logic*, [masters thesis](http://www.itu.dk/people/biering/papers/speciale.ps)

* David Pym, *The Semantics and Proof Theory of the Logic of Bunched Implications*, [Google books](https://books.google.com/books/about/The_Semantics_and_Proof_Theory_of_the_Lo.html?id=0bAfqhzDuOcC&redir_esc=y)
 {#Pym2002}

* Brotherston and Calcagno, *Classical BI: Its Semantics and Proof Theory*, [arxiv](http://arxiv.org/abs/1005.2340)

[[!redirects bunched logics]]
[[!redirects bunch]]
[[!redirects bunches]]
[[!redirects bunched implication]]
[[!redirects bunched implications]]
[[!redirects BI]]
[[!redirects structural connective]]
[[!redirects structural connectives]]

#Contents#
* table of contents
{:toc}

Charles Sanders Peirce (1839-1914), a philosopher, logician and scientist, was one of the founders of modern symbolic [[logic]]. In particular, he developed a form of [[predicate logic]]. Peirce is seen as the father of pragmatism, although he later distanced himself from other American philosophers who identified them as pragmatists, by adopting the term _pragmaticism_.

Peirce was a prolific thinker who left behind an enormous corpus of work, much unpublished. Where his _Collected Papers_ run to 8 volumes, an ongoing edition aims to publish 30 volumes.

Peirce's philosophy may be seen as Schellingism transformed in light of (in Peirce's time) modern physics, as Peirce himself notes in an 1894 letter to William James:

> My views were probably influenced by [[Schelling]] - by all stages of Schelling, but especially the _Philosophie der Natur_. I consider Schelling as enormous, and one thing I admire about him is his freedom from the trammels of system, and his holding himself uncommitted to any previous utterance. in that, he is like a scientific man. If you were to call my philosophy Schellingism transformed in the light of modern physics, I should not take it hard.


## Existential graphs

Peirce devised a graphical notation, known as **existential graphs**, to represent logical calculi. There were three systems of such graphs: the system _alpha_, to represent [[propositional logic]], the system _beta_, to represent [[predicate logic]], and the system _gamma_, to represent [[modal logic]] ([MaPiet 18](#MaPiet18)).

[[Geraldine Brady]] and [[Todd Trimble]] have given a category theoretic interpretation of the alpha and beta systems. The latter, a form of [[string diagram|string diagrammatic]] notation, was developed ([PontoShul](#PontoShul)) into a [[string diagram]] notation for [[indexed monoidal categories]]. A development also appears in [MellZeil](#MellZeil), see also [BSS18](#BSS18).

## Deduction, induction, abduction

In a series of [lectures](#Peirce98) by Peirce on reasoning, he gives one of those triads he loves so much concerning different modes of inference: deductive, inductive, and [abductive](https://ncatlab.org/nlab/show/abductive+reasoning) (or retroductive), as filling in different parts of a syllogism. Given logical relations between three concepts, $M$, $P$ and $S$,

* Deduction strings together, say, $M$ is $P$ and $P$ is $S$ to give $M$ is $S$.

* Induction looks to generalise from $M$ is $S$, taking $M$ as a sample of $P$, to conclude that $P$ is $S$.

* Abduction looks to explain why $M$ is $S$, having noted that $P$ is $S$, by hypothesising that $M$ is $P$.

Peirce gives related examples:

* **Deduction**
  * All beans in that bag are white.
  * These beans are from that bag.
  * Therefore, these beans are white.


* **Induction**
  * These beans are from that bag.
  * These beans are white.
  * Therefore, all beans in that bag are white.


* **Abduction**
  * These beans are white.
  * All beans in that bag are white.
  * Therefore, these beans are from that bag.

Seen from the point of view of category theory, these would seem to resemble: [[composition]], [[extension]], and [[lifting]]. This thesis is elaborated in [Corf 25]{#Corf25}.

##References

Stanford Encyclopedia of Philosophy entries:

* [Charles Sanders Peirce](https://plato.stanford.edu/entries/peirce/)
* [Peirce's Deductive Logic](https://plato.stanford.edu/entries/peirce-logic/)
* [Peirce's Theory of Signs](https://plato.stanford.edu/entries/peirce-semiotics/)
* [Peirce's View of the Relationship Between His Own Work and German Idealism](https://plato.stanford.edu/entries/peirce/self-contextualization.html)
* [Peirce on Abduction](https://plato.stanford.edu/entries/abduction/peirce.html)

Charles S. Peirce studies

* [website](http://www.peirce.org/)

* {#Peirce98} [Reasoning and the Logic of Things: The Cambridge Conferences Lectures of 1898](http://www.hup.harvard.edu/catalog.php?isbn=9780674749672)

Other references

* [[Geraldine Brady]] and [[Todd Trimble]] (2000a). A Categorical Interpretation of C. S. Peirce's Propositional Logic Alpha. Journal of Pure and Applied Algebra 149 (2000): 213-239, ([pdf](https://core.ac.uk/download/pdf/82545173.pdf))

* {#BradyTrimble} [[Geraldine Brady]] and [[Todd Trimble]] (2000b). _[[A string diagram calculus for predicate logic|A String Diagram Calculus for Predicate Logic and C. S. Peirce's System Beta]]_, preprint 

* [[Kate Ponto]] and [[Mike Shulman]], Duality and traces in indexed monoidal categories, ([web](http://www.sandiego.edu/~shulman/papers/indexed-color.pdf))
{#PontoShul}

* [[Fernando Zalamea]] (2012), Peirce's Logic of Continuity: A Conceptual and Mathematical Approach

* Frederik Stjernfelt (2014), Natural Propositions: The Actuality of Peirce's Doctrine of Dicisigns

* Rosa Maria Perez-Teran Mayorga (2008), From Realism to 'Realicism': The Metaphysics of Charles Sanders Peirce

* Andrew Reynolds (2002), Peirce's Scientific Metaphysics: The Philosophy of Chance, Law, and Evolution

* Matthew Moore (ed) (2010), New Essays on Peirce's Mathematical Philosophy

* [[Louis Kauffman]] (2001), [The Mathematics of Charles Sanders Peirce](http://homepages.math.uic.edu/~kauffman/CHK.pdf)

* C.S. Peirce & Matthew Moore (ed) (2010), Philosophy of Mathematics: Selected Writings

* {#MellZeil} [[Paul-André Melliès]] and [[Noam Zeilberger]] (2016) _A bifibrational reconstruction of Lawvere's presheaf hyperdoctrine_, ([	arXiv:1601.06098, cs.LO](http://arxiv.org/abs/1601.06098))

* Fernando Zalamea, Peirce's logic of continuity, a conceptual and mathematical approach, [link](https://www.academia.edu/31948393/ZalameaPeirceCont.pdf)

* {#MaPiet18} Minghui Ma, Ahti-Veikko Pietarinen (2018), _Gamma graph calculi for modal logics_, Synthese 195: 3621, ([doi](https://doi.org/10.1007/s11229-017-1390-3))

* {#BSS18} Filippo Bonchi, Jens Seeber, Pawel Sobocinski, _Graphical Conjunctive Queries_, ([arXiv:1804.07626](https://arxiv.org/abs/1804.07626))

* Nathan Haydon and Paweł Sobociński, _Compositional diagrammatic first-order logic_, in A.-V. Pietarinen, P. Chapman, L. Bosveld-de Smet, V. Giardino, J. Corter, and S. Linker, editors, Diagrammatic Representation and Inference, pages 402–418, Cham, 2020. Springer International Publishing, &lbrack;[pdf](https://www.ioc.ee/~pawel/papers/peirce.pdf)&rbrack;

* Filippo Bonchi, Alessandro Di Giorgio, Nathan Haydon and Paweł Sobociński. _Diagrammatic algebra of first
order logic_ To appear at LICS, 2024, &lbrack;[arXiv:2401.07055](https://arxiv.org/abs/2401.07055)&rbrack;

* Filippo Bonchi, Alessandro Di Giorgio, Davide Trotta, _When Lawvere meets Peirce: an equational presentation of boolean hyperdoctrines_ &lbrack;[arXiv:2404.18795](https://arxiv.org/abs/2404.18795)&rbrack;

* {#Corf25} [[David Corfield]], *Charles Peirce, Inference, and Category Theory*, [webpage](https://ncatlab.org/davidcorfield/show/Charles+Peirce%2C+Inference%2C+and+Category+Theory)



[[!redirects C.S. Peirce]]
[[!redirects Charles Peirce]]
[[!redirects Charles S. Peirce]]
[[!redirects Peirce]] 

category: people, philosophy
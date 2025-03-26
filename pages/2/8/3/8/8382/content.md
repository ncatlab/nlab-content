#Contents#
* table of contents
{:toc}

##General idea

**Abductive** [[reasoning]] is a process whereby one reasons to the truth of an explanation from its ability to account for what is observed. It is therefore sometimes also known as **inference to the best explanation**.

[[Charles Peirce]], the originator of the term, illustrated the differences between [[deductive reasoning|deduction]], [[inductive reasoning|induction]], and abduction by the following example.

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

It is not completely clear what Peirce meant by abduction, which he also termed **retroduction**. Clearly the inference cannot be to just any possible explanation, e.g., in the case above, there might have been many other bags full of white beans. But before we decide what constitutes a **best** explanation, we had been inquire into the nature of explanation itself.

There is an extensive literature about explanation in the Philosophy of Science, for example, ([FourDecades](#FourDecades)). Clearly it is not merely a matter of devising propositions, perhaps a general law and a particular statement, which have the thing to be explained (explicandum) as a consequence. We want the proposed explanation to 'give the reason for' the observation. A thorough account of what constitutes the 'reason' for something is notoriously difficult to formulate. For some, it is a matter of subsuming the observation under a general covering law, while for others, it is a matter of giving a causal or mechanistic story with the observation as the outcome. 

Note also that there is a growing literature now on the concept of 'explanatory proofs' in mathematics, it being felt that one may have proved a mathematical fact without understanding 'why' it is true.

For some, abduction also signifies the creative process of coming up with a good explanation. Otherwise, if it is merely a case of assessing a range of existing rival hypotheses as explanations, it may be possible to employ [[Bayesian reasoning]], generally taken to be a form of [[inductive reasoning]].

> If you really can find an explanation having sufficient probability to be worth consideration, you escape in great measure from reposing upon retroduction [abduction] and make your inference inductive. (Peirce, [Harvard Lectures, p. 193](#Harvard))

## Abduction as lifting

In Peirce's [Harvard lectures, p. 135](#Harvard), he describes the triad -- _deduction_, _induction_, _abduction_ -- in terms of the logical relations between three concepts, $M$, $P$ and $S$.

* Deduction strings together, say, $M$ is $P$ and $P$ is $S$ to give $M$ is $S$.

* Induction looks to generalise from $M$ is $S$, taking $M$ as a sample of $P$, to conclude that $P$ is $S$.

* Abduction looks to explain why $M$ is $S$, having noted that $P$ is $S$, by hypothesising that $M$ is $P$.

Seen from the point of view of category theory, this would seem rather like: [[composition]], [[extension]], and [[lifting]]. Induction as a kind of extension seems quite reasonable. Abduction may account for an instance of some concept, $E$, by lifting to a concept, $C$, through a law connecting cause, $C$, to effect, $E$. See ([Corf 25](#Corf25)) for more on this perspective.


## References

* Wesley Salmon, 1989, _Four Decades of Scientific Explanation_, University of Pittsburgh Press. {#FourDecades}

* Proposed formalization as a functor between [categories of structures](structure+in+model+theory#categories_of_structures) can be found in Fernando Tohm&#233;, Gianluca Caterina, Rocco Gangle, [_Abduction: A categorical characterization_](http://doi.org/10.1016/j.jal.2014.12.004), Journal of Applied Logic, Volume 13, Issue 1, March 2015, Pages 78-90

* Gerhard Schurz, 2008, _Patterns of abduction_, Synthese 164:201&#8211;234.

* {#Harvard} [[Charles Peirce]], 1992, _Reasoning and the logic of things_, Harvard University Press (lectures from 1898, [book](http://www.hup.harvard.edu/catalog.php?isbn=9780674749672))

* Peter Krause, _Presupposition and abduction in type theory_, In Working Notes of. CLNLP-95: Computational Logic and Natural Language Processing. 

* {#Corf25} [[David Corfield]], _Charles Peirce, Inference, and Category Theory_ &lbrack;[slides](https://ncatlab.org/davidcorfield/show/Charles+Peirce%2C+Inference%2C+and+Category+Theory)&rbrack;

[[!redirects abduction]]
[[!redirects abductive reasoning]]
[[!redirects abductive inference]]
[[!redirects abductive logic]]

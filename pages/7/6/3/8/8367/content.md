
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
=--
=--

# Inductive reasoning
* table of contents
{: toc}

## Idea

Inductive [[reasoning]] concerns assessments of how likely a statement is to be true, given observations of its consequences. In the classical concept of induction, once enough specific instances $P(a), P(b), P(c)$ have been verified (with no instance $\neg{P(k)}$), we are justified in concluding the [[universal quantification|universally quantified statement]] $\forall x,\, P(x)$, or at least one of its consequences $P(k)$.  Stated as a [[rule of inference]] this appears as follows:
\[ \array {
             & \vdash & P(a) \\
             & \vdash & P(b) \\
             & \vdash & P(c) \\
             & \vdots \\
   k\colon S & \vdash & P(k)
   } \label{RoI} \]
Here, the list of [[premise]]s is finite, possibly long but still [[feasible number|feasible]] (at least in an informal sense), while the size of the set $S$ may be infeasibly large (or indeed [[infinite set|infinite]]).

Not everybody holds that inductive reasoning occurs. [[Karl Popper]] famously claimed that "Induction, i.e. inference based on many observations, is a myth. It is neither a psychological fact, nor a fact of ordinary life, nor one of scientific procedure." (Conjectures and Refutations, p. 53). This claim was made primarily about the process of coming to believe in a universal law from the observation of a finite number of instances.


## Mathematical induction
 {#MathematicalInduction}

There is no problem if one can be sure that one is sampling a _complete_ list of instances of a general law. From that one may indeed _induce_ the general law through _[[deductive reasoning|deductive]]_ reasoning. This is _[[induction|mathematical induction]]_. 

The simplest case is induction over a [[finite set]]; if we add the premise
$$ k\colon S \vdash k = a \;\vee\; k = b \;\vee\; k = c \;\vee\; \cdots $$
to the rule \eqref{RoI}, then it becomes a valid deduction (in, say, [[minimal logic]]).  That is, we have actually checked every case, and the universal statement is induced deductively.

A subtler but classic case is induction over the [[natural numbers]]: if one knows that a statement about elements of the set $\mathbb{N}$ holds for the element $0$ and if one knows that if the statement holds for any $n \in \mathbb{N}$, then it also holds for $n+1$, then one can in fact be certain that it holds for each and every $n \in \mathbb{N}$, and again the universal statement is induced deductively. 

This is reflected for instance in the German use of the word: in German, _Induktion_ refers to inductive reasoning, but the mathematical induction over the natural numbers is mandatorily called _[vollst&#228;ndige Induktion](http://de.wikipedia.org/wiki/Vollst%C3%A4ndige_Induktion)_: complete induction.

As explained at _[[induction|mathematical induction]]_, there is a large class of "complete inductions" available in mathematics. In the notion of _[[inductive types]]_, this concept reaches down to the very [[foundations]] of mathematics.


## As Bayesian probability
 {#AsBayesianProbability}

Another approach is to couch inductive reasoning in terms of [[probability theory]].  If we change the conclusions of the sequents in \eqref{RoI} from truth to high [[probability|probabilities]], then the inference may be valid; however, the exact calculation requires the use of [[Bayes's rule]] and depends on the background information.

With [[deductive reasoning]], once I derive (say) $Q$ from $P$ and $P \Rightarrow Q$, my learning new facts does not affect the derivation.  When I reason inductively, however, changes to background knowledge frequently cause me to alter my inferences. For example, from observations that ten fish caught randomly from a pond are trout, I may assess the claim that all fish in the pond are trout as having a certain probability. But learning about the number of fish species present in other ponds nearby (even without observing any more fish from the pond in question) may cause me to alter this assessment. It is clear that many factors may have a bearing on our assessment of a degree of belief.

Interestingly, one of the first people to give a qualitative sketch of how such an approach would work was [[George Polya]] in 'Mathematics and Plausible Reasoning' ([Polya](#Polya)), where examples from mathematics are widely used. The idea of a Bayesian account of plausible reasoning in mathematics surprises many, it being assumed that mathematicians rely solely on [[deductive reasoning|deduction]].

See [[Bayesian reasoning]].


## Related concepts

* [[deductive reasoning]]

* [[Bayesian reasoning]]

## References

* [[Edwin Jaynes]], 2003, _Probability Theory: The Logic of Science_, Cambridge University Press, ([web](http://omega.albany.edu:8008/JaynesBook.html)).

* [[George Polya]], 1954, _Mathematics and Plausible Reasoning, Volume 2:
Patterns of Plausible Inference_, Princeton University Press.
 {#Polya}

Chapter 4 of 

* [[David Corfield]], 2003, _Towards a Philosophy of Real Mathematics_, Cambridge University Press.

From the [[nPOV]], of interest is 

* [[Bob Coecke]], [[Robert Spekkens]]' _Picturing classical and quantum Bayesian inference_ ([pdf](http://www.cs.ox.ac.uk/people/bob.coecke/PDFS/05-Coecke-Spekkens.pdf)).


[[!redirects inductive reasoning]]
[[!redirects inductive inference]]
[[!redirects inductive logic]]


+-- {: .query}

[[Urs Schreiber]]: This page contains what turned out to be the beginning of a discussion that was further had on the nForum [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=1232&page=1#Item_21). 

Eventually, I suggest, we should have a page [[probability theory]] following the usual [[template page]] that contains a remark on the fact that there is a certain philosophical discussion to be had about the nature of probability theory. That remark should then point to this page here, or to a page like it, which would contain this philosophical material.

This page here should eventually be more structured, so that the reader gets a better idea of what it is about. Roughly following the [[template page]], what we need here is

1. A brief indication of what the issue is.

1. A brief summary of what the proposals for answering it are.

1. A structured section list reflecting what the different pieces of the material given here are about.

=--



Andrei N. Kolmogorov is often held to have shown that probability theory is [[measure theory]] of spaces of measure 1.  Sometimes it is asserted that the difference between probability and measure theory is that in the former one is concerned with the concepts of independence of events and independence of random variables.  By these accounts, one who does probability theory is doing mathematics.

A different view is that probability theory is a science that, like physics, must rely very heavily upon mathematics, but some questions in probability theory are not questions of mathematics.  That seems at least consonant with views of the physicist Edwin Jaynes in his book ''Probability Theory: The Logic of Science.''  Perhaps probability theory may be viewed as a branch of epistemology.

Some reasons for holding that view follow.

Consider an "unfair" die whose outcome 2/7 of the time is "1", and for which the other outcomes---"2" through "6"---occur with equal frequencies, thus each in 1 trial out of 7.

A question that must be considered vague or, at best, ambiguous asks: "What is the probability that a '1' appeared the first time the die was cast?"

All probabilities are conditional.  If one follows Kolmogorov's conventions, whereby a probability space consists of an underlying set $\Omega$ and a countably additive probability measure $P$ on a $\sigma$-algebra of subsets of $\Omega$, then one could say that the probability of a measurable subset $A$ of $\Omega$ is the conditional probability $P(A | \Omega)$.

* If one asks for the conditional probability that a "1" appeared on the first toss, given the whole record of outcomes, then the answer is either 0 or 1.

* If one asks for the conditional probability that a "1" appeared on the first toss, given only the information about relative frequencies above, then the answer is 2/7.

* But what if one asks for the conditional probability that a "1" appeared on the first toss given even less information: one knows there are six possible outcomes but one is wholly ignorant of the relative frequencies above?

The answer proposed to the question after the second bullet above may appear to be uncontroversial.  But it is not necessitated by Kolmogorov's theory unless one construes the question in a way that makes it trivial.  If it is construed as meaning "How sure should we be, given the state of our knowledge", then Kolmogorov's theory neither answers it nor understands it.

The question after the third bullet does not express a well-formed mathematical problem about measure spaces.  It is anything but clear which measure space it asks about.  Nonetheless, it seems like a perfectly sensible question if such a thing as epistemic probabilities can exist.  And it does not seem unreasonable to say that the conditional probability that a "1" appeared on the first trial, given that particular state of knowledge, is 1/6.

Within Kolmogorov's theory, one can ask the following sort of question: Suppose the 6-tuple $(p_1,\dots,p_6)$ is uniformly distributed in the space $p_1+\cdots+p_6 = 1,\quad p_1,\dots,p_6 \ge 0$.  Suppose that given the value of $(p_1,\dots,p_6)$, the probability that the outcome of any throw of the die is $i$ is $p_i$.  Finally, suppose that the outcomes on different trials are conditionally independent given the value of $(p_1,\dots,p_6)$.  Then what is the "unconditional" probability that the outcome of the first throw was "1"?  The answer is 1/6.  What is the conditional probability that the outcome of the 1st throw was "1", given that a "1" appeared on each of the 2nd through 5th trials?  The answer is substantially more than 1/6, since the given information about the record makes it probable that $p_1$ is large.  (The trials, although conditionally independent given $(p_1,\dots,p_6)$, are thus seen not to be "unconditionally" independent.)

The reasonable lay person unschooled in the mathematics of probability theory, observing a long string of consecutive "1"s, or even a less extreme case of unusually high frequency of "1"s, will begin to suspect bias. If one were to attempt to model such a layperson's behavior as some probability distribution assigned to the aforementioned vector $(p_1,\dots,p_6)$, it is not immediately clear how, or even whether, one could do so. However, one aspect of the answer that appeals to common sense, is that, given symmetry of information that treats the six outcomes equally, the conditional epistemic probability distribution of the vector $(p_1,\dots,p_6)$ would be symmetric under permutations of the six indices. Among the consequences of this observation are:

* The probability of a "1" on the first toss is 1/6; and
* The probability that a "1" appeared on the first toss, given the record of outcomes a long sequence of subsequent tosses, will approach the observed relative frequency with which a "1" has appeared.

But how fast will it approach that observed relative frequency?

From Kolmogorov's point of view, that depends on what probability distribution has been assigned to the vector $(p_1,\dots,p_6)$.  Only when that has been specified is there a well-defined mathematical problem.  But one does not approach the question of how to model the reasonable layperson's inferences with such a distribution already assigned. We might nonetheless reasonably approach it with the constraint of symmetry in the six indices. That is enough to draw the conclusion stated in the bullet point above that says the probability of a "1" on the first toss is 1/6. It is not enough to answer the question: how fast?

Richard von Mises said that it makes no more sense to say the conditional probability that the outcome of the first trial was "1", given the state of complete ignorance of relative frequencies, is 1/6, than it does to say that the heights of all members of a group of people are estimated to be equal because one is ignorant of their heights.  von Mises missed the point.  The problem was not to estimate the relative frequencies, but to say how epistemically probable that outcome on the first trial is, given a particular state of knowledge.

From the point of view of probability-as-measure-theory put forth by Kolmogorov, it makes sense to speak of the probability of ["1" on the first trial], but it does not make sense to speak of the die's probability of landing on "1" divorced from any particular trial and thought of as a relative frequency or propensity.  One assigns a probability only to a measurable subset of a probability space.

But Kolmogorov took a philosophical position on how his mathematical theory should be applied to the world: he wanted to assign probabilities only when they could be viewed as relative frequencies or proportions.  That is called "frequentism".

When one applies frequentism to statistical inference, one finds oneself making subjective economic decisions about the frequencies of false positives and false negatives one is willing to tolerate.

On the frequentist view, one must not assign probability 1/3, or any number, to the proposition that there was life on Mars a billion years ago, because one cannot say that that happened in 1/3 of all cases.

An alternative view is called Bayesianism, after the 18th-century English Presbyterian minister and mathematician Thomas Bayes.  On the Bayesian view, probabilities are degrees of belief in uncertain propositions, not relative frequencies or proportions.

When one applies Bayesianism to statistical inference, one faces the problem of what probability distribution to assign to the vector $(p_1,\dots,p_6)$.  It is often asserted by both Bayesians and frequentists that that is subjective.

Thus Bayesians and frequentists put their subjectivity in different places.

It can be argued that it is a principle of logic that the conditional probability, given an epistemic state of complete ignorance of the relative frequencies of the die's outcomes, that a "1" appeared on the first trial, is 1/6.  If that is viewed as eliminating the subjectivity from that particular epistemic probability, it nonetheless falls short of solving the problem of logically rather than subjectively determining the distribution of $(p_1,\dots,p_6)$.

+-- {: .query}
[[Michael Hardy]]: Much of this material appeared in a subpage of my Wikipedia user page.
=--






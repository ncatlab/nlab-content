
> {#Blurb} **Cover blurb:** This book presents a novel development of fundamental and fascinating aspects of [[algebraic topology]] and [[mathematical physics]]: “[[Whitehead-generalized cohomology|extra-ordinary]]” and further [[generalized cohomology theories]] enhanced to "[[twisted cohomology|twisted]]" and [[differential cohomology|differential]]-geometric form with focus on their [[rational homotopy theory|rational approximation]] by [[Chern-Dold character|generalized Chern character]] maps and on the resulting [[charge quantization]] laws in [[higher gauge theory|higher $n$-form gauge field theories]] appearing in [[string theory]] and in the [[K-theory classification of topological phases of matter|classification of]] [[topological phase of matter|topological]] [[quantum materials]]. 

> Motivation for the conceptual re-development is the observation, laid out in the introductory chapter, that famous and famously elusive effects in strongly interacting (“[[non-perturbative physics|non-perturbative]]”) [[quantum field theory|physics]] demand "[[non-abelian cohomology|non-abelian]]” generalization of much of established [[generalized cohomology theory]]. But the relevant higher [[non-abelian cohomology]] theory ("[[principal infinity-bundle|higher gerbes]]") has an esoteric reputation and has remained underdeveloped.

> The book's theme is that variously [[generalized cohomology theories]] are best viewed through their [[classifying spaces]] -- possibly but not necessarily [[infinite-loop spaces]] -- from which perspective the [[Chern-Dold character|character map]] is really an incarnation of the [[fundamental theorem of dg-algebraic rational homotopy theory|fundamental theorem of rational homotopy theory]], thereby uniformly subsuming not only the classical [[Chern character]] and a multitude of scattered variants that have been proposed, but now seamlessly applying in the previously elusive generality of ([[twisted cohomology|twisted]], [[differential cohomology|differential]] and) [[non-abelian cohomology]].

> In laying out this result with plenty of examples, we provide modernized introduction and review of fundamental classical topics: 1. abstract [[homotopy theory]] via [[model categories]], 2. [[generalized cohomology]] in [[homotopy theory|homotopical]] incarnation, 3. [[dg-algebra|dg-algebraic]] [[rational homotopy theory]], whose [[fundamental theorem of dg-algebraic rational homotopy theory|fundamental theorem]] we re-cast as a (twisted) non-abelian de Rham theorem which naturally induces the (twisted) non-abelian character map.


$\Sigma$

$\mathfrak{M}$
$\mathcal{M}$

I don't know if all of you know this, but when the QPL workshop series was first founded it was called "*Quantum Programming Languages*". And then one year I wasn't participating, and while I wasn't looking they changed the name to "*Quantum Physics and Logic*" --- same acronym! 

Back in those days in the early 21st century we were actually trying to do programming languages for quantum computing, but the sad thing is: In those days nobody really cared. 

Because, the algorithms-people said: "Who needs a programming language? Everything is equivalent to a Turing-machine anyway!"; and the programming-language people were interested but didn't really understand quantum, and they were not really end-customers&lbrack;?&rbrack; for such programming languages, because we didn't have -- and we still don't have -- any actual quantum computers. And then some people said: "Well, there is only five quantum algorithms, so why don't you just hard-code those in a chip and use that? Why do you need to program if there is only a fixed number of algorithms?"

Now it's 15 years later and, in fact, several of these parameters have changed. The interest in quantum programming languages in the last 3 or 4 years has &lbrack;increased&rbrack;, there has been a renewed interest, from government agencies and also from companies who are actually building quantum computers. They are starting to think about what they might actually do when they get ready. 

So now people are working on quantum programming languages *again*.

\begin{proposition}
**(normal form for 2d cobordisms)**
\linebreak
Every *[[connected topological space|connected]]* [[cobordism]] with

* $n_{in}$ ingoing boundary components

* $n_{ouy}$ outgoing boundary components

* [[genus of a surfce|genus]] $g$

is equivalent ([[diffeomorphism|diffeomorphic]]) to the [[composition]] of 

* $n_{in}-1$ [[trinions]] regarded as $S^1 \times S^1 \to S^1$

* $g$ 2-punctured [[tori]] $S^1 \to S^1$

* $n_{out}-1$ [[trinions]] regared as $S^1 \to S^1 \times S^1$

as shown in the following example for 

* $n_{in} = 5$

* $g = 4$

* $n_{out}$

<center>
<img src="/nlab/files/2dCObordismNormalForm.jpg" width="600">
</center>

> (graphics from [Kock 2004, p. 64](#Kock2004))

\end{proposition}
This fact probably ought to be regarded as classical; an explicit account is given in [Kock 2004, §3.1.2](#Kock2004).

By the [relation](#RelationTo2DTQFT) between 2d cobordism and Frobenius algebras this means equivalently that:



\begin{corollary}\label{NormalFormForFrobeniusMaps}
**(normal form for Frobenius maps)**
\linebreak
Given a Frobenius algebra

$$
  \big(
    A 
    ,\,
    unit
    ,\,
    counit
    ,\,
    prod
    ,\,
    coprod
  \big)
$$

then every linear map of the form

$$
  A^{\otimes^{n_{in}}}
  \longrightarrow
  A^{\otimes^{n_{out}}}
$$

which is 

1. entirely the composite of the algebra's structure maps, ie. of the (co)unit and the (co)product, 

1. *connected* in that it does not decompose as a tensor product of such morphisms,

is equal to the composite of

* $n_{in}-1$ copies of $prod$

* some number ($g$) of copies of $prod \circ coprod$

* $n_{out}$ copies of $coprod$ 
  
\end{corollary}

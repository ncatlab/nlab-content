
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

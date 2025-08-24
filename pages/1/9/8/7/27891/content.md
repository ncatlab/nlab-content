
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents


## Idea

What is now called the *busy beaver function* $BB \colon \mathbb{N} \longrightarrow \mathbb{N}$ (originally discussed by [Radó 1962](#Radó62) who spoke of the *shift function* $S$) is defined such that $BB(n)$ is the [[maximum]] number of steps that can be taken by [[halting problem|halting]] [[Turing machines]] with (2 symbols and) $n$ states.

Variants of this function include the "ones function" $\Sigma \colon \mathbb{N} \longrightarrow \mathbb{N}$, giving the maximal number of times that halting Turing machines with 2 symbols and $n$ states print a given one of these two symbols.

## Properties

The busy beaver function is [[computability|non-computable]].

Some of its values are known or have been argued to be independent of the [[ZFC]]-[[axioms]] of [[set theory]] &lbrack;[Riebel 2023](#Riebel23)&rbrack;.

The values of the busy beaver function grow excessively fast with $n$. The first few values are (bounded below by)

\[
  \label{ValuesAndBoundsForSmalln}
  \begin{array}{ll}
    BB(1) & = 1
    \\
    BB(2) & = 6
    \\
    BB(3) & = 21
    \\
    BB(4) & = 107
    \\
    BB(5) & = 47,176,870
    \\
    BB(6) & \geq {}^15 10
    \coloneqq
10^{10^{10^{10^{10^{10^{10^{10^{10^{10^{10^{10^{10^{10^{10}}}}}}}}}}}}}}
  \end{array}
\]

(from  [Aaronson 2020 p. 9](#Aaronson20), [2022](https://scottaaronson.blog/?p=6673))


## References

The original article:

* {#Radó62} [[Tibor Radó]]: *On non-computable functions*, Bell System Technical Journal **41** 3 (1962) 877–884 &lbrack;[doi:10.1002/j.1538-7305.1962.tb00480.x](https://doi.org/10.1002/j.1538-7305.1962.tb00480.x), [ark:/13960/t3rv1w56b](https://archive.org/details/bstj41-3-877/mode/2up&rbrack), [pdf](https://data.jigsaw.nl/Rado_1962_OnNonComputableFunctions_Remastered.pdf), [pdf](https://gwern.net/doc/cs/computable/1962-rado.pdf)&rbrack;

Early discussion:

* Allen H. Brady: *The Determination of the Value of Rado's Noncomputable Function $\Sigma(k)$ for Four-State Turing Machines*, Mathematics of Computation **40** 162 (1983) 647-665 &lbrack;[doi:10.1090/S0025-5718-1983-0689479-6](https://doi.org/10.1090/S0025-5718-1983-0689479-6), [pdf](https://www.ams.org/journals/mcom/1983-40-162/S0025-5718-1983-0689479-6/S0025-5718-1983-0689479-6.pdf)&rbrack;

Computation of BB(5):

* The bbchallenge Collaboration. Determination of the fifth Busy Beaver value. 2025. [PDF](https://github.com/bbchallenge/bbchallenge-paper/raw/refs/heads/build-paper-pdf/bbchallenge-paper.pdf), [Coq code](https://github.com/ccz181078/Coq-BB5).

Review:

* {#Aaronson20} [[Scott Aaronson]]: *The Busy Beaver Frontier*, ACM SIGACT News **51** 3 (2020) 32-54 &lbrack;[doi:10.1145/3427361.342736](https://doi.org/10.1145/3427361.342736), [pdf](https://www.scottaaronson.com/papers/bb.pdf)&rbrack;

* Ling (Esther) Fu, Sarah Pan: *The Busy Beaver Problem*, MIT Menezes Challenge PRIMES Circle (2022) &lbrack;[pdf](https://math.mit.edu/research/highschool/primes/circle/documents/2022/Esther%20&%20Sarah.pdf)&rbrack;

See also:

* Wikipedia: *[Busy beaver](https://en.wikipedia.org/wiki/Busy_beaver)*

* The Busy Beaver Challenge Wiki &lbrack;[web](https://wiki.bbchallenge.org/wiki/Main_Page)&rbrack;


On undecidability of values of the busy beaver function:

* {#Riebel23} Johannes Riebel: *The Undecidability of BB(748) -- Understanding Gödel’s Incompleteness Theorems*, Bachelor Thesis, Augsburg (2023) &lbrack;[pdf](https://www.ingo-blechschmidt.eu/assets/bachelor-thesis-undecidability-bb748.pdf)&rbrack;

* {#Aaronson23} [[Scott Aaronson]], *Life, blogging, and the Busy Beaver function go on*, blog entry (5 July 2023) &lbrack;[web](https://scottaaronson.blog/?p=7388)&rbrack;

* {#BBCWiki} *Independence from ZFC*, the Busy Beaver Challenge Wiki &lbrack;[web](https://wiki.bbchallenge.org/wiki/Independence_from_ZFC)&rbrack;


For an argument that BB(6) will be hard to find in a technical sense (it requires solving a [Collatz](https://en.wikipedia.org/wiki/Collatz_conjecture)-like problem for a candidate TM), see 

* Shawn Ligocki, _BB(6) is Hard (Antihydra)_, [blog post](https://www.sligocki.com/2024/07/06/bb-6-2-is-hard.html)



[[!redirects busy beaver]]

[[!redirects Busy Beaver function]]
[[!redirects Busy Beaver]]


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

What is now called the *busy beaver function* $BB \colon \mathbb{N} \longrightarrow \mathbb{N}$ (originally discussed by [Radó 1962](#Radó62) who spoke of the *shift function*) is defined such that $BB(n)$ is the [[maximum]] number of steps that can be taken by [[halting problem|halting]] [[Turing machines]] with (2 symbols and) $n$ states.


## Properties

The busy beaver function is [[computability|non-computable]].

Some of its values are known or have been argued to be independent of the [[ZFC]]-[[axioms]] of [[set theory]] &lbrack;[Riebel 2023](#Riebel23)&rbrack;.

The values of the busy beaver function grow excessively fast with $n$. The first few values are

$$
  \begin{array}{ll}
    BB(1) & = 1
    \\
    BB(2) & = 4
    \\
    BB(3) & = 6
    \\
    BB(4) & = 13
    \\
    BB(5) & = 4098
  \end{array}
$$

The next value is not known but known to be bounded from below by (from [here](https://scottaaronson.blog/?p=6673)):

$$
  BB(6) \geq {}^15 10
  \;=\;
  10^{10^{10^{10^{10^{10^{10^{10^{10^{10^{10^{10^{10^{10^{10}}}}}}}}}}}}}}
  \,,
$$


## References

The original article:

* {#Radó62} T. Radó: On non-computable functions. Bell System Technical Journal **41** 3 (1962) 877–884 &lbrack;[ark:/13960/t3rv1w56b](https://archive.org/details/bstj41-3-877/mode/2up&rbrack);

Review:

* {#Aaronson20} [[Scott Aaronson]]: *The Busy Beaver Frontier*, ACM SIGACT News **51** 3 (2020) 32-54 &lbrack;[doi:10.1145/3427361.342736](https://doi.org/10.1145/3427361.342736), [pdf](https://www.scottaaronson.com/papers/bb.pdf)&rbrack;

* Ling (Esther) Fu and Sarah Pan: *The Busy Beaver Problem*, MIT Menezes Challenge PRIMES Circle (2022) &lbrack;[pdf](https://math.mit.edu/research/highschool/primes/circle/documents/2022/Esther%20&%20Sarah.pdf)&rbrack;

See also:

* Wikipedia: *[Busy beaver](https://en.wikipedia.org/wiki/Busy_beaver)*

* The Busy Beaver Challenge Wiki, [web](https://wiki.bbchallenge.org/wiki/Main_Page)


On undecidability of values of the busy beaver function:

* {#Riebel23} Johannes Riebel: *The Undecidability of BB(748) -- Understanding Gödel’s Incompleteness Theorems*, Bachelor Thesis, Augsburg (2023) &lbrack;[pdf](https://www.ingo-blechschmidt.eu/assets/bachelor-thesis-undecidability-bb748.pdf)&rbrack;

* {#Aaronson23} [[Scott Aaronson]], *Life, blogging, and the Busy Beaver function go on*, blog entry (5 July 2023) &lbrack;[web](https://scottaaronson.blog/?p=7388)&rbrack;

* {#BBCWiki} *Independence from ZFC*, the Busy Beaver Challenge Wiki &lbrack;[web](https://wiki.bbchallenge.org/wiki/Independence_from_ZFC)&rbrack;


For an argument that BB(6) will be hard to find in a technical sense (it requires solving a [Collatz](https://en.wikipedia.org/wiki/Collatz_conjecture)-like problem for a candidate TM), see 

* Shawn Ligocki, _BB(6) is Hard (Antihydra)_, [blog post](https://www.sligocki.com/2024/07/06/bb-6-2-is-hard.html)



[[!redirects busy beaver]]

[[!redirects Busy Beaver function]]
[[!redirects Busy Beaver]]

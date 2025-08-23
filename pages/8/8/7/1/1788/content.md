> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

***


&auml;


* Sen Hu, Xuexing Lu, Yu Ye: *A graphical calculus for semi-groupal categories*, Appl Categor Struct **27** (2019) 163–197 &lbrack;[arXiv:1604.07276](https://arxiv.org/abs/1604.07276), [doi:10.1007/s10485-018-9549-8](https://doi.org/10.1007/s10485-018-9549-8)&rbrack;

* Xuexing Lu, Yu Ye: *Combinatorial characterization of upward planarity*, Commun. Math. Stat. **7** (2019) 207–223  &lbrack;[arXiv:1608.07255](https://arxiv.org/abs/1608.07255), [doi:10.1007/s40304-018-0169-2](https://doi.org/10.1007/s40304-018-0169-2)&rbrack;


## Idea

What is now called the *busy beaver function* (originally discussed by [Radó 1962](#Radó62) who spoke of the *shift function*) is defined to be the [[function]] $BB(n) \colon \mathbb{N} \longrightarrow{N}$ such that $BB(n)$ is the [[maximum]] number of steps that can be taken by halting [[Turing machines]] with (2 symbols and) $n$ states.

## Properties


The beasy beaver function is [[computability|non-computible]].

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

* [[Scott Aaronson]]: *The Busy Beaver Frontier*, ACM SIGACT News **51** 3 (2020) 32-54 &lbrack;[doi:10.1145/3427361.342736](https://doi.org/10.1145/3427361.342736), [pdf](https://www.scottaaronson.com/papers/bb.pdf)&rbrack;

* Ling (Esther) Fu and Sarah Pan: *The Busy Beaver Problem*, MIT Menezes Challenge PRIMES Circle (2022) &lbrack;[pdf](https://math.mit.edu/research/highschool/primes/circle/documents/2022/Esther%20&%20Sarah.pdf)&rbrack;

See also:

* Wipipedia: *[Busy beaver](https://en.wikipedia.org/wiki/Busy_beaver)*


On undecidability of values of the busy beaver function:

* {#Riebel23} Johannes Riebel: *The Undecidability of BB(748) -- Understanding Gödel’s Incompleteness Theorems*, Bachelor Thesis, Augsburg (2023) &lbrack;[pdf](https://www.ingo-blechschmidt.eu/assets/bachelor-thesis-undecidability-bb748.pdf)&rbrack;





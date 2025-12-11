#Contents#
* table of contents
{:toc}

## Idea

*Graded linear logic* can refer to multiple extensions of [[bounded linear logic]],
but most notably to $\mathrm{B}_\mathcal{S}\mathrm{LL}$,
where the [[derelictions|exponentials]] are indexed by elements of a [[semiring]] $\mathcal{S}$.

It can be used as a [[type system]] for tracking function sensitivity (types are then interpreted in the cateogry of [[metric spaces]] and [[short maps]]; see [Reed & Pierce 2010](#ReedPierce2010) and [Arthur Azevedo de Amorim et al. 2017](#AdA2017)) or [[information flow]] (see [Liepelt et al. 2025](#Liepelt2025)).

Graded linear logic can be seen as a simple (structural) [[coeffect]] system.

## Literature

* {#ReedPierce2010} Jason Reed and Benjamin C. Pierce, _Distance Makes the Types Grow Stronger_, ICFP'10 &lbrack;[pdf](https://www.cis.upenn.edu/~bcpierce/papers/dp.pdf)&rbrack;
* Dan Ghica and Alex I. Smith, _Bounded linear types in a resource semiring_, Programming Languages and Systems (2014)
* Aloïs Brunel, Marco Gaboardi, Damiano Mazza, and Steve Zdancewic, _A core quantitative coeffect calculus_, Programming Languages and Systems (2014)
* Marco Gaboardi, [[Shin-ya Katsumata]], [[Dominic Orchard]], Flavien Breuvart, and [[Tarmo Uustalu]], _Combining effects and coeffects via grading_,  ACM SIGPLAN International Conference on Functional Programming (2016)
* {#AdA2017} Arthur Azevedo de Amorim, Marco Gaboardi, Justin Hsu, Shin-ya Katsumata & Ikram Cherigui, _A semantic account of metric preservation_, POPL'17 (2017) &lbrack;[doi](https://dl.acm.org/doi/10.1145/3009837.3009890)&rbrack;
* Dominic Orchard, Vilem-Benjamin Liepelt and Harley Eades III, _Quantitative Program Reasoning with Graded Modal Types_ (2019) &lbrack;[pdf](https://dl.acm.org/doi/pdf/10.1145/3341714)&rbrack;
* Yōji Fukihara and [[Shin-ya Katsumata]], _Generalized bounded linear logic and its categorical semantics_, Foundations of Software Science and Computation Structure (2021)
* Flavien Breuvart, Marie Kerjean and Simon Mirwasser, _Unifying Graded Linear Logic and Differential Operators_, International Conference on Formal Structures for Computation and Deduction (2023) &lbrack;[pdf](https://drops.dagstuhl.de/storage/00lipics/lipics-vol260-fscd2023/LIPIcs.FSCD.2023.21/LIPIcs.FSCD.2023.21.pdf)&rbrack;
* {#Liepelt2025} Vilem-Benjamin Liepelt, Danielle Marshall, Dominic Orchard, Vineet Rajani & Michael Vollmer, LNCS 15500 (2025) &lbrack;[doi](https://link.springer.com/chapter/10.1007/978-3-032-08187-2_7)&rbrack;

[[!redirects Graded Linear Logic]]
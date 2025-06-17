
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


\tableofcontents

## Preliminaries

\begin{definition}\label{FredholmOperator}
A [[continuous function|continuous]] [[linear operator]] $F \colon B_1\to B_2$ between [[Banach spaces]] is **Fredholm** if it has [[finite set|finite]] [[dimension|dimensional]] [[kernel]] and finite dimensional [[cokernel]]. 
\end{definition}

\begin{definition}\label{Parametrix}
A **parametrix** of a [[bounded operator|bounded]] [[linear operator]] $F \colon \mathcal{H}_1 \to \mathcal{H}_2$ is a reverse operator $P \colon \mathcal{H}_2 \to \mathcal{H}_1$ which is an "[[inverse]] up to [[compact operators]]", i.e. such that $F \circ P - id_{\mathcal{H}_2}$ and $P \circ F - id_{\mathcal{H}_1}$ are both [[compact operators]].
\end{definition}


## Statement

\begin{theorem}\label{FredholmViaParametrix}
**([Atkinson 1951](#Atkinson51))**
\linebreak
A [[bounded operator|bounded]] [[linear operator]] $ F \colon B_1\to B_2$ between [[Banach spaces]] is Fredholm, def. \ref{FredholmOperator} precisely it is has a parametrix, def. \ref{Parametrix}.
\end{theorem}

## References

The original article:

* {#Atkinson51} F. V. Atkinson: *The normal solubility of linear equations in normed spaces*, Sb. Math. **70**  (1951) &lbrack;[mathnet:sm5589](https://www.mathnet.ru/eng/sm5589)&rbrack;

Review:

* Wikipedia: *[Atkinson's theorem](https://en.wikipedia.org/wiki/Atkinson%27s_theorem)*

* [[Martin Schechter]]: *Basic theory of Fredholm operators*, Annali della Scuola Normale Superiore di Pisa - Scienze Fisiche e Matematiche, Serie 3, **21** 2 (1967) 261-280 &lbrack;[numdam:ASNSP_1967_3_21_2_261_0](https://www.numdam.org/item/ASNSP_1967_3_21_2_261_0)&rbrack;


* Ethan Y. Jaffe: *Atkinson’s Theorem* &lbrack;[pdf](https://r-grande.github.io/Expository/Atkinson%27s%20Theorem.pdf)&rbrack;




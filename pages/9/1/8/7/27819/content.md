
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
A [[bounded operator|bounded]] [[linear operator]] $F \colon B_1\to B_2$ between [[Banach spaces]] is **Fredholm** if it has [[finite set|finite]] [[dimension|dimensional]] [[kernel]] and finite dimensional [[cokernel]]. 
\end{definition}

\begin{definition}\label{Parametrix}
A **parametrix** of a [[bounded operator|bounded]] [[linear operator]] $F \colon \mathcal{H}_1 \to \mathcal{H}_2$ is a reverse operator $P \colon \mathcal{H}_2 \to \mathcal{H}_1$ which is an "[[inverse]] up to [[compact operators]]", i.e. such that $F \circ P - id_{\mathcal{H}_2}$ and $P \circ F - id_{\mathcal{H}_1}$ are both [[compact operators]].
\end{definition}


## Statement

\begin{theorem}\label{FredholmViaParametrix}
**([Atkinson 1951](#Atkinson51))**
\linebreak
A [[bounded operator|bounded]] [[linear operator]] $ F \colon B_1\to B_2$ between [[Banach spaces]] is Fredholm, def. \ref{FredholmOperator}, precisely if it admits a parametrix, def. \ref{Parametrix}.
\end{theorem}

(cf. [Pedersen 1989 Prop. 3.3.11](#Pedersen89), [Murphy 1990 Thm. 1.4.16](#Murphy90))

## References

The original article:

* {#Atkinson51} F. V. Atkinson: *The normal solubility of linear equations in normed spaces*, Sb. Math. **70**  (1951) &lbrack;[mathnet:sm5589](https://www.mathnet.ru/eng/sm5589)&rbrack;

Review:

* [[Martin Schechter]]: *Basic theory of Fredholm operators*, Annali della Scuola Normale Superiore di Pisa - Scienze Fisiche e Matematiche, Serie 3, **21** 2 (1967) 261-280 &lbrack;[numdam:ASNSP_1967_3_21_2_261_0](https://www.numdam.org/item/ASNSP_1967_3_21_2_261_0)&rbrack;

* {#Pedersen89} [[Gert K. Pedersen]]: *Analysis Now*, Graduate Texts in Mathematics **118**, Springer (1989) &lbrack;[doi;10.1007/978-1-4612-1007-8](https://doi.org/10.1007/978-1-4612-1007-8)&rbrack;

* {#Murphy90} [[Gerard Murphy]]: §1.4 in: *$C^\ast$-algebras and Operator Theory*, Academic Press (1990) &lbrack;[doi:10.1016/C2009-0-22289-6](https://doi.org/10.1016/C2009-0-22289-6)&rbrack;

See also:

* Wikipedia: *[Atkinson's theorem](https://en.wikipedia.org/wiki/Atkinson%27s_theorem)*

* Ethan Y. Jaffe: *Atkinson’s Theorem* &lbrack;[pdf](https://r-grande.github.io/Expository/Atkinson%27s%20Theorem.pdf)&rbrack;


[[!redirects Atkinson theorem]]

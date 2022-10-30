[[!redirects Minimal Negation Operator]]

**External links**

* [Minimal Negation Operator @ MyWikiBiz](http://mywikibiz.com/Minimal_negation_operator)
* [Minimal Negation Operator @ PlanetMath](http://planetmath.org/encyclopedia/MinimalNegationOperator.html)
* [Minimal Negation Operator @ PlanetPhysics](http://planetphysics.org/encyclopedia/MinimalNegationOperator.html)
* [Minimal Negation Operator @ ProofWiki](http://www.proofwiki.org/wiki/Definition:Minimal_Negation_Operator)

(Not all of the above links work all the time on all browsers.)

**NB.**  I'll be using this entry as a test case for importing some content and learning the local syntax.

Refs
: [itex](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html)
: [arrays](http://physics.wku.edu/webeq-test/docs/WebTeX/wtxsec7.html)

**Test Area**

\mathbb{B} &#8594; $\mathbb{B}$ &#8594; not showing on Firefox 3.5

**Raw TeX import from PlanetPhysics to work on ...**

The \textbf{minimal negation operator} $\nu$ is a multigrade operator $(\nu_k)_{k \in \mathbb{N}}$ where each $\nu_k$ is a $k$-ary boolean function $\nu_k : \mathbb{B}^k \to \mathbb{B}$ defined in such a way that $\nu_k (x_1, \ldots, x_k) = 1$ in just those cases where exactly one of the arguments $x_j$ is $0$.

In contexts where the initial letter $\nu$ is understood, the minimal negation operators can be indicated by argument lists in parentheses.  In the following text a distinctive typeface will be used for logical expressions based on minimal negation operators, for example, $\texttt{(x, y, z)}$ = $\nu (x, y, z).$

The first four members of this family of operators are shown below, with paraphrases in a couple of other notations, where tildes and primes, respectively, indicate logical negation.

\begin{center}$\begin{matrix}
\texttt{()}
& = & \nu_0
& = & 0
& = & \operatorname{false}
\\[6pt]
\texttt{(x)}
& = & \nu_1 (x)
& = & \tilde{x}
& = & x^\prime
\\[6pt]
\texttt{(x, y)}
& = & \nu_2 (x, y)
& = & \tilde{x}y \lor x\tilde{y}
& = & x^\prime y \lor x y^\prime
\\[6pt]
\texttt{(x, y, z)}
& = & \nu_3 (x, y, z)
& = & \tilde{x}yz \lor x\tilde{y}z \lor xy\tilde{z}
& = & x^\prime y z \lor x y^\prime z \lor x y z^\prime
\end{matrix}$\end{center}

To express the general case of $\nu_k$ in terms of familiar operations, it helps to introduce an intermediary concept:

\textbf{Definition.}  Let the function $\lnot_j : \mathbb{B}^k \to \mathbb{B}$ be defined for each integer $j$ in the interval $[1, k]$ by the following equation:

\[ \lnot_j (x_1, \ldots, x_j, \ldots, x_k) ~=~ x_1 \land \ldots \land x_{j-1} \land \lnot x_j \land x_{j+1} \land \ldots \land x_k. \]

Then $\nu_k : \mathbb{B}^k \to \mathbb{B}$ is defined by the following equation:

\[ \nu_k (x_1, \ldots, x_k) ~=~ \lnot_1 (x_1, \ldots, x_k) \lor \ldots \lor \lnot_j (x_1, \ldots, x_k) \lor \ldots \lor \lnot_k (x_1, \ldots, x_k). \]

If we think of the point $x = (x_1, \ldots, x_k) \in \mathbb{B}^k$ as indicated by the boolean product $x_1 \cdot \ldots \cdot x_k$ or the logical conjunction $x_1 \land \ldots \land x_k,$ then the minimal negation $\texttt{(} x_1, \ldots, x_k \texttt{)}$ indicates the set of points in $\mathbb{B}^k$ that differ from $x$ in exactly one coordinate.  This makes $\texttt{(} x_1, \ldots, x_k \texttt{)}$ a discrete functional analogue of a \textit{point omitted neighborhood} in analysis, more exactly, a \textit{point omitted distance one neighborhood}.  In this light, the minimal negation operator can be recognized as a differential construction, an observation that opens a very wide field.  It also serves to explain a variety of other names for the same concept, for example, \textit{logical boundary operator}, \textit{limen operator}, \textit{least action operator}, or \textit{hedge operator}, to name but a few.  The rationale for these names is visible in the venn diagrams of the corresponding operations on sets.

The remainder of this discussion proceeds on the \textit{algebraic boolean convention} that the plus sign $(+)$ and the summation symbol $(\textstyle\sum)$ both refer to addition modulo 2.  Unless otherwise noted, the boolean domain $\mathbb{B} = \{ 0, 1 \}$ is interpreted so that $0 = \operatorname{false}$ and $1 = \operatorname{true}.$  This has the following consequences:

\begin{itemize}

\item
The operation $x + y$ is a function equivalent to the exclusive disjunction of $x$ and $y,$ while its fiber of $1$ is the relation of inequality between $x$ and $y.$

\item
The operation $\textstyle\sum_{j=1}^k x_j$ maps the bit sequence $(x_1, \ldots, x_k)$ to its \textit{parity}.

\end{itemize}

The following properties of the minimal negation operators $\nu_k : \mathbb{B}^k \to \mathbb{B}$ may be noted:

\begin{itemize}

\item
The function $\texttt{(x, y)}$ is the same as that associated with the operation $x + y$ and the relation $x \ne y.$

\item
In contrast, $\texttt{(x, y, z)}$ is not identical to $x + y + z.$

\item
More generally, the function $\nu_k (x_1, \dots, x_k)$ for $k > 2$ is not identical to the boolean sum $\textstyle\sum_{j=1}^k x_j.$

\item
The inclusive disjunctions indicated for the $\nu_k$ of more than one argument may be replaced with exclusive disjunctions without affecting the meaning, since the terms disjoined are already disjoint.

\end{itemize}

\section{Truth tables}

Table 1 is a truth table for the sixteen boolean functions of type $f : \mathbb{B}^3 \to \mathbb{B}$, each of which is either a boundary of a point in $\mathbb{B}^3$ or the complement of such a boundary.

\begin{center}
\begin{tabular}{|c|c|c|c|c|}
\multicolumn{5}{c}{\textbf{Table 1.  Logical Boundaries and Their Complements}}
\\[2pt]\hline
$L_1$   & $L_2$            &       & $L_3$           & $L_4$
\\[2pt]
Decimal & Binary           &       & Sequential      & Parenthetical
\\[2pt]\hline
        &                  & $p =$ & 1 1 1 1 0 0 0 0 &
\\[2pt]
        &                  & $q =$ & 1 1 0 0 1 1 0 0 &
\\[2pt]
        &                  & $r =$ & 1 0 1 0 1 0 1 0 &
\\[2pt]\hline
$f_{104}$ & $f_{01101000}$ &       & 0 1 1 0 1 0 0 0 & $\texttt{(~p~,~q~,~r~)}$
\\[2pt]
$f_{148}$ & $f_{10010100}$ &       & 1 0 0 1 0 1 0 0 & $\texttt{(~p~,~q~,(r))}$
\\[2pt]
$f_{146}$ & $f_{10010010}$ &       & 1 0 0 1 0 0 1 0 & $\texttt{(~p~,(q),~r~)}$
\\[2pt]
$f_{97}$  & $f_{01100001}$ &       & 0 1 1 0 0 0 0 1 & $\texttt{(~p~,(q),(r))}$
\\[2pt]
$f_{134}$ & $f_{10000110}$ &       & 1 0 0 0 0 1 1 0 & $\texttt{((p),~q~,~r~)}$
\\[2pt]
$f_{73}$  & $f_{01001001}$ &       & 0 1 0 0 1 0 0 1 & $\texttt{((p),~q~,(r))}$
\\[2pt]
$f_{41}$  & $f_{00101001}$ &       & 0 0 1 0 1 0 0 1 & $\texttt{((p),(q),~r~)}$
\\[2pt]
$f_{22}$  & $f_{00010110}$ &       & 0 0 0 1 0 1 1 0 & $\texttt{((p),(q),(r))}$
\\[2pt]\hline
$f_{233}$ & $f_{11101001}$ &       & 1 1 1 0 1 0 0 1 & $\texttt{(((p),(q),(r)))}$
\\[2pt]
$f_{214}$ & $f_{11010110}$ &       & 1 1 0 1 0 1 1 0 & $\texttt{(((p),(q),~r~))}$
\\[2pt]
$f_{182}$ & $f_{10110110}$ &       & 1 0 1 1 0 1 1 0 & $\texttt{(((p),~q~,(r)))}$
\\[2pt]
$f_{121}$ & $f_{01111001}$ &       & 0 1 1 1 1 0 0 1 & $\texttt{(((p),~q~,~r~))}$
\\[2pt]
$f_{158}$ & $f_{10011110}$ &       & 1 0 0 1 1 1 1 0 & $\texttt{((~p~,(q),(r)))}$
\\[2pt]
$f_{109}$ & $f_{01101101}$ &       & 0 1 1 0 1 1 0 1 & $\texttt{((~p~,(q),~r~))}$
\\[2pt]
$f_{107}$ & $f_{01101011}$ &       & 0 1 1 0 1 0 1 1 & $\texttt{((~p~,~q~,(r)))}$
\\[2pt]
$f_{151}$ & $f_{10010111}$ &       & 1 0 0 1 0 1 1 1 & $\texttt{((~p~,~q~,~r~))}$
\\[2pt]\hline
\end{tabular}
\end{center}

\section{Charts and graphs}

This section presents two ways of visualizing the operation of minimal negation operators.  A few bits of terminology will be needed as a language for talking about the pictures, but the formal details are tedious reading, and may be familiar to many readers, so the full definitions of the terms marked in bold are relegated to a Glossary at the end of the article.

Two ways of visualizing the space $\mathbb{B}^k$ of $2^k$ points are the \textit{hypercube} picture and the \textit{venn diagram} picture.  Depending on how literally or figuratively one regards these pictures, each point of $\mathbb{B}^k$ is either identified with or represented by a point of the $k$-cube and also by a cell of the $k$- ``circle" venn diagram.

In addition, each point of $\mathbb{B}^k$ is the unique point in the \textbf{fiber of truth} $[|s|]$ of a \textbf{singular proposition} $s : \mathbb{B}^k \to \mathbb{B}$, and thus it is the unique point where a \textbf{singular conjunction} of $k$ \textbf{literals} is equal to 1.

For example, consider two cases at opposite vertices of the $k$-cube:

\begin{itemize}

\item
The point $(1, 1, \ldots, 1, 1)$ with all 1's as coordinates is the point where the conjunction of all posited variables evaluates to 1, namely, the point where:

\[ x_1 ~ x_2 ~\ldots~ x_{k-1} ~ x_k ~=~ 1 \]

\item
The point $(0, 0, \ldots, 0, 0)$ with all 0's as coordinates is the point where the conjunction of all negated variables evaluates to 1, namely, the point where:

\[ \texttt{(} x_1 \texttt{)(} x_2 \texttt{)} \ldots \texttt{(} x_{k-1} \texttt{)(} x_k \texttt{)} ~=~ 1 \]

\end{itemize}

To pass from these limiting examples to the general case, observe that a singular proposition $s : \mathbb{B}^k \to \mathbb{B}$ can be given canonical expression as a conjunction of literals, $s = e_1 ~ e_2 ~\ldots~ e_{k-1} ~ e_k$.  Then the proposition $\nu(e_1, e_2, \ldots, e_{k-1}, e_k)$ is 1 on the points adjacent to the point where $s$ is 1, and 0 everywhere else on the cube.

For example, consider the case where $k = 3$.  Then the minimal negation operation $\nu(p, q, r)$ --- written more simply as $\texttt{(p, q, r)}$ --- has the following venn diagram:

\begin{center}\begin{tabular}{c}
\includegraphics[scale=0.8]{MinimalNegationOperator1}
\\
Figure 2. ~ $\texttt{(p, q, r)}$
\end{tabular}\end{center}

For a contrasting example, the boolean function expressed by the form $\texttt{((p),(q),(r))}$ has the following venn diagram:

\begin{center}\begin{tabular}{c}
\includegraphics[scale=0.8]{MinimalNegationOperator2}
\\
Figure 3. ~ $\texttt{((p),(q),(r))}$
\end{tabular}\end{center}

\section{Glossary of basic terms}

\begin{itemize}

\item
A \textbf{boolean domain} $\mathbb{B}$ is a generic 2-element set, say, $\mathbb{B} = \{ 0, 1 \}$, whose elements are interpreted as logical values, usually but not invariably with 0 = \textit{false} and 1 = \textit{true}.

\item
A \textbf{boolean variable} $x$ is a variable that takes its value from a boolean domain, as $x \in \mathbb{B}$.

\item
In situations where boolean values are interpreted as logical values, a boolean-valued function $f : X \to \mathbb{B}$ or a boolean function $g : \mathbb{B}^k \to \mathbb{B}$ is frequently called a \textbf{proposition}.

\item
Given a sequence of $k$ boolean variables, $x_1, \ldots, x_k$, each variable $x_j$ may be treated either as a basis element of the space $\mathbb{B}^k$ or as a coordinate projection $x_j : \mathbb{B}^k \to \mathbb{B}$.

\item
This means that the $k$ objects $x_j$ for $j$ = $1$ to $k$ are just so many boolean functions $x_j : \mathbb{B}^k \to \mathbb{B}$, subject to logical interpretation as a set of \textit{basic propositions} that generate the complete set of $2^{2^k}$ propositions over $\mathbb{B}^k$.

\item
A \textbf{literal} is one of the $2k$ propositions $x_1, \ldots, x_k, \texttt{(} x_1 \texttt{)}, \ldots, \texttt{(} x_k \texttt{)}$, in other words, either a \textit{posited} basic proposition $x_j$ or a \textit{negated} basic proposition $\texttt{(} x_j \texttt{)}$, for some $j$ = $1$ to $k$.

\item
In mathematics generally, the \textbf{fiber} of a point $y$ under a function $f : X \to Y$ is defined as the inverse image $f^{-1}(y)$.

\item
In the case of a boolean-valued function $f : X \to \mathbb{B}$, there are just two fibers:

\begin{quote}
The fiber of 0 under $f$, defined as $f^{-1}(0)$, is the set of points where $f$ is 0.

The fiber of 1 under $f$, defined as $f^{-1}(1)$, is the set of points where $f$ is 1.
\end{quote}

\item
When 1 is interpreted as the logical value \textit{true}, then $f^{-1}(1)$ is called the \textbf{fiber of truth} in the proposition $f$.  Frequent mention of this fiber makes it useful to have a shorter way of referring to it.  This leads to the definition of the notation $[|f|] = f^{-1}(1)$ for the fiber of truth in the proposition $f$.

\item
A \textbf{singular boolean function} $s : \mathbb{B}^k \to \mathbb{B}$ is a boolean function whose fiber of 1 is a single point of $\mathbb{B}^k$.

\item
In the interpretation where 1 equals \textit{true}, a singular boolean function is called a \textbf{singular proposition}.

\item
Singular boolean functions and singular propositions serve as functional or logical representatives of the points in $\mathbb{B}^k$.

\item
A \textbf{singular conjunction} in $(\mathbb{B}^k \to \mathbb{B})$ is a conjunction of $k$ literals that includes just one conjunct of the pair $\{ x_j, ~ \nu(x_j) \}$ for each $j$ = $1$ to $k$.

\item
A singular proposition $s : \mathbb{B}^k \to \mathbb{B}$ can be expressed as a singular conjunction:

\begin{quote}$\begin{array}{lll}
s & = & e_1 ~ e_2 ~\ldots~ e_{k-1} ~ e_k
\\
\text{where} & e_j & = x_j
\\
\text{or}    & e_j & = \nu(x_j)
\\
\text{for}   & j   & = 1 ~\text{to}~ k
\end{array}$\end{quote}

\end{itemize}

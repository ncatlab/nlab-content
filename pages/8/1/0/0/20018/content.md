\tableofcontents

\section{Introduction}

A _word_ in the elements of a set is roughly speaking a concatenation of elements of that. To make this precise, one typically uses the machinery of [[free object|free algebraic structures]]. One may allow in the concatenation certain canonical elements of the free algebraic gadget constructed from the elements of the set one started with, such as inverses. 

By extension, one may also refer to elements of any algebraic structure, at least when described in terms of generators and relations (i.e. explicitly as a quotient of a free algebraic structure), as words.

\section{Prototypical example}

The prototypical algebraic structure to make sense of the notion of a word is that of a [[monoid]]. If 'word' is used in a context where the intended algebraic structure is not made clear, use of free monoids is likely intended.

\begin{defn} Let $X$ be a set. A _word_ in the elements of $X$ is an element of the [[free monoid]] on $X$. \end{defn}

\begin{rmk} A free monoid has in particular an identity element, which is the _empty word_. \end{rmk} 

\begin{rmk} We do not assume commutativity. \end{rmk}

\begin{example} Let $X = \{a, b\}$ be a set. Examples of words in $X$ are the empty word, $a$, $b$, $ab$, $a^{5}$, $ab^{3}$, $ababab$, $b^{3}a^{2}b^{5}$ and so on. \end{example}

\section{In groups}

Another common case is that in which the algebraic structure is that of groups.

\begin{defn} Let $X$ be a set. A _word_ in the free group on the elements of $X$ is an element of the [[free group]] on $X$. \end{defn}

\begin{rmk} As for monoids, a free group has in particular an identity element, which is the _empty word_. \end{rmk} 

\begin{rmk} As for monoids, we do not assume commutativity. \end{rmk}

\begin{example} Let $X = \{a, b\}$ be a set. Examples of words in the free group on $X$ are the empty word, $a$, $b$, $ab$, $a^{5}$, $a^{-5}$, $ab^{3}$, $ababab$, $a^{-1}b^{-1}a^{-1}b^{-1}a^{-1}b^{-1}$, $ab^{-1}$, $b^{3}a^{2}b^{5}$, $a^{-3}b^{2}a^{7}b^{-2}$, and so on. \end{example}
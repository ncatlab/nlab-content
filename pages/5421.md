+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linguistics
+-- {: .hide}
[[!include linguistics - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The notion of context-free grammar, now used in [[linguistics]], [[computer science]] and [[mathematics]], was introduced in the works of [[Noam Chomsky]]. 


## Traditional definition

We write $X + Y$ for the [[disjoint union]] of two sets and use vector notation and the Kleene star $\vec{v} \in X^\star$ to denote sequences in the [[free monoid]].

A context-free grammar is a tuple $(\Sigma, X, R, s)$ where $\Sigma$ and $X$ are finite sets called the _vocabulary_ (also called the _terminals_) and the _non-terminals_ respectively, $R \subseteq X \times (X + \Sigma)^\star$ is a finite set of _production rules_ and $s \in X$ is called the _start symbol_.

The _language_ of a context-free grammar is given by $L(G) = \{ \vec{u} \in V^\star \vert s \to_R \vec{u} \}$ where the rewriting relation $(\to_R) \subseteq (V + X)^\star \times (V + X)^\star$ is traditionally defined as the transitive closure of the following directed graph:

$$
\big\{ (\vec{u} x \vec{w}, \vec{u v w}) \quad \vert \quad \vec{u}, \vec{w} \in (V + X)^\star, (x, \vec{v}) \in R \big\}
$$

## With string diagrams

One may redefine $L(G) = \big\{ \vec{u} \in \Sigma^\star \vert \C_G(s, \vec{u}) \neq \emptyset \big\}$ where $C_G$ is the free [[monoidal category]] with:

* generating objects the [[disjoint union]] $\Sigma + X$,
* generating arrows the production rules $(x, \vec{v}) \in R$ with $dom(x, \vec{v}) = x$ and $cod(x, \vec{v}) = \vec{v}$.

That is, a string $\vec{u} \in \Sigma^\star$ is _grammatical_ whenever there exists an arrow from the start symbol $s$ to $\vec{u}$ in $C_G$. Arrows in $C_G$ may be encoded as a _syntax tree_, seen as a special case of a [[string diagram]], e.g.:

![syntax tree for "Colorless green ideas sleep furiously"](https://upload.wikimedia.org/wikipedia/commons/thumb/a/aa/Syntax_tree.svg/280px-Syntax_tree.svg.png)

Note that context-free grammar is weakly equivalent to [[Lambek|Lambek's]] [[pregroup grammar]] i.e. they generate the same class of languages, see:

*  {#BuszkowskiMoroz08} Wojciech Buszkowski, Katarzyna Moroz, _Pregroup Grammars and Context-free Grammars_, Computational Algebraic Approaches to Natural Language, Polimetrica (2008) ([pdf](https://pdfs.semanticscholar.org/1924/30f2252b6e0a7f982a3ae69a3ccf9c2981c0.pdf))


## Early sources

Here is list of some of the original references in English and also of their Russian translations. 

* N. Chomsky, _Three models for the description of language, I. R. E.
Trans. PGIT 2 (1956), 113&#8212;124. (&#1056;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081; &#1087;&#1077;&#1088;&#1077;&#1074;&#1086;&#1076;: &#1061;&#1086;&#1084;&#1089;&#1082;&#1080;&#1081; &#1053;., &#1058;&#1088;&#1080;
&#1084;&#1086;&#1076;&#1077;&#1083;&#1080; &#1076;&#1083;&#1103; &#1086;&#1087;&#1080;&#1089;&#1072;&#1085;&#1080;&#1103; &#1103;&#1079;&#1099;&#1082;&#1072;, &#1050;&#1080;&#1073;&#1077;&#1088;&#1085;&#1077;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1081; &#1089;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1074;&#1099;&#1087;. 2, &#1048;&#1051; 1961, 237-266)
* N. Chomsky, _On certain formal properties of grammars_, Information
and Control __2__ (1959), 137&#8212;267; _A note on phrase structure grammars_, Information andControl __2__ 1959_, 393&#8212;395. (&#1061;&#1086;&#1084;&#1089;&#1082;&#1080;&#1081; &#1050;, &#1047;&#1072;&#1084;&#1077;&#1090;&#1082;&#1080; o &#1075;&#1088;&#1072;&#1084;&#1084;&#1072;&#1090;&#1080;&#1082;&#1072;&#1093; &#1085;&#1077;&#1087;&#1086;&#1089;&#1088;&#1077;&#1076;&#1089;&#1090;&#1074;&#1077;&#1085;&#1085;&#1099;&#1093; &#1089;&#1086;&#1089;&#1090;&#1072;&#1074;&#1083;&#1103;&#1102;&#1097;&#1080;&#1093;. &#1050;&#1080;&#1073;&#1077;&#1088;&#1085;&#1077;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1081;
&#1089;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1074;&#1099;&#1087;. 5, &#1048;&#1051;, 1962, 312&#8212;315.)
* N. Chomsky, _On the notion &#171;Rule of Grammar&#187;_, Proc. Symp. Applied
Math., 12. Amer. Math. Soc. (1961). (&#1061;&#1086;&#1084;&#1089;&#1082;&#1080;&#1081; &#1053;.,
&#1054; &#1087;&#1086;&#1085;&#1103;&#1090;&#1080;&#1080; &#171;&#1087;&#1088;&#1072;&#1074;&#1080;&#1083;&#1086; &#1075;&#1088;&#1072;&#1084;&#1084;&#1072;&#1090;&#1080;&#1082;&#1080;&#187;, &#1089;&#1073;. &#1053;&#1086;&#1074;&#1086;&#1077; &#1074; &#1083;&#1080;&#1085;&#1075;&#1074;&#1080;&#1089;&#1090;&#1080;&#1082;&#1077;, &#1074;&#1099;&#1087;. 4,
&#171;&#1055;&#1088;&#1086;&#1075;&#1088;&#1077;&#1089;&#1089;&#187;, 1965, &#1089;&#1090;&#1088;. 34&#8212;65.)
* N. Chomsky, _Context-free grammars and pushdown storage_, Quarterly
Progress Reports, &#8470; 65, Research Laboratory of Electronics, M. I. T.,
1962.
* N. Chomsky, _Formal properties of grammars_, in Handbook of Mathemati-
Mathematical Psychology, 2, ch. 12, Wiley, 1963, p. 323&#8212;418. (&#1061;&#1086;&#1084;&#1089;&#1082;&#1080;&#1081; &#1053;., &#1060;&#1086;&#1088;&#1084;&#1072;&#1083;&#1100;&#1085;&#1099;&#1077; &#1089;&#1074;&#1086;&#1081;&#1089;&#1090;&#1074;&#1072; &#1075;&#1088;&#1072;&#1084;&#1084;&#1072;&#1090;&#1080;&#1082;, &#1050;&#1080;&#1073;&#1077;&#1088;&#1085;&#1077;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1081;
&#1089;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1074;&#1099;&#1087;. 2, &#171;&#1052;&#1080;&#1088;&#187;, 1966, 121&#8212;-230.)
* N. Chomsky, The logical basis for linguistic theory, Proc. IX-th Int.
Cong. Linguists (1962). (&#1061;&#1086;&#1084;&#1089;&#1082;&#1080;&#1081; &#1053;" &#1051;&#1086;&#1075;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1077;
&#1086;&#1089;&#1085;&#1086;&#1074;&#1099; &#1083;&#1080;&#1085;&#1075;&#1074;&#1080;&#1089;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1086;&#1081; &#1090;&#1077;&#1086;&#1088;&#1080;&#1080;, &#1089;&#1073;. &#1053;&#1086;&#1074;&#1086;&#1077; &#1074; &#1083;&#1080;&#1085;&#1075;&#1074;&#1080;&#1089;&#1090;&#1080;&#1082;&#1077;, &#1074;&#1099;&#1087;. 4,
&#171;&#1055;&#1088;&#1086;&#1075;&#1088;&#1077;&#1089;&#1089;&#187;, 1965, 465&#8212;-575.)
* N. &#1057;h&#1086;msk&#1091;, G. A. Miller G. A.. Finite state languages, Information and
Control __1__ (1958), 91&#8212;-112. (&#1061;&#1086;&#1084;&#1089;&#1082;&#1080;&#1081; &#1053;., &#1052;&#1080;&#1083;&#1083;&#1077;&#1088; &#1044;., &#1071;&#1079;&#1099;&#1082;&#1080; &#1089; &#1082;&#1086;&#1085;&#1077;&#1095;&#1085;&#1099;&#1084; &#1095;&#1080;&#1089;&#1083;&#1086;&#1084; &#1089;&#1086;&#1089;&#1090;&#1086;&#1103;&#1085;&#1080;&#1081;, &#1050;&#1080;&#1073;&#1077;&#1088;&#1085;&#1077;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1081; &#1089;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1074;&#1099;&#1087;. 4, &#1048;&#1051;, 1962, 231&#8212;-255.), _Introduction to the formal analysis of natural languages_. Handbook of Mathematical Psychology __2__, Ch. 12, Wiley, 1963, 269&#8212;-322 (&#1042;&#1074;&#1077;&#1076;&#1077;&#1085;&#1080;&#1077; &#1074; &#1092;&#1086;&#1088;&#1084;&#1072;&#1083;&#1100;&#1085;&#1099;&#1081; &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1077;&#1089;&#1090;&#1077;&#1089;&#1090;&#1074;&#1077;&#1085;&#1085;&#1099;&#1093; &#1103;&#1079;&#1099;&#1082;&#1086;&#1074;, &#1050;&#1080;&#1073;&#1077;&#1088;&#1085;&#1077;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1081; &#1089;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1074;&#1099;&#1087;. 1, &#171;&#1052;&#1080;&#1088;&#187;, 1965, &#1089;&#1090;&#1088;. 229&#8212;-290.)
* N. Chomsky, M. P. Sch&#252;tzenberger, _The algebraic theory of
context-free languages_, in: Computer programming and formal systems, 118&#8211;161 North-Holland 1963, Amsterdam [MR152391](http://www.ams.org/mathscinet-getitem?mr=152391) (&#1050;&#1080;&#1073;&#1077;&#1088;&#1085;&#1077;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1081; &#1089;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082; __3__, 195--242, 1966)


## Modern literature

* wikipedia: [context-free language](http://en.wikipedia.org/wiki/Context-free_language)
* A. V. Aho, J. D. Ullman, _The theory of parsing, translation, and compiling_, vol 1, Parsing; vol. 2, Compiling. Prentice Hall, 1972.
* A. V. Aho, J. D. Ullman, _Principles of compiler design_, Addison-Wesley, 1977.

Some chapters in "Handbook of formal language theory" (3 vols.), G. Rozenberg, A. Salomaa (eds.), Springer 1997:

* Jean-Michel Autebert, Jean Berstel, Luc Boasson, _Context-free languages and push-down automata_, vol. 1, ch. 3 

## Related entries

* [[formal grammar]]
* [[context-sensitive grammar]]
* [[mildly context-sensitive grammar]]
* [[pregroup grammar]]
* [[dependency grammar]]


[[!redirects context-free grammar]]
[[!redirects context-free grammars]]
[[!redirects context free grammar]]
[[!redirects context free grammars]]
[[!redirects context-free language]]
[[!redirects context-free languages]]
[[!redirects context free language]]
[[!redirects context free languages]]

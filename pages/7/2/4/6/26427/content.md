[[!redirects n-valued group]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of *$n$-valued groups* is an analogue of [[groups]] where the multiplication takes values in the $n$-th "symmetric power" of the [[underlying]] set. 2-valued [[formal groups]] appeared first in the study of [[characteristic classes]] by [Buchstaber & Novikov 1971](#BuchstaberNovikov71).

## Definition

Let $n$ be a [[positive number|positive]] [[integer]]. Denote by $Sym^n(G)$ the $n$-th symmetric power of a set $G$, or equivalently the set of [[multisets]] of $n$ not necessarily different elements $[g_1,\ldots,g_n]$ in $G$.

An *$n$-valued group* is given by a [[set]] $G$ together with a function ("multiplication")
$$
  \ast 
    \;\colon\; 
  G \times G \longrightarrow Sym^n(G)
  \,,
$$

satisfying:

* ([[associativity]]) The following $n^2$-element 
multisets are equal:

  $\big[ a\ast (b\ast c)_1, a\ast (b\ast c)_2,\ldots, a\ast
(b\ast c)_n\big]$ and $\big[(a\ast b)_1\ast c,\ldots,(a\ast b)_n\ast c\big]$,

* ([[unitality]]) there is a [[neutral element]] $\mathrm{e}$ such that for all $x\in G$, $\mathrm{e} \ast x = x \ast \mathrm{e} = [x,x,\ldots,x]$,

* ([[inverses]]) For every $g\in G$ there exists $g^{-1}\in G$ such that $\mathrm{e} \in g^{-1}\ast g$ and $\mathrm{e} \in g\ast g^{-1}$.


## Literature

Origin of the notion in multivalued [[formal groups]] appearing in [[complex oriented cohomology theory]]:

* {#BuchstaberNovikov71} В. М. Бухштабер, С. П. Новиков, Формальные группы, степенные системы и операторы Адамса, Мат. 
Сборник (Н.С.) 84 (1971) 81--118; 

  English translation:

  [[Victor M. Buchstaber]], [[Sergei P. Novikov]], _Formal groups, power systems and Adams operators_, Math. USSR-Sb. **13** (1971) 80-116 &lbrack;[doi:10.1070/SM1971v013n01ABEH001030](https://iopscience.iop.org/article/10.1070/SM1971v013n01ABEH001030)&rbrack;

* [[Victor M. Buchstaber]], Two-valued formal groups. Some applications to cobordisms, Uspehi Mat. Nauk **26** 3 (1971),  (159) 195–196 &lbrack;MR 0461533&rbrack;

* [[Victor Buchstaber]], §5 in: _Cobordisms in problems of algebraic topology_,  J Math Sci **7** (1977) 629–653 &lbrack;[doi:10.1007/BF01084983](https://doi.org/10.1007/BF01084983)&rbrack;


The notion has in fact been sporadically studied much earlier, e.g. in the context of hypergroups.

* J. Delsarte, _Hypergroupes et opérateurs de permutation et de transmutation_, La théorie des équations aux dérivées partielles. Nancy, 9-15 avril 1956, pp. 29--45
Colloq. Internat. CNRS, LXXI [International Colloquia of the CNRS] Centre National de la Recherche Scientifique, Paris, 1956 [MR0116151](https://mathscinet.ams.org/mathscinet/relay-station?mr=MR0116151)

Some newer articles

* D. Coulette, F. Déglise, J Fasel, J. Hornbostel, _Formal ternary laws and Buchstaber’s 2-groups_, Manuscripta Math. (2023) [doi](https://doi.org/10.1007/s00229-023-01512-4)

* В. М. Бухштабер, Функциональные уравнения ассоциированные с теоремами сложения для эллиптических функций и двузначные алгебраические группы, Успехи Мат. Наук 45:3 (1990) 185--186 (transl.: V. M. Bukhstaber, _Functional equations that are associated with addition theorems for elliptic functions and two-valued algebraic groups_, Russian Math. Surveys 45:3 (1990) 213--215.)

In 2010. V. Dragović has observed that the integrability of Kovalevskaia top is related to associativity of certain $n$-valued group. A related later developments on [[integrable systems]] are touched upon in:

* [[Victor M. Buchstaber]], Vladimir Dragović, _Two-valued groups, Kummer varieties, and integrable billiards_, Arnold Math J. 4, 27--57 (2018) &lbrack;[doi:10.1007/s40598-018-0085-2](https://doi.org/10.1007/s40598-018-0085-2)&rbrack;

[[!redirects multivalued groups]]

[[!redirects n-valued group]]
[[!redirects n-valued groups]]

[[!redirects 2-valued group]]
[[!redirects 2-valued groups]]

category: algebra


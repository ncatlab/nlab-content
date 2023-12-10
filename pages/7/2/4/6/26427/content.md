# Idea

$n$-valued group is an analogue of a [[group]] where the multiplication takes values in $n$-th symmetric power. 2-valued formal groups appeared first in the study of characteristic classes, in works of [[Victor Buchstaber]] and Novikov.

# Axioms

Let $n$ be a positive integer. Denote by $Sym^n(G)$ the $n$-th symmetric power of a set $G$, or equivalently the 
set of [[multiset]]s of $n$ not necessarily different elements $[g_1,\ldots,g_n]$ in $G$.
An $n$-valued group is given by a set $G$ together with a multiplication
$$
\ast : G\times G\to Sym^n(G), 
$$
satisfying

* (associativity) The following $n^2$-element 
multisets are equal:
$[ a\ast (b\ast c)_1, a\ast (b\ast c)_2,\ldots, a\ast
(b\ast c)_n]$ and $[(a\ast b)_1\ast c,\ldots,(a\ast b)_n\ast c]$

* (unit) there is an element $e$ such that for all $x\in G$, $e\ast x = x\ast e = [x,x,\ldots,x]$

* (inverse) For every $g\in G$ there is $g^{-1}\in G$ such that $e\in g^{-1}\ast g$ and $e\in g\ast g^{-1}$.

# Literature

Origins are in 

* В. М. Бухштабер, С. П. Новиков, Формальные группы, степенные системы и операторы Адамса, Мат. 
Сборник (Н.С.) 84 (1971) 81--118; English: V. M. Buchstaber, S. P. Novikov, _Formal groups, power systems and Adams operators_, Math. USSR-Sb.13 (1971) 80--116 [doi](https://doi.org/10.1070/SM1971v013n01ABEH001030)
* V. M. Buchstaber, Two-valued formal groups. Some applications to cobordisms, Uspehi Mat.
Nauk 26 (1971), no. 3 (159), 195–196. MR 0461533

The notion has in fact been sporadically studied much earlier, e.g. in the context of hypergroups.

* J. Delsarte, _Hypergroupes et opérateurs de permutation et de transmutation_, La théorie des équations aux dérivées partielles. Nancy, 9-15 avril 1956, pp. 29--45
Colloq. Internat. CNRS, LXXI [International Colloquia of the CNRS] Centre National de la Recherche Scientifique, Paris, 1956 [MR0116151](https://mathscinet.ams.org/mathscinet/relay-station?mr=MR0116151)

Some newer articles

* D. Coulette, F. Déglise, J Fasel, J. Hornbostel, _Formal ternary laws and Buchstaber’s 2-groups_, Manuscripta Math. (2023) [doi](https://doi.org/10.1007/s00229-023-01512-4)
* В. М. Бухштабер, Функциональные уравнения ассоциированные с теоремами сложения для эллиптических функций и двузначные алгебраические группы, Успехи Мат. Наук 45:3 (1990) 185--186 (transl.: V. M. Bukhstaber, _Functional equations that are associated with addition theorems for elliptic functions and two-valued algebraic groups_, Russian Math. Surveys 45:3 (1990) 213--215.)

In 2010. V. Dragović has observed that the integrability of Kovalevskaia top is related to associativity of certain $n$-valued group. A related later developments on [[integrable system]]s are touched upon in  

* Victor M. Buchstaber, Vladimir Dragović, _Two-valued groups, Kummer varieties, and integrable billiards_, Arnold Math J. 4, 27--57 (2018) [doi](https://doi.org/10.1007/s40598-018-0085-2)

category: algebra
[[!redirects 2-valued group]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

Taketa's theorem and related statements say that a necessary condition on a [[finite group]] to have all its complex [[irreps]] be suitably [[induced representations]] is that it is a *[[solvable group]]*.

## Terminology: "M-groups"

A [[finite group]] $G$ is called an *$M$-group* if all its [[complex numbers|complex]] [[irreducible representations]] are [[induced representation|induced]] from [[dimension of a vector space|1-dimensional]] representations, hence if for each [[irrep]] $rho$ of $G$ there exists a [[subgroup]] $H \subset G$ and a 1-dimensional rep $\nu$ of $H$, such that $\rho \,\simeq\, Ind^G_H \rho$, where $Ind_H^G \,\colon\, H Rep \to G Rep$ is the [[induced representation|induction]] [[functor]].

More generally, for $k \in \mathbb{N}_+$ a [[positive number|positive]] [[natural number]], a [[finite group]] is called an *$M_k$-group* if all its [[irreps]] are [[induced representation|induced]] from irreps of [[dimension of a vector space|dimension]] $\leq k$. (cf. [Berkovich 1996](#Berkovich96))

## Statement

\begin{theorem}
**(Taketa's theorem)**
\linebreak
M-groups are [[solvable group|solvable]].
\end{theorem}
([Taketa 1930](#Taketa30), [Isaacs 1976 thm. 5.12](#Isaacs76))

In fact:

\begin{theorem}
 If a [[finite group]] has the property that for each of its [[complex numbers|complex]] [[irreps]] of [[dimension of a vector space|dimension]] $\geq 2$ *some multiple* of it is [[induced representation|induced]] from an [[irrep]] of a proper [[subgroup]], then the group is [[solvable group|solvable]].
\end{theorem}
([LMT 2013](#LMT13))


## References

Taketa's theorem is due to

* {#Taketa30} Kiyosi Taketa: *Über die Gruppen, deren Darstellungen sich sämtlich auf monomiale Gestalt transformieren lassen*, Proc. Imp. Acad. **6** 2 (1930) 31-33 &lbrack;[euclid:pia/1195581421](https://projecteuclid.org/journals/proceedings-of-the-japan-academy-series-a-mathematical-sciences/volume-6/issue-2/%C3%9Cber-die-Gruppen-deren-Darstellungen-sich-s%C3%A4mtlich-auf-monomiale-Gestalt/10.3792/pia/1195581421.full)&rbrack;

Textbook account:

* {#Isaacs76} [[I. Martin Isaacs]], theorem 5.12 in: *Character theory of finite groups*, Academic Press, New York (1976) &lbrack;[ISBN:978-0-8218-4229-4](https://bookstore.ams.org/view?ProductCode=CHEL/359.H)&rbrack;

Further discussion:

* [[I. Martin Isaacs]]: *Generalizations of Taketa's Theorem on the Solvability of M-Groups*, Proceedings of the American Mathematical Society **91** 2 (1984) 192-194 &lbrack;[doi:10.2307/2044624](https://doi.org/10.2307/2044624), [jstor:2044624](https://www.jstor.org/stable/2044624)&rbrack;

* {#Berkovich96} Yakov Berkovich: *On the Taketa Theorem*, Journal of Algebra **182** 2 (1996) 501-510 &lbrack;[doi:10.1006/jabr.1996.0183](https://doi.org/10.1006/jabr.1996.0183)&rbrack;

* {#LMT13} Tung Le, Jamshid Moori, Hung P. Tong-Viet: *On a generalization of M-group*, Journal of Algebra
**374** (2013) 27-41 &lbrack;[arXiv:1206.5067](https://arxiv.org/abs/1206.5067), [doi:10.1016/j.jalgebra.2012.10.018](https://doi.org/10.1016/j.jalgebra.2012.10.018)&rbrack;

[[!redirects Taketa theorem]]
[[!redirects M-group]]
[[!redirects M-groups]]


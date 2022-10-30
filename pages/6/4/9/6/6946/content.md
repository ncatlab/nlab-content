[[!redirects Provability Logic]]
[[!redirects Gödel-Löb logic]]
[[!redirects Goedel-Loeb logic]]
[[!redirects provability logics]]
[[!redirects Provability logics]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}



##Idea

**Provability logic** studies the properties of a formal provability predicate  $\Box F$ interpreted as 'F is provable'. This gives rise to [[modal logics]] kindred to **K4** and its variations.

For the best known of these systems, the **G&#246;del-L&#246;b logic** of provability $GL$, topological interpretations have been pioneered by H. Simmons and L. Esakia in the 1970s.

## GL in Hilbert-style

The language of $GL$ has propositional variables $p_0,p_1,\dots$ and logical connectives $\to$, $\bot$, $\top$ and one unary modality $\Box$. Besides all tautologies of classical propositional logic, GL has the following axiom schemes:

* $\Box (\varphi\to\psi) \to (\Box\varphi\to\Box\psi)$ . (Normality)

* $\Box (\Box \varphi\to \varphi)\to \Box\varphi $ . (L&#246;b's axiom)

with inference rules

* $\array{
\arrayopts{\rowlines{solid}}
\varphi ,\quad\varphi\to\psi\\
\psi
}$  (Modus ponens)

*  $\array{
\arrayopts{\rowlines{solid}}
\varphi\\
\Box\varphi
}$  (Necessitation)

$GL$ proves the _transitivity rule_ $\Box\varphi\to\Box\Box\varphi$ but not the _reflexivity rule_ $\Box\varphi\to\varphi$ whence it is an extension of $K4$ but not of $S4$.

##Links

* [Stanford Encyclopedia of Philosophy entry](http://plato.stanford.edu/entries/logic-provability/)

##Related entries

* [[scattered topos]]

* [[epistemic logic]]

* [[Brouwer-Heyting-Kolmogorov interpretation]]

* [[Gödel's incompleteness theorem]]

* [[arithmetic pretopos]]

##References

* S. Artemov, L. Beklemishev, _Provability logic_ , pp.229-403 in Gabbay, Guenthner (eds.), _Handbook of Philosophical Logic vol. 13_ , Kluwer Dordrecht 2004$^2$.  ([draft](http://sartemov.ws.gc.cuny.edu/files/2012/10/Artemov-Beklemishev.-Provability-logic.pdf))

* L. Beklemishev, D. Gabelaia, _Topological interpretations of provability logic_ , arXiv:1210.7317 (2012).  ([abstract](http://arxiv.org/abs/1210.7317))

* A. Macintyre, H. Simmons, _G&#246;del's diagonalization technique and related properties of theories_ , Coll. Math. **28** no.2 (1973) pp.165-180. ([pdf](http://yadda.icm.edu.pl/yadda/element/bwmeta1.element.desklight-8bd6a8c7-d547-43f0-b220-eda51556c1ad/c/cm28_2_01.pdf))

* R. M. Solovay, _Provability interpretations of modal logic_ , Israel J. Math. **28** (1976) pp.33&#8211;71.
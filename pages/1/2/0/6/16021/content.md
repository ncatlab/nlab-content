
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[modal logic]] the moniker "S5" refers to the logic obtained from [[S4 modal logic]] by adjoining the [[axiom scheme]] that there is the [[implication]]

$$
  \lozenge p \to \Box \lozenge p
  \,.
$$

In the [[possible worlds semantics]] for modal logic, S5 corresponds  precisely to those [[Kripke frames]] $\big(W \colon Set, \, R \colon W \times W \to Prop\big)$ where the [[relation]] $R$ is an *[[equivalence relation]]* &lbrack;[Kripke (1959)](#Kripke59) [(1964)](#Kripke63), cf. [Fagin, Halpern, Moses & Vardi (1995) Thm. 3.1.5 (c)](#FaginHalpernMosesVardi95)&rbrack;.


## Via dependent type theory
 {#ViaDependentTypeTheory}

In mild generalization of the discussion at *[necessity & possibility -- Via dependent types](necessity+and+possibility#InFirstOrderLogicAndTypeTheory)*, we may observe that the [[modal operators]] in S5 Kripke semantics 

<center>
<img src="/nlab/files/StandardTranslationKripkeSemantics-230801.jpg" width="740">
</center>

> {#SubtypeNotation} (Here we write --- following notation for *[[subtypes]]* --- $P \,\colon\,W \to Prop$ for a $W$-[[dependent type|dependent]] [[proposition]], equivalently a proposition about the elements of $W$, equivalently the [[subset]] of $W$ where the proposition holds.)

are precisely those arising as [[adjoint pairs]] of ([[comonad|co]])[[monads]] induced on the left from a [[base change]] [[adjoint triple]] (the [[categorical semantics of dependent types|categorical semantics]] in [[Set]] of [[dependent pair type]] $\dashv$ [[context extension]] $\dashv$ [[dependent function type]]-[[type formation|formation]]) along [[display maps]] $W \to \Gamma \equiv W_{/R}$ identified with the [[quotient]] [[coprojection]] of the Kripke frame:

<center>
<img src="/nlab/files/S5KripkeSemanticsAsMonadicDescent-230801.jpf" width="600">
</center>

(Obvious as this may be, the only existing reflection of this fact in the literature may be a side remark in [Awodey 2006, p. 279](#Awodey06), which goes in this direction, albeit not connecting to dependent type formation.)

\begin{remark}
This suggests that one may equivalently regard [[dependent type theory]] as a universal form of [[epistemic logic|epistemic]] [[modal type theory]], in generalization of how [[modal logics]] may be viewed as just another perspective on ([[fragments]] of) [[first-order logic]] (as in [Blackburn, van Benthem & Wolter (2007) pp. xiii](modal+logic#BlackburnvanBenthemWolter07)): In both cases one switches perspective from type formation by [[base change]] [[adjoint triples]] (of [[quantification]] or dependent (co)product formation, respectively) to the induced [[adjoint pair]] of ([[comonad|co]])[[monads]]. (Another example of a change in perspective of this form occurs when describing [[descent]] as *[[monadic descent]]*).
\end{remark}

\begin{remark}
  \label{HaxagonOfEpistemicEntailments}
  The above (co)monadic formulation of modal logic makes manifest another basic point not usually discussed in the subject, namely that the canonical epistemic entailments

<center>
<img src="/nlab/files/EpistemicEntailments-230802b.jpg" width="600">
</center>

are *[[natural transformations]]*. 

This means that the following [[commuting square|squares commute]]. Their [[pasting diagram|pasting]] to the hexagonal [[commuting diagram]] as shown may not have received attention (?):

<center>
<img src="/nlab/files/HexagonalEpistemicEntailments-230802.jpg" width="700">
</center>

\end{remark}

\linebreak

## Related concepts

[[!include flavors of modal logics and relations -- table]]

* [[modal logic]], [[S4 modal logic]]

* [[epistemic modal logic]], [[necessity and possibility]]

* [[K modal logic]]
  
* [[T modal logic]]

* [[Kripke frame]]

* [[Löb's axiom]]



## References

### General 

The terminology "S5" in modal logic originates with:

* [[Clarence I. Lewis]], [[Cooper H. Langford]], App. II, p 501 of: *Symbolic Logic* (1932), Dover (2000) &lbrack;App. II [pdf](https://www.hist-analytic.com/Lewisstrict.pdf)&rbrack;

The [[geometric model for modal logics|geometric model]] for S5 modal logic via [[Kripke frames]] originates with: 

* {#Kripke59} [[Saul A. Kripke]], *A Completeness Theorem in Modal Logic*, The Journal of Symbolic Logic **24** 1 (1959) 1-14 &lbrack;[doi:10.2307/2964568](https://doi.org/10.2307/2964568), [jstor:2964568](https://www.jstor.org/stable/2964568), [pdf](https://www.filosoficas.unam.mx/~morado/Cursos/17Modal/Kripke1959.pdf)&rbrack;

* {#Kripke63} [[Saul A. Kripke]], *Semantical Analysis of Modal Logic I. Normal Modal Propositional Calculi*, Mathematical Logic Quaterly **9** 5-6 (1963) 67-96 &lbrack;[doi:10.1002/malq.19630090502](https://doi.org/10.1002/malq.19630090502)&rbrack;


See also:

* Wikipedia, *[S5 (modal logic)](http://en.wikipedia.org/wiki/S5_%28modal_logic%29)*

A [[natural deduction]]-formulation and making explicit the [[modal operator]] as a [[comonad]]:


* {#BiermanDePaiva96} [[Gavin M. Bierman]], [[Valeria de Paiva]], *Intuitionistic necessity revisited*, School of Computer Science research reports-University of Birmingham CSR (1996) &lbrack;[researchgate](https://www.researchgate.net/publication/2810611_Intuitionistic_Necessity_Revisited), [[Bierman-dePaiva-NecessityRevisited.pdf:file]]&rbrack;


* [[Gavin M. Bierman]], [[Valeria de Paiva]], _On an Intuitionistic Modal Logic_ Studia Logica **65** (2000) 383–416 &lbrack;[doi:10.1023/A:1005291931660](https://doi.org/10.1023/A:1005291931660), [pdf] (https://www.researchgate.net/profile/Valeria-De-Paiva/publication/226515897_On_An_Intuitionistic_Modal_Logic/links/00b4951ed416906ccc000000/On-An-Intuitionistic-Modal-Logic.pdf)&rbrack;

* {#Kobayashi97} [[Satoshi Kobayashi]], *Monad as modality*, Theoretical Computer Science **175** 1 (1997) 29-74 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(96)00169-7">doi:10.1016/S0304-3975(96)00169-7</a>&rbrack;


* Natasha Alechina, Michael Mendler, [[Valeria de Paiva]], Eike Ritter: *Categorical and Kripke Semantics for Constructive S4 Modal Logic*, in *Computer Science Logic. CSL 2001* Lecture Notes in Computer Science **2142**, Springer (2001) 292 &lbrack;[doi:10.1007/3-540-44802-0_21](https://doi.org/10.1007/3-540-44802-0_21)&rbrack;

Understanding of S5 [[Kripke semantics]] as [[base change]] along the lines discussed at *[necessity and possibility -- via dependent types](necessity+and+possibility#InFirstOrderLogicAndTypeTheory)*:

* {#Awodey06} [[Steve Awodey]], p. 279 in: *Category theory*, Oxford University Press (2006, 2010) &lbrack;[doi:10.1093/acprof:oso/9780198568612.001.0001](https://doi.org/10.1093/acprof:oso/9780198568612.001.0001), [ISBN:9780199237180](https://global.oup.com/ukhe/product/category-theory-9780199237180), [pdf](http://englishonlineclub.com/pdf/Category%20Teory%20%5BEnglishOnlineClub.com%5D.pdf)&rbrack;




[[!include S5 modal logic as epistemic logic -- references]]






[[!redirects S5 modal logics]]

[[!redirects S5]]


[[!redirects S5-modal logic]]
[[!redirects S5-modal logics]]
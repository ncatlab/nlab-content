
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Broadly speaking, _quantum logic_ is meant to be a kind of [[formal logic]] that is to traditional formal logic as [[quantum mechanics]] is to [[classical mechanics]]: a formal framework which is supposed to be able to _express_ the statements whose [[semantics]] is the totality of all what is verifiable by [[measurement]] in a [[quantum system]] ([[quantum measurement]]).

In its traditional and default meaning due to ([Birkhoff-vonNeumann 1936](#BirkhoffvonNeumann36)) "quantum logic" refers specifically to the [[orthocomplemented lattice]] of [[closed subspace|closed]] [[linear subspaces]] of a [[Hilbert space]] [[space of quantum states|of quantum states]]. Later it was proposed ([Yetter 90](#Yetter90), [Pratt 92](#Pratt92), [93](#Pratt93), [Abramsky-Duncan 05](#AbramskyDuncan05), [Girard 11](#Girard11)) that a better way to think of the BvN quantum lattices is as the [[propositions]] in [[linear logic]] ([Girard 87](#Girard)), the [[categorical logic]] of [[symmetric monoidal categories]]. 

There is also the proposal ([Heunen-Landsman-Spitters 07](#HeunenLandsmanSpitters07)) that quantum logic should be understood as being the [[internal logic]] of [[Bohr toposes]].

In [[quantum computing]] the quantum analog of classical [[logic gates]] are called _[[quantum logic gates]]_.


## History and Critique
 {#History}

Typically  in the literature the term "quantum logic" is taken to refer very specifically to the first proposal for such a formalization due to [Birkhoff-von Neumann 1936](#BirkhoffvonNeumann36). In this proposal, given a [[quantum mechanical system]] with a [[Hilbert space]] [[space of states|of states]], the logical [[propositions]] about the system are taken to correspond to (the [[projections]] to) [[closed subspaces]], with [[implication]] given by inclusion of such subspaces.  Hence Birkhoff-von Neumann quantum logic is given by the [[lattice]] of [[closed subspace|closed]] [[linear subspaces]] of [[Hilbert spaces]] (regarded as a [[Hilbert lattice]]).

This formalization is often understood as being the default meaning of "quantum logic". But the proposal has later been much criticised, for its lack of key properties that one would demand of any [[formal logic]]. 

{#NonLogic} For instance in [Abramsky & Coecke (2007)](#AbramskyCoecke2007) it is called a "non-logic":

> {#NonLogic} The term quantum logic is usually understood in connection with the 1936 Birkhoff-von Neumann proposal to consider the ([[closed subspace|closed]]) [[linear subspaces]] of a [[Hilbert space]] ordered by inclusion as the formal expression of the logical distinction between quantum and classical physics. While in classical logic we have deduction, the linear subspaces of a Hilbert space form a non-distributive lattice and hence there is no obvious notion of implication or deduction. Quantum logic was therefore always seen as logically very weak, or even as a non-logic. In addition, it has never given a satisfactory account of compound systems and entanglement.

Here by "no [[deduction]]" is meant "no [[deduction theorem]]".

And for example in ([Heunen-Landsman-Spitters 07, p. 4](#HeunenLandsmanSpitters07)) it says the following:

> Attractive and revolutionary as this spatial quantum "logic" may appear  it faces severe problems. The main logical drawbacks are:

> 1. Due to its lack of distributivity, quantum 'logic' is difficult to interpret as a logical structure.

> 2. In particular, despite various proposals no satisfactory implication operator has been found (so that there is no deductive system in quantum logic).

> 3. Quantum 'logic' is a [[propositional logic|propositional]] language; no satisfactory generalization to [[predicate logic]] has been found. 

> Quantum logic is also problematic from a physical perspective. Since (by various theorems and wide agreement) quantum probabilities do not admit an ignorance interpretation, $[0, 1]$-valued truth values attributed to propositions by pure states via the [[Born rule]] cannot be regarded as sharp (i.e. {0, 1}-valued) truth values muddled by human ignorance. This implies that, if $X = [a \in \Delta]$ represents a quantum-mechanical proposition, it is wrong to say that either $x$ or its [[negation]] holds, but we just do not know which of these alternatives applies. However, in quantum logic one has the law of the excluded middle in the form $x \vee x^\perp = 1$ for all $x$. Thus the formalism of quantum logic does not match the probabilistic structure of quantum theory responsible for its empirical content.

But notice that one may argue that the first three points here are squarely resolved by thinking of BvN-quantum logic as embedded into [[linear logic]], we come back to this in a moment. Concerning the last point one might argue that the propositions in BvN-quantum logic concern the [[quantum measurement]]-outcomes (only), for which, at least in some  [[interpretation of quantum mechanics|interpretations]], it does make sense to speak of a definite result.

In [Girard 2011, page xii](#Girard11) it says:

> {#MagisteralMistake} Among the magisterial mistakes of logic, one will first mention quantum logic, whose ridiculousness can only be ascribed to a feeling of superiority of the language &#8211; and ideas, even bad, as soon as they take a written form &#8211; over the physical world. Quantum logic is indeed a sort of punishment inflicted on nature, guilty of not yielding to the prejudices of logicians... just like Xerxes had the Hellespont &#8211; which had destroyed a boat bridge &#8211; whipped.


For more and more objective criticism see [Girard 2011, section 17](#Girard11).

Girard had introduced the class of [[formal logic]] systems called _[[linear logic]]_ and it has been argued that [[linear logic]] and more generally _[[linear type theory]]_ does faithfully capture the essence of [[quantum mechanics]] ([Yetter 90](#Yetter90). [Pratt 92](#Pratt92), [Abramsky-Duncan 05](#AbramskyDuncan05), [Duncan 06](#Duncan06)), see ([Baez-Stay 09](#BaezStay09) for an introductory exposition). This is due to the fact that the [[categorical semantics]] of linear logic is in [[symmetric monoidal categories]] such as those used in the description of [[finite quantum mechanics in terms of dagger-compact categories]]. In particular the [[category]] of (finite dimensional) [[Hilbert spaces]] whose [[subobjects]]/[[propositions]] form the Birkhoff-von Neumann style quantum logic does interpret [[linear logic]].

This is stated explicitly for instance in ([Pratt 92, p.4](#Pratt92)):

> These objections are overcome in the extension of quantum logic to linear logic as a dynamic quantum logic.

Notice that the [[subobjects]] in a category of ([[finite-dimensional vector space|finite dimensional]]) [[Hilbert spaces]], and hence the [[propositions]] in the [[categorical logic]] of [[Hilbert spaces]], are the ([[closed subspace|closed]]) [[linear subspaces]]. Therefore Birkhoff-von Neumann quantum logic is indeed subsumed as a fragment of [[linear logic]]. This (obvious) fact was highlighted in [Crown 1975](#Crown75) and then later with more of [[categorical logic]] in place and emphasizing [[dagger-category|dagger]]-structures in [Heunen 2008](#Heunen08), [Harding 2008](#Harding08) [Heunen-Jacobs 2009](#HeunenJacobs09), [Coecke-Heunen-Kissinger 2013](#CoeckeHeunenKissinger13). Also [CCGP 09, section 9.3](#CCGP09)):

> both orthologic (or weakenings thereof) and linear logic share the failure of lattice distributivity. In particular, the fragment of linear logic that includes just [[negation]] and the additive connectives is nothing but a version of the paraconsistent quantum logic PQL.
 
That seems to make much of the above-listed criticism appear in a different light. For instance there is also a natural notion of [[dependent linear type theory]] and that does yield a well-behaved kind of [[predicate logic]] with [[quantifiers]] for linear logic.




## Approaches


### Birkhoff-von Neumann quantum logic
 {#BirkhoffVonNeumannQuantumLogic}

The original proposal for quantum logic by [Birkhoff & von Neumann 1936](#BirkhoffvonNeumann36) (BvN quantum logic) is to regard, given a [[quantum system]] with [[Hilbert space]] [[space of quantum states|of states]] $\mathscr{H}$, the [[Hilbert lattice]] of [[closed subspace|closed]] [[linear subspaces]] $V \subset_{cl} \mathscr{H}$ as the set of [[propositions]] about the quantum system. 

Then:

* logical [[conjunction]] is given by intersection of  [[linear subspaces]] 

  $$
    V_1 \wedge V_2
    \;\coloneqq\;
    V_1 \cap_{\mathscr{H}} V_2
    \,,
  $$

* logical [[disjunction]] is given by forming the [[linear span]] 

  $$
    V_1 \vee V_2
    \;\coloneqq\;
    Span_{\mathscr{H}}(V_1 \, V_2)
  $$ 
  
  of two [[linear subspaces]]. 

* logical [[negation]] is given by forming [[orthogonal complement]]:

  $$
    \not V \;\coloneqq\; V^{\perp_{\mathscr{H}}}
    \,.
  $$


Notice that [[quantum states]] in the conjunction $V_1 \vee V_2$ may be [[linear combinations]] of states in $V_1$ and $V_2$, in reflection of the [[superposition principle]] of [[quantum mechanics]].
As a result, the BvN disjunction does not [[distributivity|distribute]] over conjunction, and hence the BvN lattice of quantum propositions is not a [[distributive lattice]].

### Tensor logic of Quantales

The [[tensor product of Hilbert spaces]] -- which in the jargon of [[linear logic]] would be called the *[[multiplicative conjunction]]* $\otimes$ --  makes the [above](#BirkhoffVonNeumannQuantumLogic) [[Hilbert lattice]] a _[[quantale]]_.


### Linear logic and dependent linear type theory
 {#LinearLogicAndDependentLinearTypeTheory}

We point out that --- at least for the [finite dimensional Hilbert spaces](Hilbert+space#FiniteDimensionalInnerProductSpaces) relevant in [[quantum information theory]] --- [BvN quantum logic](#BirkhoffVonNeumannQuantumLogic) is just the [[linear logic]] of a kind of [[linear type|linearly]]-[[dependent type|dependent]] [[linear types]] inside [[dependent linear type theory]] [[categorical semantics|interpreted]] in [[VectBund]] over the [[complex numbers]]. 

(Notice that it is the linearity of [[linear logic]], which enforces (see [there](linear+logic#AbsenceOfWeakeningAndContraction) for more) both the [[no-cloning theorem]] and the [[no-deleting theorem]] of [[quantum physics]]/[[quantum information theory]].)

Namely, the [[linear types]] in [[VectBund]] form the subcategory [[FinDimVect]]. Any [[finite dimensional vector space]] admits a [[hermitian inner product]] making it a [[Hilbert space]]. For the discussion of logical [[conjunction]] and [[disjunction]] this Hilbert space structure plays no role and we may and will ignore it.

So given $\mathscr{H} \in FinDimVect$, a [[proposition]] about it in the [[internal logic]] sense of [[dependent type theory]] is, in [[categorical semantics]], a [[(-1)-truncation|(-1)-truncated]] [[object]] in the [[slice category]] over $\mathscr{H}$, hence a [[linear subspace]]

$$
  (\mathscr{V} \hookrightarrow \mathscr{H})
  \;\in\;
  \tau_{-1}\big(FinDimVect_{/\mathscr{H}}\big)
  \,.
$$

We need to consider the (co)fiber products of such objects (discussed [here](FinDimVect#FiberCoProducts) at *[[FinDimVect]]*):

Logical [[conjunction]] of such slice objects is given by their [[cartesian product]] in the slice, hence by the [[fiber product]] of their inclusion maps in $FinDimVect$. This is evidently given by the intersection of the subspaces:

\begin{tikzcd}[
  sep=20pt
]
  &
  \mathcal{V}_1 \cap_{_{\mathcal{H}}} \mathcal{V}_2
  \ar[d, phantom, "\simeq"{rotate=-90}]
  \\[-10pt]
  & 
  \mathcal{V}_1 \times_{\mathcal{H}} \mathcal{V}_2
  \ar[dl]
  \ar[dr]
  \ar[dd, phantom, "\scalebox{.6}{(pb)}"]
  \\
  \mathcal{V}_1
  \ar[dr, hook]
  &&
  \mathcal{V}_2
  \ar[dl, hook']
  \\
  &
  \mathcal{H}
\end{tikzcd} 

Logical [[disjunction]] of such slice objects is given by the [[(-1)-truncation]] of their [[coproduct]] in the slice. Using that coproducts in slices are computed in the ambient category (see [there](over+category#LimitsAndColimits)) this is given by the [[image]] of the abstract [[direct sum]] of the subspaces, which is the [[linear span]]:

\begin{tikzcd}[
  sep=30pt
]
  \mathcal{V}_1
  \ar[r, hook]
  \ar[ddr, hook]
  &
  \mathcal{V}_1 \oplus \mathcal{V}_2
  \ar[d, ->>]
  &
  \mathcal{V}_2
  \ar[l, hook']
  \ar[ddl, hook']
  \\[-10pt]
  &
  \mathrm{Span}_{\mathcal{H}}(\mathcal{V}_1, \mathcal{V}_2)
  \ar[d, hook]
  \\[+10pt]
  &
  \mathcal{H}
\end{tikzcd}


<center>
<img src="/nlab/files/InternalLogicInSlicesOfVect-230406.jpg" width="600">
</center>

The historical debate [above](#History) about justifying BvN logic as a formal logic is ultimately rooted in the fact that [[Vect]] is not a [[cartesian closed category]] (much less a [[locally cartesian closed category]]) so that its [[internal logic]] is exotic.





### Bohr toposes

See at _[[Bohr topos]]_ for more.


## Related concepts

* [[linear logic]]

* [[quantum programming language]], [[quantum computation]]

* [[quantum probability]]

* [[interpretation of quantum mechanics]]

* [[order-theoretic structure in quantum mechanics]]

  * [[Kochen-Specker theorem]]

  * [[Alfsen-Shultz theorem]]

  * [[Harding-Döring-Hamhalter theorem]]

* [[Fell's theorem]]

* [[Gleason's theorem]]

* [[Wigner theorem]]

* [[Bell's theorem]]

* [[Bub-Clifton theorem]]

* [[Kadison-Singer problem]]

* [[collapse of the wave function]]

* [[qbit]]

* [[quantum circuit]]


* [[effect algebra]]

* [[quantum mechanics]]

  * [[quantum computing]]

  * [[beable]]

* [[computable physics]]

* [[quantale]], 

* [[Bohr topos]]



## Literature
 {#References}

### Original articles

The original proposal on quantum logic:

* {#BirkhoffvonNeumann36} [[Garrett Birkhoff]], [[John von Neumann]]: *The logic of quantum mechanics*, Annals of Mathematics **37** 823-843 (1936) &lbrack;[doi:10.2307/1968621](https://doi.org/10.2307/1968621)&rbrack;

Historical account of [[John von Neumann]]'s further reasoning on quantum logic, which led him to develop the theory of [[von Neumann algebra factors]]:

* [[Miklos Rédei]], *Why John von Neumann did not Like the Hilbert Space formalism of quantum mechanics (and what he liked instead)*, Studies in History and Philosophy of Modern Physics **27** 4 (1996) 493-510 &lbrack;<a href="https://doi.org/10.1016/S1355-2198(96)00017-2">doi:10.1016/S1355-2198(96)00017-2</a>&rbrack;

Review:

* [[Karl Svozil]]: *Quantum Logic*,  Discrete Mathematics and Theoretical Computer Science, Springer (1998) &lbrack;[ISBN:9789814021074](https://link.springer.com/book/9789814021074)&rbrack;

* [[Karl Svozil]]: *Quantum logic. A brief outline* &lbrack;[arXiv:quant-ph/9902042](https://arxiv.org/abs/quant-ph/9902042)&rbrack;


Proposal for an enhancement of the Birkhoff-von Neumann axioms by [[probability measures]]:

* [[George Mackey]], Section 2-2 of: *The Mathematical Foundations of Quantum Mechanics: a Lecture-note Volume*, Mathematical physics monograph series, Benjamin (1963), Dover (2004) &lbrack;[google books](https://books.google.de/books?id=qlpb2mWYmfYC&printsec=frontcover&hl=de&source=gbs_ge_summary_r&cad=0#v=onepage&q&f=false)&rbrack;

further discussed in:

* {#Gleason57} [[Andrew Gleason]], _Measures on the closed subspaces of a Hilbert space_, Journal of Mathematics and Mechanics,  Indiana Univ. Math. J. **6** 4 (1957), 885-893 &lbrack;[IUMJ:56050](http://www.iumj.indiana.edu/IUMJ/FULLTEXT/1957/6/56050), [pdf](http://www.iumj.indiana.edu/IUMJ/FTDLOAD/1957/6/56050/pdf)&rbrack;

  > ([[Gleason's theorem]])

* Samuel S. Holland Jr., _Orthomodularity in infinite dimensions; a theorem of M. Sol&#232;r_, Bull. Amer. Math. Soc. (N.S.) __32__ (1995) 205-234 &lbrack;[arXiv:math.RA/9504224](http://arxiv.org/abs/math/9504224)&rbrack;

* Pavlos Kazakopoulos, Georgios Regkas, *Infinite Permutation Groups and the Origin of Quantum Mechanics* &lbrack;[arXiv:2307.13044](https://arxiv.org/abs/2307.13044)&rbrack;


An account of quantum logic within a comprehensive discussion of [[quantum mechanics]] and its [[interpretation of quantum mechanics]]:

* {#Scheibe73} [[Erhard Scheibe]], pp 71 in: *The logical analysis of quantum mechanics*, Pergamon Press Oxford (1973)


Discussion of [[categorical logic]] in [[symmetric monoidal categories]] (not just of [[vector spaces]] but of [[vector bundles]]) and hence of [[linear logic]] as quantum logic:

* {#Crown75} G. D. Crown, *On some orthomodular posets of vector bundles*, Journ. of Natural Sci. and Math. **15** 1-2 (1975) 11-25

much later followed up in:

* [[John Harding]], Taewon Yang, *The Logic of Bundles*, International Journal of Theoretical Physics **54** 12 (2015) &lbrack;[doi:10.1007/s10773-015-2760-6](http://dx.doi.org/10.1007/s10773-015-2760-6)&rbrack;
 
The introduction of [[linear logic]] with the suggestion of a possible relation to [[quantum physics]]:

* {#Girard87} [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science **50** 1 (1987)  &lbrack;<a href="https://doi.org/10.1016/0304-3975(87)90045-4">doi:10.1016/0304-3975(87)90045-4</a>&rbrack;
  
but remaining undecided:

> {#WildHopes} [Girard (1987), p. 7](#Girard87): "One of the wild hopes that this suggests is the possibility of a direct connection with quantum mechanics... but let's not dream too much!"

The relation of [[linear logic]] to [[quantales]], which have otherwise been proposed as providing a quantum logic:

* {#Yetter90} [[David Yetter]], *Quantales and (noncommutative) linear logic*, Journal of Symbolic Logic **55** (1990) 41-64 &lbrack;[doi:10.2307/2274953](https://doi.org/10.2307/2274953)&rbrack;

Maybe the first to really say that linear logic is a good kind of quantum logic:

* {#Pratt92} [[Vaughan Pratt]], *Linear logic for generalized quantum mechanics*, in Proceedings of *[Workshop on Physics and Computation (PhysComp'92)](https://www.computer.org/csdl/proceedings/phycmp/1992/12OmNx19jVS)* (1992) 166-180 &lbrack;[doi:10.1109/PHYCMP.1992.615518](https://doi.ieeecomputersociety.org/10.1109/PHYCMP.1992.615518), [pdf](http://boole.stanford.edu/pub/ql.pdf), [[Pratt-LinearLogicForQuantum.pdf:file]]&rbrack;

* {#Pratt93} [[Vaughan Pratt]], *The second calculus of binary relations*, Mathematical Foundations of Computer Science 1993. MFCS 1993, Lecture Notes in Computer Science **711**, Springer (1993) &lbrack;[doi:10.1007/3-540-57182-5_9](https://doi.org/10.1007/3-540-57182-5_9)&rbrack;

  > "Linear logic is seen in its best light as the realization of the [[Curry-Howard isomorphism]] for [[linear algebra]]"
 
First practical development of this perspective (see *[[quantum information theory in terms of dagger-compact categories]]):

* {#AbramskyCoecke} [[Samson Abramsky]], [[Bob Coecke]], *A categorical semantics of quantum protocols*, Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) &lbrack;[arXiv:quant-ph/0402130](http://arxiv.org/abs/quant-ph/0402130), [doi:10.1109/LICS.2004.1319636](https://doi.org/10.1109/LICS.2004.1319636)&rbrack;

* {#AbramskyDuncan05} [[Samson Abramsky]], [[Ross Duncan]], _A Categorical Quantum Logic_, Mathematical Structures in Computer Science, Volume 16, Issue 3 (2006)  pp. 469 - 489  ([arXiv:quant-ph/0512114](http://arxiv.org/abs/quant-ph/0512114), [doi:10.1017/S0960129506005275](https://doi.org/10.1017/S0960129506005275))

* {#Duncan06} [[Ross Duncan]], _Types for quantum mechanics_, 2006 ([pdf](http://personal.strath.ac.uk/ross.duncan/papers/rduncan-thesis.pdf), [slides](http://www.cs.ox.ac.uk/people/ross.duncan/talks/2005/pps-22-05-2005.pdf)) 

and as a paradigm for [[quantum programming languages]] ([[quantum lambda-calculus]]):

* [[Benoît Valiron]], *A functional programming language for quantum computation with classical control*, MSc thesis, University of Ottawa (2004) &lbrack;[doi:10.20381/ruor-18372](http://dx.doi.org/10.20381/ruor-18372), [pdf](https://ruor.uottawa.ca/bitstream/10393/26790/1/MR01625.PDF)&rbrack;

* {#SelingerValiron04} [[Peter Selinger]], [[Benoît Valiron]], *A lambda calculus for quantum computation with classical control*, Proc. of TLCA 2005 &lbrack;[arXiv:cs/0404056](https://arxiv.org/abs/cs/0404056), [doi:10.1007/11417170_26](https://doi.org/10.1007/11417170_26)&rbrack;

* {#SelingerValiron09} [[Peter Selinger]], [[Benoît Valiron]], *Quantum Lambda Calculus*, in: *Semantic Techniques in Quantum Computation*, Cambridge University Press (2009) 135-172 &lbrack;[doi:10.1017/CBO9781139193313.005](https://doi.org/10.1017/CBO9781139193313.005), [pdf](https://www.mscs.dal.ca/~selinger/papers/qlambdabook.pdf)&rbrack;


That therefore in particular categories of [[phase spaces]] and [[categories of cobordisms]] (the [[domains]] of [[FQFT|functorial quantum field theory]]) interpret quantum logic qua [[linear logic]] has been highlighted in 

* {#Baez04} [[John Baez]], *Quantum Quandaries: a Category-Theoretic Perspective*, in D. Rickles et al. (ed.) *The structural foundations of quantum gravity*, Clarendon Press (2006) 240-265 &lbrack;[arXiv:quant-ph/0404040](https://arxiv.org/abs/quant-ph/0404040), [ISBN:9780199269693](https://global.oup.com/academic/product/the-structural-foundations-of-quantum-gravity-9780199269693)&rbrack;

* {#Slavnov05} [[Sergey Slavnov]], *From proof-nets to bordisms: the geometric meaning of multiplicative connectives*, Mathematical Structures in Computer Science **15** 06 (2005) 1151-1178 &lbrack;[doi:10.1017/S0960129505004974](https://doi.org/10.1017/S0960129505004974)&rbrack;

* [[Sergey Slavnov]], *Geometrical semantics for linear logic (multiplicative fragment)*, Theoretical Computer Science **357** 1-3 (2006) 215-229 &lbrack;[doi:10.1016/j.tcs.2006.03.020](https://doi.org/10.1016/j.tcs.2006.03.020)&rbrack;

For more exposition along these lines see [Baez & Stay (2009)](#BaezStay09).

Interpreting the [[linear logic]]-sector of [[bunched logic]] as a quantum logic:

* [[Li Zhou]], [[Gilles Barthe]], [[Justin Hsu]], [[Mingsheng Ying]], [[Nengkun Yu]], *A Quantum Interpretation of Bunched Logic for Quantum Separation Logic*, LICS '21: Proceedings of the 36th Annual ACM/IEEE Symposium on Logic in Computer Science  75 (2021) 1–14 &lbrack;[arXiv:2102.00329](https://arxiv.org/abs/2102.00329), [doi:10.1109/LICS52264.2021.9470673](https://doi.org/10.1109/LICS52264.2021.9470673)&rbrack;


### Review and Exposition

Early general introductions and survey:


* [[Itamar Pitowsky]], *Quantum Probability -- Quantum Logic*, Lecture Notes in Physics **321**, Springer (1989) &lbrack;[doi:10.1007/BFb0021186](https://doi.org/10.1007/BFb0021186)&rbrack;

  > (including discussion of [[quantum probability theory]])

* [[Roland Omnès]], §5 of: *[[The Interpretation of Quantum Mechanics]]*, Princeton University Press (1994) &lbrack;[ISBN:9780691036694](http://press.princeton.edu/titles/5525.html)&rbrack;

* Pavel Pták , Sylvia Pulmannová , *Orthomodular structures as quantum logics*, Fundamental Theories of Physics **44** Kluwer, Springer (1991) &lbrack;[ISBN:978-0-7923-1207-9](https://link.springer.com/book/9780792312079)&rbrack;

* Kurt Engesser, Dov M. Gabbay, Daniel Lehmann (eds.) *[[Handbook of Quantum Logic and Quantum Structures]]* Elsevier (2009) &lbrack;[ISBN:9780080931661](https://www.sciencedirect.com/book/9780444528698)&rbrack;

A bibliography of hundreds of works up to 1992:

* [[Mladen Pavičić]], *Bibliography on quantum logics and related structures*,  Int J Theor Phys **31** (1992) 373–455 &lbrack;[doi:10.1007/BF00739999](https://doi.org/10.1007/BF00739999), [pdf](http://www.irb.hr/users/mpavicic/papers-ps-pdf/quantum-logic/1992-int-j-theor-phys-1.pdf)&rbrack;



See also:

* [[Franco Strocchi]], §2.5 in: *An introduction to the mathematical structure of quantum mechanics*, Advanced Series in Mathematical Physics **28**, World Scientific (2008) &lbrack;[doi:10.1142/7038](https://doi.org/10.1142/7038)&rbrack;


* Wikipedia, _[Quantum logic](http://en.wikipedia.org/wiki/Quantum_logic)_

* Stanford encyclopaedia of philosophy, _[Quantum logic and probability theory](http://plato.stanford.edu/entries/qt-quantlog)_


Critique of Birkhoff-von Neumann logic in contrast to [[quantum information via dagger-compact categories]]:

* {#AbramskyCoecke2007} [[Samson Abramsky]], [[Bob Coecke]], *Physics from Computer Science: a Position Statement*, [International Journal of Unconventional Computing **3** 3 (2007)](https://www.oldcitypublishing.com/journals/ijuc-home/ijuc-issue-contents/ijuc-volume-3-number-3-2007/) &lbrack;[pdf](https://www.cs.ox.ac.uk/files/349/YORKIJUC.pdf), [ijuc-3-3-p-179-197](https://www.oldcitypublishing.com/journals/ijuc-home/ijuc-issue-contents/ijuc-volume-3-number-3-2007/ijuc-3-3-p-179-197/)&rbrack;

Further exposition of non-cartesian [[monoidal categories]] as [[categorical semantics]] for quantum logic qua [[linear logic]]:

* {#Baez04} [[John Baez]], *Quantum Quandaries: a Category-Theoretic Perspective*, in D. Rickles et al. (ed.) *The structural foundations of quantum gravity*, Clarendon Press (2006) 240-265 &lbrack;[arXiv:quant-ph/0404040](https://arxiv.org/abs/quant-ph/0404040), [ISBN:9780199269693](https://global.oup.com/academic/product/the-structural-foundations-of-quantum-gravity-9780199269693)&rbrack;

* {#BaezStay09} [[John Baez]], [[Mike Stay]], *Physics, topology, logic and computation: a rosetta stone*, ([arxiv/0903.0340](http://arxiv.org/abs/0903.0340)); in "New Structures for Physics", ed. Bob Coecke, Lecture Notes in Physics __813__, Springer (2011) 95-174 &lbrack;[doi:10.1007/978-3-642-12821-9](https://link.springer.com/book/10.1007/978-3-642-12821-9)&rbrack;

Review of of quantum logic with an eye towards the [[EPR paradox]] and [[Bell's inequalities]]:

* Laura Molenaar, *Quantum logic and the EPR paradox*, Delft (2014) &lbrack;[uuid:cfee567c-425a-4b2d-9550-f7d7eea41b8b](http://resolver.tudelft.nl/uuid:cfee567c-425a-4b2d-9550-f7d7eea41b8b)&rbrack;


### Further development

* {#Heunen08} [[Chris Heunen]], _Quantifiers for quantum logic_ ([arXiv:0811.1457](http://arxiv.org/abs/0811.1457))
 

* {#Harding08} [[John Harding]], _A link between quantum logic and categorical quantum mechanics_, Int J Theor Phys (2009) 48: 769&#8211;802

* {#HeunenJacobs09} [[Chris Heunen]], [[Bart Jacobs]], _Quantum Logic in Dagger Kernel Categories_, Order, July 2010, Volume 27, Issue 2, pp 177-212,  ([arXiv:0902.2355](http://arxiv.org/abs/0902.2355))
 

* {#CCGP09} Gianpiero Cattaneo, Maria Luisa Dalla Chiara, Roberto Giuntini and Francesco Paoli, section 9 of _Quantum Logic and Nonclassical Logics_, p. 127 in  Kurt Engesser, Dov M. Gabbay, Daniel Lehmann (eds.) _Handbook of Quantum Logic and Quantum Structures: Quantum Logic_, 2009 North Holland
  

* [[Samson Abramsky]], _Temperley-Lieb Algebra: From Knot Theory to Logic and Computation via Quantum Mechanics_, In Goong Chen, [[Louis Kauffman]],
and [[Samuel Lomonaco]] (eds.), _Mathematics of Quantum Computing and Technology_, pages 415&#8211;458. Taylor and Francis, 2007. ([arXiv:0910.2737](http://arxiv.org/abs/0910.2737))

* {#Girard11} [[Jean-Yves Girard]], _[[Lectures on Logic]]_, European Mathematical Society 2011
 

* {#LagoFaffian12} [[Ugo Dal Lago]], Claudia Faggian, _On Multiplicative Linear Logic, Modality and Quantum Circuits_ &lbrack;[arXiv:1210.0613](http://arxiv.org/abs/1210.0613)&rbrack;
 

* {#CoeckeHeunenKissinger13} [[Bob Coecke]], [[Chris Heunen]], [[Aleks Kissinger]], _Compositional Quantum Logic_ ([arXiv:1302.4900](http://arxiv.org/abs/1302.4900))
 

 

Discussion of [[Fock space]]-type free [[quantum field theory]] in [[linear logic]] is in 

*  [[Marcelo Fiore]], _Differential Structure in Models of Multiplicative Biadditive Intuitionistic Linear Logic_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.109.2328))


The proposal that the [[internal logic]] of [[Bohr toposes]] is a good notion of quantum logic is made in

* {#HeunenLandsmanSpitters07} [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _A topos for algebraic quantum theory_, Comm. Math. Phys. 291:63&#8211;110, 2009, free access [doi](http://dx.doi.org/10.1007/s00220-009-0865-6), [arXiv:0709.4364](http://arxiv.org/abs/0709.4364)
 

* [[Steve Vickers]], slides from Midland Grad. School 2010, quantum topos theory, [web](http://www.cs.bham.ac.uk/~sjv/teaching/MGS2010), most relevant part IV: [pdf](http://www.cs.bham.ac.uk/~sjv/teaching/MGS2010/slides4.pdf)


See also

* [[Yuri Manin]], _A course in mathematical logic_, Springer 

*  &#1044;.&#1048;. &#1041;&#1083;&#1086;&#1093;&#1080;&#1085;&#1094;&#1077;&#1074;, &#1055;&#1088;&#1080;&#1085;&#1094;&#1080;&#1087;&#1080;&#1072;&#1083;&#1100;&#1085;&#1099;&#1077; &#1074;&#1086;&#1087;&#1088;&#1086;&#1089;&#1099; &#1082;&#1074;&#1072;&#1085;&#1090;&#1086;&#1074;&#1086;&#1081; &#1084;&#1077;&#1093;&#1072;&#1085;&#1080;&#1082;&#1080;, 1966, 162 &#1089;.


* A. Sudbery, _Quantum mechanics and the particles of nature_, An outline for mathematicians, Camb. Univ. Press 1986

* Stanford Encyclopedia of Philosophy, [qm: von Neumann vs. Dirac](http://plato.stanford.edu/entries/qt-nvd), 

[[!redirects quantum logics]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[modal logic]] and specifically in [[epistemic modal logic]], two key [[modalities]] that one wants to consider are those of _necessity_ and _possibility_.

The idea is to consider for any [[proposition]] $p$ 

* a proposition labeled $\Box p$ expressing the idea that "$p$ is necessarily true";

* a proposition labeled $\diamondsuit p$ expressing the idea that "$p$ is possibly true".

## Via S4 modal logic
 {#ViaS4ModalLogic}

A common formalization of necessity/possibility is via [[S4 modal logic|S4]] or [[S5 modal logic]], whose [[axioms]] are motivated as follows:


For every comonadic [[modality]] like necessity $\Box$, one typically demands that it preserves [[implication]], in the sense that

$$\Box(p \to q) \to (\Box p \to \Box q).$$

This preservation of implication is called the *[[axiom K (modal logic)|axiom K]]*.  In traditional non-[[categorical logic|categorical]] [[modal logic]] this is often all that is considered ("[[K modal logic]]), because the operators are considered [[de Morgan duality|de Morgan dual]]: 

$$
  \label{deMorganDualityBetweenNecessiryAndPossibility}
  \Box A
  \;=\;
  \neg 
  \big(
    \diamondsuit (\neg A)
  \big)
  \,.
$$  

In an intuitionistic modal logic, one would also demand that $\diamondsuit$ preserves implication in a suitable sense, such as 

$$\Box(p\to q) \to (\diamondsuit p \to \diamondsuit q).$$

One may also ask for a further compatibility such as $(\diamondsuit p \to \Box q) \to \Box(p\to q)$, as [Simpson](#Simpson) does.

Similarly, the axiom $\Box(p \to q) \to (\Box p \to \Box q)$ implies that $\Box$ preserves [[logical conjunction]], i.e. $\Box(p\wedge q) \leftrightarrow (\Box p \wedge \Box q)$.  The nullary version $\Box(\top)\leftrightarrow \top$ follows from the "necessitation rule" which says that if $p$ is provable in the empty context, then so is $\Box p$.  (This is an additional rule assumed in modal logics.)  From duality (eq:deMorganDualityBetweenNecessiryAndPossibility) it follows that $\diamondsuit$ preserves [[logical disjunction]] (both binary and nullary), while intuitionistically one may want to ask for this separately ([Simpson](#Simpson) does, but [Biermann & de Paiva 2000](#BiermanDePaiva00) don't).

A minimum further requirement on a formalization of $\Box$ and $\diamondsuit$ to have the interpretation of "necessity" and "possibility" is arguably that there are [[implications]]

* $\Box p \rightarrow p$;

* $p \rightarrow \diamondsuit p$,

expressing that if something is necessarily true, then that should mean that it is true in all instances, and that if something is true in one instance, then it is evidently possible for it to be true.  With these additions to the above [[K modal logic]], one speaks of *[[T modal logic]]*.

By similar plausibility arguments one often demands that

* $\Box p \to \Box \Box p$

* $\diamondsuit \diamondsuit p \to \diamondsuit p$

which may be read as expressing that iterating the previous reasoning does not yield any new insight.  This additional enhancement to [[T modal logic]] yields *[[S4 modal logic]]*. 

\linebreak

In terms of [[categorical logic]] interpreting propositional logic into a [[Heyting algebra]], the S4 axioms just say ([Bierman & de Paiva 1996](#BiermanDePaiva96), [2000](#BiermanDePaiva00)) that:

* $\Box$ is a (necessarily [[idempotent comonad|idempotent]]) [[comonad]] which is [[monoidal functor|monoidal]], hence product-preserving; and

* $\diamondsuit$ is a (necessarily [[idempotent monad|idempotent]]) [[monad]] which is a "$\Box$-[[strong functor|strong]] functor", and (perhaps) preserves coproducts.

As usual, we can also replace the Heyting algebra by a [[cartesian closed category]], thereby obtaining a "proof-relevant" system; in this case monoidality of $\Box$ does not imply directly that it preserves products, although one might reasonably ask that it does (see [[strong monads]] [[monad in computer science|in computer science]]).
Note that if one moves from Heyting algebras to cartesian closed categories the (co)monads are not necessarily idempotent (and there are good proof-theoretical reasons why they should not be so).

The above reasoning makes plausible that any operators expressing "necessity" and "possibility" should *at least* satisfy these (co)monad axioms.  However, not every (co)monad is sensibly interpreted this way.

For example, there is

* the (idempotent) comonad $\varnothing$ which sends every proposition to [[false]] (the [[nothing|non-being]]-modality);

* the (idempotent) monad $\ast$ which sends every proposition to [[true]] (the [[being]]-modality).

These $\emptyset \dashv \ast$ satisfy all of the above axioms (as well as more axioms that are being considered, such as those called [[S5 modal logic]]) but they are not a very good interpretation of the informal concepts of "possibility" and "necessity".  Under this interpretation nothing is necessarily true, and everything is possibly true.  While this is not nonsensical, it is not very interesting and doesn't correspond well to our intuitive meanings of "necessary" and "possible".

This issue becomes more pronounced as one generalizes from the small realm of [[propositional logic]] to include both or either of:

* [[types]] more general than [[propositions]] (in [[modal type theory]]);

* [[first-order logic]] with [[quantifiers]], hence [[hyperdoctrines]]/[[dependent types]].

There are many [[modal operators]] in such contexts which are all modeled by (idempotent) (co)monads but which do not have the interpretation of expressing the modes of "necessity" or "possibility". See at _[[modal operator]]_ for some examples.

Therefore it makes sense to ask which _additional_ axioms on a modal operator make it an accurate formalization of the informal concepts of necessity and possibility.  The answer to this may depend on context and intention (after all one is trying to find a precise formulation of an a priori informal idea).


## Possible worlds via dependent types
 {#InFirstOrderLogicAndTypeTheory}

One common philosophical interpretation of "necessarily" and "possibly" is ([[Kripke semantics]]) in terms of a collection of "[[possible worlds]]" that are similar to the "real world", but not the same.  Under this interpretation, a proposition is necessarily true if it is true in all possible worlds, and possibly true if it is true in some possible world.

Now the idea of a proposition being true "necessarily in all possible cases" or "possibly at least in one case" is formally very well established in *predicate* logic: it is just the interpretation of the [[universal quantifier]] "for all" $\forall$ and of the [[existential quantifier]] "there exists" $\exists$.  In [[categorical logic]], these [[quantifiers]] (see there for details) are part of [[adjoint triple]] whose middle piece is [[context]] extension, and as such they naturally induce a [[comonad]] and a [[monad]].  Thus, if we interpret "necessarily" and "possibly" according to [[S5 modal logic]] in terms of [[possible worlds]], we can model them by this [[base change]] [[adjoint triple]] (cf. [Awodey 2006, p. 279](#Awodey06)):

### Globally
 {#Globally}

In more detail, let $W$ be the [[context]] [[type]] of [[variables]]/[[terms]] on which the propositions depend, i.e. the collection "of all [[possible worlds semantics|possible worlds]]" (in fact a [[Kripke frame]] for [[S5 modal logic]], see [there](Kripke+frame#NecessityLogic)).  Any specific choice of $W$ may be taken as specifying what is to be understood as a "possible world".

Writing $\mathbf{H}_{\ast}$ for the [[category]] of all context-free [[types]] under consideration and writing $\mathbf{H}_{/W}$ for the category of types in [[context]] "$W$", then in [[categorical logic]] (for instance $\mathbf{H}_{/(-)}$ might be a [[hyperdoctrine]] over a [[category of contexts]] containing objects $W$ and $\ast$) the [[quantifiers]] $\forall_{w\colon W}$ and $\exists_{w\colon W}$ participate in a [[base change]] [[adjoint triple]] 

$$
  (\exists_W \dashv W^\ast \dashv \forall_W)
  \;\colon\;
  \mathbf{H}_{/W}
    \stackrel{\stackrel{\forall_{w \colon W}}{\longrightarrow}}{\stackrel{\stackrel{W^\ast}{\longleftarrow}}{\underset{\exists_{w\colon W}}{\longrightarrow}}}
  \mathbf{H}
  \,.
$$

In a context of pure [[logic]] this would be called

[[existential quantifier]] $\dashv$ [[context extension]] $\dashv$ [[universal quantifier]]

whereas in a context of [[dependent type theory]] this would be called

[[dependent sum]] $\dashv$ [[context extension]] $\dashv$ [[dependent product]].

In either case, under the suitable version of [[propositions as types]] (and using [[bracket types]] etc. if desired), the operations $\forall$ and $\exists$ have the usual interpretation of "for all" and "there exists".

Note, however, that these operations change the context from $W$ to $\ast$.  In other words, if a proposition $P$ depends on $W$, so that it may be true in some worlds and false in others, then $\exists_W P$ and $\forall_W P$ no longer depend on $W$.  The idea of a necessity and a possibility modality is to send a proposition in some context to a proposition in the *same* context, so that we can for instance say that $\Box P \to P$ and so on.  Thus we need to make $\exists_W P$ and $\forall_W P$ into propositions that again depend on $W$ --- even if they now depend trivially on $W$, being [[context extension|extended]] back from the absolute context $\ast$ to $W$.

This is just what is accomplished by passing from the above [[adjoint triple]] to the induced [[adjoint pair]] on $\mathbf{H}_{/W}$ by forming composites with the [[context extension]] operation $W^\ast$

\[
  \label{PossibilityNecessityAdjunctionViaBaseChange}
  (\underset{W}{\diamondsuit} \dashv \underset{W}{\Box})
  \coloneqq
  \left(
     \left(
     W^\ast \circ \underset{w\colon W}{\exists}
     \right)
     \dashv
     \left(
     W^\ast \circ \underset{w\colon W}{\forall}
     \right)
  \right)
  \;\colon\;
  \mathbf{H}_{/W}
    \longrightarrow
  \mathbf{H}_{/W}
  \,.
\]

With this, if $p\in \mathbf{H}_{/W}$ is a [[proposition]] about terms $w$ of $W$ (a $W$-[[dependent type]]) then 

* $\underset{W}{\diamondsuit}(p)$ is [[true]]/[[inhabited type|inhabited]] precisely if $\underset{w \colon W}{\exists} p(w)$ is [[true]]/[[inhabited type|inhabited]], hence (that is the standard interpretation of the [[quantifier]]) if it is possible for $p(w)$ to be true for some $w$;

* $\underset{W}{\Box}(p)$ is [[true]]/[[inhabited type|inhabited]] precisely if $\underset{w \colon W}{\forall} p(w)$ is [[true]]/[[inhabited type|inhabited]], hence (that is again the standard interpretation of the quantifier) if $p(w)$ necessarily holds for all $w$.


Thus, this gives one [[syntax|syntactic]] formalization of the informal meaning of "necessity" and "possibility".  The natural [[semantics]] for these [[base change]] operations is a generalization of the simple traditional _[[possible worlds semantics]]_ of propositional necessity and possibility modalities.  (There are, however, more complicated possible worlds semantics.)

Moreover, with this formalization, the modal operator $\underset{W}{\diamondsuit}$ is [[left adjoint]] to $\underset{W}{\Box}$ and hence both form an [[adjoint modality]]. As discussed there, this is a formalization of [[unity of opposites|opposite]] concepts, which reflects well the opposition of necessity and possibility in their informal meaning.

Observe how the corresponding [[unit of a monad|unit]] and [[counit of a comonad|counit]] maps properly reflect the intended logic of necessity, actuality and possibility:

\[
  \label{NecessityActualityPossibility}
\]
\begin{imagefromfile}
    "file_name": "QCwthLHT-ClassicalNecessity-221003.jpg",
    "width": "900",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Some technical remarks:

1. In general, $\underset{W}{\diamondsuit}$ and $\underset{W}{\Box}$ as defined above are, while being a [[monad]] and [[comonad]], respectively, not an [[idempotent monad]] and [[idempotent comonad]] if generalized from [[first-order hyperdoctrines]] to more general [[dependent type theories]]. But this just reflects the usual issues with [[propositions as types]], see there for more discussion.

1. While [[base change]]-[[adjunctions]] are essentially unique and not free to choose, there is a genuine choice in the above given by the choice of [[context]] $W$. This is reflected in the subscripts of $\underset{W}{\diamondsuit}$ and $\underset{W}{\Box}$ above. It is the choice of this $W$ that gives different kinds of possibility and necessity. More generally there is in fact not just a choice of a context, but of a morphism of contexts, reflecting what is often called "accessibility of possible worlds". This we come to [below](#ViaBaseChangeRelatively).


### Relation to Potentiality
 {#RelationToPotentiality}


There is also an [[adjoint pair]] on the other side, $\mathbf{H}_{/\ast}$, of the [[base change]] maps, in which the [[left adjoint]] is given by [[context extension]] back to $\mathbf{H}_{/W}$ followed by $\exists_W$, and dually the [[right adjoint]] is given by $W^\ast$ followed by $\forall_W$. The former is the [[coreader comonad]], whereas the latter is the [[reader monad]] (aka [[function monad]]):

\[
  \label{ModalitiesFromDependentTypeFormers}
\]
<center>
<img src="/nlab/files/TheFourModalitiesOfBaseChange-221109.jpg" width="500">
</center>



If we think of the types $P_\bullet \,\in\, Type_B$ in the given context -- now called "$B$" -- as *[[actuality|actual types]]* (eq:NecessityActualityPossibility) then the types down in the base context $P \,\in\, Type$ should be thought of as [[potentiality|potential types]] that fail to be actual in that they are missing information about their $B$-dependency (see also at *[[nondeterministic computation]]*, [here](nondeterministic+computation#FormalizationViaIndefinitenessEffects)):

The definiteness-counit $\star P \rightarrow P$ witnesses their inhabitation as following from that of a definite type after forgetting which definite world $b \colon B$ was used to inhabit it.

{#PotentialityAsMonadicDescent} More in detail, since $(p_B)^\ast$ is a [[conservative functor]], the [[monadicity theorem]] (see [this example](monadicity+theorem#BaseChangeOfPresheavesAlongFullyFaithfulFunctor)) says 

\begin{imagefromfile}
    "file_name": "PotentialTypesAsPossibilityModules-221101b.jpg",
    "width": "580",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


that the types $P \,\in\, Type$ are equivalently 

1. those actual types $P_\bullet$ which carry a possibility-[[algebra over a monad|monad action]] 
   $
     \diamondsuit_B P_\bullet
       \longrightarrow 
     P_\bullet
   $

1. those actual types $P_\bullet$ which carry a necessity-[[coalgebra over a comonad|co-monad co-action]]
   $
     P_\bullet
       \longrightarrow 
     \Box_B P_\bullet
   $

(The same conclusion in known in the theory of [[lenses in computer science]], see [there](lens+in+computer+science#PossibilityMonadicity).)

{#PotentialDataAsPossibilityModalData} Hence:

<center>
<img src="https://ncatlab.org/nlab/files/PotentialDataAsPossibilityModalData-230804.jpg" width="780">
</center>


{#PotentialAxiomsComparedToAristotle} This formalization compares reasonably well with [[Aristotle]]'s discussion, who wrote (in the translation from [Ferroni & Gili (2016)](potentiality+and+actuality#FerroniGili16), [§44](https://www.cairn.info/revue-de-philologie-litterature-et-histoire-anciennes-2016-1-page-81.htm#pa44)) first that:

> of non-existent things some exist potentially

which is our

$$
 \underset{
   \color{blue}
   \text{non-existent thing}
 }{
  \big(
    \varnothing
    ,\,
    \diamondsuit_W \varnothing \xrightarrow{\exists !} \varnothing
  \big) 
  }
  \underset{
    \color{blue}
    \text{is a}
  }{
    \phantom{\vert}
    \colon\;
    \phantom{\vert}
  }
  \;
  \underset{
    \color{blue}
    \text{potential thing}
  }{
    Type^{\diamondsuit_W}_W
  }
$$

and then:

> if they exist ... it is not possible that it is true to say that: this is possible but will not be the case.

hence (unwinding the double negation)

> if potential things exist ... and are possible then they will be the case (ie: will be actual)

which is our

$$
  \underset{
    \color{blue}\text{given a potential thing}
  }{
  (D_\bullet, \rho_\bullet)
  \,\colon\, 
  Type_W^{\diamondsuit_W}
  }
  \;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;
  \underset{
   \color{blue} \text{which is possible}
  }{
    \diamondsuit_W D_\bullet 
  }
  \underset{
   \color{blue}\text{then}
  }{
    \phantom{\vert}
    \xrightarrow{\;\; \rho_\bullet \;\;} 
    \phantom{\vert}
  }
  \underset{
   \color{blue}\text{it is actual}
  }{
    D_\bullet
    \mathrlap{\phantom{vert_{g}}}
  }
$$





\linebreak

### Relative version
  {#ViaBaseChangeRelatively}

With this axiomatization via [[base change]], it is immediate to consider the more general relative case where instead of [[base change]] to a [[unit type]] $W \to \ast$ one considers [[base change]] 

$$
  (\exists_\omega \dashv \omega^\ast \dashv \forall_\omega)
  \;\colon\;
  \mathbf{H}_{/W}
    \stackrel{\stackrel{\forall_{w \colon \omega^{-1}(-)}}{\longrightarrow}}{\stackrel{\stackrel{\omega^\ast}{\longleftarrow}}{\underset{\exists_{w\colon \omega^{-1}(-)}}{\longrightarrow}}}
  \mathbf{H}_{/W_0}
  \,.
$$

along any [[morphism]] 

$$
  \omega \colon W \longrightarrow W_0
$$

and sets

$$
  (\underset{\omega}{\diamondsuit} \dashv \underset{\omega}{\Box})
  \coloneqq
  \left(
     \left(
     \omega^\ast \circ \underset{w\colon \omega^{-1}(-)}{\exists}
     \right)
     \dashv
     \left(
     \omega^\ast \circ \underset{w\colon \omega^{-1}(-)}{\forall}
     \right)
  \right)
  \;\colon\;
  \mathbf{H}_{/W}
    \longrightarrow
  \mathbf{H}_{/W}
  \,.
$$

If here $\omega$ is an [[effective epimorphism]] (a [[1-epimorphism]]) then it exibits an [[equivalence relation]] on $W$, where $w_1\sim w_2$ is given by $\omega(w_1) = \omega(w_2)$. In traditional [[possible worlds semantics]] such equivalence relation in a [[Kripke frame]] is called an "accessibility relation between possible worlds" for the case of [[S5 modal logic]]. Now 

*  $\underset{\omega}{\diamondsuit} p$ is true/inhabited at $w\in W$ iff it is true/inhabited at at least one $\tilde w$ in the same equivalence class of $w$;

*  $\underset{\omega}{\Box} p$ is true/inhabited at $w\in W$ iff it is true/inhabited at all $\tilde w$ in the same equivalence classes of $w$.

For more on this see at *[[S5 modal logic]]* -- *[via dependent types](S5+modal+logic#ViaDependentTypeTheory)*.

\linebreak

### Examples
 {#Examples}

#### Historical examples

Historically, one informal example whose formalization in [[modal logic]] has been controversially discussed (see for instance [IEP "Rudolf Carnap: Modal Logic"](#IEPCarnapModal)) is the pair of informal assertions

1. "9 is necessarily greater than 7."

1. "The number of planets in the solar system is 9."

(**Remark.** It maybe adds to the joy of modal logic to notice that the second sentence, which was regarded as true in our world at the time the above example was brought up, actually [no longer is](http://www.universetoday.com/15568/how-many-planets-are-in-the-solar-system/). Of course this only highlights  that indeed this statement is not to be expected to be "necessarily true" in any sense.)

The issue with this example is that if one does not fix a decent formalization of these statements, then naively they seem to imply as correct the statement "The number of planets in the solar system is necessarily greater than 7.", which however sounds like it ought to be wrong.

We now formalize and then analyze this example with the [above](#InFirstOrderLogicAndTypeTheory) prescription.

So let $W$ be any [[type]], to be thought of as the type of [[possible worlds]]. Write 

$$
  w\colon W \vdash \mathbb{N}(w) \colon Type
$$

for the $W$-dependent type that is constant on the ordinary [[type of natural numbers]], i.e.$\mathbb{N}(w) = \mathbb{N}$ for all $w\colon W$.

The terms of $\mathbb{N}$, i.e. the [[natural numbers]], canonically extend to $W$-dependent terms of this dependent type

$$
  w\colon W \vdash 9 \colon \mathbb{N}(w) 
$$

namely to the constant terms, which take the same value (here: 9) for all $w \colon W$.

In contrast to this, assume now that $W$ is such there is at least one non-[[constant function]] $W \to \mathbb{N}$. In fact, in the spirit of the informal problem at hand, we require a surjective function.
This gives a non-constant term of the constantly $W$-dependent type of natural numbers, which we may just as well call

$$
  w \colon W \vdash NumberOfPlanetsInSolarSystem(w) \colon \mathbb{N}(w)
  \,.
$$

That is the formalization of the above example we consider, and it should be evident enough. Now we may step back and see what the [above formalization](#InFirstOrderLogicAndTypeTheory) produce from this.

So consider the $W$-dependent [[identity type]]

$$
  w \colon W \vdash (9 = NumberOfPlanetsInTheSolarSystem)(w) \colon Type
  \,.
$$

By the assumption that $NumberOfPlanetsInTheSolarSystem(w)$ is not constant in $W$ it follows that the [[dependent product]] over $W$ of that dependent identity type is the [[empty type]], and so the same is true for $\Box_W$ applied to it:

* $[\Box_W (9 = NumberOfPlanetsInTheSolarSystem)]$ is [[false]].

However, if we assume that there is one $w$ for which indeed $NumberOfPlanetsInTheSolarSystem(w)$ takes the value 9, then the [[dependent sum]] over the dependent identity type contains that coincidence as a term, and so $\diamondsuit_W$ of our dependent identity type is [[inhabited type|inhabited]]. Hence

* $[\diamondsuit_W (9 = NumberOfPlanetsInTheSolarSystem)]$ is [[true]].

In English words, these formal consequences are to be pronounced as:

1. "It is false that it is necessary that the number of planets in the solar system is 9."

1. "It is true that it is possible that the number of planets in the solar system is 9."

Which is just as it should be.

Similarly, the $W$-dependent type

$$
  w \colon W \vdash (NumberOfPlanetsInTheSolarSystem \gt 7)(w) \colon \mathbb{N}(w)
$$

is only going to be [[inhabited type|inhabited]] if indeed the value $NumberOfPlanetsInTheSolarSystem(w)$ is greater than 7 for all $w\colon W$. With our formalization assumption above this is not the case, and so one finds that 

* $[\Box_W (NumberOfPlanetsInTheSolarSystem \gt 7)]$ is [[false]].

hence 

* "It is false that it is necessary that the number of planets in the solar system is greater than 7."

\linebreak

#### Quantum modal logic
 {#ModalQuantumLogic}

> under construction

We discuss[^1] the modal logic induced from base change of [[dependent types]], as [above](#Globally), now applied to [[dependent linear types]] over [[finite sets]] ([[family of finite types]]) --- to find a natural [[modal logic|modal]] [[quantum logic]] (and in fact a natural [[quantum programming language]] for [[quantum circuits]], see at *[[quantum circuits via dependent linear types]]* for more on this).

[^1]: Following discussion at *[[schreiber:Topological Quantum Programming in Linear Homotopy Type Theory]]* 

\linebreak

Given a base [[type]] (which we take to be  [[family of finite types|finite]])

\[
  \label{FiniteBaseType}
  B \;\in\; FinType
  \,,
\]

write $LinType_B$ for the $B$-[[dependent linear types]]

$$
  \mathscr{H}_\bullet \,\in\, \mathrm{LinType}_B
  \;\;\;\;\;\;\leftrightarrow\;\;\;\;\;\;
  b : B \;\;\vdash\;\; \mathscr{H}_b : \mathrm{LinType}
  \,.
$$

The intended [[categorical semantics]] is obtained by [[relation between type theory and category theory|interpreting]] $\mathscr{H}_\bullet$ as a $B$-[[indexed set]] of [[complex vector spaces]] (or rather: [[Hermitian inner product spaces]]) which the reader may want to think of as being [[finite dimensional vector space|finite dimensional]] ([hence](Hilbert+space#FiniteDimensionalInnerProductSpaces): as [[Hilbert spaces]] if positive definite), though this finite-dimensionality condition of $\mathscr{H}_b$ is not used in the following (as opposed to the finiteness condition on $B$, which is used).

We assume that our [[dependent linear type theory]] realizes [[base change]] of linear types along maps of non-linear base types in the form of [[Wirthmüller context|Wirthmüller]]-type [[yoga of six operations]]:

\begin{imagefromfile}
    "file_name": "QCwthLHT-BaseChange-221001.jpg",
    "width": "680",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Moreover, we assume that along maps with [[finite type|finite]]-[[fibers]], such as the [[terminal object|terminal]] map $B \to \ast$, the left [[base change]] agrees with the right [[base change]] ("[[ambidextrous adjunction|ambidexterity]]", so that both give the dependent *[[biproduct]]* $\otimes_{b : B}$ over $B$):

$$
  \mathrm{stability}
  \;:\;
  (p_B)_! \mathscr{H}_\bullet
  \;\;\simeq\;\;
  (p_B)_\ast \mathscr{H}_\bullet
  \;\;=:\;\;
  \underset{b : B}{\bigoplus}  
  \mathscr{H}_b
  \;\;\;
  \text{(biproducts)}
$$

Curiously, in terms of [[modal logic]], this is the *[[Gell-Mann principle]]* of quantum physics, in that it means:

$$
  \array{
    \llap{\text{The}}\;\text{possible}
    &
    \text{is} 
    &
    \text{necessary}
    &
    \text{and hence} 
    &
    \text{actualized}
    \\
    \diamondsuit \mathcal{H}_\bullet
    &
    \simeq
    &
    \Box \mathcal{H}_\bullet 
    &
    \xrightarrow{\phantom{--} \epsilon \phantom{--}} 
    &
    \mathcal{H}_{
      \bullet   
      \;
      \mathrlap{\text{with some probability}}
    }
  }
$$

Both these assumptions are verified in the [[linear homotopy type theory]] of [Riley (2022),  §2.4](dependent+linear+type+theory#Riley22Thesis), which should have [[categorical semantics]] in (a [[type-theoretic model category]] [[presentable (infinity,1)-category|presenting]]) the [[(infinity,1)-topos|$(\infty,1)$-topos]] of [[parameterized spectrum|parameterized]] [[Eilenberg-MacLane spectrum|$H\mathbb{C}$]]-[[module spectra]], among which [[complex vector spaces]] $\mathscr{H}$ [[full (infinity,1)-subcategory|embed]] as their [[Eilenberg-MacLane spectra|Eilenberg-MacLane]] [[module spectra]] $H\mathscr{H}$.


Recalling from [above](#RelationToPotentiality) the quadruple of ([[comonad|co-]])[[monad|monadic]] [[modalities]] associated with any [[base change]]
one finds that its quantum analog for [[dependent linear types]] (along [[family of finite types|finite fibers]] (eq:FiniteBaseType)) 

\[
  \label{ModalitiesFromDependentLineaTypeFormers}
\]
<center>
<img src="/nlab/files/TheFourModalitiesOfLinearBaseChange-221109.jpg" width="700">
</center>


where the interpretation of the modal ([[counit of a comonad|co-]])[[unit of a monad|units]] is as follows:

\[
  \label{QuantumModalUnits}
\]
\begin{imagefromfile}
    "file_name": "QCwthLHT-QuantumModalUnits-230806.jpg",
    "width": "810",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


In the context of linear types not just $(p_B)^\ast$ is [[monadic functor|monadic]], but also $(p_B)_!$/$(p_B)_\ast$ (for details see the *[quantum reader monad](function+monad#QuantumReaderMonad)*), so that the factorization [above](#PotentialityAsMonadicDescent) enhances to the following situation:

\[
  \label{DependentLinearTypesAsIndefiniteLinearTypes}
\]
\begin{imagefromfile}
    "file_name": "LinearTypesAsModalModules-221113.jpg",
    "width": "810",
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


\linebreak


\[
  \label{NotationalConvention}
\text{It is convenient and meaningful to declare notational conventions to:}
  \phantom{--------------------}
\]
1. abbreviate $\mathscr{H} \,\coloneqq\, p_! \mathscr{H}_\bullet \,\simeq\, p_\ast \mathscr{H}_\bullet$

1. notationally suppress any outer application of $(p_B)^\ast \colon LinType \to LinType_B$;

Thereby, the definiteness/randomness modalities in relation to [[necessity and possibility]] of classical modal logic ([above](#ClassicalModalLogic)) may be expressed in quantum modal logic by:

\begin{imagefromfile}
    "file_name": "DefinitelyRandomlyViaPossiblyNecessarily.jpg",
    "width": "210",
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Considering the basic dependent linear type

$$
  \mathbb{C}_\bullet \;\coloneqq\; (p_B)^\ast \mathbb{C}
$$
$$
  b \colon B 
  \;\;\;\vdash\;\;\;
  \mathbb{C} \;\colon\; LinType
$$

(which is the [[tensor unit]] in $LinType_B$) we may understand 

$$
  \mathscr{H} \;\coloneqq\; \Box_B \mathbb{C}_\bullet
$$

as the [[Hilbert space]] which is spanned by a measurement basis $\vert b \rangle$.

From all this we find, first of all, that 

1. the [[necessity]]-[[counit of a comonad|counit]] exhibits the *[[collapse of the wavefunction|collapse]]* of [[quantum states]] under a [[quantum measurement]] in the $B$-basis

1. the [[possibility]]-[[unit of a monad|unit]] exhibits the condition quantum state preparation in this basis:

\begin{imagefromfile}
    "file_name": "QCwthLHT-QuantumNecessity-221021.jpg",
    "width": "900",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\begin{remark}
  The [[collapse of the wavefunction|collapse]]-principle of [[quantum measurement]] accurately expressed by the above linear [[necessity]]$\to$actuality$\to$[[possibility]] map was maybe first highlighted and made explicit in [von Neumann (1932), §III.3](wave+function+collapse#vonNeumann32), at least for the special case that (in our notation here) $\mathscr{H}_\bullet \,=\, (p_B)^\ast \mathbb{C}$ (cf. [Lüders (1951)](wave+function+collapse#Lüders51)).
\end{remark}

\begin{remark}
We see that the base type $B$ (eq:FiniteBaseType) *of [[quantum measurement]] outcomes* plays the role of *both*

1. the *[[possible worlds semantics|possible worlds]]* of [[modal logic|classical modal logicians]];

1. the *[[many-worlds interpretation of quantum mechanics|many worlds]]* of [[interpretation of quantum mechanics|quantum interpretationists]].

\end{remark}

(...)


## Related concepts

* [[modal logic]], [[modal type theory]]

* [[epistemic modal logic]]

## References

Discussion of [[modal logic]] of necessity and possibility goes back to [[Aristotle]], as nicely reviewed in

* {#LemmonScott77} [[E. John Lemmon]] with [[Dana Scott]], pp 1-12 of: *An Introduction to Modal Logic -- The "Lemmon Notes"*, B. Blackwell (1977) &lbrack;[ark:/13960/t3gz25k3h](https://archive.org/details/introductiontomo0000lemm/)&rbrack;

In 

* [[Kant]], _Critique of pure reason_ 1781

is discussion of _modality_ as one of the [[category (philosophy)|categories of pure thought]], with sub-categories _necessity_, _possibility_ and _actuality_ (Wirklichkeit).

In 

* [[Georg Hegel]], [book 2, section 3](http://ncatlab.org/nlab/show/Science+of+Logic#DieWirklichkeit), especially [book 2, section 3, chapter 2](http://ncatlab.org/nlab/show/Science+of+Logic#DieWirklichkeitKapitel2) in  _[[Science of Logic]]_ (1812)

this is picked up and claimed to be refined to a [[dialectic]] system of [[unity of opposites|unities of opposites]].

Early discussion in the context of [[alethic modal logic]]:

* {#Wright51} [[Georg H. von Wright]], *An Essay in Modal Logic*, North-Holland Publishing (1951)

See also:

* {#Kripke80} [[Saul Kripke]], _[[Naming and Necessity]]_ (1980)

* Stanford Encyclopedia of Philosophy, _[Modal Logic](http://plato.stanford.edu/entries/logic-modal/#PosWorSem)_

Making explicit the [[necessity]] [[modal operator]] as a [[comonad]]:

* {#BiermanDePaiva96} [[Gavin M. Bierman]], [[Valeria de Paiva]], *Intuitionistic necessity revisited*, School of Computer Science research reports-University of Birmingham CSR (1996) &lbrack;[researchgate](https://www.researchgate.net/publication/2810611_Intuitionistic_Necessity_Revisited), [[Bierman-dePaiva-NecessityRevisited.pdf:file]]&rbrack;

* {#BiermanDePaiva00} [[Gavin M. Bierman]], [[Valeria de Paiva]], *On an Intuitionistic Modal Logic*, Studia Logica **65** (2000) 383–416 &lbrack;[doi:10.1023/A:1005291931660](https://doi.org/10.1023/A:1005291931660), [pdf] (https://www.researchgate.net/profile/Valeria-De-Paiva/publication/226515897_On_An_Intuitionistic_Modal_Logic/links/00b4951ed416906ccc000000/On-An-Intuitionistic-Modal-Logic.pdf)&rbrack;

* {#Kobayashi97} [[Satoshi Kobayashi]], *Monad as modality*, Theoretical Computer Science **175** 1 (1997) 29-74 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(96)00169-7">doi:10.1016/S0304-3975(96)00169-7</a>&rbrack;

* Natasha Alechina, Michael Mendler, [[Valeria de Paiva]], Eike Ritter: *Categorical and Kripke Semantics for Constructive S4 Modal Logic*, in *Computer Science Logic. CSL 2001* Lecture Notes in Computer Science **2142**, Springer (2001) 292 &lbrack;[doi:10.1007/3-540-44802-0_21](https://doi.org/10.1007/3-540-44802-0_21)&rbrack;


The understanding of [[Kripke semantics]] for [[S5 modal logic]] as [[base change]] is indicated in:

* {#Awodey06} [[Steve Awodey]], p. 279 in: *Category theory*, Oxford University Press (2006, 2010) &lbrack;[doi:10.1093/acprof:oso/9780198568612.001.0001](https://doi.org/10.1093/acprof:oso/9780198568612.001.0001), [ISBN:9780199237180](https://global.oup.com/ukhe/product/category-theory-9780199237180), [pdf](http://englishonlineclub.com/pdf/Category%20Teory%20%5BEnglishOnlineClub.com%5D.pdf)&rbrack;

* [[David Corfield]], Chap. 4 of: _[Modal Homotopy Type Theory: The Prospect of a New Logic for Philosophy](https://ncatlab.org/davidcorfield/show/Modal+Homotopy+Type+Theory)_ (2020)

See also:

* [[Jake Chandler]], _Modality: Necessity and Possibility_, lecture notes ([pdf](http://www.jakechandler.com/assets/2006MetaphysicsBBK/%5B6%5D%20%5BModality%5D.pdf))



* {#Simpson} [[Alex Simpson]], _The Proof Theory and Semantics of Intuitionistic Modal Logic_, Ph.D. Thesis, University of Edinburgh, 1994, [web](http://homepages.inf.ed.ac.uk/als/Research/thesis.pdf).

* {#IEPCarnapModal} Internet Encyclopedia of Philosophy, _[Rudolf Carnap: Modal Logic](http://www.iep.utm.edu/cmlogic/)_

[[!redirects necessity]]
[[!redirects possibility]]

[[!redirects necesecarily]]
[[!redirects possibly]]

[[!redirects definiteness and randomness]]

[[!redirects alethic modal logic]]
[[!redirects alethic modality]]

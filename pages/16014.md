
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

In the context of [[modal logic]], two key [[modalities]] that one wants to consider are those of _necessity_ and _possibility_.

The idea is to consider for any [[proposition]] $p$ 

* a proposition labeled $\Box p$ expressing the idea that "$p$ is necessarily true";

* a proposition labeled $\lozenge p$ expressing the idea that "$p$ is possibly true".

## The S4 axioms

For every comonadic [[modality]] $\Box$, one typically demands that it preserves implication, in the sense that

$$\Box(p \to q) \to (\Box p \to \Box q).$$

This preservation of implication is called the [[K modal logic|K-axiom]].  In traditional non-[[categorical logic]] this is often all that is considered, because in traditional classical modal logic, the operators are considered dual, i.e. $\Box A= \neg (\lozenge (\neg A))$.  In an intuitionistic modal logic, one would also demand that $\lozenge$ preserves implication in a suitable sense, such as 

$$\Box(p\to q) \to (\lozenge p \to \lozenge q).$$

One may also ask for a further compatibility such as $(\lozenge p \to \Box q) \to \Box(p\to q)$, as [Simpson](#Simpson) does.

Similarly, the axiom $\Box(p \to q) \to (\Box p \to \Box q)$ implies that $\Box$ preserves conjunctions, i.e. $\Box(p\wedge q) \leftrightarrow (\Box p \wedge \Box q)$.  The nullary version $\Box(\top)\leftrightarrow \top$ follows from the "necessitation rule" which says that if $p$ is provable in the empty context, then so is $\Box p$.  (This is an additional rule assumed in modal logics.)  From duality, $\Box A= \neg (\lozenge (\neg A))$ it follows that $\lozenge$ preserves disjunctions (both binary and nullary), while intuitionistically one may want to ask for this separately ([Simpson](#Simpson) does, but [Biermann and de Paiva](#BiermanPaiva92) don't).

A minimum further requirement on a formalization of $\Box$ and $\lozenge$ to have the interpretation of "necessity" and "possibility" is arguably that there are [[implications]]

* $\Box p \rightarrow p$;

* $p \rightarrow \lozenge p$,

expressing that if something is necessarily true, then that should mean that it is true in all instances, and that if something is true in one instance, then it is evidently possible for it to be true.  With these additions to the above [[K modal logic]], one speaks of [[T modal logic]].

By similar plausibility arguments one often demands that

* $\Box p \to \Box \Box p$

* $\lozenge \lozenge p \to \lozenge p$

which may be read as expressing that iterating the previous reasoning does not yield any new insight.  This additional enhancement to T modal logic yields _[[S4 modal logic]]_. 

### The generality of S4 

In terms of [[categorical logic]] interpreting propositional logic into a [[Heyting algebra]], the S4 axioms just say ([Bierman & de Paiva 92](#BiermanPaiva92)) that 

* $\Box$ is a (necessarily [[idempotent comonad|idempotent]]) [[comonad]] which is [[monoidal functor|monoidal]], hence product-preserving; and

* $\lozenge$ is a (necessarily [[idempotent monad|idempotent]]) [[monad]] which is a "$\Box$-[[strong functor|strong]] functor", and (perhaps) preserves coproducts.

As usual, we can also replace the Heyting algebra by a [[cartesian closed category]], thereby obtaining a "proof-relevant" system; in this case monoidality of $\Box$ doesn't imply directly that it preserves products, although one might reasonably ask that it does.  See _[[monad in computer science]]_.

The above reasoning makes plausible that any operators expressing "necessity" and "possibility" should *at least* satisfy these (co)monad axioms.  However, not every (co)monad is sensibly interpreted this way.

For example, there is

* the (idempotent) comonad $\emptyset$ which sends every proposition to [[false]] (the [[nothing|non-being]]-modality);

* the (idempotent) monad $\ast$ which sends every proposition to [[true]] (the [[being]]-modality).

These $\emptyset \dashv \ast$ satisfy all of the above axioms (as well as more axioms that are being considered, such as those called [[S5 modal logic]]) but they are not a very good interpretation of the informal concepts of "possibility" and "necessity".  Under this interpretation nothing is necessarily true, and everything is possibly true.  While this is not nonsensical, it is not very interesting and doesn't correspond well to our intuitive meanings of "necessary" and "possible".

This issue becomes more pronounced as one generalizes from the small realm of [[propositional logic]] to include both or either of:

* [[types]] more general than [[propositions]] (in [[modal type theory]]);

* [[first-order logic]] with [[quantifiers]], hence [[hyperdoctrines]]/[[dependent types]].

There are many [[modal operators]] in such contexts which are all modeled by (idempotent) (co)monads but which do not have the interpretation of expressing the modes of "necessity" or "possibility". See at _[[modal operator]]_ for some examples.

Therefore it makes sense to ask which _additional_ axioms on a modal operator make it an accurate formalization of the informal concepts of necessity and possibility.  The answer to this may depend on context and intention (after all one is trying to find a precise formulation of an a priori informal idea).


## Possible worlds via first-order logic and type theory
 {#InFirstOrderLogicAndTypeTheory}

One common philosophical interpretation of "necessarily" and "possibly" is in terms of a collection of "possible worlds" that are similar to the "real world", but not the same.  Under this interpretation, a proposition is necessarily true if it is true in all possible worlds, and possibly true if it is true in some possible world.

Now the idea of a proposition being true "necessarily in all possible cases" or "possibly at least in one case" is formally very well established in *predicate* logic: it is just the interpretation of the [[universal quantifier]] "for all" $\forall$ and of the [[existential quantifier]] "there exists" $\exists$.  In [[categorical logic]], these [[quantifiers]] (see there for details) are part of an [[adjoint triple]] whose middle piece is [[context]] extension, and as such they naturally induce a [[comonad]] and a [[monad]].  Thus, if we interpret "necessarily" and "possibly" in terms of possible worlds, we can model them by this [[base change]] [[adjoint triple]].

### Globally

In more detail, let $W$ be the [[context]] [[type]] of [[variables]]/[[terms]] on which the propositions depend, i.e. the collection "of all [[possible worlds semantics|possible worlds]]".  Any specific choice of $W$ may be taken as specifying what is to be understood as a "possible world".

Writing $\mathbf{H}_{\ast}$ for the [[category]] of all context-free [[types]] under consideration and writing $\mathbf{H}_{/W}$ for the category of types in [[context]] "$W$", then in [[categorical logic]] (for instance $\mathbf{H}_{/(-)}$ might be a [[hyperdoctrine]] over a [[category of contexts]] containing objects $W$ and $\ast$) the [[quantifiers]] $\forall_{x\colon X}$ and $\exists_{x\colon X}$ participate in a [[base change]] [[adjoint triple]] 

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

$$
  (\underset{W}{\lozenge} \dashv \underset{W}{\Box})
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
$$

With this, if $p\in \mathbf{H}_{/W}$ is a [[proposition]] about terms $w$ of $W$ (a $W$-[[dependent type]]) then 

* $\underset{W}{\lozenge}(p)$ is [[true]]/[[inhabited type|inhabited]] precisely if $\underset{w \colon W}{\exists} p(w)$ is [[true]]/[[inhabited type|inhabited]], hence (that is the standard interpretation of the [[quantifier]]) if it is possible for $p(w)$ to be true for some $w$;

* $\underset{W}{\Box}(p)$ is [[true]]/[[inhabited type|inhabited]] precisely if $\underset{w \colon W}{\forall} p(w)$ is [[true]]/[[inhabited type|inhabited]], hence (that is again the standard interpretation of the quantifier) if $p(w)$ necessarily holds for all $w$.

(Note that there is also an adjoint pair on $\mathbf{H}_{/\ast}$ in which the left adjoint is given by context extension back to $\mathbf{H}_{/W}$ followed by $\exists_W$, and dually the right adjoint is given by $W^\ast$ followed by $\forall_W$. The former is the [[writer comonad]], whereas the latter is the [[function monad]] (or reader monad).)

Thus, this gives one [[syntax|syntactic]] formalization of the informal meaning of "necessity" and "possibility".  The natural [[semantics]] for these [[base change]] operations is a generalization of the simple traditional _[[possible worlds semantics]]_ of propositional necessity and possibility modalities.  (There are, however, more complicated possible worlds semantics.)

Moreover, with this formalization, the modal operator $\underset{W}{\lozenge}$ is [[left adjoint]] to $\underset{W}{\Box}$ and hence both form an [[adjoint modality]]. As discussed there, this is a formalization of [[unity of opposites|opposite]] concepts, which reflects well the opposition of necessity and possibility in their informal meaning.


Some technical remarks:

1. In general, $\underset{W}{\lozenge}$ and $\underset{W}{\Box}$ as defined above are, while being a [[monad]] and [[comonad]], respectively, not an [[idempotent monad]] and [[idempotent comonad]] if generalized from [[first-order hyperdoctrines]] to more general [[dependent type theories]]. But this just reflects the usual issues with [[propositions as types]], see there for more discussion.

1. While [[base change]]-[[adjunctions]] are essentially unique and not free to choose, there is a genuine choice in the above given by the choice of [[context]] $W$. This is reflected in the subscripts of $\underset{W}{\lozenge}$ and $\underset{W}{\Box}$ above. It is the choice of this $W$ that gives different kinds of possibility and necessity. More generally there is in fact not just a choice of a context, but of a morphism of contexts, reflecting what is often called "accessibility of possible worlds". This we come to [below](#ViaBaseChangeRelatively).

### Relatively
  {#ViaBaseChangeRelatively}

With this axiomatization via [[base change]], it is immediate to consider the relative case where instead of [[base change]] to a [[unit type]] $W \to \ast$ one considers [[base change]] 

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

and set

$$
  (\underset{\omega}{\lozenge} \dashv \underset{\omega}{\Box})
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

If here $\omega$ is an [[effective epimorphism]] (a [[1-epimorphism]]) then it exibits an [[equivalence relation]] on $W$, where $w_1\sim w_2$ is given by $\omega(w_1) = \omega(w_2)$. In traditional [[possible worlds semantics]] such equivalence relation is called an "accessibility relation between possible worlds". Now 

*  $\underset{\omega}{\lozenge} p$ is true/inhabited at $w\in W$ iff it is true/inhabited at at least one $\tilde w$ in the same equivalence class of $w$;

*  $\underset{\omega}{\Box} p$ is true/inhabited at $w\in W$ iff it is true/inhabited at all $\tilde w$ in the same equivalence classes of $w$.

### Examples
 {#Examples}

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

However, if we assume that there is one $w$ for which indeed $NumberOfPlanetsInTheSolarSystem(w)$ takes the value 9, then the [[dependent sum]] over the dependent identity type contains that coincidence as a term, and so $\lozenge_W$ of our dependent identity type is [[inhabited type|inhabited]]. Hence

* $[\lozenge_W (9 = NumberOfPlanetsInTheSolarSystem)]$ is [[true]].

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



## Related concepts

* [[modal logic]], [[modal type theory]]


## References

In 

* [[Kant]], _Critique of pure reason_ 1781

is discussion of _modality_ as one of the [[category (philosophy)|categories of pure thought]], with sub-categories _necessity_, _possibility_ and _actuality_ (Wirklichkeit).

In 

* [[Georg Hegel]], [book 2, section 3](http://ncatlab.org/nlab/show/Science+of+Logic#DieWirklichkeit), especially [book 2, section 3, chapter 2](http://ncatlab.org/nlab/show/Science+of+Logic#DieWirklichkeitKapitel2) in  _[[Science of Logic]]_ (1812)

this is picked up and claimed to be refined to a [[dialectic]] system of [[unity of opposites|unities of opposites]].

* {#Kripke80} [[Saul Kripke]], _[[Naming and Necessity]]_ (1980)

* Stanford Encyclopedia of Philosophy, _[Modal Logic](http://plato.stanford.edu/entries/logic-modal/#PosWorSem)_

* [[Jake Chandler]], _Modality: Necessity and Possibility_, lecture notes ([pdf](http://www.jakechandler.com/assets/2006MetaphysicsBBK/%5B6%5D%20%5BModality%5D.pdf))

* {#BiermanPaiva92} Gavin Bierman and [[Valeria de Paiva]], _On an Intuitionistic Modal Logic_, Studia Logica (65):383-416, 2000 (preprint from 1992) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.30.5279))

* {#Simpson} Alex K. Simpson, _The Proof Theory and Semantics of Intuitionistic Modal Logic_, Ph.D. Thesis, University of Edinburgh, 1994, [web](http://homepages.inf.ed.ac.uk/als/Research/thesis.pdf).

* {#IEPCarnapModal} Internet Encyclopedia of Philosophy, _[Rudolf Carnap: Modal Logic](http://www.iep.utm.edu/cmlogic/)_

[[!redirects necessity]]
[[!redirects possibility]]

[[!redirects necesecarily]]
[[!redirects possibly]]
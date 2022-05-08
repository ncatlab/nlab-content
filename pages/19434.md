

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea

The concept of a **Yoneda structure** provides in a general 2-categorical setting the axiomatic description of the formal properties of the usual [[category of presheaves|presheaf construction]] and [[Yoneda embedding]] of ([[locally small category|locally]]) [[small category|small categories]]. The size issues arising in that context are absorbed directly into the structure via a class of (locally) "small" maps. 

## Preliminaries

The axioms of a Yoneda structure are out to capture the properties of the presheaf construction with [[CAT]] replaced by general 2-category $\mathcal{K}$. In order to handle size issues a class of "legitimate" or "admissible" 0-cells is singled out in $|\mathcal{K}|$ as well as a class of 1-cells that behave well with respect to this class and the presheaf construction. In fact, it suffices to describe the admissible 1-cells since one can then identify the admissible 0-cells with the admissible identity 1-cells.

In $CAT$ relative to the usual presheaf construction one should think of the [[locally small category|locally small categories]] as the admissible 0-cells i.e. those categories $\mathcal{C}$ with all Hom-sets $\mathcal{C}(x,y)$ contained in a category $Set$ of "small" sets itself contained as object in a larger [[Grothendieck universe]] $U_0$. In this setting admissible functors $f:\mathcal{A}\to\mathcal{B}$ are those with all relative Hom-sets $\mathcal{B}(f(a),b)\in Set$. Furthermore, one can show ([Freyd-Street 1995](FS95)) that _a category_ $\mathcal{C}\in CAT$ _is small_ i.e. $|\mathcal{C}|\in Set$ precisely if $\mathcal{C}$ and $Set^{\mathcal{C}^{op}}$ _are locally small_.

Admissible functors $f$ in this sense in $CAT$ are closed under precomposition not only among themselves but with respect to arbitrary (composable) $g$ since the relative Hom-sets $\mathcal{B}(f{}g(x),b)$ are simply a subclass of $\mathcal{B}(f(a),b)$ namely those for which $a\in im(g)$. Whence these "relatively small" functors form a [[right ideal]]. Given the close connection between [[KZ doctrines]] and Yoneda structures it will nevertheless be useful to consider the more general case of closure in itself under composition as well, a situation which we acknowledge terminologically with the prefix "proto".

+-- {: .num_defn #admissible_1cell}
###### Definition 
Let $\mathcal{K}$ be a [[2-category]] and $\mathbb{A}$ be a class of 1-cells. The 1-cells $f\in \mathbb{A}$ (and by abuse, the class $\mathbb{A}$ as well) are called _admissible_ if for all $f\in \mathbb{A}$ and composable 1-cells $g\in \mathcal{K}$,  $f\circ g\in \mathbb{A}$. $f\in \mathbb{A}$ and $\mathbb{A}$ are called _proto-admissible_ if this closure property holds for $g\in \mathbb{A}$.
=--

+-- {: .num_defn #admissible_0cell}
###### Definition 
Let $\mathcal{K}$ be a [[2-category]] and $\mathbb{A}$ be an admissible (resp. proto-admissible) class of 1-cells. A 0-cell $C\in |\mathcal{K}|$ is called _admissible_ (resp. _proto-admissible_) if $id_C$ is admissible (resp. proto-admissible). We denote the corresponding class of 0-cells by $|\mathbb{A}|$.
=--

For admissible $\mathbb{A}$, $C\in|\mathbb{A}|$ iff all 1-cells with codomain $C$ are admissible. This formulation has the advantage that it makes sense for [[semi-category|semi-categories]] as well.

Having now "taken care" of the size issues we recall/introduce some terminology concerning [[Kan extensions]] and [[relative adjoint functor|relative adjoint functors]] that will prove effective in yielding a surprisingly concise axiomatic description of the presheaf construction.

+-- {: .num_defn #left_extension}
###### Definition 
Let $\mathcal{K}$ be a [[2-category]] and $\eta:f\Rightarrow e\circ g$ be a 2-cell:
$$
  \array{
     A& & \overset{f}{\longrightarrow} & &B
     \\
     &{}_g\searrow & \Downarrow _\eta& \nearrow _e&
     \\
      & & C & &
  }
$$
We say that $\eta$ (or, by abuse, the diagram) exhibits $e:C\to B$ as a _left extension_ of $f:A\to B$ _along_ $g:A\to C$ if for all parallel maps $k:C\to B$ pasting with $\eta$ induces a bijection between 2-cells $\sigma:e\Rightarrow k$ and 2-cells $f\Rightarrow k\circ g$.

We say that a 1-cell $h:B\to D$ _preserves_ this left extension if the following diagram exhibits $h\circ e$ as a left extension of $h\circ f$ along $g$ :

$$
  \array{ &     &D    & &
     \\

      &{}^{h{}f}{\nearrow}&\seArrow^{id} &{\nwarrow}^h&
     \\
     A& & \overset{f}{\longrightarrow} & &B
     \\
     &{}_g\searrow & \Downarrow _\eta& \nearrow _e&
     \\
      & & C & &
  }
$$
The left extension is called _absolute_ if it is preserved by all 1-cells with domain $B$.
=--

+-- {: .num_defn #left_lifting}
###### Definition 
Let $\phi:f\Rightarrow g\circ l$ be a 2-cell:

$$
  \array{
      
     A& & \overset{l}{\longrightarrow} & &C
     \\
     &{}_f\searrow & \neArrow _\phi& \swarrow _g&
     \\
      & & B & &
  }
$$

We say that $\phi$ (or, by abuse, the diagram) exhibits $l:A\to C$ as a _left lifting_ of $f:A\to B$ _through_ $g:C\to B$ iff for all parallel maps $k:A\to C$ pasting with $\phi$ induces a bijection between 2-cells $\sigma:l\Rightarrow k$ and 2-cells $f\Rightarrow g\circ k$.

We say that a 1-cell $j:D\to A$ preserves this left lifting if the following diagram exhibits $l\circ j$ as a left lifting of $f\circ j$ through $g$ :

$$
  \array{
     D &\overset{j}{\longrightarrow} & A& \overset{l}{\longrightarrow}  &C
     \\
     &{}_{f{}j}\searrow{}^{id}{\neArrow} &{}_f\downarrow & \overset{\phi}{\Rightarrow} \swarrow_g & 
     \\
      & & B & & 
  }
$$

We say that the left lifting is _absolute_ if it is preserved by all 1-cells with codomain $A$.

=--

+-- {: .num_example #fully_faithfull}
###### Example 
The following diagram 

$$
  \array{
      
     A& & \overset{id_A}{\longrightarrow} & &A
     \\
     &{}_f\searrow & \neArrow _{id}& \swarrow _f&
     \\
      & & B & &
  }
$$
exhibits $id_A$ as an absolute left lifting of $f:A\to B$ through itself iff $f:A\to B$ is _representably fully-faithful_ i.e. the functor "postcomposition with $f$" $\mathcal{K}(X,f):\mathcal{K}(X,A)\to\mathcal{K}(X,B)$ is fully-faithful for all $X\in|\mathcal{K}|$. This holds since the Hom-set $Hom_{\mathcal{K}(X,A)}(k,g)$ is precisely the set of 2-cells $k\Rightarrow g$ and $\mathcal{K}(X,f)$ acts on them by pasting with $id_f$.

=--


+-- {: .num_example #adjunction}
###### Example
The following diagram 

$$
  \array{
      
     B& & \overset{g}{\longrightarrow} & &A
     \\
     &{}_{id_B}\searrow & \neArrow _\eta& \swarrow _f&
     \\
      & & B & &
  }
$$
exhibits $g$ as an absolute left lifting of $id_B$ through $f$ iff there exists a 2-cell 
$$
  \array{
      
     A& & \overset{id_A}{\longrightarrow} & &A
     \\
&{}_{f}\searrow & \Uparrow _\epsilon& \nearrow _g&
     \\
      & & B & &
  }
$$
such that the pasting of $\epsilon$ on $\eta$ at $g$
$$
  \array{
    & &A & &
     \\
&{}_{f}\swarrow & \neArrow _\epsilon& \searrow _{id_A}&
     \\   
     B& & \overset{g}{\longrightarrow} & &A
     \\
     &{}_{id_B}\searrow & \neArrow _\eta& \swarrow _f&
     \\
      & & B & &
  }
$$
and the pasting of $\epsilon$ on $\eta$ at $f$
$$
  \array{
     B &\overset{g}{\longrightarrow} & A& \overset{id_A}{\longrightarrow}  &A
     \\
     &{}_{id_B}\searrow{}^{\eta}{\neArrow} &{}_f\downarrow & \overset{\epsilon}{\neArrow} \nearrow_g & 
     \\
      & & B & & 
  }
$$

yield identity 2-cells.

Of course, this situation expresses an **adjunction** $g\dashv f$ with _unit_ $\eta$ and _counit_ $\epsilon$.  Here the absolute left lifting property of $\eta$ is furthermore equivalent to the left lifting property of $\eta$ plus preservation by $f:A\to B$ (cf. [Street-Walters 1978](#SW78), prop.2).

=--

## Definition

We are now ready to give the definition of a Yoneda structure:

+-- {: .num_defn #yoneda_structure}
###### Definition 
Let $\mathcal{K}$ be a [[2-category]] and $\mathbb{A}$ be an admissible class of 1-cells.

A _presheaf construction_ $\mathcal{P}$ for $\mathbb{A}$ assigns to every admissible object $A\in |\mathbb{A}|$ an object $\mathcal{P}A\in |\mathcal{K}|$ called its _object of presheaves_ and an admissible 1-cell $y_A:A\to\mathcal{P}A$ called its _Yoneda morphism_ subject to the following conditions:

* (**YS1**) For each admissible 1-cell $f:A\to B$ with admissible domain $A\in |\mathbb{A}|$ there is given a 2-cell $\chi_f:y_A\Rightarrow e_f\circ f$ such that the following diagram

$$
  \array{
     A& & \overset{f}{\longrightarrow} & &B
     \\
     &{}_{y_A}\searrow & {}^{\chi_f}\neArrow& \swarrow _{e_f}&
     \\
      & & \mathcal{P}A & &
  }
$$
exhibits $f$ as an absolute left lifting of $y_A$ through $e_f$ and $e_f$ as a left extension of $y_A$ along $f$.

* (**YS2**) For all $A\in|\mathbb{A}|$, $id_{\mathcal{P}A}$ is the left extension of $y_A$ along itself as exhibited in

$$
  \array{
     A& & \overset{y_A}{\longrightarrow} & &\mathcal{P}A
     \\
     &{}_{y_A}\searrow & \Downarrow _{id}& \nearrow _{id_{\mathcal{P}A}}&
     \\
      & & \mathcal{P}A & &
  }
$$

* (**YS3**) For all $i:A\to B$, $j:B\to C$ such that $A,B\in |\mathbb{A}|$ and $i,j\in\mathbb{A}$ the following diagram

$$
  \array{
   A &\overset{i}{\rightarrow}& B& \overset{j}{\rightarrow} & C
  \\
  {}_{y_A}\downarrow &\overset{\chi_{{y_B}\circ i}}{\Rightarrow}&\downarrow_{y_B}&\overset{\chi_j}{\Rightarrow}\swarrow &{}_{e_j}
  \\
  \mathcal{P}A&\underset{e_{y_B\circ i}}{\leftarrow} &\mathcal{P}B& &
  }
$$

exhibits $e_{{y_B}i}\circ e_j$ as the left extension of $y_A$ along $j\circ i$.


The pair $(\mathbb{A},\mathcal{P})$ is called a **Yoneda structure** on the 2-category $\mathcal{K}$.
=--

We desisted from tracking the prefix 'proto' through the foregoing but it should clear that a _proto-Yoneda structure_ results from replacing 'admissible' by 'proto-admissible' throughout the definition. Indeed, in (YS3) the assumption that $i\in\mathbb{A}$ was made in proviso for the case of proto-admissible 1-cells (cf. [Walker 2017](#Walker17)) since in presence of the right ideal property this already follows from the admissibility of $id_B$.

In cases where we need to keep track of from which (proto-)Yoneda structure the various structural 1- and 2-cells come from we will use the presheaf construction as a superscript for disambiguation: for (proto-)Yoneda structure $(\mathbb{A},\mathcal{P})$ we write $y_A^\mathcal{P}$ and $\chi_f^{\mathcal{P}}$ etc.

In Street-Walters ([1978](#SW78)) a stronger axiom (YS2') is also considered:

* (**YS2'**) If the following diagram

$$
  \array{
     A& & \overset{f}{\longrightarrow} & B&
     \\
     &{}_{y_A}\searrow & \overset{\chi_f}{\Rightarrow}& \swarrow \overset{\sigma}{\Rightarrow}\swarrow_g
     \\
      & & \mathcal{P}A & &
  }
$$
exhibits $f$ as an absolute left lifting of $y_A$ through $g$ then $\sigma:e_f\Rightarrow g$ is an isomorphism.

It is shown there (prop.11) that (YS1) and (YS2') imply (YS2) and (YS3).

Together with a finite-completeness assumption on $\mathcal{K}$ and pointwiseness of the left extensions the resulting Yoneda structures are called **good** in Weber ([2007](#Weber07)) where it is also shown that Yoneda structures arising from presheaf constructions of the form $\mathcal{P}({}_-) = [({}_-)^{op},\Omega]$ have this property, $\Omega$ being an abstract "object of small sets" in a cartesian closed 2-category $\mathcal{K}$ with an involution $({}_-)^{op}$.

## Properties

....

## Examples

* The primordial example is $CAT$ with $\mathcal{P}:C\mapsto Set^{C^{op}}$ with $y_C:a\mapsto Hom_C({}_-,a)$ , the Yoneda embedding. A functor $f:C\to D$ is admissible if the relative $Hom_D(f{}_-,{}_-):D\to SET^{C^{op}}$ factors through $Set^{C^{op}}$. Admissible categories are precisely the locally small categories.



## The relation to KZ doctrines{#extension_KZ-doctrine}

Whereas it was shown already in the 1970s that ordinary monads on a 1-category can be brought into an [[extension system|extension form]] that avoids the iteration of the endofunctor similar presentations for 2-dimensional monad theory evolved more recently. For the comparison of [[lax-idempotent 2-monad|lax-idempotent 2-monads]] aka _KZ doctrines_ to Yoneda structures such presentations provided in the work of Marmolejo and Wood ([2012](#MW12)) come in handy. The link to Yoneda structures has been made in Walker ([2017](#Walker17)).

+-- {: .num_defn #KZ_doctrine}
###### Definition
Let $\mathcal{K}$ be a [[2-category]]. A _KZ-doctrine (in extension form)_ on $\mathcal{K}$ is a pair $(P,y)$ where $P$ assigns to every 0-cell $A\in\mathcal{K}$ a 0-cell $P(A)\in\mathcal{K}$ and $y$ is a family of 1-cells $y_A:A\to P(A)$ indexed by the 0-cells $A\in\mathcal{K}$ such that

* For every pair of 0-cells $A$, $B$ and 1-cells $f:A\to P(B)$ there exists an invertible 2-cell $\epsilon_f$

$$
  \array{
     A& & \overset{f}{\longrightarrow} & &P(B)
     \\
     &{}_{y_A}\searrow & \Downarrow _{\epsilon_f}& \nearrow _\overline{f}&
     \\
      & & P(A) & &
  }
$$

that exhibits $\overline{f}$ as left extension of $f$ along $y_A$. Furthermore, in case $B=A$ and $f=y_A$ then $\epsilon_{y_A}$ is given by the identity 2-cell $id_{y_A}:y_A\Rightarrow id_{P(A)}\circ y_A$.

* For any 1-cell $g:B\to P(C)$, the 1-cell $\overline{g}:P(B)\to P(C)$ given itself by the left extension along $y_B$ preserves the left extension of $f:A\to B$ along $y_A$ exhibited by $\epsilon_f$.
=--

Clearly, with $(P,y)$ the presheaf construction of a Yoneda structure comes into sight though we still need to define a suitable class of admissible maps from $(P,y)$.

But before we do this we will introduce the concept that corresponds to the familiar notion of a pseudoalgebra for a lax-idempotent 2-monad thereby hopefully making it plausible that $(P,y)$ indeed is equivalent to the usual algebraic concept.

The main idea of the following definition is that the "pseudoalgebras" $X\in|\mathcal{K}|$ mimic the extension properties of the $P(A)$, in particular, all $P(A)$ satisfy the condition trivially and should be thought of as free algebras.

+-- {: .num_defn #P-complete}
###### Definition
Given a KZ-doctrine $(P,y)$ on $\mathcal{K}$. A 0-cell $X\in|\mathcal{K}|$ is called _P-cocomplete_ if for every $g:B\to X$ there exists an invertible 2-cell $\epsilon_g$

$$
  \array{
     B& & \overset{g}{\longrightarrow} & &X
     \\
     &{}_{y_B}\searrow & \Downarrow _{\epsilon_g}& \nearrow _\overline{g}&
     \\
      & & P(B) & &
  }
$$
that exhibits $\overline{g}$ as left extension of $g$ along $y_B$. Moreover, this left extension $\overline{g}:P(B)\to X$ preserves all the left extensions $\overline{f}:P(A)\to P(B)$ along $y_A$ of arbitrary $f:A\to P(B)$.
=--
+-- {: .num_defn #P-cell}
###### Definition
A 1-cell $h:X\to Y$ between two P-cocomplete objects $X$, $Y$ is called a _P-homomorphism_ (, or a _P-cell_) if $h$ preserves the left extension $\overline{f}:P(A)\to X$ along $y_A:A\to P(A)$ for every $f:A\to X$.
=--

+-- {: .num_prop #P-algebra}
###### Proposition
Given a KZ-doctrine $(P,y)$ on $\mathcal{K}$. The following are equivalent:

* $A\in|\mathcal{K}|$ is P-cocomplete;

* $y_A:A\to P(A)$ has a left adjoint with invertible counit;

* $A$ is the underlying object of a pseudoalgebra.

=--

**Proof**.  A combination of results from Bunge-Funk ([1999](#BF99)) and Marmolejo-Wood ([2012](#MW12)). $\qed$

We now attend the problem of defining a class $\mathbb{A}$ of admissible maps for $(P,y)$. 

+-- {: .num_defn #P-admissible}
###### Definition
Given a KZ-doctrine $(P,y)$ on $\mathcal{K}$. A 1-cell $a:B\to C$ is called _P-admissible_ if the left extension of $y_B:B\to P(B)$ along $a$ exists and moreover is preserved by all left extensions $\overline{h}:P(B)\to X$ along $y_B$ of 1-cells $h:B\to X$ into a P-cocomplete 0-cell $X$.
=--

A crucial property of the Yoneda embedding is of course that is in fact an _embedding_ whence we must demand the same for the units of a KZ-doctrine: 

+-- {: .num_defn #locally_fully_faithful}
###### Definition
A KZ-doctrine $(P,y)$ on a 2-category $\mathcal{K}$ is called _locally fully-faithful_ if all $y_A: A\to P(A)$ are representably fully-faithful (cf. [ex.](#fully_faithful)).
=--

Now we are ready to state the main result of this section.

+-- {: .num_prop #Yoneda_monad}
###### Theorem (Walker)
Let $(P,y)$ be a locally fully-faithful KZ-doctrine on 2-category $\mathcal{K}$ with $\mathbb{A}_P$ the class of P-admissible 1-cells. The pair $(\mathbb{A}_P,P)$ defines a proto-Yoneda structure on $\mathcal{K}$.

=--

**Proof**. cf. Walker ([2017](#Walker17), p.9). $\qed$

Jokingly, we may say that _a general KZ-doctrine is nothing but unfaithful Yoneda-structure without size problems!_ Conversely, the main difference between a locally fully-faithful KZ-doctrine and a Yoneda structure concerns size: For the KZ-doctrine every identity morphism is admissible and, accordingly, its presheaf construction is total whereas this need not be the case for general Yoneda structures. 

## In retrospective

The following is a quote from [[Ross Street|Ross Street's]] "Australian conspectus of higher categories" ([Street 2010](#Street10), p. 241):

>In 1971 Bob Walters and I began work on Yoneda structures on 2-categories $[$[KS1](#KS73)$]$, $[$[StW](#SW78)$]$. The idea was to axiomatize the deeper aspects of categories beyond their merely being algebraic structures. This work centred on the Yoneda embedding $A\to \mathcal{P}A$ of a category $A$ into its presheaf category $\mathcal{P}A =[ A^{op} ,Set]$ . We covered the more general example of categories enriched in a base $\mathcal{V}$ where $\mathcal{P}A = [A^{op} ,\mathcal {V}]$ . Clearly size considerations needed to be taken seriously although a motivating size-free example was preordered sets with $\mathcal{P}A$ the inclusion-ordered set of right order ideals in $A$. Size was just an extra part of the structure. With the advent of elementary topos theory and the stimulation of the work of Anders Kock and Christian Mikkelsen, we showed that the preordered objects in a topos provided a good example. We were happy to realize $[$[KS1](#KS73)$]$ that an elementary topos was precisely a finitely complete category with a _power object_ (that is, a relations classifier). This meant that my work with Walters could be viewed as a higher-dimensional version of topos theory. As usual when raising dimension, what we might mean by a 2-dimensional topos could be many things, several of which could be useful. I looked $[$[St6](#Street74)$]$, $[$[St8](#Street80)$]$ at those special Yoneda structures where $\mathcal{P}A$ classified two-sided discrete fibrations.

## Related entries

* [[Yoneda embedding]]

* [[Yoneda lemma]]

* [[pro-arrow equipment]]

* [[2-topos]]

* [[cosmos]]

* [[relative adjoint functor]]

* [[Kan extension]]

* [[lax-idempotent 2-monad]]

* [[exact square]]

## Link

* n-café seminar blog on the Street-Walters paper: ([link](http://golem.ph.utexas.edu/category/2014/03/an_exegesis_of_yoneda_structur.html))

## References

The original sources are

* {#W71}[[Bob Walters]], _Yoneda 2Categories_ , talk at the University of New South Wales December 1971. ([manuscript](https://dl.dropboxusercontent.com/u/92056191/Archive/temporary_new_material/yoneda.pdf))

* {#KS73}[[Max Kelly]], [[Ross Street]] (eds.), _Abstracts of the Sydney Category Theory Seminar 1972/73_ , Macquarie University.

* {#SW78}[[Ross Street]], [[Bob Walters]], _Yoneda structures on 2-categories_ ,  JPAA **50** (1978) pp.350-379.

Early variations on the theme are in

* {#Street74}[[Ross Street]], _Elementary cosmoi I_ , pp.104-133 in Springer LNM **420** 1974.

* {#Street80}[[Ross Street]], _Cosmoi of internal categories_ , Transactions AMS **258** (1980) pp.271-318.

The Street quote stems from

* {#Street10}[[Ross Street]], _An Australian conspectus of higher categories_ , pp.237-264 in Baez, May (eds.), _Towards Higher Categories_ , Springer Heidelberg 2010. ([draft](http://maths.mq.edu.au/~street/Minneapolis.pdf))

The result on locally small categories suggesting the definition of a small object is reported in

* {#FS95}[[Peter Freyd]], [[Ross Street]], _On the size of categories_ , TAC **1** (1995) pp.174-185. ([abstract](http://www.tac.mta.ca/tac/volumes/1995/n9/1-09abs.html))

Exact squares in Yoneda structures are studied in

* [[René Guitart]], _Relations et carrés exacts_ , Ann. Sc. Math. Québec **IV** no.2 (1980) pp.103-125. ([draft](http://rene.guitart.pagesperso-orange.fr/textespublications/rg42.pdf))

* L. Van den Bril, _Exactitude dans les Yoneda-structures_ , Cah. Top. Géo. Diff. Cat. **XXIII** no.2 (1982) pp.215-224.

The following explores Yoneda structures arising from 2-categories with a discrete-opfibration classifier:

* {#Weber07} [[Mark Weber]], _Yoneda structures from 2-toposes_ , Appl. Cat. Struc. **15** (2007) pp.259-323. ([preprint](https://sites.google.com/site/markwebersmaths/home/yoneda-structures-from-2-toposes))

The following two investigate the connections with KZ doctrines:

* {#Walker17} C. Walker, _Yoneda Structures and KZ Doctrines_ , arXiv:1703.08693 (2017). ([abstract](http://arxiv.org/pdf/1703.08693v3))

* {#Walker18} C. Walker, _Distributive Laws via Admissibility_ , arXiv:1706.09575 (2018). ([abstract](https://arxiv.org/abs/1706.09575))

The interplay of Yoneda structures and KZ doctrines is employed to some effect in

* {#DL18} Ivan Di Liberti, [[Fosco Loregian]], _Accessibility and Presentability in 2-Categories_ , arXiv:1804.08710 (2018). ([abstract](https://arxiv.org/abs/1804.08710))

The pertaining technical ingredients on KZ doctrines are due to the following two papers

* {#BF99} [[Marta Bunge]], [[Jonathon Funk]], _On a bicomma object condition for KZ-doctrines_ , JPAA **143** (1999) pp.69-105.

* {#MW12} Francisco Marmolejo, [[Richard J. Wood]], _Kan extensions and lax idempotent pseudomonads_ , TAC **26** no.1 (2012) pp.1-19. ([abstract](http://www.tac.mta.ca/tac/volumes/26/1/26-01abs.html))

The relation to pro-arrow equipments, the presheaf construction and Isbell duality is discused in

* {#DL19} Ivan Di Liberti, [[Fosco Loregian]], _On the Unicity of Formal Category Theories_ , arXiv:1901.01594 (2019). ([abstract](https://arxiv.org/abs/1901.01594))

[[!redirects yoneda structure]]
[[!redirects Yoneda Structure]]
[[!redirects Yoneda-structure]]
[[!redirects Yoneda structures]]
[[!redirects admissible 1-cell]]


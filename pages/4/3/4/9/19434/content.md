

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

The concept of a **Yoneda structure** provides in a general 2-categorical setting the axiomatic description of the formal properties of the usual presheaf construction and Yoneda embedding of (locally) [[small category|small categories]]. The size issues arising in that context are absorbed directly into the structure via a class of (locally) "small" maps. 

## Preliminaries

The axioms of a Yoneda structure are out to capture the properties of the presheaf construction with [[CAT]] replaced by general 2-category $\mathcal{K}$. In order to handle size issues a class of "legitimate" or "amissible" 0-cells is singled out in $|\mathcal{K}|$ as well as a class of 1-cells that behave well with respect to this class and the presheaf construction. In fact, it suffices to describe the "admissible" 1-cells since one can then identify the admissible 0-cells with the admissible identity 1-cells.

In $CAT$ relative to the usual presheaf construction one should think of the [[locally small category|locally small categories]] as the admissible 0-cells i.e. those categories $\mathcal{C}$ with all Hom-sets $\mathcal{C}(x,y)$ contained in a category $Set$ of "small" sets itself contained in a [[Grothendieck universe]] $U_0$ whereas general 0-cells of $\mathcal{K}$ live in a larger universe $U_1\supset U_0$. In this setting admissible functors $f:\mathcal{A}\to\mathcal{B}$ are those with all relative Hom-sets $\mathcal{B}(f(a),b)\in Set$. Furthermore, one can show ([Freyd-Street 1995](FS95)) that _a category $\mathcal{C}\in CAT$ is small i.e. $|\mathcal{C}|\in Set$ precisely if $\mathcal{C}$ and $Set^{\mathcal{C}^{op}}$ are locally small_.

Admissible functors $f$ in this sense in $CAT$ are closed under precomposition not only among themselves but with respect to arbitrary (composable) $g$ since the relative Hom-sets $\mathcal{B}(f{}g(x),b)$ are simply a subclass of $\mathcal{B}(f(a),b)$ namely those for which $a\in im(g)$. Whence these "relatively small" functors form a [[right ideal]]. Given the close connection between [[KZ doctrines]] and Yoneda structures it will nevertheless be useful to consider the more general case of closure in itself under composition as well, a situation which we acknowledge terminologically with the prefix "proto".

+-- {: .num_defn #admissible_1cell}
###### Definition 
Let $\mathcal{K}$ be a [[2-category]] and $A$ be a class of 1-cells. The 1-cells $f\in A$ (and by abuse, the class $A$ as well) are called _admissible_ if for all $f\in A$ and composable 1-cells $g\in \mathcal{K}$,  $f\circ g\in  A$. $f\in A$ and $A$ are called _proto-admissible_ if this closure property holds for $g\in A$.
=--

+-- {: .num_defn #admissible_0cell}
###### Definition 
Let $\mathcal{K}$ be a [[2-category]] and $A$ be an admissible (resp. proto-admissible) class of 1-cells. A 0-cell $C\in |\mathcal{K}|$ is called _admissible_ (resp. _proto-admissible_) if $id_C$ is admissible (resp. proto-admissible).
=--

Note that the closure properties of $A$ imply that all 1-cells into an admissible (resp. a proto-admissible) 0-cell are admissible (resp. proto-admissible).

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
We say that $\eta$ (or, by abuse, the diagram) exhibits $e:C\to B$ as a _left extension_ of $f:A\to B$ along $g:A\to C$ iff for all parallel maps $k:C\to B$ pasting with $\eta$ induces a bijection between 2-cells $\sigma:e\Rightarrow k$ and 2-cells $f\Rightarrow k\circ g$.

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
We say that $\phi$ (or, by abuse, the diagram) exhibits $l:A\to C$ as a _left lifting_ of $f:A\to B$ along $g:C\to B$ iff for all parallel maps $k:A\to C$ pasting with $\phi$ induces a bijection between 2-cells $\sigma:l\Rightarrow k$ and 2-cells $f\Rightarrow g\circ k$.

We say that a 1-cell $j:D\to A$ preserves this left lifting if the following diagram exhibits $l\circ j$ as a left lifting of $f\circ j$ along $g$ :

$$
  \array{
      &  &D& &
     \\
       &{}^{j}\swarrow &\overset{id}{\Rightarrow}&\searrow^{l{}j}
     \\
     A& & \overset{l}{\longrightarrow} & &C
     \\
     &{}_f\searrow & \neArrow _\phi& \swarrow _g&
     \\
      & & B & &
  }
$$
We say that the left lifting is _absolute_ if it is preserved by all 1-cells with codomain $A$.

=--

## Definition

+-- {: .num_defn #yoneda_structure}
###### Definition 
Let $\mathcal{K}$ be a [[2-category]] and $A$ be an admissible class of 1-cells.

=--

## Properties

....

## Examples

...

## The relation to KZ doctrines

...

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

The following explores Yoneda structure arising from 2-categories with a discrete-opfibration classifier:

* {#Weber07} [[Mark Weber]], _Yoneda structures from 2-toposes_ , Appl. Cat. Struc. **15** (2007) pp.259-323. ([preprint](https://sites.google.com/site/markwebersmaths/home/yoneda-structures-from-2-toposes))

The following two investigate the connections with KZ doctrines:

* {#Walker17} C. Walker, _Yoneda Structures and KZ Doctrines_ , arXiv:1703.08693 (2017). ([abstract](http://arxiv.org/pdf/1703.08693v3))

* {#Walker18} C. Walker, _Distributive Laws via Admissibility_ , arXiv:1706.09575 (2018). ([abstract](https://arxiv.org/abs/1706.09575))

The interplay of Yoneda structures and KZ doctrines is employed to some effect in

* {#DL18} Ivan Di Liberti, [[Fosco Loregian]], _Accessibility and Presentability in 2-Categories_ , arXiv:1804.08710 (2018). ([abstract](https://arxiv.org/abs/1804.08710))


[[!redirects yoneda structure]]
[[!redirects Yoneda Structure]]
[[!redirects Yoneda-structure]]
[[!redirects Yoneda structures]]
[[!redirects admissible 1-cell]]


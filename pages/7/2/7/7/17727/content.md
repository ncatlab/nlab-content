
#Contents#
* table of contents
{:toc}

## Idea

**Synthetic domain theory**, as its name suggests, is a [[synthetic mathematics|synthetic]] axiomatization of [[domain theory]], typically in [[toposes]]. The slogan for synthetic domain theory is that "domains are sets", or more precisely, "domains are certain intuitionistic sets" in that one works in an [[intuitionistic mathematics|intuitionistic]] [[set theory]] with certain anti-classical [[axioms]] and defines a notion of domain internally. These synthetic domains act like the analytic notions in that domains support arbitrary [[fixed points]] and solutions to non-well-founded recursive domain equations.

## Axiomatics

Specific axioms of SDT vary, but a category for synthetic domain theory is typically a [[topos]] equipped with a [[dominance]] $\Sigma$. From this dominance, a $\Sigma$-[[partial map classifier]] can be constructed called the "lift" [[monad]] $L A$. The lift monad has [[initial algebra of an endofunctor|initial and final algebras]] (as a functor, rather than a monad) called $\omega$ and $\overline\omega$ respectively, with an induced [[monomorphism]] $\omega \to \overline \omega$. Then it is required that the induced function $\Sigma^{\overline \omega} \to \Sigma^\omega$ has an [[inverse]]. 

An intuition is that maps out of $\omega$ are a synthetic notion of $\omega$-chains (as in [[CPO|$\omega$-CPOs]]) and maps out of $\overline \omega$ are $\omega$-chains with a limit point. Requiring the inverse above then amounts to requiring that every chain in $\Sigma$ has a *unique* limit point.

## Models

There are two main classes of models of synthetic domain theory: [[realizability toposes]] and [[Grothendieck toposes]].

A Grothendieck topos model that is very closely related to the analytic notion of $\omega$-CPO is given by taking sheaves with respect to the [[canonical topology]] on the full subcategory of $\omega$-CPO whose objects are finite products of $\overline \omega$, i.e., the ordinal $\omega + 1$. This model embeds $\omega$-CPO and the embedding preserves (among other things) limits, coproducts and the [[natural numbers object]]. The $\omega$-CPOs can be characterized as certain $\neg\neg$-separated sheaves.

## Related pages

* [[synthetic guarded domain theory]]
* [[synthetic topology]]
* [[synthetic computability theory]]
* [[Phoa's principle]]

##References

* [[Martin Hyland]], _First Steps in Synthetic Domain Theory_, Category Theory. Lecture Notes in Mathematics, vol 1488 ([pdf](https://www.dpmms.cam.ac.uk/~jmeh1/Research/Oldpapers/synthetic91.pdf))

* [[Marcelo Fiore]] and [[Gordon Plotkin]], _An extension of models of Axiomatic Domain Theory to models of Synthetic Domain Theory_, CSL 1996 ([doi](https://doi.org/10.1007/3-540-63172-0_36))

* [[Marcelo Fiore]] and [[Giuseppe Rosolini]], _The Category of Cpos From a Synthetic Viewpoint_, ENTCS Vol 6, 1997, ([doi](https://doi.org/10.1016/S1571-0661%2805%2980165-3))

* [[Marcelo Fiore]] and [[Giuseppe Rosolini]], _Two models of synthetic domain theory_, Journal of Pure and Applied Algebra, Volume 116, Issues 1–3, 28 March 1997, ([doi](https://doi.org/10.1016/S0022-4049%2896%2900164-8))

On [[synthetic domain theory]] in [[homotopy type theory]]:

* [[Jonathan Sterling]], *Baby steps in higher domain theory*, talk at [Homotopy Type Theory and Computing – Classical and Quantum](https://nyuad.nyu.edu/en/events/2024/april/homotopy-type-theory-and-computing.html), [[Center for Quantum and Topological Systems]] ([video](https://cdnapisec.kaltura.com/html5/html5lib/v2.73.2/mwEmbedFrame.php/p/1674401/uiconf_id/23435151/entry_id/1_b57uwin3?wid=_1674401&iframeembed=true&playerId=kaltura_player&entry_id=1_b57uwin3))

* {#PS25} [[Leoni Pugh]], [[Jonathan Sterling]], *When is the partial map classifier a Sierpiński cone?* ([arXiv:2504.06789](https://arxiv.org/abs/2504.06789))

and via [[classifying toposes]]:

* [[Jonathan Sterling]], [[Lingyuan Ye]], *Domains and Classifying Topoi* &lbrack;[arXiv:2505.13096](https://arxiv.org/abs/2505.13096)&rbrack;


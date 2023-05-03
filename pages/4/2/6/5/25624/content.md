
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categories of categories
+--{: .hide}
[[!include categories of categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

By $AccCat$ (often just $Acc$ or $\mathbf{Acc}$ etc.) one typically means the ([[very large category|very large]]) [[2-category]] whose

* [[objects]] are [[accessible categories]], 

* [[1-morphisms]] are [[accessible functors]] 

* [[2-morphisms]] are [[natural transformations]].

Hence [[forgetful functor|forgetting]] the accessiblity conditions yields a (non-full) [[2-functor]] from $AccCat$ to the 2-category [[Cat]] of all categories, [[functors]] and [[natural transformations]].

## Properties

### 2-Limits

\begin{proposition}
\label{AccCatHasAllPIELimits}
  The [[2-category]] [[AccCat]] has all (lax) [[2-limits]] and these are [[preserved limit|preserved]] by the inclusion $AccCat \to$ [[Cat]].
\end{proposition}
This appears as [Makkai & Paré (1989), Thm. 5.1.6, Cor. 5.1.8](#MakkaiParé1989), [Adámek & Rosický (1994) around Thm. 2.77](#AdámekRosický1994).

\begin{proposition}
Given a [[cosmos for enrichment]] $\mathcal{V}$ which is ([[symmetric monoidal category|symmetric monoidal]] [[closed monoidal category|closed]] and) [[locally presentable category|locally presentable]], then the [[2-category]] $\mathcal{V}$-[[AccCat]] of $\mathcal{V}$-[[enriched category|enriched]] [[accessible categories]] has all [[PIE 2-limits]] and [[split idempotent|splittings]] of [[idempotent]] [[equivalence in a 2-category|equivalences]], equivalently it has all [[flexible 2-limits]] as well as [[2-pullbacks]] along [[isofibrations]].

The analogous statements holds for $\mathcal{V}$-enriched and *[[conical limit|conically]]* accessible categories, in which case the [[forgetful functor]] $\mathcal{V}\text{-}ConAccCat \to \mathcal{V}\text{-}Cat$ [[preserved limit|preserves]] these [[2-limits]].
\end{proposition}
This is [Lack & Tendas (2023), Thm. 5.5, Thm. 5.9](#LackTendas23).

\begin{proposition}
**(directed unions)**
\linebreak
The [[2-category]] [[AccCat]] has [[directed colimits|directed]] [[2-colimits]] of systems of [[fully faithful functors]].  If there is a proper class of [[strongly compact cardinals]], then it has directed colimits of systems of [[faithful functors]].
\end{proposition}

[Paré & Rosický (2013)](#ParéRosický13)



## Related entries

* [[accessible category]] (see the respective section [there](accessible+category#TheTwoCategoryOfAccessibleCategories))

* [[Cat]]

## References

* {#MakkaiParé1989} [[Michael Makkai]], [[Robert Paré]],  _Accessible categories: The foundations of categorical model theory_,  Contemporary Mathematics 104. American Mathematical Society (1989) &lbrack;[ISBN:978-0-8218-7692-3](https://bookstore.ams.org/conm-104)&rbrack;

* {#AdámekRosický1994} [[Jiří Adámek]], [[Jiří Rosický]], *[[Locally presentable and accessible categories]]*, London Mathematical Society Lecture Note Series **189**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511600579](https://doi.org/10.1017/CBO9780511600579)&rbrack;

* {#ParéRosický13} [[Robert Paré]], [[Jiří Rosický]], *Colimits of accessible categories*, Math. Proc. Cambr. Phil. Soc. **155** (2013) 47-50 &lbrack;[doi:10.1017/S0305004113000030](https://doi.org/10.1017/S0305004113000030), [arXiv:1110.0767](http://arxiv.org/abs/1110.0767)&rbrack;

* {#LackTendas23} [[Stephen Lack]], [[Giacomo Tendas]], *Virtual concepts in the theory of accessible categories*, Journal of Pure and Applied Algebra **227** 2 (2023) 107196 &lbrack;[arXiv:10.1016/j.jpaa.2022.107196](https://doi.org/10.1016/j.jpaa.2022.107196), [arXiv:2205.11056](https://arxiv.org/abs/2205.11056)&rbrack;

 




> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

***


I'd like to get a handle on the content of the recent

* [[Germán Stefanich]]: *Categorification of sheaf theory* &lbrack;[arXiv:2511.09553](https://arxiv.org/abs/2511.09553)&rbrack;

(which is based on the author's thesis and other articles grown out of that, listed [here](https://ncatlab.org/nlab/show/Germ%C3%A1n+Stefanich#OnCOrrespondences)).

Here "sheaf" is really short for "abelian sheaf" as in "quasicoherent sheaf", and generally stands for systems of coefficients satisfying "six functor formalism" on any kind of category $\mathcal{C}$ of domain spaces ($\mathcal{C}$ only required to have the finite limits needed to make sense of correspondences of such). So in other terms this is about what I would call dependent linear homotopy types satisfying the motivic yoga, and then boosted to the directed $(\infty,n)$-situation.

In any case, the article claims something like that any choice of such presentable six-functor coefficients (denoted "$Sh$" and neatly encoded as a lax symmetric monoidal functor from $Corr(\mathcal{C})$ to (locally) presentable $\infty$-categories) induces (Theorem 1.2) 

* for any target space $X \in \mathcal{C}$, 

* for any $n \ge 2 $, 

* an $(n+1)$d-dimensional extended TQFT, denoted $\chi_{(n+1)Sh,X}$,

* with coefficients in something like the $(n+1)$-fold categorification $(n+1)Pr_Sh$ of the category of values of $Sh$ 

* which in codimension 1 assigns to an $n$-manifold $M$ the $Sh$-eaves on the derived mapping space: 

  $$
    M \mapsto Sh\big(Map(M,X)\big)
  $$

  (i.e. represent the homotopy type of $M$ as a homotopy colimit in $\infty$-groupoids of a functor constant on the point and then form the corresponding homtopy limit in $\mathcal{C}$ of the functor constant on $X$ and evaluate $Sh \colon Corr(\mathcal{C}) \to PresCat$ on that).

(There is a crucial degree shift here: $\chi_{(n+1)Sh,X} \colon (n+1)Corr(\mathcal{C}) \longrightarrow (n+1)Pr_{Sh}$ goes from the $(n+1)$-category of correspondendes to an $(n+2)$-category.)

Such kind of situation is not unheard of, as the author recalls, but here it looks like one is getting to the bottom of what makes this work in great generality.

But the definitions are dense, even granting the abstract way of speaking about $(\infty,n)$-categories synthetically, and I'd like to penetrate them better.

The pivotal definition of $(n+1)Pr_{Sh}$ is first not easy to spot and then not easy to unwind. It happens parenthetically in the second but last line of Construction 3.4., where it says:

$$
  n Pr_{Sh} = n Mod_{Sh_! n Corr^{enr}(\mathcal{C})}
$$ 

Here 

* $Corr^{enr}(\mathcal{C})$ (Ntn. 2.10, Rem. 3.5) is the $(\infty,n)$-category of correspondences in $\mathcal{C}$ equipped with $Corr(\mathcal{C})$-enrichment in top degree,

* $Sh_!$ denotes change of enrichment along $Sh$ (Notation 2.1),

* $n Mod_{(-)}$ (Notation 3.3) is advertized as the "canonical functor" taking $n$-categories which in top degree are enriched in locally presentable categories to locally presentable $(n+1)$-categories (which the author develops in his thesis and a previous article [arXiv:2011.03035](https://arxiv.org/abs/2011.03035)) given by "freely adding colimits" in dimension $\leq n$. So I am guessing that the notation "$n Mod_{\mathcal{D}}$" refers to passing to a Yoneda-like embedding by forming functors on $\mathcal{D}^{op}$, but I don't see the actual definition at the moment,

So in (my) tentative vague words it appears that $n Pr_{Sh}$ is something like the $(n+1)$-category obtained from that of  $n+1$-fold correspondences which in degrees $\neq n$ is somehow completed under colimits (cf. Ntn. 3.3.) and in top degree is enriched by the $Sh$-eaves sitting on the tips of the correspondences.

So why I see where this is all headed, it's a mouthful and some crucial ingredients (like $n Mod$ in Ntn. 3.3) are a little sketchy (maybe they are spelled out in other articles?)

So what I would like to look at is an example. My favorite case to start with would be

* $\mathcal{C} \coloneqq Grpd_\infty \equiv An$, the $\infty$-category of $\infty$-gorupoids

* $Sh(-) \coloneqq Vect(-)$ the $\infty$-category of chain complexes of vector spaces over some groups field,

and my first question would be: What is the $(\infty,2)$-category $ 1Pr_{Sh} =  1 Pr_{Vect}$? 

So the objects of $1 Corr(Grpd_\infty)^{enr}$ are $\infty$-groupoids, and  the hom-object (in $Corr(Grpd_\infty)$) between a pair $(X, Y)$ of these ought to be the product $X \times Y$, whence $Sh_! Corr(Grpd_\infty)^{enr}$ should have hom-object $Vect(X \times Y)$ between this pair, in our case.

This describes $Sh_! Corr(\mathcal{C})^{enr} = Vect_! Corr(Grpd_\infty)$ in our case.

Now what is $1Mod_{Vect_! Corr(Grpd_\infty)^{enr}}$ ? 

I am guessing it's meant to be the 2-category of $Pr$-enriched functors (though I am not sure where this is stated)
$$
  Vect_! Corr(Grpd_\infty)^{enr}
  \longrightarrow
  Pr^L
  \,.
$$
Over the point, such functors pick a presentable category with a $Vect(\ast)$-module structure, hence a presentable dg-category. 

And that sounds like it out to be the answer: 

$$
  1 Mod_{Vect_! Corr(Grpd_\infty)^{enr}}
  \simeq
  Pr dg Cat
  \equiv
  2 Vect
  \,.
$$

which is denoted $2 \mathcal{Vect}$ in section 1.2 of [the thesis](https://ncatlab.org/nlab/show/Germ%C3%A1n+Stefanich#Stefanich21Thesis). 


?
#Idea#

The [[homotopy theory|model category structure]] on [[omega-category|omega-categories]] known as the _folk_ model structure (in contrast to the [[Thomason model structure]] on certain flavors of $n$-categories) is designed such such the [[weak equivalence]]s capture the proper notion of categorical equivalences.

In the folk model structure

 * an **acyclic fibration** is a functor which is [[k-surjectivity|k-surjective]] for all $k \in \mathbb{N}$;

 * an **weak equivalence** is a functor which is [[k-surjectivity|essentially k-surjective]] for all $k \in \mathbb{N}$;

 * **cofibrations** are [[cofibrantly generated model structure|generated]] from the inclusions 
$\partial G_n \hookrightarrow G_n$ of of the boundary of the $n$-[[globe]] into the $n$-[[globe]].

#Internalization#

A common problem is to transport the (a) model structure on plain $\omega$-categories, i.e. $\omega$-categories [[internalization|internal to]] $Sets$ to another [[internalization|internal context]], notably for the case that $Sets$ is replaced with some kind of category of $Spaces$. This is relevant for the discussion of the homotopy theory of topological and smooth $\omega$-categories.

The general problem of [[internalization]] of model structures is described [[internalization of model structures|here]]. For the special case of $\omega$-categories internal to [[generalized smooth spaces]] see [[schreiber:Differential Nonabelian Cohomology]].

Usually, such internalization of model structures has the consequence that some properties invoked in the description of the original model structure, notably some of the lifting properties, will only continue to hold "locally".
One way to deal with this is to pass to a notion slightly weaker than that of a [[homotopy theory|model category]] called a [[category of fibrant objects]] as used in [[homotopical cohomology theory]].


#Literature#

* for $n \leq 2$: 

  * Steven Lack, _A Quillen Model Structure for 2-Categories_, K-Theory 26: 171&#8211;205, 2002. ([website](http://www.maths.usyd.edu.au/u/stevel/papers/qmc2cat.html))

* for $n = \omega$: 

  * Yves Lafont, Francois M&#233;tayer, Krzysztof Worytkiewicz, _A folk model structure on omega-cat_ ([arXiv](http://arxiv.org/abs/0712.0617))


* for $n = \omega$ and all morphisms invertible: 

  * R. Brown and M. Golasinski, _A model structure for the homotopy theory of crossed complexes_, Cah. Top. G&#233;om. Diff. Cat. 30 (1989) 61-82 ([pdf](http://www.bangor.ac.uk/~mas010/pdffiles/RB-golskyrev.pdf))
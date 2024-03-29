
Noncommutative algebraic geometry studies objects much more general than a single algebra: one wants to glue algebras to more general "systems". This idea has been around from 1980-s. Of course, one needs a good equivalence among systems. One idea is to replace the algebra by a module and glue categories of modules and then look if the categories are equivalent. But the categories of modules loose the track of the Morita equivalence class, which one would like to keep. For example, one wants to define morphisms between such systems as some class of geometric morphisms, but when one restricts to algebras one would like to have only morphisms of algebras, not the bimodules corresponding to nonaffine morphisms. 

This is nicely achieved in a formalism which significantly refines the standard techniques of gluing via corings sketched in chapter 2 of

* [[Alexander Rosenberg]], [[Maxim Kontsevich]], _Noncommutative smooth spaces_, Noncommutative smooth spaces, The Gelfand Mathematical Seminars, 1996&#8211;1999, 85&#8211;108, Gelfand Math. Seminars, [gBooks](http://books.google.hr/books?id=1xI6j05m7NUC&lpg=PA85&ots=FEtnAU-ImI&dq=alexander%20rosenberg%20gelfand%20seminar%20kontsevich&hl=en&pg=PA85#v=onepage&q&f=false), [math.AG/9812158](http://arxiv.org/abs/math/9812158)

#### STEP 1: Category of Covers

Given a $k$-algebra $R$, a $R$-[[coring]] $M = (M,\delta^M,\epsilon^M)$ is a comonoid in the category of $R$-bimodules (i.e. $R\otimes R^{op}$-modules). One defines a category of covers as the category of pairs $(R,M)$ where $R$ is a $k$-algebra and $M$ is an $R$-coring; one requires that $M$ is faithfully flat as the right  $R$-module i.e. tensoring $M\otimes_R$ is exact and faithful functor. The morphisms $(R_1,M_1)\to (R_2,M_2)$ are given by pairs of algebraic maps in opposite direction, i.e. an algebra map $f_R : R_2\to R_1$ and a bimodule map $f_M:M_2\to M_1$ satisfying the obvious compatibility conditions with the rest of the structure. This defines the category of covers, $Cover_k$. 

One also defines the category of quasicoherent modules $QCoh(R,M)$ as the category of left $M$-comodules, i.e. left $R$-modules $X$ together with the coaction $X\to M\otimes_R X$. 

#### STEP 2: Introducing structure morphism $s_C$

The objects of the category of "space covers" $Cover_k^{sp}$ is the category of pairs $(C,s_C)$ where $C = (R,M) = (R,M,\delta^M,\epsilon^M)$ is a cover
and $s^C: R\otimes_k R\to M$ is a surjective homomorphism of coalgebras in the category of $R$-bimodules. The morphisms in $Cover_k^{sp}$ are the morphisms in $Cover_k$ compatible with "structure morphisms" $s^C$. 

#### STEP 3: Equivalence relation for the morphisms

Still some morphisms induce the same inverse image functors for $QCoh$ categories. To eliminate this, one calls two morphisms $f,g:(C,s_C)\to (C',s_{C'})$ equivalent if for any element $u = \sum x_\alpha\otimes y_\alpha$ in $Ker(s_C)$ the tensor product $(f\otimes g)(u) = 0$ and $(g\otimes f)(u)=0$. After moding out this equivalence we obtain $\widetilde{Cover}^{sp}_k$

#### STEP 4: Localizing on refinements

Any cover $(R,M)$ in $Cover_k$ together with a monomorphism of $k$-algebras $R\hookrightarrow S$ induces a cover $(S,S\otimes_R M\otimes_R S)$ together with a canonical morphism $(S,S\otimes_R M\otimes S)\to (R,M)$ in $Cover_k$. Morphisms of this type are called refinement morphisms; they are closed under composition and pullback. Thus one can define the localized category $Cover_k[Ref^{-1}]$; moreover, $(S,S\otimes_R M\otimes S)$ can be canonically equipped with a structure morphism and we can in this vain obtain the category of noncommutative spaces $NSpace_k := \tilde{Cover}^{sp}_k[Ref^{-1}]$.

### Properties 

Theorem. (AR/MK, sec.2.2) The category of separated quasi-compact schemes over $k$ is equivalent to a full subcategory of $NSpace_k$. The category $Alg^{op}_k$ is also equivalent to a full subcategory of
$NSpace_k$. Category $NSpace_k$ has finite limits.

Theorem. (AR/MK, sec.2.2) Construction $(B,M)\to QCoh(B,M)$ extends to a functor from the category $NSpace_k$ to the category of abelian $k$-linear categories. For separated quasi-compact schemes, it gives usual quasi-coherent sheaves of commutative algebraic geometry. For associative algebras, it gives categories of left modules.

[[!redirects noncommutative spaces as covers]]
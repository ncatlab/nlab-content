A derived affine scheme is a special kind of [[generalized scheme]].

In a version of the theory of [[derived algebraic stack]]s due To&#235;n, Vezzosi and Vaquie, __the category of derived affine schemes__ is $sComm^{op}$, the [[opposite category|opposite]] of the category of [[simplicial object|simplicial]] [[commutative unital rings]]. The category of [[simplicial presheaves]] on $sComm^{op}$ has several [[model category]] structures. If a [[projective model structure]] is used, this category of simplicial presheaves is denoted $SPr(dAff)$ where weak equivalences and fibrations are defined levelwise. By $dAff^{\hat{}}$ one denotes the left [[Bousfield localization]] of the model category $SPr(dAff)$ with respect to the [[Yoneda embedding|Yoneda images]] $h_X\to h_Y$ of equivalences in $dAff$; this model category $dAff^{\hat{}}$ is called the _model category of prestacks_ over $dAff$. The fibrant objects in $dAff^{\hat{}}$ are the simplicial presheaves $F:dAff^{op}\to sSet$ such that 

* (anodyne condition) for all $X\in dAff$, the simplicial set $F(X)$ is fibrant; and

* (prestack condition) for each equivalence $X\to Y$ in $dAff$, the induced morphism $F(Y)\to F(X)$ is a weak equivalence of simplicial sets. 

The [[homotopy category]] $Ho(dAff^{\hat{}})$ is naturally equivalent to the [[full subcategory]] of $Ho(SPr(dAff))$ whose objects are the simplicial presheaves satisfying the above prestack condition. 

* [[Bertrand Toën|B. Toën]], _Simplicial presheaves and derived algebraic geometry_, lecture notes CRM, Barcelona 2008; ([crm-2008.pdf](http://www.math.univ-toulouse.fr/~toen/crm-2008.pdf))
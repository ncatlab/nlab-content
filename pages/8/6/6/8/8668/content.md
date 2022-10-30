
We say an object $X$ is _presentable_ if there is an [[epimorphism]]

$$
  \hat X \to X
$$

out of an object $\hat X$ which is [[free object|free]] in some sense. 

the [[category of presheaves]] functor

$$
  C \mapsto PSh(C)
$$

is such a free construction, [[free cocompletion]]

So we should say that a category $\mathcal{C}$ is presentable if there is a suitable epimorphism

$$
  L \colon PSh(K) \to \mathcal{C}
$$

for some small category $K$. We want here just presentability of the objects, hence "local presentability". hence we demand that $L$ has a [[section]] by a [[full and faithful functor]] $i \colon \mathcal{C}\hookrightarrow PSh(K)$. 

$L \circ i \simeq id_{\mathcal{C}}$.

this is implied if we demand $L$ to be a [[left adjoint]] to 


* [[generators and relations]]

* [[regular cardinal]]

* [[small object]]

(...)


**Locally presentable categories:** [[large categories|Large categories]] whose [[objects]] arise from [[small object|small]] [[generators]] under [[small colimit|small]] [[relations]].

| [[(n,r)-categories]]... | satisfying [[Giraud's axioms]] |  inclusion of [[left exact functor|left exaxt]] [[localizations]] |  [[generators and relations|generated]] under [[colimits]] from [[small objects]] |   | [[localization]] of [[free cocompletion]] |  | [[generators and relations|generated]] under [[filtered colimits]] from [[small objects]]   |
|--|--|--|--|--|----|--|--|
| **[[(0,1)-category theory]]** | [[(0,1)-toposes]] | $\hookrightarrow$ | [[algebraic lattices]] | $\simeq$ [Porst's theorem](algebraic+lattice#RelationToLocallyFinitelyPresentableCategories) | [[subobject lattices]] in [[accessible functor|accessible]] [[reflective subcategories]] of [[presheaf categories]] | | |
| **[[category theory]]** | [[toposes]] | $\hookrightarrow$ | [[locally presentable categories]] | $\simeq$ [Ad&#225;mek-Rosick&#253;'s theorem](locally+presentable+category#AsLocalizationsOfPresheafCategories) | [[accessible functor|accessible]] [[reflective subcategories]] of [[presheaf categories]] |
$\hookrightarrow$ | [[accessible categories]]  |
| **[[model category|model category theory]]** | [[model toposes]] | $\hookrightarrow$ | [[combinatorial model categories]] | $\simeq$ [Dugger's theorem](combinatorial+model+category#DuggerTheoreml) | [[left Bousfield localization]] of global [[model structures on simplicial presheaves]]  | | |
| **[[(∞,1)-topos theory]]** | [[(∞,1)-toposes]] |$\hookrightarrow$ | [[locally presentable (∞,1)-categories]] | $\simeq$ <br/> [Simpson's theorem](locally+presentable+infinity-category#Definition) | [[accessible (∞,1)-functor|accessible]] [[reflective sub-(∞,1)-categories]] of [[(∞,1)-presheaf (∞,1)-categories]] |
$\hookrightarrow$ |[[accessible (∞,1)-categories]] |


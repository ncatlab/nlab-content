In 1980-s, [[Grothendieck]] introduced test categories to make the variants of the [[homotopy theory]] based on the usage if combinatorial models with some kind of cell structure (e.g. simplicial, cubical and cellular sets) independent of a particular combinatorial model.

Given any small category $\mathcal{C}$, one considers $\mathcal{C}$-sets, i.e. contravariant functors from $\mathcal{C}$ to $Set$. Given an object $c\in C$, one considers the [[representable functor]] $Hom_{\mathcal{C}}(-,c)=:\Delta^c$. If $X:\mathcal{C}\to Set$ is a $\mathcal{C}$-set, the elements of $X(c)$ are called the $c$-cells. By Yoneda, they correspond to the natural transformations $\Delta^c\to X$. Let the **cell category** of $X$, denoted $i_{\mathcal{C}} X$, be the full subcategory of the [[overcategory]] $\mathcal{C}Set/X$ whose objects are the transformations of the form $\Delta^c\to X$. The correspondence $X\mapsto i_{\mathcal{C}}X$ extends to a functor $i_{\mathcal{C}}:\mathcal{C}Set\to Cat$ which has a right adjoint $i_{\mathcal{C}}^*:Cat\to\mathcal{C}Set$ whose object part is given by the formula

$$ i_{\mathcal{C}}^*(D)(c):= Hom_{\mathcal{C}}(\mathcal{C}/c,D).$$

Denote the counit of the adjunction $\epsilon : i_{\mathcal{C}}i_{\mathcal{C}}^*\to Id_{Cat}$. 

Two $\mathcal{C}$-sets $X$ and $Y$ are **weakly equivalent** if there is a map $f:X\to Y$ inducing an equivalence $f_* : i_{\mathcal{C}} X\to i_{\mathcal{C}} Y$ of their cell categories, i.e. the induced map of classifying spaces $B(i_{\mathcal{C}} X)\to B(i_{\mathcal{C}} Y)$ is a weak equivalence of simplicial sets. Functor $i_{\mathcal{C}}:\mathcal{C}Set\to Cat$ induces a functor $i_{\mathcal{C}*}:Ho(\mathcal{C}Set)\to Ho(Cat)$ of the homotopy categories.  

A **weak test category** is a small category $\mathcal{C}$ such that, 
for any category $D$ in $Cat$, the component of the counit $\epsilon_D : i_{\mathcal{C}}i_{\mathcal{C}}^* D \to D$ is an equivalence of categories. 

A **test category** is any small category $\mathcal{A}$ such that 

* ($\mathcal{A}$ is aspherical) its [[classifying space]] $B\mathcal{A}$ is contractible

* ($\mathcal{A}$ is a "local test category") for every object $a$ in $\mathcal{A}$ require the overcategory $\mathcal{A}/a$ to be a weak test category. Thus for any category $D$ in $Cat$, $\epsilon_D : i_{\mathcal{A}/a}i_{\mathcal{A}/a}^* D \to D$ is an equivalence of categories. 

Then one proceeds with $\mathcal{A}$-sets.

If $\mathcal{A}$ is a test category and $\mathcal{C}$ any small category whose classifying space is contractible (which may or may not be a test category itself), then their cartesian product $\mathcal{A}\times\mathcal{C}$ is a test category. 

* J. F. Jardine, _Categorical homotopy theory_, Homot. Homol. Appl. __8__ (1), 2006, pp.71&#8211;144, [pdf](http://www.intlpress.com/HHA/v8/n1/a3/v8n1a3.pdf)
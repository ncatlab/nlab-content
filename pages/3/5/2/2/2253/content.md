A morphism $i = (i,i^\sharp):Y\hookrightarrow X$ of algebraic [[schemes]] is a __[[closed immersion of schemes|closed immersion]]__ if, as a topological space, $i(Y)$ is a closed subspace of $X$, $i$ is a homeomorphism on the image, and the [[comorphism]] $i^\sharp:\mathcal{O}_X\to i_*\mathcal{O}_Y$ is a surjective map of rings. 

A closed subscheme of $X$ is an [[equivalence class]] of closed immersions into $X$ (morphisms of schemes $i:Y\to X$ and $i':Y'\to X$ are equivalent if there is an isomorphism $eq:Y\cong Y'$ of schemes such that $i'\circ eq = i$)

In an equivalent description of closed subschemes, there is a sheaf of ideals $\mathcal{I}\subset\mathcal{O}_X$ such that the quotient sheaf $\mathcal{O}_X/\mathcal{I}$ is *supported* on the image set $i(Y)\cong Y$. One says that $\mathcal{I}$ is the [[defining sheaf of ideals]] (or in more French style, *the ideal of definition*) of the subscheme $Y$. The structure sheaf $\mathcal{O}_Y$ of the subscheme $Y$ is the quotient sheaf $\mathcal{O}_X/\mathcal{I}$ restricted to $Y$. The [[conormal sheaf]] of the closed immersion $Y\hookrightarrow X$ is the quasicoherent sheaf of modules defined by formula $\mathcal{I}/\mathcal{I}^2$. 

In the affine case, one can take $X=Spec\,R$ and $Y=Spec\,R/I$ where $I=\Gamma_X(\mathcal{I})$ is the __defining ideal__ of the closed affine subscheme $Y$. The underlying set of $Y$ is precisely the set $V(I)$ of all prime ideals in $R$ which contain $I$. 

See also [[open subscheme]]. 

category: algebraic geometry
[[!redirects closed immersion of schemes]]
[[!redirects closed subschemes]]


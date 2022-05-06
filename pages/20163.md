# Cellular models

* table of contents
{: toc}

## Definition

Let $E$ be a [[Grothendieck topos]].  A **cellular model** for $E$ is a [[set]] of [[monomorphisms]] $I$ in $E$ that [[combinatorial wfs|cofibrantly generates]] a [[weak factorization system]] whose left class is precisely the monomorphisms.

## Existence

\begin{theorem}
A cellular model exists in any Grothendieck topos.
\end{theorem}

For presheaf toposes this is [Cisinski 06, prop. 1.2.27](#Cisinski06); the result for general toposes is stated without proof as [Cisinski 03, prop. 1.2.2](#Cisinski03).  The proof below is a direct generalization of the presheaf version.

\begin{proof}
Let $E=Sh(C)$ be the category of [[sheaves]] on some small [[site]] $C$, let $a : [C^{op},Set] \to Sh(C)$ be the [[associated sheaf]] functor, and for each $c\in C$ let $y_c = C(-,c)$ denote the [[representable presheaf]].  Let $I$ be a set of representatives for isomorphism classes of all monomorphisms $i:A\to B$ such that there exists an [[epimorphism]] $a y_c \to B$ in $E$ for some $c\in C$.  Since toposes are both [[well-powered category|well-powered]] and well-copowered, $I$ is a small set.

It suffices to show that every monomorphism in $E$ can be written as an $I$-[[cell complex]].  Let $f:X\to Y$ be a monomorphism and choose an surjection $w : \lambda \to  \coprod_{c\in C} Y(c)$ for some [[ordinal number]] $\lambda$.  For each $\beta\le \lambda$, let $X_\beta$ be the smallest subobject of $Y$ that contains $X$ and also $w_\alpha$ for all $\alpha\lt\beta$.  Then $X_0 = X$ and $X_\lambda = Y$, exhibiting $f$ as the transfinite composite of the inclusions $X_\beta \hookrightarrow X_{\beta+1}$, so it will suffice to show that each of these inclusions is a pushout of a morphism in $I$.

Now by the Yoneda lemma, $w_\beta\in Y(c)$ corresponds to a map of presheaves $y_c \to Y$, hence a map of sheaves $a y_c \to Y$.  Let $D_\beta$ be the [[image]] of $a y_c \to Y$ in $E$ (which may not coincide with the image in $[C^{op},Set]$, of course).  Then $X_{\beta+1} = X_\beta \cup D_\beta$ as subobjects of $Y$, so since $E$ is a [[coherent category]] we can write it as a pushout $X_{\beta+1} = X_\beta \sqcup_{(X_\beta \cap D_\beta)} D_\beta$.  However, the inclusion $X_\beta \cap D_\beta \hookrightarrow D_\beta$ is (isomorphic to) some morphism in $I$.
\end{proof}


## Related pages

* [[Cisinski model structure]]

## References

* [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie|Les préfaisceaux comme modèles des types d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 {#Cisinski06}

* [[Denis-Charles Cisinski]], _Faisceaux localement asphériques_ (preliminary version), 2003, [pdf](http://www.mathematik.uni-regensburg.de/cisinski/mtest2.pdf)
 {#Cisinski03}

[[!redirects cellular models]]
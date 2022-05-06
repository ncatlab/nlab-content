Given any subset $S\subset A$, we can consider the corresponding inclusion $i_S:S\hookrightarrow A$ as a function. More generally, for a subobject $S\subset A$
(an equivalence class of monos) we can consider any representative monomorphism $i_S:S\hookrightarrow A$.

Then for any morphism $f:A\to B$, the [[restriction]] $f|_S:S\to B$ of a morphism $f$ onto $S$ is the precomposition $f|_S = f\circ i_S$ of $f$ by $i_S$. 
For a different representative of the subobject, $i_{\tilde{S}}:\tilde{S}\to A$ there is a unique iso $b:S\to\tilde{S}$ such that $i_{\tilde{S}}\circ b = i_S$, hence $f_{\tilde{S}} = f\circ b$. 

This way one has replaced the domain by a subobject. The standard notion of a corestriction is to replace the _co_domain by a subobject. Thus for a mono $i_T:T\hookrightarrow B$ the corestriction $f|^T:A\to T$ of $f$ onto $S$ is the unique morphism $f|^T$ such that there is a decomposition $f = i_T\circ f|^T$. The corestriction exists if and only if $T$ contains the image of $f$, that is $i_{Im(f)}$ factors through $i_{T}$. In particular, by the universal property of the image, the corestriction onto the image always exists and it is sometimes simply called the corestriction of $f$. 

The notion of a corestriction is well known, while rarely practically used in print, e.g. in Definition 3.1 and Remarks 3.2 in Gabriella Böhm, Hopf algebroids, in Handbook of algebra (2008) [arXiv:0805.3806](https://arxiv.org/abs/0805.3806).

At page 14 (paragraph 2-14) of Andreotti, A., Généralités sur les catégories abéliennes (suite)
Séminaire A. Grothendieck, Tome 1 (1957) Exposé no. 2, [numdam](http://www.numdam.org/item/SG_1957__1__A2_0) the author introduces the above notion under the name coastriction, while the name corestriction reserves to the notion categorically dual to the notion of a restriction. Namely, if $p^U:B\to U$ is an epimorphism,  then for a morphism $f:A\to B$, then by a corestriction Andreotti understands the postcomposition $p^U\circ f:A\to U$ of $f$ by $p^U$, which surely always exists. 

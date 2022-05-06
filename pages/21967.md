
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition


The notion of _co-restriction_ of a [[function]], or more generally of a [[morphism]], is either the [[formal duality|formal dual]] of that of _[[restriction]]_, or something similar. For the latter, recall:

Given any [[subset]] $S\subset A$, we may consider the corresponding inclusion $i_S \colon S \hookrightarrow A$ as a [[function]]. More generally, for a [[subobject]] $S\subset A$ (an [[equivalence class]] of [[monomorphisms]] in some ambient [[category]]) we may consider any representative monomorphism $i_S \colon S\hookrightarrow A$.

Then for any [[morphism]] $f \colon A\to B$, the _[[restriction]]_ $f|_S \colon S \to B$ of $f$ onto $S$ is the [[composition|precomposition]] $f|_S \coloneqq f \circ i_S$ of $f$ by $i_S$. 
(For a different representative of the subobject, $i_{\tilde{S}} \colon \tilde{S}\to A$ there is a unique [[isomorphism]] $b \colon S\to\tilde{S}$ such that $i_{\tilde{S}}\circ b = i_S$, hence $f_{\tilde{S}} = f\circ b$.) 

This way, restriction of a [[morphism]] amounts to replacing its [[domain]] by one of its [[subobjects]]. 

### As factorization through the image
  {#AsFactorizationThroughTheImage}

Similarly, the standard notion of _corestriction_ (e.g. [Böhm 08, Def. 3.1](#Bohm08)) of a [[morphism]] $f \colon A \longrightarrow B$ is to instead replace the [[codomain|*co*domain]] $B$ by a [[subobject]]: 

For a [[monomorphism]] $i_T \colon T \hookrightarrow B$, the _corestriction_ $f|^T \colon A \to T$ of $f$ onto $S$ is, if it exists, the unique morphism $f|^T \colon A \to S$ such that there is a decomposition $f = i_T \circ f|^T$. 

The corestriction exists if and only if $T$ contains the [[image]] of $f$, that is $i_{Im(f)}$ factors through $i_{T}$. In particular, by the [[universal property]] of the image, the corestriction onto the [[image]] $S = Im(f)$ always exists and this is sometimes understood as the corestriction of $f$, by default.

### As the formal dual of restriction

Alternatively, one may consider the notion of corestriction to be the [[formal dual]] to the notion of a restriction: if $p^U \colon B\to U$ is an [[epimorphism]], then the co-restriction of a morphism $f \colon A\to B$, in this dual sense, is the [[composition|postcomposition]] $p^U \circ f \colon \colon A\to U$ of $f$ by $p^U$, which surely always exists. 

This is the notion of corestriction considered e.g. in [Andreotti 57, page 14](#Andreotti57), where the factorization through the image ([above](#AsFactorizationThroughTheImage)) is instead called _coastriction_.


## References

The notion of corestriction is well known, while rarely made explicit in print. One may find it e.g. in 

* {#Bohm08} [[Gabriella Böhm]], Definition 3.1 and Remarks 3.2 in: _Hopf algebroids_, in: _Handbook of Algebra_, Volume 6, 2009, Pages 173-235 ([arXiv:0805.3806](https://arxiv.org/abs/0805.3806), <a href="https://doi.org/10.1016/S1570-7954(08)00205-2">doi:10.1016/S1570-7954(08)00205-2</a>)

See also:

* {#Andreotti57} A. Andreotti, page 14 (paragraph 2-14) in: _Généralités sur les catégories abéliennes_ (suite) Séminaire A. Grothendieck, Tome 1 (1957) Exposé no. 2 ([numdam:SG_1957__1__A2_0](http://www.numdam.org/item/SG_1957__1__A2_0))

[[!redirects corestrictions]]

[[!redirects co-restriction]]
[[!redirects co-restrictions]]


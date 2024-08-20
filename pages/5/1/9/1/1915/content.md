
#Contents#
* table of contents
{:toc}

## Definition 

The __restriction__ of a [[function]] $f: X \to Y$ to a [[subset]] $U$ of $X$ is simply the [[composite]] of $f$ and the [[inclusion function]] of $U$:

$$ U \stackrel{i_U}\to X \stackrel{f}\to Y .$$

It is often written as $f_{|U}: U \to Y$, or $f|_U$, or a variation.

More generally, in any category $C$, a monomorphism $i_U : U\hookrightarrow X$, and a [[morphism]] $f \colon X\to Y$, the _[[restriction]]_ $f|_U \colon U \to Y$ of $f$ onto $U$ is the [[composition|precomposition]] $f|_U \coloneqq f \circ i_U$ of $f$ by $i_U$. A [[subobject]] is an equivalence class of monomorphisms. For a different representative of the subobject, $i_{\tilde{U}} \colon \tilde{U}\to X$ there is a unique [[isomorphism]] $b \colon U\to\tilde{U}$ such that $i_{\tilde{U}}\circ b = i_U$, hence $f_{\tilde{U}} = f\circ b$. 

## Related concepts

* [[extension]]

* [[lift]]

* [[Cauchy principal value]]

[[!redirects restrictions]]
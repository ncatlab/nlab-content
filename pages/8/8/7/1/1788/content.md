
## Idea

According to [Kornell 2020](#Kornell20), in mild paraphrase (following the discussion at *[[quantum circuits via dependent linear types]]*):

* **quantum sets** are  [[indexed sets]] of [[finite-dimensional Hilbert spaces]], hence finite-[[rank of a vector bundle|rank]] [[Hilbert bundle|Hilbert]]-[[vector bundles]] over a [[discrete topological spaces]] regarded as a [[sets]], and regarded as equipped with the [[external tensor product]] $\boxtimes$ [of vector bundles](VectBund#TensorMonoidalStructure);

* a **[[quantum relation]]** between quantum sets $(x \colon X) \times \mathscr{H}_x$ and $(x' \colon X') \times \mathscr{H}'_x$ is a [[monomorphism]] from a quantum set $\big((x,x') \colon X \times X'\big) \times \mathscr{R}_{(x,x')}$ to $\mathscr{H}^\ast_\bullet \boxtimes \mathscr{H}'_\bullet$:

  $$
    (x,x') \colon X \times X'
    \;\;\;
    \vdash
    \;\;\;
    \mathscr{R}_{(x,y)}
    \hookrightarrow
    \mathscr{H}^\ast_{(x,y)} 
      \otimes
    \mathscr{H}^'_{(x,y)} 
  $$

## References

* {#Kornell20} [[Andre Kornell]], *Quantum Sets*, J. Math. Phys. **61** 102202 (2020) &lbrack;[doi:10.1063/1.5054128](https://doi.org/10.1063/1.5054128)&rbrack;

* [[Andre Kornell]], [[Bert Lindenhovius]], [[Michael Mislove]], §2 in: *Quantum CPOs*, EPTCS **340** (2021) 174-187 &lbrack;[arXiv:2109.02196](https://arxiv.org/abs/2109.02196), [doi:10.4204/EPTCS.340.9](https://doi.org/10.4204/EPTCS.340.9)&rbrack;

  > (in the context of [[quantum CPOs]])




The category $\Delta$ has generators (cofaces and codegeneracies) and relations and
a every morphism can be canonically represented via cofaces and codegeneracies. Consequently, for [[simplicial set]]s, hence functors $\Delta^{op}\to Set$ have canonical representation via face and degeneracy maps. We can now look at categorification of this situation to pseudofunctors, say $\Delta^{op}\to Cat$ ([[pseudosimplicial categories]]). While the simplicial identities now hold up to 
invertible 2-cells, the canonical representation of general morphisms as sequences of face and degeneracy maps suggest that one should be able to write down the corresponding 2-cells from generating 2-cells corresponding to the quadratic identities, and that different choices of sequences generating 2-cells should be the
same composite 2-cells. 

Jardine has proved that the generating 2-cells 

$$\array{
\partial_j \partial_i \implies \partial_i \partial_{j+1} & (i \leq j)\\
\partial_i \sigma_j \implies \sigma_{j-1} \partial_i & (i \lt j) \\
\partial_i \sigma_j \implies Id & (i = j, i = j + 1)\\
\partial_i \sigma_j \implies \sigma_j \partial_{i-1} & (i \gt j + 1) \\
\sigma_i \sigma_j \implies \sigma_{j+1} \sigma_i & (i \leq j) 
}$$

coming from the pseudosimplicial objects satisfy 17 coherence relations which in turn enable one to reconstruct the 2-cells among more complicated chains of face and degeneracy maps in unique way. To write those, all generating will be denoted by $\alpha$ with some additional superscripts, but for simplicity we skip the superscript as in Jardine's paper (as they are obvious to fill):

...

In particular, this way one can check when one has a pseudosimplicial object coming from a concrete construction by producing just those 2-cells which are generating  and checking the 17 diagrams. He calls the corresponding structure $(X_n, \partial_i, \sigma_j, \alpha)$ of 0-cells, faces, degeneracies and generating 2-cells the supercoherence. They are therefore equivalent to a pseudosimplicial object $X_\bullet$.

* J. F. Jardine, _Supercoherence_, J. Pure Appl. Algebra __75__ (1991), no. 2, 103&#8211;194 [MR1138365](http://www.ams.org/mathscinet-getitem?mr=1138365) <a href="http://dx.doi.org/10.1016/0022-4049(91)90122-I">doi</a>

  
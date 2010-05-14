
<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}


## Idea

An object in an [[(∞,1)-topos]] $\mathbf{H}$ is _hypercomplete_ if it regards the [[Whitehead theorem]] to be true in $\mathbf{H}$, i.e. if homming [[weak homotopy equivalence]]s into it produces an equivalence.

## Definition 

Let $\mathbf{H}$ be an [[(∞,1)-topos]].

An [[object]] $A \in \mathbf{H}$ is **hypercomplete** if it is a [[local object]] with respect to all $\infty$-[[connected]] [[morphism]]s. 

This means: if for every morphism $f : X \to Y$ which is $\infty$-[[connected]] as an object of the [[over quasi-category|over category]] $\mathbf{H}_{/Y}$ (roughly: all its [[homotopy fiber]]s have vanishing [[homotopy group in an (∞,1)-topos|homotopy groups]]), then the induced morphism

$$
  \mathbf{H}(f,A) : \mathbf{H}(Y,A) \to \mathbf{H}(X,A)
$$

is an [[equivalence in a quasi-category]] in [[∞Grpd]].


The $(\infty,1)$-topos $\mathbf{H}$ itself is a 
  **[[hypercomplete (∞,1)-topos]]** if all its objects are hyercomplete. See there for more details.

## Remarks

* Hypercompleteness is a notion that appears only due to the possible unboundedness of the degree of [[homotopy groups in an (∞,1)-topos]]. The notion is empty in an [[(n,1)-topos]] for finite $n$.

* An object being hypercomplete in $\mathbf{H}$ means that it regards the [[Whitehead theorem]] to be true in $\mathbf{H}$. If $\mathbf{H}$ itself is hypercomplete, then the Whitehead theorem _is_ true in $\mathbf{H}$.


## References

This is the topic of section 6.5.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The definition appears before lemma 6.5.2.9

[[!redirects hypercomplete]]
[[!redirects hypercomplete objects]]
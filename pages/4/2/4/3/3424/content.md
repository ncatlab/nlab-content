
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The general notion of [[opposite (∞,1)-category]] leads to a notion of **opposite of a quasi-category** , when [[(∞,1)-categories]] are incarnated as [[quasi-categories]]. 

So the notion of **opposite** of a [[quasi-category]] generalizes the notion of [[opposite category]] from [[category theory]].


## Definition

Under the [[relation between quasi-categories and simplicial categories]] the opposite quasi-category is that corresponding to the obvious opposite [[SSet]]-[[enriched category]]. Concretely in terms of the [[simplicial set]] $S$ underlying the quasi-category, this amounts to reversing the order of the [[simplicial identities|face and degenracy maps]]:

$$
  (d_i : S_n^{op} \to S_{n-1}^{op}) = 
  (d_{n-i} : S_n \to S_{n-1})
$$

$$
  (s_i : S_n^{op} \to S_{n+1}^{op})
  =
  (s_{n-i} : S_n \to S_{n+1})
  \,.
$$

## References

Secton 1.2.1 in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
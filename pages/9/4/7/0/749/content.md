
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $S$ a small [[site]] let $SimpSh(S)$ be the full category of [[simplicial presheaf|simplicial presheaves]] on $S$ which satisfy the [[sheaf]] condition: the category of [[simplicial sheaf|simplicial sheaves]].

The local [[model category]] structure on $SimpSh(S)$ is originally due to Joyal. It is closely related to the local [[model structure on simplicial presheaves]].

## Local injective model structure

+-- {: .un_theorem }
###### Theorem 

There is a proper closed [[simplicially enriched category|simplicially enriched]] [[model category]] structure on $SimpSh(S)$ such that

* cofibrations are precisely the objectwise cofibrations (monomorphisms) of [[simplicial set]]s;


* weak equivalences are the _local weak equivalences_ of the underlying simplicial presheaves as defined at [[model structure on simplicial presheaves]].

=--

See theorem 5 in _Jardine07_.

+-- {: .un_theorem }
###### Theorem 

The inclusion of sheaves into simplicial presheaves
$SimpSh(S) \hookrightarrow SimpPr(S)$ and the sheafification functor 
$SimpPr(S) \to SimpSh(S)$ constitute a 
[[Quillen equivalence]] with respect to the above
_first local model structure_ on $SimpPr(S)$ ans the local 
[[model structure on simplicial sheaves]].

=--

See _Jardine07_, theorem 5.



## References

* [[Sjoerd Crans]], _Quillen closed model structure for sheaves_,  J. Pure Appl. Algebra  101 (1995), 35-57 ([web](http://home.tiscali.nl/secrans/papers/thcms.html))

see also [[model structure on simplicial presheaves]] for more literature

Jardine's lectures

* **Jardine07** J. Jardine, _Field Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))

discuss the Quillen equivalence between the model structure on simplicial sheaves and the [[model structure on simplicial presheaves]].

Wendt discusses "the construction of classifying spaces of fibre sequences in model categories of simplicial sheaves" in 

* Matthias Wendt, _Classifying spaces and fibrations of simplicial sheaves_, [arxiv/1009.2930](http://arxiv.org/abs/1009.2930) 

[[!redirects model structures on simplicial sheaves]]
[[!redirects model structure on the category of simplicial sheaves]]
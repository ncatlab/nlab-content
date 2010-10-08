A **forgetful functor** is a [[functor]] which is defined by 'forgetting' something.  For example, the forgetful functor from [[Grp]] to [[Set]] forgets the group structure of a [[group]], remembering only the underlying [[set]].

In common parlance, the term 'forgetful functor' has no precise definition, being simply used whenever a functor is obviously defined by forgetting something.  Many forgetful functors of this sort have left or right [[adjoint functor|adjoints]] (and many are actually [[monadic functor|monadic]] or [[comonadic functor|comonadic]]), leading to the paradigmatic adjunction "free $\dashv$ forgetful."

On the other hand, from the perspective of [[stuff, structure, property]], _every_ functor is regarded as a forgetful functor and classified by how much it forgets (namely, stuff, structure, or properties).  From this perspective, the forgetful functor from $Grp$ to $Set$ forgets the structure of a group and the property of admitting a group structure, as usual; but its left adjoint (the [[free group]] functor) is *also* forgetful: if you identify $Set$ with the category of free groups with specified generators, then it forgets the structure of a set of free generators and the property of being free.

See [[stuff, structure, property]] and also section 2.4 [page 15](http://arxiv.org/PS_cache/math/pdf/0608/0608420v2.pdf#page=15) of 

* John C. Baez, Michael Shulman, _Lectures on n-Categories and Cohomology_ ([arXiv](http://arxiv.org/abs/math.CT/0608420)).

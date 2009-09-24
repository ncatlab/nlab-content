Given a (directed) graph _D_, that is, a collection of vertices and of labeled arrows between them, the **free groupoid** _G_( _D_ ) **on** _D_ is the category that has the vertices of _D_ as objects, and whose morphisms are constructed recursively by formal composition (i.e., juxtaposition) from identity maps, the arrows of _D_ and formal inverses for the arrows of _D_. The only relations between morphisms of _G_( _D_ ) are the necessary ones defining the identity of each object, the inverse of each arrow in _D_ and the associativity of composition. 
This is clearly a groupoid, which comes with an evident morphism _D_ --> _G_( _D_ ) of directed graphs. 

The above sketched construction could be made more precise, but what really matters is the _universal property_ it enjoyes: the free groupoid _G_( _D_ ) is the universal (initial) groupoid mapping out of _D_. By varying _D_, the free groupoid yields a functor _G_ from directed graphs to groupoids, left adjoint to the forgetful functor. 

This last conceptual characterization is best taken as the definition. Similarly, it is possible to construct the left adjoint to the forgetful functor from groupoids to categories, that is the **free groupoid over a category**.


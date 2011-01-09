[_Sheaf Semantics for Concurrent Interacting Objects_](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.4296) is a paper by [[Joseph Goguen]], which formulates the behaviour of
systems of concurrent interacting objects categorically. Goguen uses [[sheaf|sheaves]] to represent the behaviours of individual objects, and [[limits]] to combine the behaviours of objects into that of the system. The approach is very general, and is not restricted to "objects" in the sense of object-oriented programming, or indeed to computation. 

### Relevance to computing ###

In [[A Categorical Manifesto]], Goguen writes that:
> Given a species of structure, say widgets, then the result of 
> interconnecting a system of widgets to form a super-widget corresponds to
> taking the
> colimit of the diagram of widgets in which the morphisms show how
> they are interconnected.
He continues by saying that, at least for him, this dogma arose in the context of General Systems Theory. I don't know how widely recognised the use of colimits for "putting together" is, but to the extent that it is, it this paper and earlier ones on which it's based may have helped promote the idea.

### Abstract ###

> This paper uses concepts from sheaf theory to explain phenomena in 
> concurrent systems, including object, inheritance, deadlock, and 
> non-interference, as used in computer security. The approach is very; 
> general, and applies not only to concurrent object oriented systems, but 
> also to systems of differential equations, electrical circuits, hardware 
> description languages, and much more. Time can be discrete or continuous, 
> linear or branching, and distribution is allowed over space as well as 
> time. Concepts from categpru theory help to achieve this generality: 
> objects are modelled by sheaves; inheritance by sheaf morphisms; systems by 
> diagrams; and interconnection by diagrams of diagrams. In addition, 
> behaviour is given by limit, and the result of interconnection by colimit. 
> The approach is illustrated with many examples, including a semantics for a 
> simple concurrent object-based programming language.

### Reference ###

Joseph A. Goguen, _Sheaf Semantics for Concurrent Interacting Objects_, in _
Mathematical Structures in Computing Science_, volume 2, pages 159-91, 1992.

### Link ###

[_Sheaf Semantics for Concurrent Interacting Objects_](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.4296). CiteSeerX page.


This page is to record the reference

* [[Joseph Goguen]]:

  \linebreak

  **Sheaf Semantics for Concurrent Interacting Objects** 

  \linebreak

  Mathematical Structures in Computing Science **2** (1992) 159-91

  [doi:10.1017/S0960129500001420](https://doi.org/10.1017/S0960129500001420), [[Goguen-SheafSemantics.pdf:file]]

which aims to formulate with [[category theory]] the behaviour of "systems of concurrent interacting objects. 

Goguen uses [[sheaf|sheaves]] to represent the behaviours of individual objects, and [[limits]] to combine the behaviours of objects into that of the system. The approach is very general, and is not restricted to computation. 

> **Abstract.** This paper uses concepts from sheaf theory to explain phenomena in  concurrent systems, including object, inheritance, deadlock, and non-interference, as used in computer security. The approach is very general, and applies not only to concurrent object oriented systems, but also to systems of differential equations, electrical circuits, hardware description languages, and much more. Time can be discrete or continuous, linear or branching, and distribution is allowed over space as well as time. Concepts from category theory help to achieve this generality: objects are modelled by sheaves; inheritance by sheaf morphisms; systems by diagrams; and interconnection by diagrams of diagrams. In addition, behaviour is given by limit, and the result of interconnection by colimit. The approach is illustrated with many examples, including a semantics for a simple concurrent object-based programming language.


In *[[A Categorical Manifesto]]*, Goguen writes that:

> Given a species of structure, say widgets, then the result of interconnecting a system of widgets to form a super-widget corresponds to taking the colimit of the diagram of widgets in which the morphisms show how they are interconnected.

> He continues by saying that, at least for him, this dogma arose in the context of [[dynamical system|General Systems Theory]]. I don't know how widely recognised the use of [[colimit|colimits]] for "putting together" is, but to the extent that it is, it this paper and earlier ones on which it's based may have helped promote the idea, and thereby be of historical interest.

> Moreover, if one is having trouble designing a system to describe or run simulations &#8212; whether on a computer or not &#8212; Goguen's formulation seems, to me (JNIP) at least, to offer a clean elegant starting place. Certainly cleaner than the semantics of most object-oriented programming languages.






category: reference

[[!redirects sheaf semantics of concurrent interacting objects]]
[[!redirects Sheaf semantics of concurrent interacting objects]]


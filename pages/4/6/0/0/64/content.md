# Contents 
* table of contents 
{: toc} 




## Idea

> If the decision to let every commutative ring define a scheme gives
standing to bizarre schemes, allowing it gives a category of schemes
with nice properties ([Deligne](#Deligne98))

In the context of [[category theory]], it is a general phenomenon that

 * Nice [[objects]] tend to form non-nice [[categories]]. 
  
 * Nice categories tend to contain non-nice objects.

Here we take a category to be the "nicer" the more [[limits]], [[colimits]] etc. it admits, and additionally the more good properties like [[exactness properties]], being a [[topos]], etc. it has.

On the other hand, a "nice object" is, loosely speaking, an object in some context which has more special [[properties]] than the generic object in that context will have. For instance [[manifolds]] are nice objects in the context of [[generalized smooth space|generalized smooth spaces]]. [[field|Fields]] are nice objects in the context of [[commutative rings]]. 

Clearly, the more extra properties one imposes, the less likely it is that these are preserved under limits and colimits. For instance 

* not all [[quotients]] $X/G$ of a manifold $X$ by the action of a group $G$ are again manifolds (this is a colimit which fails to exist);

* not all [[fiber products]] $Y \times_X Y$ of surjections $Y \to X$ of manifolds are again manifolds (this is a limit that fails to exist).

* it is often false that the [[coproduct]] of fields (in the category of commutative rings) is again a field. 

## Some nPOV rules of thumb 

Without making any sweeping judgments, a general [[nPOV]] heuristic is that faced with a choice between working with a non-nice category of nice objects and a larger nice category of non-nice objects, it is usually preferable to switch attention to the nice category. For example, instead of working with the category of smooth manifolds, work instead with an ambient category with better properties, such as a category of [[diffeological spaces]] or a model of [[synthetic differential geometry]], in which the category of manifolds is fully embedded. [Moerdijk-Reyes](#MR) can be read largely as an implementation of that philosophy. 

On the other hand, another methodological heuristic is to move from a nice object to a nice category attached to it. For instance, the category of [[modules]] over a field is about as well behaved as it could possibly be, and similarly one often contemplates the category of [[vector bundles]] over a smooth compact manifold. 

## Formalization

The notion of "nice objects" can be formalized to some degree for instance in terms of _Isbell self-duality_ as described in [Lawvere](#Law). 

## References 
 
* {#Deligne98} [[Pierre Deligne]], _Quelques id&#233;es ma&#238;tresses de l'&#339;uvre de A. Grothendieck_, [[Matériaux pour l’histoire des mathématiques au XXe siècle|Mat&#233;riaux pour l'histoire des math&#233;matiques au XX]]$^e$ siecle (Nice, 1996), Societ&#233; Math&#233;matique de France, 1998, pp. 11&#8211;19.

* {#MR} [[Ieke Moerdijk]] and [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]]
 

* {#Law}  [[William Lawvere]], _Taking categories seriously_ ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))


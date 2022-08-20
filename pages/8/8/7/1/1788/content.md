
In fact, a [[simplicial set]] is the [[nerve]] of a [[category]] iff it has *unique* [[inner horn|inner $n$-horn]]-fillers for $n \geq 2$ (e.g. [this Prop.](nerve#sSetIsNerveOfCategoryIffAllInnerHornsHaveUniqueFillers)).
But [[coskeleton|2-coskeletality]] already implies that all $k \geq 4$-horns have unique filles (first uniquely fill the missing $k-1$-face then the interior $k$)-cell. Together with implies that

A [[simplicial set]] is the [[nerve]] of [[category]] iff

1. it is [[coskeleton|2-coskeletal]],

1. all [[inner horn|inner]] 2- and 3-[[horns]] have unique fillers.


So a simplicial set is the nerve of a [[1-category]] iff it is 

1. an [[inner Kan complex]],

2. [[coskeleton|2-coskeletal]] 

(cf. e.g. [[Higher Topos Theory|Lurie 2009, Def. 2.3.4.1]])

and the nerve of an actual [[category]] if the inner $\leq 3$-horn fillers are unique.

In particular, a simplicial set is the nerve of a [[1-groupoid]] iff it is 

1. a [[Kan complex]],

2. [[coskeleton|2-coskeletal]]

and the nerve of an actual [[groupoid]] if the $\leq 3$-horn fillers are unique.

But this characterization now has a lot of redundancy, since with the unique fillers of boundaries of $n \geq 3$-simplices given by 2-coskeltality, we obtain fillers also of all $n \geq 3+1$-horns (first fill the missing $(n-1)$-face and then the interior $n$-cell). Therefore a simplicial set is the nerve of a [[1-groupoid]] already iff it

1. has unique fillers of $\leq 3$-[[horns]] (encoding: (i) [[inverse morphisms]], (ii) [[composition]] and (iii) [[associativity]]);

1. is [[coskeleton|2-coskeletal]] (encoding that associativity in a [[1-category]] is a [[property]], not a [[stuff, structure, property|structure]]).

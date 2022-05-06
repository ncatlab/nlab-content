# Contents
* table of contents
{: toc}

## Definitions

### Definition using the category of simplices

The __fundamental groupoid__ of a [[simplicial set]] $X$
is the [[localization]] $C[C^{-1}]$
of its [[category of simplices]] $C$
(a special case of the [[category of elements]] of a [[presheaf]]).

### Definition using the fundamental category

The __fundamental groupoid__ of a [[simplicial set]] $X$
is the [[localization]] $C[C^{-1}]$
of its [[fundamental category]] $C$,
defined as the [[left adjoint functor]] to the [[nerve functor]]
$$N\colon Cat \to sSet.$$

### Definition using generators and relations

The __fundamental groupoid__ of a [[simplicial set]] $X$
is a [[groupoid]] defined via the following system
of [[generators and relations]] for a [[groupoid]]:

* objects are precisely the vertices of $X$;

* generating isomorphisms are precisely the edges of $X$;

* for every 2-simplex of $X$ we have a relation
$$d_1(\sigma)=d_0(\sigma)\circ d_2(\sigma).$$

## See also

* [[fundamental groupoid]]
* [[fundamental category]]
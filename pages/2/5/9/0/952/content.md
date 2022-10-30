A __symmetric set__ (or __symmetric simplicial set__) is a [[simplicial set]] $X$ equipped with additional _transposition maps_ $t^n_i: X_n \to X_n$ for $i=0,\ldots,n-1$.  These transition maps generate an [[action]] of the [[symmetric group]] $\Sigma_{n+1}$ on $X_n$ and satisfy certain commutation relations with the face and degeneracy maps.  The result is that a symmetric set is a [[presheaf]] of sets on the category [[FinSet]] of [[finite set]]s (or on its [[skeleton]]).

An analogy to keep in mind is
: symmetric set : simplicial set :: [[groupoid]] : [[category]].

This analogy can be formalized by noticing that the skeletal category of finite sets is simply the [[full subcategory]] of [[Cat]] whose objects are the [[localization]]s $[n]^{-1}[n]$ which are groupoids. By the universal property of localization, the usual (simplicial) [[nerve]] of a groupoid has a canonical symmetric structure.

The notion of [[cyclic set]] is intermediate between symmetric sets and simplicial sets.  In particular, any symmetric set, such as the nerve of a groupoid, also has a cyclic structure.


+--{: .query}
[[Mike Shulman|Mike]]: I've never seen this called a "symmetric set" only a "symmetric simplicial set," which additionally has the advantage of being more descriptive.  "Symmetric set" sounds to me like it might also refer to a presheaf on the _groupoid_ of finite sets (sometimes called a "symmetric sequence").  Is there an advantage of "symmetric set" over "symmetric simplicial set?"

[[Zoran Skoda]]: You are right, topologists more often say symmetric simplicial sets/objects, for example one of the papers devoted to the topic by Marco Grandis. But symmetric sets is also used, see for example the quote in Getzler's paper on L-infty integration where he quotes Loday and Fiedorowicz, I heard this shorter term many time from conversations with Jibladze and many others. There is an advantage and that is exactly the theory of crossed simplicial groups in the sense of Loday and Fiedorowicz or skewsimplicial groups in the sense of a bit earlier work fo Krasauskas. The point is to treat dihedral, cyclic, symmetric etc. homologies on the same footing, hence symmetric, cyclic, dihedral etc. sets.
The term symmetric homology is for example in Loday-Fiedorowicz and then in Pirashvili-Richer and so on. I did not hear somebody saying dihedral simplicial sets, or cyclic simplicial sets, though it would be OK with me. I am happy with any solution for nlab and personally
use both expressions in my writings and every day usage. 

[[Mike Shulman|Mike]]: I see the point.  Also, for instance, a [[symmetric spectrum]] is a particular sort of symmetric space, i.e. a symmetric object in spaces in this sense.  So I'm okay with "symmetric set" as a name for this page.
=--

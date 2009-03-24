I was until 2006 a professor of mathematics at the University of Wales Bangor (aka University of Bangor). The University closed down the Mathematics degree and I was retired! Since then I have been on various interesting visiting positions, whilst being Emeritus, retaining an office in the Computer Science section of the university and continuing to work at least as hard as before (I claim).

+--{.query}
Not offering a maths degree is one thing, but it seems that they don\'t even have a maths *department*! Who teaches basic maths courses to the CS (and chemistry, biology, electronics, ...) majors? &#8212;[[Toby Bartels|Toby]]


Your first question is a good one!!!! [[Tim Porter|Tim]]




=--

I am writing a series of notes on the theory and application of crossed gadgetry in algebra and topology, and some parts of these notes (approximately first 7 chapters) have been made available on the web at various times. I am currently trying to write a new chapter on 2-vector spaces and 2-vector bundles, with the emphasis on 'trying'.  


I am also very interested in directed homotopy theory and the application of ideas form the general area of the infinity category/homotopy toolkit in topological data analysis, artificial intelligence, and computer science.




+-- {: .query}
Tim,

This is my first post on any wiki so I am probably violating some protocol. I apologize for that.  

My question is about the Moore complex of a simplicial abelian group. Specifically, it's about the definition of the homotopy groups of a simplicial abelian group A as the homology groups of it's Moore complex. Please bear with me here as I tell you what's on my mind. I hope the source of my confusion will be apparent by the end of this rant. 

A homotopy from X to Y in the category of simplicial abelian groups can be expressed as a morphism X x I --> Y, where I is the analogue in this category of the topological interval and X x I is the diagonal of the obvious bisimplicial abelian group formed from X and I, henceforth called the tensor product of X and I. There is a similar characterisation of homotopies in the category of chain complexes of abelian groups. 

The Dold Kan theorem gives an equivalence of categories:

N : simplicial abelian groups &lt;--> positive chain complexes  of abelian groups: Gamma

It's clear that N preserves the interval and Eilenberg-zilber says that N preserves the tensor product (the tensor product in chain complexes is the Tot of the obvious bicomplex) so N preserves homotopies. In particular it preserves the relation "homotopy equivalent". I suspect that Gamma has the same behaviour, so N is also an "bijection of homotopies".  

Now homotopy groups are defined in terms of homotopies, so it seems to me that the homotopy groups of the two categories should correspond. Why do we define the homotopy groups of a simp ab group to be the homology groups of its Moore complex? 

dan
 
[[Tim Porter|Tim]]:  I think you are meant to ask questions via e-mail, rather than here, but the question is a good one. You can check up the answer in detail in for instance Peter May's old book on Simplicial objects in ALg Top (or similar), but I imagine you want to know WHY as well as the gory details.

An n-simplex in a simplicial abelian group, A, is in the Moore complex if all but the zeroth face is at 0.  Imagine you want to look at an element in $\pi_n(A)$, then it corresponds to a map of a $n$-simplex into $A$, ALL of whose faces are at 0.  It thus gives an element in the kernel of the boundary map of the Moore complex at that level. Of course that element is determined up to homotopy only, so you look at a homotopy between two such elements, and this corresponds to a homotopy between their difference and 0.  But that gives a boundary  as it is a cone on an $n$-simplex and hence is an $n+1$  simplex. (think of this in dimensions 1 and 2 first to see what is happening.)

We thus have that the element in $\pi_n(A)$ corresponded to an element in the Moore coomplex kernel modulo boundaries (and vice versa) so the homotopy of $A$ is isomorphic to the homology of the Moore complex. (This works for non-Abelian simplicial groups as well.)  

Tim


=--
category: people
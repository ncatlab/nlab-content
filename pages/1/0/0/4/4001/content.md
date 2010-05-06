1. [Introduction](#intro)
2. [[Loopy Notation]]
3. [[Smoothly Does It]]
  1. [[Curvaceous Calculus]]
  2. [[Euclidean Loop Spaces]]
  3. [[The Smooth Structure of an Arbitrary Loop Space]]
  4. [[The Loop Space of the Tangent Space]]
  5. [[The Topology of the Loop Space]]
  6. [[Loopy Maps]]
  7. [[Vector Space Idol]]
4. [[Looping Bundles]]
  1. [[The Tangent Space]]
  2. [[Vector Bundles]]
  3. [[Principal and Gauge Bundles]]
  4. [[Connections]]
  5. [[The Enemy of my Enemy is not my Friend]]
5. [[Submanifolds and Tubular Neighbourhoods]]
  1. [[The Fundamental Fibration]]
  2. [[Tubular Neighbourhoods]]
  3. [[Equivariant Tubular Neighbourhoods]]
  4. [[A Not-So-Nice Submanifold]]
6. [[A Miscellany]]
  1. [[Weak Riemannian Manifolds]]
  2. [[More Fun with Based Loops]]
7. References

# Introduction # {#intro}

This series of pages started out as an accompaniment to a series of seminars
given at NTNU, and subsequently at Sheffield University, entitled: "The
Differential Topology of the Loop Space". The purpose of those seminars was to
present an introduction to this topic leading up to the work contained in
[[Andrew Stacey|my]] preprint on the construction of a Dirac operator on loop spaces, [Sta].
This was intended to be accessible to anyone with knowledge of basic finite
dimensional differential topology. Thus there was a reasonable amount of
background material to be explained before the subject of Dirac operators was
broached. The overall outline of this background material was divided as
follows:
     
   1.      The differential topology of loop spaces.
   2.      Spinors in arbitrary dimension.
   3.      The  Dirac  operator  and  the  Atiyah-Singer  index  theorem  in  finite dimensions.

The latter two topics are already superbly covered by books accessible to any
differential topologist, perhaps with a little functional analysis. The book [LM89] is
an excellent introduction to both topics in finite dimensions whilst [PR94] deals
with spinors in arbitrary dimension. A group-centric viewpoint is presented
in [PS86], which is required reading for anyone seriously thinking about loop
spaces.

The main reference for the first topic is [KM97]. Whilst several of the standard
texts on differential topology and geometry deal with infinite dimensional
manifolds, they only do so rigorously with manifolds modelled on Banach
spaces, which for loop spaces this usually means either continuous or
H1-Sobolev
loops. Often smooth and piece-wise smooth loops are used as a source of "useful"
loops within these manifolds, but the space of smooth loops is not given an actual
manifold structure. This is due to the technical difficulties in extending calculus
outside the realm of Banach spaces.

The purpose of [KM97] is to deal with precisely this issue and to set up a theory
of analysis in infinite dimensions in arbitrary topological vector spaces. It goes on to
develop the theory of infinite dimensional manifolds in its broadest setting
which includes smooth loop spaces. However, this means that whilst being an
excellent book, its subject matter is perhaps too broad and too deep for
someone who just wants to know about the differential topology of loop spaces.

The statement that the smooth loop space is a smooth manifold appears
in section 42, about two-thirds of the way through the book. Whilst the
preceding four hundred pages are not all required reading to get to this
point, it is still a somewhat daunting task to extract what one needs for loop
spaces.

Therefore I started writing this document to fill in the details of what I did not
have time to say in my seminars. The intention was to provide a more gentle
introduction than [KM97] but still include the required detail to understand the
differential topology of the space of smooth loops. It subsequently grew
beyond that remit as I thought of more topics that could be included without
increasing the technical difficulty. A brief description of the topics covered is as
follows:

* The smooth structure of the space of smooth loops in a finite dimensional manifold.
      We start by discussing what it means to be smooth outside the realm of
           Banach spaces, focusing particularly on the model spaces for loop spaces.
           Using this we exhibit an atlas for the space of smooth loops and show
           that the transition functions are smooth. Also in this section we show that
           various maps involving loop spaces are smooth.
           

* The basic theory of vector bundles and associated principal and gauge
           bundles on the loop space defined by looping vector bundles on the original
           manifold.
           

      The main theme of this section is that looping something on the original
           manifold gives a corresponding object on the loop space. Thus the loop
           space of the tangent space is (diffeomorphic to) the tangent space of the
           loop space; vector bundles and their frame bundles loop to vector bundles
           and their frame bundles (in a sense) as do connections. We conclude this
           section with an important example where this loopy behaviour fails: the
           loop space of the cotangent bundle is not the cotangent bundle of the loop
           space.
           

*      Some important submanifolds with tubular neighbourhoods.
           

      We show that various submanifolds of a loop space have tubular neighbourhoods.
           In particular, we consider submanifolds defined by imposing some condition
           on values that the loops can take at certain times &#8211; for example, the based
           loop space &#8211; and we consider fixed point submanifolds coming from the
           circle action. One consequence of this is that the fundamental fibration
           $\Omega M \to L M \to M$
           is locally trivial. We conclude with a submanifold that does not have a
           tubular neighbourhood.
           

*      Basic introductions to two topics of further interest: geometry on loop
           spaces and the semi-infinite nature of loop spaces.

           

      We begin with a discussion of some of the issues in infinite dimensional
           geometry  and  prove  some  simple  results  concerning  the  Levi-Civita
           connection  and  geodesics.  We  also  give  a  very  basic  introduction  to
           semi-infinite theory.


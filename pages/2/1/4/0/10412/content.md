
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[scattering amplitudes]] in [[Yang-Mills theory]] are traditionally expressed as sums of typically very many [[Feynman diagrams]], which in turn are [[integrals]] over certain [[algebraic functions]]. At least in  highly [[supersymmetry|supersymmetric]] versions of [[Yang-Mills theory]] such as [[N=4 D=4 super Yang-Mills theory]] this can be expressed more efficiently (see [Dixon 13](#Dixon13) for a review of the general method and see at _[[string theory results applied elsewhere]]_) as fewer [[integrals]] of some integrand over some [[domain]] of certain convex [[polyhedra]] inside a [[positive Grassmanian]] (which is an infinite dimensional space related to the study of the phenomenon of [[total positivity]]). Therefore this has been called the _amplituhedron_ ([Arkani-Hamed & Trnka13](#ArkaniHameTrnka13)).

In slightly more detail, the scattering amplitudes in [[N=4 D=4 super Yang-Mills theory]] can be given as functions of  $4n$ real variables, the [[momenta]] of $n$ scattering [[particles]], and at loop number $\ell$ they are given by $4 \ell$-fold integrals of [[algebraic functions]] of $4n+4 \ell$ real variables. (When $\ell=0$, then ([ABCGPT 12, sections 16.4](#ABCGPT12)) claims that all the [[Galois conjugates]] of the [[algebraic function]] occur symmetrically; so that one indeed has [[rational functions]].)

This formulation is typically a drastic improvement of computational complexity for fixed $k$ ([[helicity]]) and fixed $\ell$ (loop number) but variable $n$. The [[Feynman diagram]] description is exponential in $n$, while the complexity of the amplituhedron description grows much more mildly.

In particular for $k = 0$ and $k = 1$ the resulting amplitude is just 0 and the amplituhedron description gives this immediately, but for $k = 1$ there are still many nontrivial Feynman integrals. That the sum of all these indeed vanish was maybe known earlier, though, due to a result by Parke and Taylor.

For $k = 2$ again there is the "[[Parke-Taylor formula]]" efficiently expressing the amplitudes [[MHV amplitudes]].


## Related concepts

* [[motives in physics]]

* [[scattering amplitudes]]

* [[Yang-Mills theory]]

  * [[super Yang-Mills theory]]

  * [[Tr(ϕ³)]]

* [[associahedron]]

* [[cosmohedron]]

* [[surfaceology]]

* [[Feynman polytope]]

## References

Review:

* {#Dixon13} [[Lance Dixon]], _Calculating Amplitudes_, December 2013 ([web](http://www.preposterousuniverse.com/blog/2013/10/03/guest-post-lance-dixon-on-calculating-amplitudes/))
 
* [[Henriette Elvang]], [[Yu-tin Huang]], *Scattering Amplitudes*, Cambridge University Press (2015) &lbrack;[arXiv:1308.1697](http://arxiv.org/abs/1308.1697), [doi:10.1017/CBO9781107706620]( https://doi.org/10.1017/CBO9781107706620)&rbrack;

* Livia Ferro, Tomasz Lukowski, _Amplituhedra, and Beyond_, Topical Review invited by Journal of Physics A: Mathematical and Theoretical ([arXiv:2007.04342 ](https://arxiv.org/abs/2007.04342))

More mathematical review:

* Shounak De, Dmitrii Pavlov, Marcus Spradlin, [[Anastasia Volovich]]: *From Feynman diagrams to the amplituhedron: a gentle review* &lbrack;[arXiv:2410.11757](https://arxiv.org/abs/2410.11757)&rbrack;

* Kristian Ranestad, Bernd Sturmfels, Simon Telen: *What is Positive Geometry?* &lbrack;[arXiv:2502.12815](https://arxiv.org/abs/2502.12815)&rbrack;



For scattering amplitudes via the "amplituhedron" the integrand is discussed in

* {#ABCGPT12} [[Nima Arkani-Hamed]], Jacob L. Bourjaily, Freddy Cachazo, [[Alexander Goncharov|Alexander B. Goncharov]], [[Alexander Postnikov]], Jaroslav Trnka, _Scattering amplitudes and the positive Grassmannian_, [arxiv/1212.5605](http://arxiv.org/abs/1212.5605) 


and the integration domain in

* {#ArkaniHameTrnka13} [[Nima Arkani-Hamed]], Jaroslav Trnka, _The Amplituhedron_, [arxiv/1312.2007](http://arxiv.org/abs/1312.2007)
 

Simple aspects of four particle scattering are treated in

* [[Nima Arkani-Hamed]], Jaroslav Trnka, _Into the Amplituhedron_, [arxiv/1312.7878](http://arxiv.org/abs/1312.7878)
 {#ArkaniHameTrnka13b}.

Earlier lecture notes and announcements include 

* Jaroslav Trnka, _The amplituhedron_, [pdf](http://www.staff.science.uu.nl/~tonge105/igst13/Trnka.pdf)

* Nima Arkani-Hamed, _Grassmannian polytopes and scattering amplitudes_, lecture at Perimeter Institute, [video](http://pirsa.org/11080047)

Informed online discussion includes 

* Logan Maingi on MathOverflow [here](http://mathoverflow.net/questions/142841/the-amplituhedron-minus-the-physics/143421#143421) 

* David Speyer [here](http://www.scottaaronson.com/blog/?p=1537#comment-88216)

Journalistic coverage includes

* Natalie Wolchover, _A Jewel at the Heart of Quantum Physics_, Quanta Magazine, Sep 17, 2013 (hosted at Simons Foundation) [html](https://www.simonsfoundation.org/quanta/20130917-a-jewel-at-the-heart-of-quantum-physics)

See also

* Wikipedia: _[Amplituhedron](http://en.wikipedia.org/wiki/Amplituhedron)_
* Thomas Lam, _Amplituhedron cells and Stanley symmetric functions_, 
[arxiv/1408.5531](http://arxiv.org/abs/1408.5531)

Some discussion about the use of amplituhedra in physics occurred on the category theory Zulip [here](https://categorytheory.zulipchat.com/#narrow/channel/411259-theory.3A-science/topic/Amplituhedron.2C.20associahedron.2C.20and.20related.20approaches). 

[[!redirects amplituhedron]]
[[!redirects amplituhedra]]
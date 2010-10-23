
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

"Unitary [[irrep]]" is a shorthand for **unitary [[irreducible representation]]** of a [[topological group]] $G$, i.e., a continuous [[group]] [[homomorphism]] 

$$U: G \to U(H)$$ 

into the [[unitary group]] of a [[Hilbert space]] $H$ that is irreducible in the usual sense of [[representation theory]]. 

In this and related articles, we study such representations in the case where 

$$G = SL_2(\mathbb{C}) \ltimes \mathbb{R}^4$$ 

is the [[universal cover]] of the [[connected]] component of the identity of the [[Poincare group]], which is important in the study of [[quantum field theory]]. A more physical name for such a representation is "[[elementary particle]]", and we will often use that term in this article. (NB: "elementary particle" will always refer to the formal mathematical notion.) 

A full rounded account could become large; see the [blog discussion](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html), which despite its size was left in a still-nascent state. However, in a nutshell, the basic theorem is that (elementary) particles are classified up to isomorphism according to their [[mass]] and [[helicity]]; mass is a continuous parameter and helicity is a discrete parameter. 

This theorem in commonly ascribed to [[Eugene Wigner]]. In the blog discussion, [[John Baez]] wrote 

* I think he completely classified the 'positive energy' representations, which are the ones of greatest importance in physics.  This leaves out exotic, unobserved representations like negative-energy particles, tachyons and other freaks too scary to mention here. But to be honest, I'm not sure exactly how far he got. What really matters to me are the positive energy reps. I hope that we can use this blog entry as a forum to find out what Wigner proved, and understand its implications for particle physics.  If we all team up, we'll all learn a lot of stuff.

I'm not sure any of these 'freaks' are too scary to mention _here_; this is mathematics after all. In any event, John later clarified what he meant by positive energy representations: 

* Those for which time translation acts as 
$$\exp(- i H t)$$ 
where $H$ is a nonnegative, nonzero selfadjoint operator. (In physics, $H$ is called the 'Hamiltonian' or 'energy'.) 

## Related entries

Relevant topics in a full account will include 

* [[spectral theorem|Spectral theorem]]

* [[rigged Hilbert space|Rigged Hilbert spaces]] and [[direct integral|direct integrals]]

* [[induced representation]]s

* [[helicity]], [[spin]]

* [[Klein-Gordon equation]] 

* [[Dirac equation]] 

* [[spin-statistics theorem]]

* [[Maxwell equation]] 

* [[Stone's theorem]] 

* [[Mackey theory]]


Much lies ahead... 

## Tentative notes, to be expanded on... 

In the first place, physicists tend to be a little carefree with the mathematics, so this account is written from the point of view of a 'stupid' mathematician (for the moment Todd Trimble) who wants to get details straight and precise. 

For example, physicists tend to talk about "eigenstates" as if they were elements of the Hilbert space, and other states as linear combinations of eigenstates, whereas really we are dealing with some more complicated technology like rigged Hilbert spaces or direct integrals instead of direct sums. Failure to mention such details places hurdles of communication between physicists and mathematicians. In addition, there are stylistic differences in presentation, where a physicist will happily deal with formulas replete with lots of subscripts and superscripts, whereas many mathematicians prefer dealing with more conceptual, less notation-heavy explanations. 

### Rigged Hilbert spaces 



[[!redirects unitary irreps of the Poincare group]]
[[!redirects unitary irrep of the Poincaré group]]
[[!redirects unitary irreps of the Poincaré group]]
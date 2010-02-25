
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[quantum mechanics]] a _state_ of a physical system with $n \in \mathbb{N}$ degrees of freedom may be thought of as being encoded by a complex [[hermitian matrix|hermitian]] $n \times n$ [[matrix]] $\rho \in Mat(n\times n, \mathbb{C})$ with non-negative [[eigenvalue]]s and unit [[trace]]. This is called a **[[density matrix]]** .

Any physical process is supposed to take physical states into physical states. Hence it must be some operation that sends density matrices to density matrices: it should be a linear map of [[vector space]]s

$$
  U : Mat(n \times n, \mathbb{C}) \to Mat(k \times k, \mathbb{C})
$$

that preserves the subset of density matrices, in that it 

* preserves the trace of matrices;

* takes hermitian matrices with non-negative eigenvalues to hermitian matrices with non-negative eigenvalues.

The relevance of this concept of **(completely) positive trace-preserving maps** apparently became widely recognized due to the article

* Choi, _Completely positive linear maps on complex matrices_ , Linear Algebra and its Applications Volume 10, Issue 3, June 1975, Pages 285-290

The concept was picked up in the physics literature, where (completely) positive trace-preserving maps were synonymously renamed to **quantum channels**, reflecting the physical interpretation of these maps: 

Notably in [[quantum information theory]] one thinks of each way to send a signal from one quantum system to another as being modeled by such a map.

A useful review of the notion in this context is in section 1.7 of

* Caleb J. O'Loan, _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([pdf](http://arxiv.org/abs/1001.3971))



More generally, the definition can be extended in a more-or-less obvious way from systems with a finite number of degrees of freedom, to general systems. This requires replacing the finite dimensional complex vector space $\mathbb{C}^n$ with an arbitrary [[Hilbert space]] $\mathcal{H}$ and the space of matrices by a suitable space of linear operators on that Hilbert space.

## Details

+-- {: .un_defn}
###### Definition

Let $k,n \in \mathbb{N}$.

A matrix $A \in Mat(n \times n, \mathbb{C})$ is called **positive** if it is hermitian -- if $A^\dagger = A$ -- and if all its eigenvalues (which then are necessarily real) are non-negative.

A linear map (morphism of [[vector space]]s of matrices)

$$
  \Phi : Mat(n \times n, \mathbb{C}) \to 
   Mat(k \times k, \mathbb{C})
$$

is called **positive** if it takes positive matrices to positive matrices.

The map $\Phi$ is called **completely positive** if for all $p \in \mathbb{N}$ the [[tensor product]]

$$
  \Phi \otimes Id_{Mat(p\times p),\mathbb{C}} :
  Mat(n \times n , \mathbb{C})\otimes
  Mat(p \times p , \mathbb{C})
  \to
  Mat(k \times k , \mathbb{C})\otimes
  Mat(p \times p , \mathbb{C})
$$

is positive.

=--

+-- {: .un_theorem}
###### Theorem

A map $\Phi$ as above is _completely positive_ precisely if there exists a [[set]] $I$ and an $I$-family $\{E_i \in Mat(k \times n, \mathbb{C}| i \in I)\}$ of matrices, such that for all $A \in Mat(n \times n, \mathbb{C})$ we have

$$
  \Phi(A) = \sum_{i \in I} E_i A E_i^\dagger
  \,.
$$

Moreover, such $\Phi$ preserves the trace of matrices precisely if 

$$
  \sum_{i \in I} E_i^\dagger E_i = Id_{Mat(n \times n, \mathbb{C})}
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is theorem 1 in 

* Choi, _Completely positive linear maps on complex matrices_ , Linear Algebra and its Applications Volume 10, Issue 3, June 1975, Pages 285-290

=--



The matrices $\{E_i\}$ that are associated to a completely positive and trace-preserving map by the above theorem are called **Kraus operators**.

In the physics literature the above theorem is then phrased as: _Every quantum channel can be represented using Kraus operators_  .

Notice that the identity map is clearly completely positive and trace preserving, and that the composite of two maps that preserve positivity and trace clearly still preserves positivity and trace. Therefore we obtain a [[category]] $QChan \subset Vect$ -- a [[subcategory]] of [[Vect]]${}_{\mathbb{C}}$ -- whose

* objects are the vector spaces $Mat(n \times n, \mathbb{C})$ fir all $n \in \mathbb{N}$;

* morphism are completely positive and trace-preserving linear maps $\Phi : Mat(n\times n , \mathbb{C}) \to Mat(m \times m, \mathbb{C})$;

* composition of morphisms is, of course, the composition in [[Vect]], i.e. the ordinary composition of linear maps.

## References


* Choi, M. (1975). _Completely positive linear maps on complex matrices_ , Linear Algebra and its Applications 10: 285&#8211;290.


* Smolin, John A., Verstraete, Frank, and Winter, Andreas _Entanglement of assistance and multipartite state distillation_ , Phys. Rev. A, vol. 72, 052317, 2005 ([arXiv:quant-ph/0505038](http://arxiv.org/abs/quant-ph/0505038))

* Mendl, Christian B. and Wolf, Michael M. (2009) _Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem_ , Commun. Math. Phys. 289, 1057-1096 (2009) ([arXiv:0806.2820](http://arxiv.org/abs/0806.2820))

* O'Loan, Caleb J.,  _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([pdf](http://arxiv.org/abs/1001.3971))

* Watrous, John (2008). _Mixing doubly stochastic quantum channels with the completely depolarizing channel_ ([arXiv](http://arxiv.org/abs/0807.2668))


***

## Previous version

> Here is a previous version of this entry started by [[Ian Durham]], that led to a lot of discussion.

+--{: .query} 

[[Urs Schreiber]]: As the following disucssion shows, there is a general feeling that this entry here is in need of clarification on what exactly it is supposed to be about, and what it is good for. It would seem to me that this could easily be achieved based on some standard authorative reference that introduces the notion and discusses it. So: what are good references on the notion "qunatum channel", in the sense apparently meant here? Pointers to a specific page in a specific article would be appreciated.

[[Ian Durham]]: Thanks for the suggestion.  (By the way, when does it become kosher to delete all the comments between people in order to make the page look a little less cluttered?)

=--
For those who are looking for some background reading on quantum channels, here is a short bibliography of papers on the arXiv that give some details about quantum channels:

The mathematical formalism and some of the initial results are due to Choi:

Choi, M. (1975). Completely positive linear maps on complex matrices, 
Linear Algebra and its Applications 10: 285&#8211;290.

Good overviews and background can be found in:

Smolin, John A., Verstraete, Frank, and Winter, Andreas (2005) [Entanglement of assistance and multipartite state distillation](http://arxiv.org/abs/quant-ph/0505038) Phys. Rev. A, vol. 72, 052317, 2005.

Mendl, Christian B. and Wolf, Michael M. (2009) [Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem](http://arxiv.org/abs/0806.2820), Commun. Math. Phys. 289, 1057-1096 (2009).

O'Loan, Caleb J. (2010). [Topics in Estimation of Quantum Channels](http://arxiv.org/abs/1001.3971), PhD thesis, University of St. Andrews, pp.13-15.

Watrous, John (2008). [Mixing doubly stochastic quantum channels with the completely depolarizing channel](http://arxiv.org/abs/0807.2668)

A __quantum channel__ is a mapping between [[Hilbert spaces]], $\Phi : L(\mathcal{H}_{A}) \to L(\mathcal{H}_{B})$, where $L(\mathcal{H}_{i})$ is the family of operators on $\mathcal{H}_{i}$. 

+--{: .query} 

[[Todd Trimble]]: Hi, Ian. I hope I can give some constructive advice. First, it's good form to specify your terms, e.g., "given a [[Hilbert space]] $H$, let $L(H)$ denote the space ... (please specify exactly: the space of all bounded linear operators $\Psi: H \to H$, or of such operators that are completely positive trace-preserving, or what?)". Terms such as "completely positive operator" or "trace-preserving operator" should be placed between double brackets so that readers can follow a link either to an existing page or to a to-be-created page, like so: [[completely positive operator]]. Then, you also need to specify how you are considering this thing $L(H)$: if you are considering it as a [[C-star algebra]], then say so. If you don't do that, the reader has no sense of what "mapping" should mean here (should it mean a morphism in the category of Banach spaces, or a morphism in the category of $C^\star$-algebras, or what?). Finally, I think I would find the following formulation less confusing: "A _quantum channel_ between Hilbert spaces $H_A$, $H_B$ (any particular reason why $H_A$ and $H_B$, as opposed to $H_1$, $H_2$ or $H$, $H'$?) is a $C^\star$-algebra mapping (or whatever kind of mapping it is) $\Phi: L(H_A) \to L(H_B)$." The way you have it, it looks as though you're suggesting that $L(H_A)$, $L(H_B)$ are the Hilbert spaces, and I don't think that's what you mean. 

Ideally, the nLab is a place where a newcomer (relative to some area) could go and not be confused by unstated context. That's perhaps the first lesson of category theory: a category is a _context_, a specification of the way we consider the objects before us (whether as vector spaces or Banach spaces or $C^\star$-algebras or what have you). Being very careful to specify the context or category in which one is working at any given moment is a fundamental precept in our business and promotes clarity of thinking. 

[[Ian Durham]]: Thanks for the assistance Todd.  I think part of the problem I'm having is that I seem to get contradictory advice from a lot of people.  So, originally, I had it as a mapping between $C^{*}$-algebras but got talked out of it.  Indeed, you are correct that by $L(H_{A})$ and $L(H_{B})$ I actually mean a mapping between the algebras on the Hilbert space.  I think the other problem is that a definition that is generally good enough for physicists is often not good enough for mathematicians and I'm finding myself struggling to improve the clarity and specificity.  As to why I use $H_{A}$ versus $H_{1}$, it's a physics thing and is usually because $A$ and $B$ are either systems or spaces of operators or something that nature. 

[[Todd Trimble]]: If you were writing a paper for an in-crowd of physicists, then I could better sympathize with taking liberties. But since you're here in the nLab, where readers and contributing authors are mostly mathematicians, a more careful and meticulous approach is required. (My own philosophy is that it's never a bad idea to submit to such discipline where the foundations of a subject are being laid down.) 

Could I get you to clarify what $L(H)$ is, exactly? The $C^\star$ algebra of all bounded linear maps from $H$ to $H$? Or something else? 

Finally: while we always welcome positive contributions, most of us are fairly busy with projects of our own. Therefore I might ask that you take the opportunity to look around the nLab and get an idea of what other people are involved in and see how your own interests fit in. (To this end, it would probably help to read the discussion and comments boards of the nForum). If you have pet projects where you're not yet ready to specify all the terms rigorously, you might consider applying for a personal webpage at the Lab where you can work stuff out and figure out how it's going to connect to other stuff on the Lab. (We don't like islands of isolated or sandbox activity scattered about the Lab proper.) If you have queries about any of that, the nForum is a proper venue. 

[[Ian Durham]]: Todd, I appreciate your comments.  I was under the impression from the front page of nLab that this is like an "open lab notebook."  My apologies if I was mistaken.  I had looked around nLab and there seemed to be a copious amount of physics-related material on here so I expected a mixed bag in the way of audience.  Honestly, I have been working on this for more than a year.  I thought I had a pretty solid statement and proof and thought it would add something to the discussion (you can take a look at the revisions).  As for being busy, you can have my job if you want it.  I'm presently scheduled for three simultaneous meetings this afternoon and am still waiting to hear from the Dean which one I should attend, not to mention the fact that I have a kid at home with a stomach bug and an 80-minute commute (one-way).  And that's just a brief overview.  So I understand but I have had very little in the way of assistance over the course of the past year so I turned to online sources like nLab and MathOverflow.

=--

+--{: .query}
[[David Roberts]]: Can we write this as:

>A __quantum channel__ is an arrow in a category whose objects are Hilbert spaces, and the arrow itself is a morphism of C-star algebras $\Phi : L(\mathcal{H}_{A}) \to L(\mathcal{H}_{B})$, where $L(\mathcal{H}_{i})$ is a *-subalgebra of $B(\mathcal{H}_i)$ (if this is the case) Clearly one cannot just take a family of operators and then say by fiat they can be considered as a C-star algebra.


[[Ian Durham]]:(What's the accepted formatting for replying to a query by the way?)  Anyway, in answer to your question, I would say "maybe."  So, the first thing I would say is that this construction (as I have it written) isn't what I originally had.  I originally had (in a paper I was working on) something akin to what you wrote, but several people commented on it and said it should be the way I wrote it here.  Here's (I think) the rationale: since quantum channels can also carry classical information, i.e. $\Phi : L(\mathcal{H}_{A}) \otimes C(X) \to L(\mathcal{H}_{B})$, where $C(X)$ where $C(X)$ is the space of [[continuous functions]] on some space $X$, the Hilbert spaces are not necessarily of the same dimension.  But in order to form a monoid (which I wish to do in order to make use of Cayley's theorem), I wanted a single object.  So I wanted to make the input and output space the same on some level.  A C*-algebra lets me do that.  Does that make sense?  So it not only generalizes it but also gives me the flexibility to use it for something else (at least that was the intent).

[[David Roberts]]: (just keep going between the last comment and the equals-hyphen-hyphen which closes the query. Also starting with your name flags to people who stumble on the entry who is \'speaking\'. I added your name above so my quotation didn't run into your reply) I would suggest, that the category is \'better\' than the monoid, and instead of Cayley the [[Yoneda lemma]] may be handy to get an analogous result. You wrote

>several people commented on it and said it should be the way I wrote it here. 

to which I reply they probably weren't category theorists :)

[[Ian Durham]]: And you would probably be right.  It's amazing how many mathematicians have no clue about category theory.  I expect it of my fellow physicists, but mathematicians?  Well, anyway, I digress.  Categories.  It's like the old saying about the turtles - it's categories all the way down (or up).  I will take a look at the Yoneda lemma.  Since we're on the topic, let me explain my justification for originally going with Cayley's theorem.  In quantum mechanics we like unitaries because they correspond to physical things like beamsplitters, phase shifters, butter knives, etc.  If I start with a monoid (a single-object category with all the arrows isomorphisms), I have a group.  Via Cayley's theorem I can then find an isomorphism to a permutation group.  If that permutation group is finite, then it has a representation in terms of unitaries.  That would be ideal.  But, on a more general note, I also want this to be useful to others (hence nLab) so categories seems the way to go.  (Thanks for all the help, by the way.  This is why I came to nLab.  In case you're interested, I'm attempting to resolve the quantum version of Bikrhoff's theorem using categories which is where this all came from.)

_Harry Gindi_: Using Cayley's theorem here or anywhere is pointless.  You're missing the point of what's going on here.  I also doubt that the people who you asked would tell you to write something that's totally incoherent.  You do yourself a great disservice by blaming this on other people.

_Yemon Choi_: the use of Cayley's theorem still puzzles me. If all you want to know is that the group is finite, then Cayley's theorem tells you nothing towards this: you would either know this at the start, or else have to find an example.

Categories would be useful if you wanted to look at groupoids, I suspect.

By the way, presuming how knowledgeable or fond of category theory some of us are might be a touch presumptuous, no?

[[Ian Durham]]: Harry, would you please just leave me the hell alone?  I've left MathOverflow.  There was no need to follow me here.  Until you showed up, people here seemed to be relatively nice and helpful (and I can't believe at my age I'm even saying this to a college sophomore - I should have learned to ignore people like you a long time ago).

Yemon, I never said anyone at MathOverflow was ignorant of category theory.  I was referring to other mathematicians I know and work with.  In regards to Cayley's theorem please see above for a rough idea of what I was attempting to do or see my paper on the arXiv about this (which Pete Clark thinks I should retract and which I will admit isn't that good).

=--
In general, we are interested in completely positive trace-preserving (CPTP) maps.  

> Zoran: what this ugly acronym means ? We should have an antiacronym point of view in nlab, whenever the acronyms are not in hugely wide use!

> Reply to Zoran: I have corrected it.  However, I was under the impression it was in wide use.  I used it on MathOverflow without a problem and certainly anyone working in quantum information theory (which is what this is under) should know it.

>Harry: What is "the family" of operators on $\mathcal{H}_i$?  A family taking values in $X$ is just a function $I\to X$, where $I$ is called the index.  

The operator spaces can be interpreted as $C^{*}$-[[C-star algebra|algebras]] and thus we can also view the channel as a mapping between $C^{*}$-algebras, $\Phi$: $A \to B$.  Since quantum channels can carry classical information as well, we could write such a combination as $\Phi : L(\mathcal{H}_{A}) \otimes C(X) \to L(\mathcal{H}_{B})$, where $C(X)$ is the space of [[continuous functions]] on some space $X$ and is also a $C^{*}$-algebra.  

+--{: .query}
[[David Roberts]]: This would constitute, continuing the remark above, another category, where the objects are Hilbert spaces and the morphisms are pairs $(X,\Phi: L(\mathcal{H}_{A}) \otimes C(X) \to L(\mathcal{H}_{B}))$. Not sure if this is the case, though, as the proof below doesn't seem to relate very well.

[[Ian Durham]]: Any suggestions on how to restructure the proof so that it works for categories?
=--

In other words, whether or not classical information is processed by the channel, it (the channel) is a mapping between $C^{*}$-algebras.  

>Zoran: the point of view that quantum channels are used for processing information is very biased point of view of one of the engineering fields. In nuclear physics multichannel processes were used half a century ago to formulate nonhermitean perturbation theory, where various emissions of particles, radiation and heat within a nucleus leads to dissipation. We should have a general point of view and not be crippled by somebody's particular engineering fad. 

> Reply to Zoran: Maybe, but the word "channel" (according to the dictionary) implies an information processing context and, besides, that is how they are used in quantum information theory which is what this page is about.  I'm not sure I'd call it a "fad" either.  I go to enough cross-disciplinary meetings to know that its a paradigm that runs across a number of fields and sub-fields.

>[[David Roberts]]:I see Zoran's use as perfectly consistent with the concept of a channel as 'a route through which anything passes or progresses'(dictionary.com - not the best reference, but sufficient) (in that case, particle emission). From an organisational point of view, I would prefer to have a page on quantum channels in generality with pointers to places they are used, and a separate page on quantum information theory, describing among other things how quantum channels are used in that context.

>[[Ian Durham]]: I would be fine with that.  My only point is that, it had always been my understanding that the use of the word "channel" in this context can be traced back to Shannon and von Neumann using it in an information theoretic context.  I've honestly never heard it used otherwise (caveat: obviously I am aware of its use in geography and elsewhere, I simply meant I'd never seen it used in physics in any other context).

> [[David Roberts]]: I was thinking more the analogy with biology, with channels passing various chemicals in and out of cells (cf particles in and out of atoms)

> [[Ian Durham]]: Doh!  Completely forgot about that use.  Well, apparently I am very much mistaken in this regard.  In any case, I definitely would be fine with a general discussion of channels with a pointer here.

Note, however, that these are not necessarily the same $C^{*}$-algebras.  Since the channels are represented by square matrices, the input and output $C^{*}$-algebras must have the same dimension, $d$.  Thus we can consider them both subsets of some $d$-dimensional $C^{*}$-algebra, $C$, i.e. $A \subset C$ and $B \subset C$. Thus a quantum channel is a mapping from $C$ to itself.


+--{: .query}
[[David Roberts]]: One needs to be careful with this approach, because it is no different to calling on the [[Nash embedding theorem]] and saying all smooth maps between finite dimensional Riemannian manifolds are maps from $\mathbf{R}^N$ to itself. They are _not_ maps from $C$ to itself, because we do not know _a priori_ where the complement of the source algebra in $C$ is mapped. 

> Mmm, ok, good point.  Hmmm.  Again, my justification is because of what I wanted to use it for and also because I wanted a nice, generalized definition that could be used in a category-theoretic way.

[[David Roberts]]: In that case I echo my claim above: stick with the category and forsake the monoid. It shouldn\'t be any more tricky.
=--



The following is a proof that a quantum channel is a [[category]].  The proof actually proves it is a [[monoid]], but the need for it to be a category becomes more clear when we start dealing with these things en masse.

+-- {: .un_prop}
###### Proposition

The quantum channels $t: L(\mathcal{H}) \to L(\mathcal{H})$, together with the $d$-dimensional $C^{*}$-algebra, $C$, on which they act, forms a category we call $\mathbf{Chan}(d)$, where $C$ is the sole object and the quantum channels $t$ are the arrows.
=--

+-- {: .proof}
###### Proof
Consider the quantum channels

$\begin{aligned}
r: L(\mathcal{H}_{\rho}) \to L(\mathcal{H}_{\sigma}) & \where &
\sigma=\sum_{i}A_{i}\rho A_{i}^{\dagger} \\
t: L(\mathcal{H}_{\sigma}) \to L(\mathcal{H}_{\tau}) &
\where &
\tau=\sum_{j}B_{j}\sigma B_{j}^{\dagger} 
\end{aligned}$

where the usual properties of such channels are assumed (e.g. trace preserving, etc.).  We form the composite $t \circ r: L(\mathcal{H}_{\rho}) \to L(\mathcal{H}_{\tau})$ where


$\begin{aligned}
\tau & = \sum_{j}B_{j}\left(\sum_{i}A_{i}\rho A_{i}^{\dagger}\right)B_{j}^{\dagger}  \\
& = \sum_{i,j}B_{j}A_{i}\rho A_{i}^{\dagger}B_{j}^{\dagger} \\
& = \sum_{k}C_{k}\rho C_{k}^{\dagger} 
\end{aligned}$

and the $A_{i}$, $B_{i}$, and $C_{i}$ are Kraus operators.

Since $A$ and $B$ are summed over separate indices the trace-preserving property is maintained, i.e. $\sum_{k} C_{k}^{\dagger}C_{k}=\mathbb{1}$.

For a similar methodology see [Nayak and Sen](http://arxiv.org/abs/quant-ph/0605041).

We take the identity arrow, $1_{\rho}: L(\mathcal{H}_{\rho}) \to L(\mathcal{H}_{\rho})$, to be the time evolution of the state $\rho$ in the absence of any channel.  Since this definition is suitably general we have that $t \circ 1_{A}=t=1_{B} \circ t \quad \forall \,\, t: A \to B$.

Consider the three unital quantum channels $r: L(\mathcal{H}_{\rho}) \to L(\mathcal{H}_{\sigma})$, $t: L(\mathcal{H}_{\sigma}) \to L(\mathcal{H}_{\tau})$, and $v: L(\mathcal{H}_{\tau}) \to L(\mathcal{H}_{\upsilon})$ where $\sigma=\sum_{i}A_{i}\rho A_{i}^{\dagger}$, $\tau=\sum_{j}B_{j}\sigma B_{j}^{\dagger}$, and $\eta=\sum_{k}C_{k}\tau C_{k}^{\dagger}$.  We have

$\begin{aligned}
v \circ (t \circ r) & = v \circ \left(\sum_{i,j}B_{j}A_{i}\rho A_{i}^{\dagger}B_{j}^{\dagger}\right) = \sum_{k}C_{k} \left(\sum_{i,j}B_{j}A_{i}\rho A_{i}^{\dagger}B_{j}^{\dagger}\right) C_{k}^{\dagger}  \\
& = \sum_{i,j,k}C_{k}B_{j}A_{i}\rho A_{i}^{\dagger}B_{j}^{\dagger}C_{k}^{\dagger} = \sum_{i,j,k}C_{k}B_{j}\left(A_{i}\rho A_{i}^{\dagger}\right)B_{j}^{\dagger}C_{k}^{\dagger}  \\
& = \left(\sum_{i,j,k}C_{k}B_{j}\tau B_{j}^{\dagger}C_{k}^{\dagger}\right) \circ r = (v \circ t) \circ r
\end{aligned}$.

and thus we have associativity.  Note that similar arguments may be made for the inverse process of the channel if it exists (it is not necessary for the channel here to be reversible).
=--


[[!redirects quantum channel]]
[[!redirects quantum channels]]

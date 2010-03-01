
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

* Caleb J. O'Loan, _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))



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

* objects are the vector spaces $Mat(n \times n, \mathbb{C})$ for all $n \in \mathbb{N}$;

+--{: .query}
[[Ian Durham]]: If the objects are the set of linear operators on the Hilbert space in question, is $QChan$ small?  Or, if we could make sub-categories of QChan for sets of linear operators of different dimension, could we then use these to make a commutative square?

[[David Roberts]]: Let me be the first to say that I'm not sure what you're asking with regard to the commutative square. But there are certainly subcategories $QChan_n$ with the only object $Mat(n \times n, \mathbb{C})$. More natural would be to allow arbitrary $End(V)$ where $V$ is an $n$-dimensional $\mathbb{C}$-vector space, as then different $V$ could correspond to different representations, say. But in respect of the next comment box, I don't think that this was the category you were after, so this may be a moot point. Unfortunately I don't know enough relevant physics to make that call.

[[Urs Schreiber]]: there is one object of $QChan$ per element $n$ of the set of natural numbers, namely the vector space $Mat(n \times n, \mathbb{C})$. So $QChan$ has a _set_ of objects, namely $Obj(QChan) \simeq \mathbb{N}$ and hence is certainly a [[small category]]. (I don't know which commuting squares are meant.)

=--

* morphism are completely positive and trace-preserving linear maps $\Phi : Mat(n\times n , \mathbb{C}) \to Mat(m \times m, \mathbb{C})$;

* composition of morphisms is, of course, the composition in [[Vect]], i.e. the ordinary composition of linear maps.

+--{: .query}
[[David Roberts]]: I was thinking that perhaps the objects of the category were the vector/Hilbert spaces, and the arrows were the completely positive and trace-preserving maps between the matrix algebras. In this instance, the category theoretical content seems that it would be more detailed than \'it\'s just a subcategory of Vect\'.

[[Ian Durham]]: Yes!  That was what my original plan was.  The idea was that it would be possible to create a monoid if the input and output Hilbert space was the same which would give it possibly interesting group theoretic properties (namely Cayley's theorem which would potentially allow me to find some morphism to unitaries which we like in quantum mechanics because they describe system evolution).

[[Urs Schreiber]]: certainly the quantum channels that go $Mat(n \times n , \mathbb{C}) \to Mat(n \times n, \mathbb{C})$ form a monoid. This is the endomorphism monoid $End_{QChan}(n)$ in $QChan$ on the object $n$, i.e. on the object $Mat(n \times n , \mathbb{C})$.

=--

## References


* Choi, M. (1975). _Completely positive linear maps on complex matrices_ , Linear Algebra and its Applications 10: 285&#8211;290.


* Smolin, John A., Verstraete, Frank, and Winter, Andreas _Entanglement of assistance and multipartite state distillation_ , Phys. Rev. A, vol. 72, 052317, 2005 ([arXiv:quant-ph/0505038](http://arxiv.org/abs/quant-ph/0505038))

* Mendl, Christian B. and Wolf, Michael M. (2009) _Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem_ , Commun. Math. Phys. 289, 1057-1096 (2009) ([arXiv:0806.2820](http://arxiv.org/abs/0806.2820))

* O'Loan, Caleb J.,  _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))

* Watrous, John (2008). _Mixing doubly stochastic quantum channels with the completely depolarizing channel_ ([arXiv](http://arxiv.org/abs/0807.2668))


***

## Previous version

> Here is a previous version of this entry started by [[Ian Durham]], that led to a lot of discussion.  The discussion has been gathered together below this previous version unless it related directly to a point in this version.


=--
In general, we are interested in completely positive trace-preserving (CPTP) maps.  

> Zoran: what this ugly acronym means ? We should have an antiacronym point of view in nlab, whenever the acronyms are not in hugely wide use!

> Reply to Zoran: I have corrected it.  However, I was under the impression it was in wide use.  I used it on MathOverflow without a problem and certainly anyone working in quantum information theory (which is what this is under) should know it.

>Harry: What is "the family" of operators on $\mathcal{H}_i$?  A family taking values in $X$ is just a function $I\to X$, where $I$ is called the index.  

The operator spaces can be interpreted as $C^{*}$-[[C-star algebra|algebras]] and thus we can also view the channel as a mapping between $C^{*}$-algebras, $\Phi$: $A \to B$.  Since quantum channels can carry classical information as well, we could write such a combination as $\Phi : L(\mathcal{H}_{A}) \otimes C(X) \to L(\mathcal{H}_{B})$, where $C(X)$ is the space of [[continuous functions]] on some space $X$ and is also a $C^{*}$-algebra.  

+--{: .query}
[[David Roberts]]: This would constitute, continuing the remark above, another category, where the objects are Hilbert spaces and the morphisms are pairs $(X,\Phi: L(\mathcal{H}_{A}) \otimes C(X) \to L(\mathcal{H}_{B}))$. Not sure if this is the case, though, as the proof below doesn't seem to relate very well.

[[Ian Durham]]: Any suggestions on how to restructure the proof so that it works for categories?

[[David Roberts]]: I'm sorry, but I don't have the time (not to say that you are not in a similar position :) I have a full-time job outside of academia and contracts and so forth to deliver on.
=--

In other words, whether or not classical information is processed by the channel, it (the channel) is a mapping between $C^{*}$-algebras.  

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

***

## Discussion

[[Urs Schreiber]]: As the following disucssion shows, there is a general feeling that this entry here is in need of clarification on what exactly it is supposed to be about, and what it is good for. It would seem to me that this could easily be achieved based on some standard authorative reference that introduces the notion and discusses it. So: what are good references on the notion "qunatum channel", in the sense apparently meant here? Pointers to a specific page in a specific article would be appreciated.

[[Ian Durham]]: Thanks for the suggestion.  (By the way, when does it become kosher to delete all the comments between people in order to make the page look a little less cluttered?) 

***

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

Yemon, I never said anyone at MathOverflow was ignorant of category theory.  I was referring to other mathematicians I know and work with.  In regards to Cayley's theorem please see above for a rough idea of what I was attempting to do or see my paper on the arXiv about this.

[[David Roberts]]: Thank you for persevering, Ian. I think that there is a slight misunderstanding about permutation groups: Cayley's theorem tells us that any group can be embedded as a _subgroup_ of a permutation group, but this is probably not a crucial distinction for the present purposes. 

And Harry, if using Cayley's theorem anywhere was pointless, I don't think we would even refer to it :) Give the guy a break. No harm has been done and we now have another physical application here on the nLab which may contain some interesting category theory. I for one am pleased we are attracting people to our project to describe the world using category theory. The \'untidy\' reasoning we have seen here (if I may call it that) is what research looks like, especially at the junction of disciplines, until things get sorted. The nLab is just exposing this hitherto hidden process to the world. Anyway, as was said in the forum, this seems to be becoming a burdensome chat page and we probably don't have any more to constructively discuss.

***

>Zoran: the point of view that quantum channels are used for processing information is very biased point of view of one of the engineering fields. In nuclear physics multichannel processes were used half a century ago to formulate nonhermitean perturbation theory, where various emissions of particles, radiation and heat within a nucleus leads to dissipation. We should have a general point of view and not be crippled by somebody's particular engineering fad. 

> Reply to Zoran: Maybe, but the word "channel" (according to the dictionary) implies an information processing context and, besides, that is how they are used in quantum information theory which is what this page is about.  I'm not sure I'd call it a "fad" either.  I go to enough cross-disciplinary meetings to know that its a paradigm that runs across a number of fields and sub-fields.

>[[David Roberts]]:I see Zoran's use as perfectly consistent with the concept of a channel as 'a route through which anything passes or progresses'(dictionary.com - not the best reference, but sufficient) (in that case, particle emission). From an organisational point of view, I would prefer to have a page on quantum channels in generality with pointers to places they are used, and a separate page on quantum information theory, describing among other things how quantum channels are used in that context.

>[[Ian Durham]]: I would be fine with that.  My only point is that, it had always been my understanding that the use of the word "channel" in this context can be traced back to Shannon and von Neumann using it in an information theoretic context.  I've honestly never heard it used otherwise (caveat: obviously I am aware of its use in geography and elsewhere, I simply meant I'd never seen it used in physics in any other context).

> [[David Roberts]]: I was thinking more the analogy with biology, with channels passing various chemicals in and out of cells (cf particles in and out of atoms)

> [[Ian Durham]]: Doh!  Completely forgot about that use.  Well, apparently I am very much mistaken in this regard.  In any case, I definitely would be fine with a general discussion of channels with a pointer here.

[[!redirects quantum channel]]
[[!redirects quantum channels]]

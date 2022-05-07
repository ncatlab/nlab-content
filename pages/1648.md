# Motivation #

Recently, [[Johan Alm]] wrote a very neat paper

* [Quantization as a Kan Extension](http://ncatlab.org/nlab/files/Kantization09May27.pdf)

A discussion is available at the [$n$Café](https://golem.ph.utexas.edu/category/2009/05/alm_on_quantization_as_a_kan_e.html).

The paper proves an aspect of 

* [The n-Cafe Quantum Conjecture](http://golem.ph.utexas.edu/category/2007/06/the_ncaf_quantum_conjecture.html)

suggested by [[Urs Schreiber]]. A summary of Alm's paper with many motivating references is provided [[Quantization as a Kan Extension|here]].

+-- {: .query}

 [[Urs Schreiber|Urs]]: Johan Alm meanwhile has a refined version of these notes, but some aspects still need more work and thinking. When things have stabilized further I'll be happy to provide more details here. 

_Eric_: Are the refined notes available?

=--

This page represents an experiment similar to the [[geometric infinity-function theory|Journal Club's]] effort to understand the papers

* **IntTrans** David Ben-Zvi, John Francis, David Nadler, _Integral transforms and Drinfeld Centers in Derived Geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))

* **CharTheo** David Ben-Zvi, David Nadler, _The Character Theory of a Complex Group_ ([arXiv](http://arxiv.org/abs/0904.1247))

The goal is to build up, step-by-step, the background knowledge required to understand Alm's paper. The finite model considered is simple enough that we hope to advance our understanding of elementary concepts that are mostly taken for granted by the experts here at n-Headquarters.

When we are done, we hope to have a complete, self-contained presentation that should be accessible to mildly sophisticated undergraduate physics and mathematics students.

We also hope that the experts will keep an eye on us and when we get stuck, might gently nudge us in the right direction. As always, this page is open to all. Any questions or contributions are more than welcome.

# Collection of Concepts #

Maybe we can start by skimming the paper and collecting some unfamiliar keywords so that we can begin the process of tracing back definitions.

* [[Kan extension]]
* etc

#References#

* [Action as a Functor](http://math.ucr.edu/home/baez/qg-fall2004/action.pdf)
* [Connections as Functors](http://math.ucr.edu/home/baez/qg-fall2004/connection.pdf)
* [Categorifying Fundamental Physics](http://math.ucr.edu/home/baez/diary/fqxi_narrative.pdf)

#Discussion

+--{.query}
>(We'll pull out any outstanding questions from the discussion below to here in order to make life a little easier for would be angels who might be willing and able to help without forcing them to read the entire discussion.)

[[Eric]]: What is a "component of a cocone"?

[[Urs Schreiber]]: where did you see that term used? Maybe the question (or its answer) belongs at [[colimit]]. Do you have an idea what a cocone itself is? It consists of lots of morphisms from the objects of a diagram to the cocone tip. If we regard the cocone as a natural transformation to a constant functor, then the components of that natural transformation are these single morphism from objects to the tip of the cocone. These I would call "components of the cocone".

[[Eric]]: It is in "Lemma 1" of [Alm's paper](http://ncatlab.org/nlab/files/Kantization09May27.pdf). I didn't quite get the bit about "constant functor", but thanks to a great Catsters video ([General Limits and Colimits](http://www.youtube.com/watch?v=g47V6qxKQNU)), I have an idea about cocones (via colimits).

_Toby_:  Answered at [[cocone]].

>(Topics are separated by horizontal lines, with topics presented in reverse chronological order, i.e. the first section is the most recent.)_

[[Eric]]: I've been reading (not exactly studying) Goldblatt and watching some Catster videos. I still feel like I am pretty far away from understanding [[Kan extension]]. John Baez is helping Mike Stay understand them on [[free cocompletion]], which might be helpful to anyone trying to understand Alm's paper.

***

_Eric_: "Let $\tilde{X}$ be the groupoid which has as objects pairs $(x,s)$, where $x\in M$ and $s\in\mathbf{R}$, and as morphisms $(x,s)\to(x',s')$ paths $\gamma:x\to x'\in\mathcal{P}_1(M)$ of proper time $\tau(\gamma)=s'-s$."

Why do we consider groupoids here? I wouldn't expect paths to have "inverses", I'd expect them to have "adjoints" or maybe "opposites". 

Shouldn't there be a [[partial order]] somewhere related to causality?

_Toby_:  Good point.  Especially since we\'re looking only at timelike (or lightlike on the boundary) paths here (those with proper time rather than proper distance), it would be quite natural to fit causality in here.  Even if you want to allow for timelike loops, the individual paths can be classified as forward or backward under very weak orientability assumptions (and assuming only one timelike dimension, of course).

_[[Eric]]:_ I keep coming to back to the idea of reformulating this on a [[double category]] and relating it to a [Feynman checkerboard](http://en.wikipedia.org/wiki/Feynman_checkerboard) somehow. Maybe even getting back to relating it to [[Position, Velocity, and Acceleration]].
=--
***

_Eric_: As I read Alm's notes, I keep getting distracted thinking things like, "Why do they do that? What if they did this instead?" For example, why not

$$e^{iS}:\mathcal{P}_1(M)\to \mathbf{B}U(1)$$

? Then with $\rho:\mathbf{B}U(1)\to Vect$, we'd have

$$\rho\circ e^{iS}:\mathcal{P}_1(M)\to\Vect.$$

That might make things a little clearer.

Now, I'm wondering if we should introduce [[double category|double categories]] as a model for the [Feynman checkerboard](http://en.wikipedia.org/wiki/Feynman_checkerboard).

***

If any experts happen to wonder by, Daniel would appreciate any clarification on these points (should be considered as questions more than statements):

* Using left and right Kan extensions simultaneously seems to be required because QM mechanics needs symmetric everywhere defined operators. 

  +-- {: .query}

   [[Urs Schreiber|Urs]]: coinciding left and right 
   Kan extensions might be relevant, but I don't see this
   very clearly yet

  =--


* The "everywhere" follows from the arbitrary path taken to carry a state. 

* "Symmetric" follows that both left and right are similar definitions, but they are different because of the direction to where tha natural functor maps. 

* Operator is the so called Z, in which the author calls the quantum theory.

* Further, such operator is self-adjoint. Using both of them at the same time makes the functorial definition of adjoint functor work as a self adjoint functor, because as stated above, given that the natural map works both ways, you can define projection operators in antagonistic, but equivalent ways.

  +-- {: .query}

   [[Urs Schreiber|Urs]]: I don't really see the 
   point about self-adjointness made here --

   _Daniel_: This is also confusing to me, but since I am trying to think about Quantum Mechanics, I want to understand how a definintion of  Lan and Ran should induce an hermitian state  representation matrix of the operator Z. To see this, take  projection operators k and j of sections 1.1 and 1.2 to another diagram such that their roles are interchanged. Both of these diagrams are the same, except that now the components of the natural transformations pho and lambda will be reveresed. Equivalentely, it is like inverting the arrow of the definitions of the natural transformations, and because of this, exchanging the definition of left and right kan extensions. Given that, both pictures must describe the evolution of Z and that  k and j ends up on their dual space, because of theorem 1, and so, I don't really know how to finish this, but it seems that we will see that Lan and Kan are self adjoint operators.

  =--



* So, using both of them leads to the proper definition of a normed operator, because you have antatonistic projections.

* The definition of Kan extension forces all natural functors to filter uniquely all paths, which means that the outcome of a measurement will be unique. Since all possible configurations will be taken into consideration and projected, it sounds to be reasonable to me to think that the operator will be unitary.

  +-- {: .query}

   [[Urs Schreiber|Urs]]: I am not sure that I understand
   what this means

   _Daniel_:Forget about that. The fact that Kan extension filters all natural transofrmations of a given kind, means that a matrix is invertible. The unitarity is ad hock, but it seems that operations involving the proof of unitarity, involving Kan exenting, will involve speaking about the filtering of natural transformations.

  =--

***

_Daniel_: On page 3, he writes: "Usually, one has a classical 'action' of some kind definedned for manifolds with some extra structure, e.g. a riemannian metric, a symplectic form, a principalbundle, or etc. Quantization is what happens when one tries to assign that same action to a manifold that does not have that structure!" We can define many structures over a manifolds. Like, a toplogy, a piecewise linear strucure, a metric, etc. Just like the layers of an onion. So, quantization is just summing over all possible new layers of every new structure? It looks like so.

_Toby_:  That seems like a wild idea to me, but it does seem to be what he\'s saying.  And what\'s really wild is that he just might be right!

_Daniel_:I am trying to understand why Kan extension were used in that way to define quantiation, and it came up to me that listing how concepts are speculatively both involved in both QM and Kan extensions might be useful. (Urs copied the questions I made to "Outstanding Questions" above, so, for the sake of brevity, I deleted them here).

_Eric_: It looks like you're making good progress! I'm still trying to understand Kan extensions. I'm even still shaky on functors :) My goal is to start with the linear map examples on [[functor]], i.e. one-object [[endomorphism|full subcategories]] of [[FinVect]] and see what Kan extension means there. I wouldn't be broken hearted if someone spoiled the fun and explained it.

_Daniel_: Actualy no! I am trying to understand Kan extensions going backwards from QM! I am just waiting to someone to tell me if the above makes sense. Otherwise, I will remain completely confused as I am indeed now... Worse, people can take seriously what I wrote! 

_Eric_: "I am trying to understand Kan extensions going backwards from QM!" I am REALLY happy to see statements like that. That is really what I hope to get out of this exercise too. If we can get to the point where the mathematical concept of "Kan extension" can actually be understood in terms of QM, that would be pretty cool.

_Daniel_:Yes, sure, but for that, I would just like anyone to tell me if what I wrote above makes sense... Otherwise, I am stuck.

***

_Eric_: There is something about Kan extension that reminds me of some kind of linear least squares. I started trying to make it explicit by building an example with finite-dimensional vector spaces. I placed the example at [[functor]]. It seems like left and right Kan extensions are like left and right inverses (which in my universe means linear least squares).

_Daniel_: Eric, I don't understand why you wrote on  [[functor]] specificaly about linear least squares, it doesn't seem to have any special relation to do with what I found [on wikipedia](http://en.wikipedia.org/wiki/Linear_least_squares), other then being just a general observation about linear spaces.

_Eric_: Hi Daniel, have a look a <a href="http://golem.ph.utexas.edu/category/2008/03/limits_and_pushforward.html#c024063">John's explanation</a> of Kan extension. What he described made me think of linear least squares (which has nothing to do with any wikipedia article). I was trying to work out an example where Kan extension really did turn out to be linear least squares, but expressed rather in terms of left and right inverses. I may be completely wrong about the relation, but before I can judge, I needed functors between vector spaces thought of as one-object categories, hence the examples on [[functor]]. My goal is to get to the point where I feel fairly comfortable with Kan extension and then try to understand it in the context of Alm's paper.

_Toby_:  Can you explain what linear least squares is, then, if it has nothing to do with what\'s on that Wikipedia article? (which is the only linear least squares that I\'m familiar with myself).

_Eric_: Hi Toby and Daniel, linear least squares is what you think it is and is what is on Wikipedia. I didn't say what I wanted to say very clearly. And now I see I didn't read Daniel's question very carefully either. It's the hazards of not having more than 5 minute spurts to pay attention to this stuff :O What I meant to say is that my thoughts about the relationship between linear least squares and Kan extension (which are nothing more than a gut feeling) were related to what John said and _not_ about anything I read on Wikipedia. I didn't mean to suggest that what Wikipedia said was not related or relevant. Of course it is. It was just a comment about what made me think of the idea. Sorry about that.

In my work, we often have a bunch of time series representing prices of financial securities. We also have time series of financial/economic factors and we try to explain the prices in terms of factors. There are not enough factors to find a true "inverse", but we do "the best we can". That spirit of doing "the best we can" sounded very close to what John was describing. That's all I was trying to say.

_Eric_: Here's how I think of it (which may be completely misguided). Given $F:C\to D$ and $p:C\to C'$, and an expression (in the linear case)

$$F = F'\circ p + \epsilon.$$

We want to find $F':C'\to D$ that minimizes $\epsilon$.

Question: How could you express this in a more general category-theoretic way?

_Toby_:  OK, maybe I have a better idea what you mean now.  In particular, just as there are left and right Kan extensions, there are really also two kinds of linear least squares.  Looking at [this picture from Wikipedia](http://commons.wikimedia.org/wiki/File:Linear_least_squares_example2.png) for reference, instead of minimising the (squares of the) lengths of the *vertical* lines marked, we could just as easily minimise the (squares of the) lengths of corresponding *horizontal* lines.  It is a (sometimes rather arbitrary) distinction between dependent and independent variable that tells us which to use.

Also, looking at your example at [[functor]], it occurs to me that at some point you\'ll have to deal with the fact that linear least squares doesn\'t happen in [[Vect]]; it happens in [[Hilb]] (or at least in [[Ban]]).  That is, to minimise $\epsilon$, you\'ve got to be able to measure the size (norm) of $\epsilon$.  And that\'s where all of those transpose matrices in formulas for linear least squares get in.

Anyway, I wouldn\'t rule out a priori the idea that linear least squares might be given by a Kan extension, but I\'m not seeing it yet myself.  But at least I see what is the analogy that is exciting you.

_Eric_: It would be neat if you could use an intrinsic property of categories, e.g. maybe Leinster measure, to minimize $\epsilon$ rather than depend on a metric within the objects of the category. I seem to remember something about "Hom" behaving like a metric in some circumstances (?)

_Toby_:  Well, in a $2$-[[2-Hilbert space|Hilbert space]] (h\'m, doesn\'t exist yet, try searching This Week\'s Finds or the Caf&#233;), $Hom$ behaves like the inner product in a Hilbert space.  Of course if your category is a $2$-Hilbert space, then your objects are vectors whose components are themselves finite-dimensional Hilbert spaces, so you\'ve still got metrics put in by hand.  ($Fin Hilb$ itself is the primordial $2$-Hilbert space.)  Still, perhaps something can be done just using the fact that you\'re in a [[dagger compact category]].

And of course! another way in which $Hom$ can be like a metric is that, in a [[metric space]] (this is described at that link), the metric really *is* the [[hom-object]] operation of a certain [[enriched category]].  That\'s probably what you were thinking of.  The enriching category is a [[poset]] (the poset of nonnegative real numbers under $\geq$), so minimising $\epsilon$ is now like taking a (co)[[limit]].  Say, maybe this will work out!

_Eric_: Neat! The vague gut feeling just got a little clearer, but still extremely fuzzy. Maybe I'll keep talking and something will make sense :)

The idea behind least squares can also be thought of in terms of orthogonal projections, so if we had some kind of intrinsic inner product (involving colimits??) then we could use that to decompose $F$ into $F'p$ and $\epsilon$ where

$$F'p\cdot\epsilon = 0.$$

In fact, you could even say the challenge is to find an $F'$ such that $F'p$ is orthogonal to the residual $\epsilon$. This $F'$ is the "best we can do".

It would be neat if we could eventually say something like "Kan extension is our best attempt to find a functor $F':C\to C'$ such that $F'p$ and the residual $\epsilon$ are orthogonal." Or something...

_Eric_: Here is an example from the world of time series. Maybe it can be a model for a more general construction. Say we have two time series $x$ and $y$ and we would like to find the constant $b$ that minimizes the variance of $a$ in the expression

$$y = a + b x.$$

This problem is equivalent to finding $b$ such that $bx$ and $a$ are uncorrelated, i.e. their covariance is zero. The computation is simple

$$cov(y,x) = cov(a,x) + b cov(x,x).$$

Setting

$$b = \frac{cov(y,x)}{cov(x,x)}$$

gives 

$$cov(a,x) = 0.$$

My suspicion is that this is somehow related to Kan extension.

Note: See also an article I wrote while ago:

<a href="http://phorgyphynance.wordpress.com/2008/02/10/visualizing-market-risk-a-physicists-perspective/">Visualizing Market Risk: A Physicists Perspective</a>

This shows, geometrically, why the minimum variance solution is also the solution that splits the original into orthogonal pieces.

category: reference
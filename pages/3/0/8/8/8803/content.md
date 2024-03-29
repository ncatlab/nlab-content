##Idea

[[modal logic|Modal logics]] are said to be the logic of [[relational structures]].  The Kripke frame semantics of modal logics provides a clear picture of this:

Recall: A _frame_ for the basic modal language $\mathcal{L}_\omega(1)$ is a pair $\mathfrak{F} = (W,R)$ with $W$ a non-empty set and $R$ a binary relation on $W$.

At their 'crudest' the objects studied are just sets and binary relations on them.  In the basic 'many worlds' interpretation, a world $w$ satisfies a modal formula $\Box\phi$ if all worlds $w\prime$ accessible from $w$ (that is satisfying $wRw\prime$) satisfy $\phi$.

Now convert $R$ into a mapping $\rho : W\to \mathcal{P}(W)$, where $\rho(w)$ is the set of worlds accessible from $w$.  It is easy to rephrase the notion of 'satisfies' in terms of $\rho$, but $(W,\rho)$ is a [[coalgebra for an endofunctor|coalgebra]] for the power set  endofunctor on $Set$, so Kripke frames provide a simple example of a coalgebraic model for modal formulae. There are many other types of [[coalgebras for  endofunctors]] and many lead to modal logics.
  



##References

* [[Corina Cirstea]], [[Alexander Kurz]], Dirk Pattinson, Lutz Schr&#246;der and [[Yde Venema]], _Modal logics are coalgebraic_ ([pdf](http://eprints.soton.ac.uk/267144/1/ModalCoalgRev.pdf))

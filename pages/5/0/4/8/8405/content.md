Higher dimensional transitions systems are thought of as modelling concurrent operation of interacting [[transition system]]s. They are related to applications of [[directed homotopy theory]], and [[directed algebraic topology]].

We will give the definition that Gaucher uses (see below).  The version of Cattani and Sassone includes some extra conditions that yield a structure nearer to that of a process algebra.

A non-empty set, $\Sigma$, of labels is fixed.


##Definition:

 A weak higher dimensional transition system is a triple, $(S,\mu:L\to \Sigma,T)$, where $S$ is a set of states, $L$ a set of actions, $\mu$ is a labelling map and $T = \bigcup_{n\geq 1}T_n$, where $T_n\subset S\times L^n\times S$ is a set of $n$-transitions, such that two axioms hold, that ensure that the $n$-transitions are closed under permutations of labels and also satisfy a coherence (patching) axiom.


The case $n=1$ corresponds to [[transition system]]s.

##References

* [[Gian Luca Cattani]], [[Vladimiro Sassone]]  _[Higher Dimensional Transition Systems](http://eprints.soton.ac.uk/261954/1/hdtsLICSoff.pdf)_ In, 11th Symposium of Logics in Computer Science, LICS '96. IEEE Press, 55-62,(1996).

* [[Philippe Gaucher]], _Directed algebraic topology and higher dimensional transition system_, New-York Journal of Mathematics 16 (2010), 409 - 461, available as [arxiv:0903.4276](http://arxiv.org/abs/0903.4276)

*  [[Philippe Gaucher]], _Towards a homotopy theory of higher dimensional transition systems_, Theory and Applications of Categories, Vol. 25, No. 12, 2011, pp. 295&#8211;341, available as [arxiv:1011.0918](http://arxiv.org/abs/1011.0918)

category:computer science
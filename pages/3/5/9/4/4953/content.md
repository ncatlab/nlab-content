# Contents
* automatic table of contents goes here
{:toc}


##Idea##
When discussing [[language|languages]], say, in the theory of [[finite automata]], the usual starting point is a set, $\Sigma$, of symbols, which is taken to be the _alphabet_ for the language.  The next step is to form the [free monoid]], $\Sigma*$, on the alphabet, and then a language is simply a subset of $\Sigma*$, and these can be used in a number of situations to describe the workings of a 'system', the symbols being used to represent certain operations or actions of the system, and the words in $\Sigma*$ thus corresponding to sequences of operations. Usually the system will not allow arbitrary sequences of operations to be performed, and so the system determines a language, namely the allowable sequences. Describing the language, helps describe and determine the 'system'.

If the system being studied has some concurrency in it, so that certain of the operations are independent of each other, then one way of modelling such a system is to use a (Mazurkiewicz) trace alphabet, that is one in which the independence is explicitly taken into consideration.



+--{: . un-definition}
##Definition##
A _(Mazurkiewicz) trace alphabet_ is a pair $(\Sigma, I)$ where $\Sigma$ is a (usually finite) set of _actions_ and $I \subseteq \Sigma \times \Sigma$ is an _irreflexive_ and _symmetric_ relation.
=--
The relation $I$ is usually refereed to as *independence*.  Its complement $D = (\Sigma \times \Sigma) - I$ is called the _dependency_ relation.  (Such a sense of 'dependency relation' is interpreted in a slightly different way from that in the use of dependency graphs in project planning.

+--{: . un-example}
##Example##

=----
##Reference

*  A Mazurkiewicz, _Trace theory_ in 'Advances in Petri Nets', volume 255 of LNCS, Springer (1987)
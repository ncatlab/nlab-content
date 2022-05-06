
## Idea

A Mealy machine is a particular type of finite state automaton

## Definition

A finite _Mealy machine_, $\mathbf{A}$, consists of

* $Q$, a finite set of _states_;

* $A$, an _input alphabet_;

* $B$, an _output alphabet_;

* $q_0$, an _initial state_;

* $\delta: Q\times A\to Q$, a _transition function_;

and

* $\lambda:Q\times A \to B$, which associates  an output symbol with each transition.



Again as for [[Moore machines]], there is an output response function $\omega_\mathbf{A}:A^*\to B^*$ defined s follows:

if $x= x_1 \ldots x_n\in A^*$ and the states that $\mathbf{A}$ passes through when processing this string are $q_0, q_1, \ldots, q_n$, so diagrammatically

$$q_0\xrightarrow{x_1} q_1\xrightarrow{x_2}\ldots \xrightarrow{x_n} q_n,$$

define $\omega_\mathbf{A}(x)= \lambda(q_0,x_1)\ldots \lambda(q_{n-1},x_n)$.

Mealy machines and [[Moore machines]] have essentially the same descriptive power.

## Related entry

* [[Moore machine]]

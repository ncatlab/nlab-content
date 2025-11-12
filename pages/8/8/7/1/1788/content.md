> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

***

The sections to folow give a summary following in spirit the account given in [Barandes 2025](#Barandes2025).

Here instead to say in short what is going on: 

For a finite (physical) system with $N \in \mathbb{N}$ states, a one-step random evolution is given by a [[stochastic matrix]] $(P_{i j})_{i, j =1}^N$ whose entry $P_{i j} \in [0,1]$ gives the [[probability]] that the system, if in state $j$, evolves to state $i$. 

If there is a (temporal) sequence of such one-step random evolutions then these [[stochastic matrices]] depend on a [[pair]] of (time) parameters $t \leq t' \in \mathbb{R}$. 

Say that the *[[stochastic process]]* defined thereby is *divisible* iff the transition matrices over some (time) interval are the [[matrix multiplication|matrix product]] $(-) \cdot (-)$ over those associated with any decomposition of the interval:

$$ 
  \text{decomposable}
  \;\;\;
  \Leftrightarrow
  \;\;\;
  \forall_{t_0 \lee t \leq t_1}
  \;\;
  P(t_1, t_0) = P(t_1, t) \cdot P(t, t_0)
  \,.
$$

Now, if these transition probabilities $P$ are given by the rules of coherent time-evolution of [[pure states|pure]] [[quantum states]] according to [[quantum mechanics]], then:

1. the *[[Born rule]]* says that the probabilities are [[norm]]-squares

   $$
     P_{i j} = \vert\Theta_{i j}\very^2
   $$

   of [[complex numbers]] known as *[[probability amplitudes]]* and traditionally denoted as on the right here:

   $$
     \begin{aligned}
       \Theta_{i j} 
         & = \langle i \vert \Theta \vert j \rangle
       \\
       P_{i j} =
         & = 
          \langle i \vert \Theta \vert j \rangle
          \langle j \vert \Theta \vert i \rangle
     \end{aligned}
   $$

  (where traditionally one writes "$U$" for Barandes' "$\Theta$")

1. (what is essentially) the [[Schrödinger equation]] says that it is these [[probability amplitudes]] that compose under [[matrix multiplication]]:

   $$
     \Theta(t_1, t_0) = \Theta(t_1, t) \cdot \Theta(t, t_0) 
     \,.
   $$ 

But with the probability amplitudes $\Theta$ composing according to matrix multiplication, then in general the corresponding probabilities $P$ will clearly *not* compose by matrix multiplication.

In conclusion: The stochastic processes given by quantum processes are generically *indivisible*.

That seems to be the key point highlighted by [Barandes 2025](#Barandes2025).



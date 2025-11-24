> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak


***

* Moiré enhanced flat band in rhombohedral graphene


Consider the path integral for a [[particle]] propagating on a [[circle]] $S^1$, and approximated for the following argument by an ordinary integral over positions $x_t$ at $N$ discrete time steps $t \in \mathbf{N} \coloneqq \{0, 1, \cdots, N-1\}$, hence over discretized trajectories 
$$
  x \colon \mathbf{N} \longrightarrow S^1
  \mathrlap\,.
$$

Recall that the [[expectation value]] of an [[observable]] $O \colon (S^1) ^{\mathbf{N}} \longrightarrow \mathbb{C}$ is
\[
  \label{ExpectationValuesForParticleOnS1ViaDiscretized}
  \big\langle
    O
  \big\rangle
  \;\coloneqq\;
  \tfrac{1}{\mathcal{N}}
  \int   
    O(x) 
   \,
   \exp\big(\tfrac{\mathrm{i}}{\hbar} S(x)\big)
   \,
   D x
   \mathrlap{\,,}
\]
where 
$$
  \mathcal{N} 
    \coloneqq   
  \int   
   \exp\big(\tfrac{\mathrm{i}}{\hbar} S(x)\big)
   \,
   D x
$$
is the normalization factor (the *[[partition function]]*), and 
$$
  \int D x 
    \,\coloneqq\,
  \int_{S^1} \cdots \int_{S^1} 
  \mathrm{d}x_0 \cdots \mathrm{d}x_{\mathbf{N}-1}
$$
(and we are disregarding in/out state data, since this does not affect the following argument).

With that simple setup, ordinary [[integration by parts]] gives for an observable which is a [[partial derivative]]
$$
  O(x) = \tfrac{\partial F}{\partial x_t} (x)
$$
that its [[expectation value]] is equivalently expressed as:
\[
  \label{PartialIntegrationInDiscretizedPathIntegral}
  \begin{aligned}
    \big\langle
      O
    \big\rangle
    & \equiv
    \big\langle
      \tfrac{\partial F}{\partial x_t}
    \big\rangle
    \\   
    & 
    -\tfrac{\mathrm{i}}{\hbar}
    \big\langle
      F
      \tfrac{\partial S}{\partial x_t} 
    \big\rangle
  \end{aligned}
\]

Specializing this to the [[free field theory|free]] [[non-relativistic particle]], for which
$$
  S(x) 
   \,=\,  
  \sum_{t \in \mathbf{N}}
  \tfrac{m}{2}
  \tfrac{
    \big(x_{t+1} - x_t\big)
  }{
    N
  }
$$
the key point is to observe that 
$$
  \tfrac{\partial S}{\partial x_t}
  =
  m
  \tfrac{
    (x_{t} - x_{t-1})
  }{N}
  -
  m
  \tfrac{
    (x_{t+1} - t_n)
  }{N}
  \mathrlap{\,.}
$$

Now, entering equation (eq:PartialIntegrationInDiscretizedPathIntegral) with
$$
  F 
    \coloneqq 
  x_t
$$ 
 gives:
$$
  \mathrm{i}\hbar
  = 
  \big\langle
    x_t 
    \, m
    \tfrac{
      (x_{t} - x_{t-1})
    }{N}
  \big\rangle
  -
  \big\langle
    m
    \tfrac{
      (x_{t+1} - x_{t})
    }{N}
    \,
    x_t
  \big\rangle
  \mathrlap{\,.}
$$

Here we recognize
$$
  p_{t+1/2} 
    \coloneqq 
    m
    \tfrac{
      (x_{t+1} - x_{t})
    }{N}
$$
as the discrete [[momentum]] observable at time $t + 1/2$, in terms of which we have found that
$$
  \begin{aligned}
  \mathrm{i}\hbar
  & = 
  \big\langle
    x_t 
    \cdot
    p_{t - 1/2}
    \,-\,
    p_{t + 1/2}
    \cdot
    x_t 
  \big\rangle
  \,.
  \end{aligned}
$$

In the time continuum limit, this becomes
$$
  \mathrm{i}\hbar
  \,=\, 
  \big\langle
    x_t 
    \cdot
    p_{t - \epsilon}
    \,-\,
    p_{t + \epsilon}
    \cdot
    x_t 
  \big\rangle
$$
for $\epsilon \to 0$.

But this is clearly the path integral expression for what in operator formalism is the [[canonical commutation relation]]
$$
  \mathrm{i}\hbar
  =
  \hat x \cdot \hat p - \hat p \cdot \hat x
  \,.
$$

In conclusion, the observable corresponding to a quantum operator product $B \cdot A$ of observables at times $t$ may be thought of as the result of first shifting the observable $B$ to a time just a little *after* $t$ and then forming the ordinary product of observed values. 


+-- {: .num_theorem #PullbackLawForACube}
###### Proposition
**(Pasting Law for Pullbacks in a Cube)**
\linebreak
Suppose we have a commutative cube in a category:

\begin{tikzcd}[sep = scriptsize]
{W'} && {Z'} \\
& {X'} && {Y'} \\
W && Z \\
& X && Y
\arrow[from=1-1, to=1-3]
\arrow[from=1-1, to=2-2]
\arrow[from=1-1, to=3-1]
\arrow[from=1-3, to=2-4]
\arrow[from=1-3, to=3-3]
\arrow[crossing over, from=2-2, to=2-4]
\arrow[from=2-4, to=4-4]
\arrow[from=3-1, to=3-3]
\arrow[from=3-1, to=4-2]
\arrow[from=3-3, to=4-4]
\arrow[from=4-2, to=4-4]
\arrow[crossing over, from=2-2, to=4-2]
\end{tikzcd}

Denote the cube faces by F (Front), B (Back), U (Up), D (Down), L (Left), and R (Right) (this is Rubik's cube Singmaster notation).

a. Assume F and D are pullback squares. Then the following are equivalent:

  1.  The total rectangle from $W'\to Z'$ to $X\to Y$ is a pullback.

  1.  T and B are pullback squares.

  1.  T or B is a pullback square.

b. Assume F, D, R are pullback squares (these are the faces sharing $Y$ as a common vertex). Then all three other faces B, T, L are also pullback squares if at least one of them is.

a'. Assume T and B are pushout squares. Then the following are equivalent:

  1.  The total rectangle from $W'\to Z'$ to $X\to Y$ is a pushout.

  1.  F and D are pushout squares.

  1.  F or D is a pushout square.

b'. Assume B, T, L are pushout squares (these are the faces sharing $W'$ as a common vertex). Then all three other faces F, D, R are also pushout squares if at least one of them is.
 =--

\begin{proof}
We only show a and b (for a' and b' are their duals).
Part a follows directly from Proposition \ref{GeneralPastingLaw}.
To see part b, consider the subgroup of order three of cube symmetries generated by a 120° rotation along the axis that goes from $W'$ to $Y$. If we let this group act on the statement of part a, we obtain three different versions of part a. Now combine these with the hypotheses of part b to obtain the claim.
\end{proof}

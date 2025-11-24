> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak


***

* Moiré enhanced flat band in rhombohedral graphene


Consider the path integral for a [[particle]] propagating on $S^1$, approximated by a sequence of ordinary integrals over positions $x_t$ at $N$ discrete time steps $t \in \mathbf{N} \coloneqq \{0, 1, \cdots, N-1\}$. Hence the path integral is over discretized trajectories $x \colon \mathbf{N} \longrightarrow S^1$.

The [[expectation value]] of an [[observable]] $O \colon (S^1) ^{\mathbf{N}} \longrightarrow \mathbb{C}$ is

$$
  \big\langle
    O
  \big\rangle
  =
  \tfrac{1}{\mathcal{N}}
  \int   
    O(x) 
   \,
   \exp\big(\tfrac{\mathrm{i}}{\hbar} S(x)\big)
   \,
   D x
   \mathrlap{\,,}
$$
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
  \prod_{n \in \mathbf{N}} \int_{S^1} \mathrm{d}x_n
  \mathrlap{\,.}
$$

Now [[integration by parts]] gives for an observable of the form 
$$
  O(x) = \tfrac{\partial F}{\partial x_n} (x)
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
      \tfrac{\partial F}{\partial x_n}
    \big\rangle
    \\   
    & 
    -\tfrac{\mathrm{i}}{\hbar}
    \big\langle
      F
      \tfrac{\partial S}{\partial x_n} 
    \big\rangle
  \end{aligned}
\]

Specializing this to the [[free field theory|free]] [[non-relativistic particle]], for which
$$
  S(x) =  
  \sum_{n \in \mathbf{N}}
  \tfrac{m}{2}
  \tfrac{
    \big(x_{n+1} - x_n\big)
  }{
    N
  }
$$
and hence
$$
  \tfrac{\partial S}{\partial x_n}
  =
  m
  \tfrac{
    (x_{n} - x_{n-1})
  }{N}
  -
  m
  \tfrac{
    (x_{n+1} - x_n)
  }{N}
$$
and to 
$$
  F \coloneqq x_n
  \mathrlap{\,,}
$$ 
equation (eq:PartialIntegrationInDiscretizedPathIntegral) gives:
$$
  \mathrm{i}\hbar
  = 
  \big\langle
    x_n 
    \, m
    \tfrac{
      (x_{n} - x_{n-1})
    }{N}
  \big\rangle
  -
  \big\langle
    m
    \tfrac{
      (x_{n+1} - x_{n})
    }{N}
    \,
    x_n 
  \big\rangle
  \mathrlap{\,.}
$$

Here we recognize
$$
  p_{n+1/2} 
    \coloneqq 
    m
    \tfrac{
      (x_{n+1} - x_{n})
    }{N}
$$
as the discrete [[momentum]] observable at time $n + 1/2$, in terms of which we have found that
$$
  \begin{aligned}
  \mathrm{i}\hbar
  & = 
  \big\langle
    x_n 
    \cdot
    p_{n - 1/2}
    \,-\,
    p_{n + 1/2}
    \cdot
    x_n 
  \big\rangle
  \end{aligned}
$$

This is the path integral expression for what in operator formalism is the [[canonical commutation relation]]
$$
  \mathrm{i}\hbar
  =
  \hat x \cdot \hat p - \hat p \cdot \hat x
$$

This shows that the observable corresponding to an operator product $B \cdot A$ of observables is obtained by taking the ordinary product of shifting the observation $B$ to a little bit *after* the observation of $A$.

(...)


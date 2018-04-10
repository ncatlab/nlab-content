

Consider the homotopy fiber sequence

$$
  S^4
    \longrightarrow 
  S^4//S^1
    \longrightarrow 
  B S^1
$$

since all three spaces are connected with abelian fundamental group, we have the corresponding long exact sequence of rational homotopy groups (e.g. cor. 1.2.2 [here](http://www.ru.nl/publish/pages/813276/rational_homotopy_theory.pdf))

$$
  \cdots
   \to
  \pi^{\bullet+1}(S^4)_{\mathbb{Q}}
    \longrightarrow 
  \pi^{\bullet+1}(S^4//S^1)_{\mathbb{Q}}
    \longrightarrow 
  \pi^{\bullet+1}(B S^1)_{\mathbb{Q}}
    \longrightarrow
  \pi^{\bullet}(S^4)_{\mathbb{Q}}
    \longrightarrow 
  \pi^\bullet(S^4//S^1)_{\mathbb{Q}}
    \longrightarrow 
  \pi^\bullet(B S^1)_{\mathbb{Q}}
    \longrightarrow
  \pi^{\bullet-1}(S^4)_{\mathbb{Q}}
    \longrightarrow 
  \pi^{\bullet-1}(S^4//S^1)_{\mathbb{Q}}
    \longrightarrow 
  \pi^{\bullet-1}(B S^1)_{\mathbb{Q}}
    \to
  \cdots
$$

This yields

$$
  \array{
  &&
  0
    &\longrightarrow&
  \pi^1(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
  &&
  0
    &\longrightarrow&
  \pi^2(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  \mathbb{Q}
    &\longrightarrow&
   0
  \\
  &&
  0
    &\longrightarrow&
  \pi^3(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
  0
    &\longrightarrow&
  \mathbb{Q}
    &\longrightarrow&
  \pi^4(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
    &&
  0
    &\longrightarrow&
  \pi^5(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
    &&
  0
    &\longrightarrow&
  \pi^6(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
  0
    &\longrightarrow&
  \mathbb{Q}
    &\longrightarrow&
  \pi^7(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  \\
  \\
  &&
  0
    &\longrightarrow&
  \pi^{2k+8}(S^4//S^1)_{\mathbb{Q}}
    &\longrightarrow&
  0
  }
$$

hence in conclusion

| $n$ | 0 | 1 | 2 | 3 | 4 |  5 | 6 | 7 | 8 | 9 | 10 | $\cdots$ |
|-----|---|---|---|---|---|----|---|---|---|----|----------|
| $\pi^n(S^4//S^1)_{\mathbb{Q}} =$ |  $\mathbb{Q}$ | $0$ | $\array{ 0 \\ \oplus \\ \mathbb{Q}}$ | $0$ | $\array{\mathbb{Q} \\ \oplus \\ 0}$ | $0$ | $\array{ 0 \\ \oplus \\ 0}$ | $\array{ \mathbb{Q} \\ \oplus \\ 0 }$   | $\array{ 0 \\ \oplus \\ 0 }$  | $0$   | $\array{ 0 \\ \oplus \\ 0 }$  |  $\cdots$ |

$\,$

{#Gysin} Now consider the corresponding [[Gysin sequence]] for

$$
  S^1 \longrightarrow S^4 \longrightarrow S^4//S^1
$$

which is of the form

$$
  \cdots
   \longrightarrow
  H^{\bullet-2}(S^4//S^1, \mathbb{Q})
    \overset{\omega_2 \cup (-)}{\longrightarrow}
  H^\bullet(S^4//S^1, \mathbb{Q})
   \longrightarrow
  H^\bullet( S^4, \mathbb{Q} )
    \longrightarrow
  H^{\bullet - 1}( S^4//S^1, \mathbb{Q} )
    \overset{\omega_2 \cup (-)}{\longrightarrow}
  H^{\bullet+1}( S^4//S^1, \mathbb{Q})
    \longrightarrow
  H^{\bullet+1}( S^4, \mathbb{Q} )
    \longrightarrow
  H^\bullet( S^4//S^1, \mathbb{Q} )
    \overset{\omega_2 \cup (-)}{\longrightarrow}
  H^{\bullet+2}( S^4//S^1, \mathbb{Q} )
    \longrightarrow
  \cdots
$$

This yields

$$
  \array{
    &&
    0
      &\longrightarrow&
    \underset{
      \mathbb{Q}
    }{
      \underbrace{H^{0}( S^4//S^1, \mathbb{Q} )}
    }
      &\overset{\omega_2 \cup (-)}{\longrightarrow}&
    H^{2}( S^4//S^1, \mathbb{Q} )
      &\longrightarrow&
    0
    \\
    &&
    0
      &\longrightarrow&
    H^{1}( S^4//S^1, \mathbb{Q} )
      &\overset{\omega_2 \cup (-)}{\longrightarrow}&
    H^{3}( S^4//S^1, \mathbb{Q} )
      &\longrightarrow&
    0
    \\
    &&
    0
      &\longrightarrow&
    H^{2}( S^4//S^1, \mathbb{Q} )
      &\overset{\omega_2 \cup (-)}{\longrightarrow}&
    H^{4}( S^4//S^1, \mathbb{Q} )
      &\longrightarrow&
    \mathbb{Q}
      &\longrightarrow&
    H^3( S^4//S^1, \mathbb{Q} )
    \\
    H^{4}( S^4//S^1, \mathbb{Q} )
      &\longrightarrow&
    \mathbb{Q}
      &\longrightarrow&
    H^{3}( S^4//S^1, \mathbb{Q} )
      &\overset{\omega_2 \cup (-)}{\longrightarrow}&
    H^{5}( S^4//S^1, \mathbb{Q} )
      &\longrightarrow&
    0
    \\
    &&
    0
     &\longrightarrow&
    H^4(S^4//S^1, \mathbb{Q})
      &\overset{\omega_2 \cup (-)}{\longrightarrow}&
    H^6(S^4//S^1, \mathbb{Q})
      &\longrightarrow&
    0
  }
$$

assuming $H^3(S^4//S^1, \mathbb{Q}) = 0$, and using the first row in the third, yields

$$
  \array{
    0
      &\longrightarrow&
    \underset{= \langle \omega_2\rangle}{\underbrace{\mathbb{Q}}}
      &\overset{\omega_2 \cup (-)}{\longrightarrow}&
    H^{4}( S^4//S^1, \mathbb{Q} )
      &\longrightarrow&
    \mathbb{Q}
      &\longrightarrow&
    0
  }
$$

and hence

$$
  H^{4}( S^4//S^1, \mathbb{Q} )
  \simeq
  \underset{\langle \omega_2 \cup \omega_2\rangle}{\underbrace{\mathbb{Q}}} \oplus \mathbb{Q}
$$

This implies with the 5th row that also


$$
  H^{6}( S^4//S^1, \mathbb{Q} )
  \simeq
  \underset{\langle \omega_2 \cup \omega_2 \cup \omega_2\rangle}{\underbrace{\mathbb{Q}}} \oplus \mathbb{Q}
$$

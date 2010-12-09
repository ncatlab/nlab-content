+-- {: .standout}
Every wiki needs a sandbox! Just test between the horizontal rules below (`***` in the source) and don't worry about messing things up.
=--

***

$$
  \begin{aligned}
    sSet(S, cdgAlg_k^{op}(Spec A,Spec B))
    & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot Hom_{sSet}(S \times \Delta[r], 
        cdgAlg_k^{op}(Spec A, Spec B))
   \\
   & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
      \int_{[k] \in \Delta}
       Hom_{Set}(S_k \times \Delta[k,r], 
        Hom_{cdgAlg_k^{op}}(Spec \Omega^\bullet_{poly}(\Delta^k) \times Spec A, Spec B))   
   \\
   & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
      \int_{[k] \in \Delta} 
        Hom_{cdgAlg_k^{op}}((S_k \times \Delta[k,r]) \cdot Spec \Omega^\bullet_{poly}(\Delta^k) \times Spec A, Spec B))   
    \\
    & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
        Hom_{cdgAlg_k^{op}}(\int^{[k] \in \Delta} 
 (S_k \times \Delta[k,r]) \cdot Spec \Omega^\bullet_{poly}(\Delta^k) \times Spec A, Spec B))       
    \\
    & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
        Hom_{cdgAlg_k^{op}}(Spec \Omega^\bullet_{poly}(S \times \Delta[r]) \times Spec A, Spec B))       
    \\
    & \simeq
    cdgAlg_k^{op}(S \cdot Spec A, Spec B)
  \end{aligned}
$$


Let 

$$
  r_\bullet A
  =
  \left(
     \cdots 
     A \times A \times A \stackrel{\to}{\stackrel{\to}{\to}} A \times A \stackrel{\to}{\to} A
  \right)
$$ 

We have 

$$
  match_k r_\bullet A = r_k A
  \,.
$$



category: meta

[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects שנה טובה]]

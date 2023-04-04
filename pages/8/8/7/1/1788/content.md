
For a given [[ground field]], we consider the category [[FinDimVect]] whose [[objects]] [[finite-dimensional vector spaces]] $V$ and whose [[morphisms]] are [[linear maps]] $V_1 \to V_2$ between these.



\begin{tikzcd}[
  row sep=20pt,
  column sep=5pt
]
  &
  \mathrm{ker}(f_1)
  \oplus 
  \big(
  f_1(V_1) \cap_B f_2(V_2) 
  \big)
  \oplus 
  \mathrm{ker}(f_2)
  \ar[d, phantom, "{\simeq}"{rotate=-90}]
  \\[-10pt]
  \mathrm{ker}(f_1)
  \ar[d, hook]
  &
  V_1 \times_{{}_{B}} V_2
  \ar[dl]
  \ar[dr]
  \ar[dd, phantom, "{\scalebox{.6}{(pb)}}"{pos=.2}]
  &
  \mathrm{ker}(f_2)
  \ar[d, hook]
  \\
  V_1 
  \ar[dr, "{f_1}"{description}]
  && 
  V_2
  \ar[dl, "{f_2}"{description}]
  \\
  & B
\end{tikzcd}
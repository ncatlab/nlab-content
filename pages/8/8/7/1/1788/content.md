
\begin{tikzcd}[column sep=small]
  \cdots
  \ar[from=dr, hook']
  &
  &
  H(X_i \cup X_{i+1})
  \ar[from=dr, hook', "{H(\iota_{i+1}^r)}"{swap}]
  &
  &
  H(X_{i+1} \cup X_{i+2})
  \ar[from=dr, hook', "{H(\iota_{i+2}^r)}"{swap}]
  &
  & 
  \cdots
  \\
  &
  H(X_i)
  \ar[ur, hook, "{H(\iota_i^l)}"]
  &
  &
  H(X_{i+1})
  \ar[ur, hook, "{H(\iota_{i+1}^l)}"]
  &
  &
  H(X_{i+2})
  \ar[ur, hook]
  & 
\end{tikzcd}

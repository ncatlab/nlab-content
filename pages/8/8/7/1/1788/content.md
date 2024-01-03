
<form  name="gsearch" method="get" action="https://bing.com"><input type="text" size="30" name="as_q"/><input type="hidden" name="as_sitesearch" value="https://ncatlab.org/nlab/"/>

...

[[Vect|Vect$_{\mathbb{K}}$]]

$$
  \begin{array}{l}
    \mathrm{d}_{X} \psi(\omega)
    + 
    \psi( \mathrm{d}_Y \omega )
    & =
    \textstyle{\int}_{[0,1]} 
      \mathrm{d}_{X} 
      \iota_{\partial_t} \Psi^*(\omega) 
    d t 
    + 
    \textstyle{\int}_{[0,1]} 
      \iota_{\partial_t} \Psi^*(\mathrm{d}_Y \omega) 
    d t
    \\
    \;=\;
    \textstyle{\int}_{[0,1]} 
      \mathrm{d}_{X} 
      \iota_{\partial_t} \Psi^*(\omega) 
    d t 
    + 
    \textstyle{\int}_{[0,1]} 
      \iota_{\partial_t} 
      \big(\mathrm{d}_X + \mathrm{d}_{[0,1]}\big)
      \Psi^*( \omega) 
    d t
    \\
    \;=\;
    \textstyle{\int}_{[0,1]} 
      \iota_{\partial_t} 
      \mathrm{d}_{[0,1]}
      \Psi^*(\omega) 
    d t
    \\
    \;=\;
    \textstyle{\int}_{[0,1]} 
      \mathrm{d}_{[0,1]}
      \Psi^*(\omega) 
    \\
    \;=\;
    \Psi_1^\ast(\omega)
    -
    \Psi_0^\ast(\omega)
    \\
    \;=\;
    f_2^\ast \omega - f_1^\ast \omega
    \,.
  \end{array}
$$

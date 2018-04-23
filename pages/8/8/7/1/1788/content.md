
$\,$

$\,$

$\,$

$\,$

+-- {: .num_prop}
###### Proposition

Let 

$$
  \mathbb{H} = \langle 1, i, j , j\rangle
$$ 

be the [[quaternions]] with canonical basis elements, and let 

$$
  \mathbb{O} = \mathbb{H} \oplus \ell \mathbb{H}
$$

be the octonions equipped with the linear basis induced by the [[Cayley-Dickson construction]]. 

Then the linear map 

$$
  L_{\ell} L_{\ell i} L_{\ell j} L_{\ell k}
  \;\colon\;
  \mathbb{O} \longrightarrow \mathbb{O}
$$

is an [[involution]] whose +1 [[eigenspace]] is $\mathbb{H}$ and whose -1 eigenspace is $\ell \mathbb{H}$, under the above identification.

(Here $L_{(-)}$ denotes the linear map on $\mathbb{O}$ given by left multiplication in $\mathbb{O}$.)

=--

+-- {: .proof}
###### Proof

We use the Cayley-Dickson relations 

$$
  a (\ell b) = \ell (\overline{a} b)
  \,,
  \phantom{AA}
  a(\ell b) = (a \overline{b}) \ell
  \,,
  \phantom{AA}
  (\ell a) (b \ell^{-1}) = \overline{a b}
$$

that hold in $\mathbb{O}$ for all $a,b \in \mathbb{H}$, as well as

$$
  \ell e = - e \ell
$$

for all imaginary elements $e \in \mathbb{H}$.

With this we compute

$$
  \begin{aligned}
    & L_{\ell} L_{\ell i} L_{\ell j} L_{\ell k} ( a)
    \\
    & =  \ell( (\ell i) ( (\ell j) ( (\ell k) a ) ) )
    \\
    & = - \ell( (\ell i) ( (\ell j) ( (k \ell) a ) ) )
    \\
    & = - \ell( (\ell i) ( (\ell j) ( (k \overline{a}) \ell ) ) )
    \\
    & = + \ell( (\ell i) ( (\ell j) ( (k \overline{a}) \ell^{-1} ) ) )
    \\
    & = + \ell( (\ell i) ( \overline{j (k \overline{a})} ) )
    \\
    & = + \ell( (\ell i) ( \overline{i \overline{a}} ) )
    \\
    & = - \ell( (i \ell) ( \overline{i \overline{a}} ) )
    \\
    & = - \ell( ( i i \overline{a}  ) \ell )
    \\
    & = + \ell( \overline{a}  \ell )
    \\
    & = - \ell( \overline{a} \ell^{-1} )
    \\
    & = - a
  \end{aligned}
$$

and

$$
  \begin{aligned}
    & L_{\ell} L_{\ell i} L_{\ell j} L_{\ell k} ( \ell a)
    \\
    & = \ell( (\ell i) ( (\ell j) ( (\ell k) (\ell a) ) ) )
    \\
    & =
      \ell( (\ell i) ( (\ell j) ( (\ell k) ( \overline{a} \ell) ) ) )
    \\
    & =
      -
      \ell( (\ell i) ( (\ell j) ( \overline{k {\overline{a}}} ) ) )
    \\
    & =
      + \ell( (\ell i) ( (j \ell) ( \overline{k {\overline{a}}} ) ) )
    \\
    & =
      + \ell( (\ell i) ( (j k {\overline{a}}) \ell ) )
    \\
    & =
      - \ell( (\ell i) ( (j k {\overline{a}}) \ell^{-1} ) )
    \\
    & =
      - \ell( \overline{ i j k {\overline{a}} } )
    \\
    & =
      + \ell( \overline{ {\overline{a}} } )
    \\
    & =
      + \ell a 
  \end{aligned}
$$

=--

$\,$

$\,$

$\,$
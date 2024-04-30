
energy-momentum tensor of $p$-form flux density

$$
  \mathrm{T}_{a b}
  \;=\;
  +
  c
  \,
  \Big(
    \tfrac{1}{2p}
    (F_p)_{c_1 \cdots c_p}
    (F_p)^{c_1 \cdots c_p}
    \,
    \eta_{a b}
    -
    (F_p)_{
      a
      \, 
      c_1 \cdots c_{p-1}
    }
    (F_p)
      _b{}
      ^{c_1 \cdots c_{p-1}}
  \Big)
$$

$$
  \mathrm{T}
  \;\equiv\;
  \mathrm{T}^a{}_a
  \;=\;
  c
  \,
  \Big(
    \tfrac
     {D}
     {2p}
     -
     1
  \Big)
    (F_p)_{c_1 \cdots c_p}
    (F_p)^{c_1 \cdots c_p}  
$$

trace of Einstein equation:

$$
  \mathrm{R}
  \big(
    1
    -
    \tfrac
      {D}
      {2}
  \big)
  \;\;=\;\;
  c
  \,
  \Big(
    \tfrac
     {D}
     {2p}
     -
     1
  \Big)
    (F_p)_{c_1 \cdots c_p}
    (F_p)^{c_1 \cdots c_p}    
$$
hence
$$
  \mathrm{R}
  \;\;=\;\;
  -
  c
  \underset{
    \tfrac{D-2p}{(D-2)p}
  }{
    \underbrace{
    \frac
      {
        D/2p - 1
      }
      {
        D/2 - 1
      }
    }
  }
  \,
    (F_p)_{c_1 \cdots c_p}
    (F_p)^{c_1 \cdots c_p}    
$$

so that the Einstein equation becomes equivalent to

$$
  \begin{array}{l}
  \mathrm{R}_{a b}
  -
  \tfrac{1}{2}
  \mathrm{R} \, \eta_{a b}
  \;\;
  =
  \;\;
  c
  \,
  \Big(
    \tfrac{1}{2p}
    (F_p)_{c_1 \cdots c_p}
    (F_p)^{c_1 \cdots c_p}
    \,
    \eta_{a b}
    -
    (F_p)_{
      a
      \, 
      c_1 \cdots c_{p-1}
    }
    (F_p)
      _b{}
      ^{c_1 \cdots c_{p-1}}
  \Big)
  \\
  \mathrm{R}_{a b}
  \;\;
  =
  \;\;
  c
  \,
  \Big(
    \underset{
      \tfrac
        { D - 4 p + 2 }
        { 4 p - 2 d p }
    }{
      \underbrace{
      \big(
        \tfrac{1}{2p}
        -
        \tfrac
        {
          D-2p
        }
        {
          (D-2)p
        }
      \big)
      }
    }
    (F_p)_{c_1 \cdots c_p}
    (F_p)^{c_1 \cdots c_p}
    \,
    \eta_{a b}
    -
    (F_p)_{
      a
      \, 
      c_1 \cdots c_{p-1}
    }
    (F_p)
      _b{}
      ^{c_1 \cdots c_{p-1}}
  \Big)
  \end{array}
$$


$$
  \begin{array}{l}
    (C_3) \wedge \star (D_3)
    \\
    \;=\;
    \epsilon^{a_1 \cdots a_{11}}
    \tfrac{1}{3!}
    (C_3)_{a_1 a_2 a_3}
    \tfrac{1}{8!}
    \tfrac{1}{3!}
    \epsilon_{ a_4 \cdots a_{11} b_1 b_2 b_3 }
    (D_3)^{b_1 b_2 b_3}
    \\
    \;=\;
    -
    \tfrac{1}{3!}
    \tfrac{1}{8!}
    \tfrac{1}{3!}
    3! \cdot 8!
    (C_3)_{a_1 a_2 a_3}
    (D_3)^{a_1 a_2 a_3}
  \end{array}
$$


\begin{tikzcd}
	{F(x) \otimes F(y)} && {F(y) \otimes F(x)} \\
	{F(x \otimes y)} && {F(y \otimes x)}
	\arrow["{\beta_{F(x),F(y)}}", from=1-1, to=1-3]
	\arrow["{\mu_{x,y}}"', from=1-1, to=2-1]
	\arrow["{\mu_{y,x}}", from=1-3, to=2-3]
	\arrow["{F(\beta_{x,y})}"', from=2-1, to=2-3]
\end{tikzcd}



We want to check that the the $L_\infty$-isomorphism sends IIA cocycles to IIB cocycles.

We use the convention that

$$
  \Gamma_{a \leq 8} 
    \coloneqq
  \left(
    \array{
      0 & \gamma_a
      \\
      \gamma_a & 0
    }
  \right)
  \;\,,\;\;
  \Gamma_{9}
   \coloneqq
  \left(
    \array{
       0 & id 
       \\
       -id & 0
    }
  \right)
  \;\,,\;\;
  \Gamma_{10}
   \coloneqq
  \left(
    \array{
      i id & 0
      \\
      0 & -i id
    }
  \right)
  \,.
$$

Notice that $\Gamma_{a b }$ for $a \lt b \leq 9$ is the same for both chiralities, except if $b = 9$.

Therefore if we write

$$
  \Gamma_a^B 
    = 
  \left\{
    \array{
      \Gamma_a & \vert \; a \leq 8
      \\
  \left(
    \array{  
      0 & id
      \\
      id & 0
    }
  \right)
     & \vert \; a = 9
    }
  \right.
$$

then the IIB spin representation is given by elements $\exp(\omega^{a b} \Gamma_a^B \Gamma_b^B)$. Notice that

$$
  \Gamma_9^B 
  =
  i \Gamma_9 \Gamma_{10}
$$

hence

$$
  \Gamma_{10} = i \Gamma_9^B \Gamma_9
$$



Now  IIA-cocycles are as follows, for some $c_{2p} \in \mathbb{R}$. The factors of "$i$" are forced by the condition that each expression is real, using the convention that $\Gamma_0^\dagger = \Gamma_0$ and $\Gamma_{spatial}^\dagger = - \Gamma_{spatial}$. Notice that these factors of $i$ all go away if one used the opposite convention for hermiticity, which is what Chryssomalokos et al do.

$$
  \begin{aligned}
    \mu_{D0}
      & =
    \overline{\psi} \Gamma_{10}\psi
    \\
    \mu_{D2}
      & =
    i
    c_2
    \overline{\psi} \Gamma_{a_1 a_2} \psi e^{a_1} e^{a_2}
    \\
    \mu_{D4}
      & =
    c_4
    \overline{\psi} \Gamma_{a_1 \cdots a_4} \Gamma_{10} \psi e^{a_1} \cdots e^{a_4}
    \\
    \mu_{D6}
      & =
    i c_6
    \overline{\psi} \Gamma_{a_1 \cdots a_6}  \psi e^{a_1} \cdots e^{a_6}
    \\
    \mu_{D8}
      & =
    c_8
    \overline{\psi} \Gamma_{a_1 \cdots a_8} \Gamma_{10} \psi e^{a_1} \cdots e^{a_8}
    \\
    \mu_{D10}
      & =
    i c_{10}
    \overline{\psi} \Gamma_{a_1 \cdots a_{10}} \psi e^{a_1} \cdots e^{a_{10}}
  \end{aligned}
$$

We decompose any element in $CE(\mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}})$ into a piece of the same degree and a piece of one degree lower, by the identification.

$$
  \mu = \mu|_{8+1} - e^9 \wedge (\pi_9)_\ast \mu
  \,.
$$

Now let's check that a IIB cocycle like $\mu_{D1}$ will turn out under sending the above data through the T-duality isomorphism.

So we write

$$
  \begin{aligned}
   \mu_{D1} 
     & =  
   \mu_{D1}|_{8+1} - e^9 (\pi_9)_\ast \mu_{D1}
  \end{aligned}
$$

and need to match this to the corresponding 1-forms that we get from the IIA data above. This gives (where the index $a$ runs in $\{0,\cdots ,8\}$)

$$
  \begin{aligned}
   \mu_{D1} 
     & =  
   (\pi_9)_\ast \mu_{D2} - e^9 \mu_{D0}|_{8+1}
   \\
   & = 
   i c_2 \overline{\psi}\Gamma_a \Gamma_9 \psi e^{a}
   -
   e^9 \overline{\psi} \Gamma_{10} \psi
   \\
   & = 
   i c_2 \overline{\psi}\Gamma^B_a \Gamma_9 \psi e^{a}
   -
   i e^9 \overline{\psi} \Gamma_9^B \Gamma_9 \psi
  \end{aligned}
$$

Now Chryssomalakos et al have $c_2 = 1$. Okay.

If now also the relative sign were "+" instead of "-" then this would come out right, and we would find

$$
  \mu_{D1} = i \overline{\psi} \Gamma_a^B \Gamma_9 \psi \wedge e^a
$$ 

where now $a$ runs in $\{0,\cdots, 9\}$. This would be correct.

So what about that relative sign?
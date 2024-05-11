
<a href="https://cdnapisec.kaltura.com/p/1674401/sp/167440100/embedIframeJs/uiconf_id/23435151/partner_id/1674401?iframeembed=true&playerId=kaltura_player&entry_id=1_vuc7b5h2&flashvars">kt</a>

[kt](https://cdnapisec.kaltura.com/html5/html5lib/v2.73.2/mwEmbedFrame.php/p/1674401/uiconf_id/23435151/entry_id/1_vuc7b5h2?wid=_1674401&iframeembed=true&playerId=kaltura_player&entry_id=1_vuc7b5h2)

$$
  \begin{array}{l}
    \mathrm{d} B^{a_1 a_2}
    -
    \omega^{a_1 a_2}{}_{a'_1 a'_2} \, B^{a'_1 a'_2}
    \;=\;
    \mathrm{d} B^{a_1 a_2}
    -\omega^{a_1}{}_{a'_1} B^{a'_1 a_2}
    -\omega^{a_2}{}_{a'_2} B^{a_1 a'_2}    
  \end{array}
$$

$$
  \omega^{a_1 a_2}{}_{a'_1 a'_2}
  \;=\;
  2
   \omega^{[a_1}{}_{[a'_1}
   \delta^{a_2]}_{a'_2]}
$$

$$
  \begin{array}{l}
    2
     \omega^{[a_1}{}_{[a'_1}
     \delta^{a_2]}_{a'_2]}
    B^{a'_1 a'_2}
    \\
    \;=\;
    2
     \omega^{[a_1}{}_{a'_1}
     \delta^{a_2]}_{a'_2}
    B^{a'_1 a'_2}    
    \\
    \;=\;
     \omega^{a_1}{}_{a'_1}
     \delta^{a_2}_{a'_2}
    B^{a'_1 a'_2}    
    -
    \underset{
     \omega^{a_2}{}_{a'_1}
     \delta^{a_1}_{a'_2}
    }{
    \underbrace{
     \omega^{a_2}{}_{a'_2}
     \delta^{a_1}_{a'_1}
    B^{a'_2 a'_1}    
    }
    }
    \\
    \;=\;
    \;=\;
     \omega^{a_1}{}_{a'_1}
     \delta^{a_2}_{a'_2}
    B^{a'_1 a'_2}    
    +
     \omega^{a_2}{}_{a'_2}
     \delta^{a_1}_{a'_1}
    B^{a'_1 a'_2}    
  \end{array}
$$

$$
  e_{a_1 a_2}
  \;=\;
  e^{a} B_{a,  a_1 a_2}
$$

$$
  \begin{array}{l}
    \mathrm{d}^\omega
    e_{a_1 a_2}
    \\
    \;=\;
    \mathrm{d}^\omega\big(e^{a} B_{a,  a_1 a_2}\big)
    \\
    \;=\;
    e^{a} e^{b} (\nabla_{b} B_{a, a_1 a_2})
  \end{array}
$$

$$
  \epsilon^{a_1 b_1 b_2 b_3}
  \nabla_{(a_2}
  B_{b_1) b_2 b_3}
$$

$$
  e_{a_1 a_2}
  \;\equiv\;
  e^{a} e^\mu_a \partial_\mu B_{a_1 a_2}
$$

$$
  e^\mu_{[a} \partial_\mu B_{a_1 a_2]}
$$



\begin{tikzcd}
	{E'} & {B'} \\
	\bullet & B \\
	E & B
	\arrow["{p'}", from=1-1, to=1-2]
	\arrow[from=2-1, to=1-1]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=2-1, to=1-2]
	\arrow[from=2-1, to=2-2]
	\arrow["{\varphi^{\sharp}}"', from=2-1, to=3-1]
	\arrow["\varphi"', from=2-2, to=1-2]
	\arrow["p"', from=3-1, to=3-2]
	\arrow[equal, from=3-2, to=2-2]
\end{tikzcd}

\begin{tikzcd}[sep= scriptsize]
	{E'} & {B'} \\
	\bullet & B \\
	E & B
	\arrow["{p'}", from=1-1, to=1-2]
	\arrow[from=2-1, to=1-1]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=2-1, to=1-2]
	\arrow[from=2-1, to=2-2]
	\arrow["{\varphi^{\sharp}}"', from=2-1, to=3-1]
	\arrow["\varphi"', from=2-2, to=1-2]
	\arrow["p"', from=3-1, to=3-2]
	\arrow[no head, from=3-2, to=2-2]
\end{tikzcd}

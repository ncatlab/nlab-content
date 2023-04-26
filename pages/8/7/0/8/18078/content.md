
Given a [[pseudofunctor]]
\[
  \label{ThePseudofunctor}
  \array{
    \mathllap{
      \mathbf{C} \,\colon\,
      \;
    }
    Base &\longrightarrow& Cat
    \\
    \mathcal{X} &\mapsto& \mathbf{C}_{\mathcal{X}}
    \\
    \Big\downarrow\mathrlap{{}^{f}}
    &&
    \mathllap{^{f^\ast}}\Big\uparrow
    \Big\downarrow\mathrlap{{}^{f_!}}
    \\
    \mathcal{Y} &\mapsto& \mathbf{C}_{\mathcal{Y}}
  }
\]
such that 

1. $Base$ is cocomplete

2. $\mathbf{C}_{\mathcal{X}}$ is [[cocomplete category|cocomplete]] for each $\mathcal{X} \in Base$ 

then also the [[Grothendieck construction]] $\int_{\mathcal{X}} \mathbf{C}_{\mathcal{X}} \,\in\, Cat$ is cocomplete.

Explicitly, [[colimits]] in $\int_{\mathcal{X}} \mathbf{C}_{\mathcal{X}}$ are computed as follows:

Given a diagram in the Grothendieck construction

$$
  \mathscr{V}_{\mathcal{X}}
  \;\colon\;
  I
  \longrightarrow
  \int \mathbf{C}_{(-)}
$$ 

its [[underlying]] diagram in $Base$

$$
  \mathcal{X}
  \;\colon\;
  I
  \overset{ \mathscr{V}_{\mathcal{X}} }{\longrightarrow}
  \int \mathbf{C}_{(-)}
  \overset{\pi}{\longrightarrow}
  Base
$$

has a colimit by assumption on $Base$, with [[coprojection]] morphisms to be denoted like this:

$$
  \mathcal{X}(i) 
   \overset{\;\; q(i) \;\;}{\longrightarrow}
  \underset{\underset{j \in I}{\longrightarrow}}{\lim}
  \mathcal{X}(j)
  \,.
$$

Now the idea is that the full colimit in $\int \mathbf{C}_{(-)}$ is obtained by 

1. first pushing all morphisms $\phi \colon f_!\mathscr{V}(i) \to \mathscr{V}(j)$ in the diagram forward along the respective $q_j$

1. to hence obtain a diagram $q_! \mathscr{V}$ in $\mathbf{C}_{\underset{\longrightarrow}{\lim} \mathcal{X}}$

1. whose colimit $\underset{\longrightarrow}{\lim} q_! \mathscr{V}$ exists by assumption on $\mathbf{C}$

and then $\big(\underset{\longrightarrow}{\lim} q_! \mathscr{V}\big)_{\underset{\longrightarrow}{\lim}\mathcal{X}}$ is the desired colimit in $\int \mathbf{C}$




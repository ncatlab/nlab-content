

$\amalg$ $\times$

For $\mathbb{K}$ a [[field]], let $R \coloneqq \mathbb{K} \oplus x \mathbb{K}$ be its [[ring of dual numbers]], i.e. with $x^2 = 0$. 

Denote its [[augmented algebra|augmentation]] by

$$
  \array{
    \mathllap{
    \epsilon
    \;\colon\;
    }
    \mathbb{K} \oplus \mathbb{K} \cdot x
    &\longrightarrow&
    \mathbb{K}
    \\
    a + b x &\mapsto& a
  }
$$

Via this [[ring homomorphism]] we regard $\mathbb{K}$ as an $R$-[[module]].

Now in the category $Ch_\bullet(R Mod)$, consider then the following unbounded chain complex:

$$
  \mathcal{A}
  \;\coloneqq\;
  \left(
  \cdots
  \to 
  \mathbb{K} \oplus \mathbb{K}x
  \xrightarrow{
    \;\;
    \cdot x
    \;\;
  }
  \mathbb{K} \oplus \mathbb{K}x
  \xrightarrow{
    \;\;
    \cdot x
    \;\;
  }
  \mathbb{K} \oplus \mathbb{K}x
  \to 
  \cdots
  \right)
  \,.
$$
Since its [[chain homology]] clearly vanishes in every degree, the morphism it receives out of the [[zero object]] is a [[quasi-isomorphism]] and hence a [[weak equivalence]]
$$
  0 \underset{\in \mathrm{W}}{\longrightarrow} \mathcal{A}
$$
and hence would be an [[acyclic cofibration]] if $\mathcal{A}$ were cofibrant.

But consider then the following [[lifting problem]] with this morphism

$$
  \array{
    &\longrightarrow&
    \big(
      \cdots \to 0 \to 0 \to R \to 0 \to 0 \to \cdots
    \big)
    \\
    \Bigg\downarrow
    &&
    \Bigg\downarrow
    {}^{
      \epsilon
    }
    \\
    \mathcal{A}
    &
    \overset{
      \;\;
      \epsilon
      \;\;\;
    }{
      \longrightarrow
    }
    &
    \big(
      \cdots \to 0 \to 0 \to \mathbb{K} \to 0 \to 0 \to \cdots
    \big)
    \mathrlap{\,,.}
  }
$$

Since the morphism on the right is clearly degreewise surjective and hence a [[fibration]] in the model structure, cofibrancy of $\mathcal{A}$ would imply that a [[lift]] in this diagram exists. But to be even a lift of the [[underlying]] [[graded modules]] this lift would have to be the [[identity morphism]] on $R$ in degree 0, in order to make (in degree 0), this [[diagram]] of $R$-[[modules]] [[commuting diagram|commute]]:

$$
  \array{
    && R
    \\
    & \mathllap{^{id}}\nearrow 
    & \downarrow \mathrlap{^\epsilon}
    \\
    R &\underset{\epsilon}{\longrightarrow}& \mathbb{K}
  }
$$

But that underlying lift fails to be a [[chain map]] in degrees (-1,0), where the following [[diagram]] does *not* [[commuting diagram|commute]]

$$
  \array{
    0 
    &\longrightarrow&
    \mathbb{K} \oplus x \mathbb{X}     
    \\
    \mathllap{^{id}}
    \Big\uparrow
    &\color{red}\times&
    \Big\uparrow
    \mathrlap{^{id}}
    \\
    \mathbb{K} \oplus x \mathbb{X} 
    &\underset{\cdot x}{\longrightarrow}&      
    \mathbb{K} \oplus x \mathbb{X} 
  }
$$

It follows that the lift does not exist, hence that the chain complex $\mathcal{A}$ is not cofibrant.





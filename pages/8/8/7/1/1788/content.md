Given the equivalence between monads in a [[2-category]] $K$ and [[lax functors]] $1 \to K$ it is straightforward to define the [[2-category]] $Mnd(K)$ of monads in $K$ to be the [[lax functor|lax]] [[functor category]] $[1,K]_\ell$, which consists of [[lax functors]], [[lax transformations]] and their[[modifications]].

Spelling this out, we see that  

1. an [[object]] in $Mnd(K)$ is a monad $(a,t,\eta,\mu)$ in $K$;

1. a [[1-morphism]] $(a,t) \to (b,s)$ in Mnd(K)$ is given by 

   1. a [[1-morphism]] $x \colon a \to b$ 

   1. a [[2-morphisms]] $\lambda \colon s x \to x t$ 

   making the following [[commuting diagram|diagrams commute]]:

   $$
   \array{
     x & \stackrel{\eta^s x}{\to} & s x 
     \\
     \mathllap{x \eta^t} 
     \big\downarrow 
       & & 
     \big\downarrow    
     \mathrlap{\lambda} 
     \\
     x t 
      & \overset{1}{\longrightarrow} & 
     x t
   }
   \qquad \qquad
   \array{
      s s x 
      & 
      \overset{s \lambda}{\to} 
      & s x t &    
      \overset{\lambda t}{\longrightarrow}
      & x t t 
      \\
      \mathllap{\mu^s x} 
      \big\downarrow 
        & & & & 
      \big\downarrow 
      \mathrlap{x \mu^t}
      \\
      s x 
      & & 
      \overset{\lambda}{\longrightarrow} 
      & & 
      x t
   }
   $$



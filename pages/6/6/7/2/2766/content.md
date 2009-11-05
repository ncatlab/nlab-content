## Definition 

Let $F:J\to C$ be a [[diagram]] in a category $C$. Also, for any objects $c,c'$ in $C$, let $T:\Delta(c)\to F$ and $T':\Delta(c')\to F$ denote [[cones]] over $F$. 

A **cone morphism** is a [[natural transformation]] $\alpha\colon \Delta(c)\to\Delta(c')$ such that the diagram
$$\array{
\Delta(c) &{}&\stackrel{\alpha}{\longrightarrow} &{}& \Delta(c') \\
{}& \mathllap{\scriptsize{T}}\searrow &{}& \swarrow\mathrlap{\scriptsize{T'}} &{}  \\
{}&{}&F&{}&{}
}
$$
commutes.  Note that naturality of any such $\alpha$ implies that for all $i,j\in J$, $\alpha_i=\alpha_j$, so that $\alpha=\Delta(\phi)$ for some $\phi : c \to c'$ in $C$.  The single component $\phi$ itself is often referred to as the cone morphism.

An equivalent definition of a cone morphism $\phi : T \to T'$ says that all component diagrams
$$\array{
c &{}&\stackrel{\phi}{\longrightarrow} &{}& c' \\
{}& \mathllap{\scriptsize{T_j}}\searrow &{}& \swarrow\mathrlap{\scriptsize{T'_j}} &{}  \\
{}&{}&F(j)&{}&{}
}
$$
commute.

## Discussion

The following discussion took place at the component diagram above:

[[Eric]]: What is the "component free" way to say that?

[[Finn Lawler]]:  I think the category of cones over $F$ is the comma category $\Delta / F$, so that a morphism $\alpha : T \to T'$ should be just a natural transformation $\alpha : \Delta c \Rightarrow \Delta c'$ such that $T' \alpha = T$.  That gives your condition in components, I think.

[[Eric]]: Thanks Finn! I'm still learning all this, so it'll take me some time to absorb what you said. It sounds good though :) Either way, it sounds like some potentially good additional content.

[[Finn Lawler]]:  I should point out that a natural transformation $\alpha: \Delta c \Rightarrow \Delta c'$ is very nearly exactly the same thing as a morphism $\phi: c \to c'$ (it's $\phi$ in each component, which you'll see if you draw $\alpha$'s naturality square, so it's $\Delta \phi$ for some $\phi$).  Now look at the triangle above, write $\Delta \phi : \Delta c \to \Delta c'$ instead of $\phi$ and erase the $j$s and you have the morphism in the comma category.

I hope this helps.  If it's done the opposite, apologies.  I've a habit of trying the one and accomplishing the other.

[[Eric]]: Hmm. I'm probably confused, but when I draw the naturality square for $\alpha:\Delta(c)\to\Delta(c')$, I get
$$
  \array{ 
    c 
    & 
    \stackrel{Id_c}{\to} 
    & 
    c 
    \\ 
    \alpha_j\downarrow 
    && 
    \downarrow \alpha_{k} 
    \\ c' 
    & 
    \stackrel{Id_{c'}}{\to} & c' 
  }
  \,. 
$$ 
for every $j,k\in J$.

[[Eric]]: I think I got it. My diagram is correct, except we have $\alpha_j = \alpha_k$ and we want this to be $\phi:c\to c'$. I made that more explicit in the definition above by adding "whose component is $\phi:c\to c'$." 

The full blown diagram looks like

$$ 
  \array{ 
    c 
    & 
    \stackrel{Id_c}{\to} 
    & 
    c 
    \\ 
    \mathllap{\scriptsize{\phi}}\downarrow
    && 
    \downarrow\mathrlap{\scriptsize{\phi}}
    \\ c' 
    & 
    \stackrel{Id_{c'}}{\to} & c' \\
    \mathllap{\scriptsize{T'_j}}\downarrow
    && 
    \downarrow\mathrlap{\scriptsize{T'_k}}
    \\ 
    F(j)&\stackrel{F(f)}{\to}&F(k)
  }
$$


[[!redirects cone morphisms]]
[[!redirects cone function]]
[[!redirects cone functions]]
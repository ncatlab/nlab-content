This implies in particular that

**higher super [[nLab:Lie integration]] preserves [[nLab:homotopy fiber sequences]]**
 
$\phantom{AAAAA}$hence in particular [[nLab:higher central extensions]]

$\phantom{AAAA}$$
  \array{
  Super L_\infty Algebras && SuperSpaces
  \\
  \array{
    \widehat{\mathfrak{g}}
    \\
    {}^{\mathllap{hofib(\mu_{p+2})}}\Big\downarrow
    \\
    \mathfrak{g}
    &\overset{ \mu_{p+2} }{\longrightarrow}&
    B^{p+1} \mathbb{R}
  }
  &
  \phantom{AAAA}
  \overset{ Spec\big(CE(-)\big) }{\mapsto}
  \phantom{AAAA}
  &
  \array{
    \mathbf{B} \widehat{G}
    \\
    {}^{\mathllap{hofib(\mathbf{c}_{p+2})}}\Big\downarrow
    \\
    \mathbf{B}G
    &\overset{ \mathbf{c}_{p+2} }{\longrightarrow}&
    \mathbf{B}^{p+2} \mathbb{R}
  }
  }
$

[[some_picture.png:pic]]

[[some_picture.png|alt_text:pic]]


$$
  \array{
    \Omega X &\overset{\Omega c}{\longrightarrow}& \Omega A
    &\overset{ \text{connecting} \atop \text{homomorphism} }{\longrightarrow}& \widehat X
    \\
    && && {}^{\mathllap{hofib(c)}}\Big\downarrow
    \\
    && && X &\underset{c}{\longrightarrow}& A
  }
$$


* {#Wellen18} [[Felix Wellen]], _[[schreiber:thesis Wellen|Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966), [thesis pdf](http://www.math.kit.edu/iag3/~wellen/media/diss.pdf))


$
  \underset{ 
     \color{blue} \text{Sullivan de Rham adjunction}
  }{
  \underbrace{
  \underset{\phantom{A} \atop \phantom{A}}{
  dgcSuperAlg^{op}_{\mathbb{R}, \geq 0, proj}
    \;
   \underset{
     \color{blue}
     {\text{higher super}
     \atop
     \text{Lie integration} }
   }{
   \underbrace{
    \underset{
      \phantom{A} \atop \phantom{A}
    }{
    \underoverset
      {\underset{ Spec }{\longrightarrow}}
      {\overset{ \mathcal{O} }{\longleftarrow}}
      {\phantom{A}\phantom{{}_{Qu}}\bot_{Qu}\phantom{A}}
   }}}
    \;
  Funct\left( SuperCartSp^{op},sSet_{Qu}\right)_{loc}
    \;
  \overset{
    \color{blue}{
    \text{include }
    \atop
    {
     \text{geometrically discrete}
     \atop
     \text{∞-groupoids}
    }}
  }{
  \overbrace{
    \overset{ \phantom{A} \atop \phantom{A} }{
    \underoverset
      {\underset{\Gamma}{\longrightarrow}}
      {\overset{const}{\longleftarrow}}
      {\phantom{A}\phantom{{}_{Qu}}\bot_{Qu}\phantom{A}}
  }}}
    \;
  sSet_{Qu}
  }}
  }
    \;
  \overset{
    \color{blue}{
    \text{regard ∞-groupoids}
    \atop
    \text{as topological spaces}
    }
  }{
  \overbrace{
    \overset{ \phantom{A} \atop \phantom{A} }{
    \underoverset
      {\underset{Sing}{\longleftarrow}}
      {\overset{{\vert- \vert}}{\longrightarrow}}
      {\phantom{A}\phantom{{}_{Qu}}\simeq_{Qu}\phantom{A}}
   }}}
    \;
  Top_{Qu}
$

Test
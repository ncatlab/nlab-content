<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

_Under construction._

## Idea

The idea here is to extend [[Bob Coecke|Coecke's]] graphical rules for completely positive maps in order to develop more sophisticated category-theoretic diagrams while maintaining the simplicity of the "object-arrow" representation ([pdf](http://www.comlab.ox.ac.uk/files/666/RR-07-05.pdf)).  Two problems that could benefit from this analysis are the [[Birkhoff-von Neumann theorem]] and the study of [[extremal quantum channel]]s.

## Simple channels

### Simple channel carrying quantum information
Consider a channel mapping a set of operators on a Hilbert space, $L(\mathcal{H}_{1})$, to another set of operators on a Hilbert space, $L(\mathcal{H}_{2})$.  It can be represented by a simple digraph with an associated arrow diagram as follows:
$$
  \array{
    Digraph && Arrow diagram
    \\
    \\
    \bullet && L(\mathcal{H}_{1})
    \\
    \downarrow && \downarrow
    \\
    \bullet && L(\mathcal{H}_{2})
  }
  \,.
$$
Notice that this is a complete graph, $K_{2}$.

### Simple channel carrying quantum and classical information
Consider a channel that takes as its input $L(\mathcal{H}_{1})\otimes C(X)$ where $C(X)$ is a set of continuous operators on some space $X$ and that represents classical information.  Take the output of this channel to be $L(\mathcal{H}_{2})$.  The associated representations are:
$$
  \array{
    & Digraph && Arrow diagram &
    \\
    \\
    \bullet && \bullet && L(\mathcal{H}_{1}) && C(X)
    \\
    \searrow && \swarrow && \searrow && \swarrow
    \\
    & \bullet &&&& L(\mathcal{H}_{1}) \otimes C(X) & \\
    & \downarrow &&&& \downarrow \\
    & \bullet &&&& L(\mathcal{H}_{2})
  }
  \,.
$$

## Copies of channels
Now consider two copies of a channel $\varepsilon: A \to R(A)$.  Coecke's model would look like:

 <svg width="250" height="300" xmlns="http://www.w3.org/2000/svg" se:nonce="41666" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <g>
  <title>Layer 1</title>
  <line x1="127" y1="152" x2="128" y2="152" id="svg_2193_1" stroke="#000000" stroke-width="2" fill="none"/>
  <text x="118" y="80" id="svg_2193_12" fill="#000000" stroke="#000000" stroke-width="0" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve"/>
  <text x="133" y="67" id="svg_2193_14" fill="#000000" stroke="#000000" stroke-width="0" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve"/>
  <g id="svg_41666_1">
   <line x1="94.00002" y1="47.2381" x2="94.00002" y2="128.2381" id="svg_2193_2" stroke="#000000" stroke-width="2" fill="none"/>
   <rect x="74.00002" y="127.2381" width="41" height="41" id="svg_2193_3" fill="#FF0000" stroke="#000000" stroke-width="2"/>
   <line x1="93.04764" y1="169.2381" x2="93.04764" y2="250.2381" stroke="#000000" stroke-width="2" fill="none" id="svg_2193_4"/>
   <line x1="86.04764" y1="208.2381" x2="92.04764" y2="216.2381" id="svg_2193_5" stroke="#000000" stroke-width="2" fill="none"/>
   <line x1="98.04764" y1="208.2381" x2="93.04764" y2="216.2381" id="svg_2193_6" stroke="#000000" stroke-width="2" fill="none"/>
   <line x1="150.00002" y1="47.2381" x2="150.00002" y2="128.2381" stroke="#000000" stroke-width="2" fill="none" id="svg_2193_7"/>
   <rect x="130.00002" y="127.2381" width="41" height="41" fill="#FF0000" stroke="#000000" stroke-width="2" id="svg_2193_8"/>
   <line x1="149.04764" y1="169.2381" x2="149.04764" y2="250.2381" stroke="#000000" stroke-width="2" fill="none" id="svg_2193_9"/>
   <line x1="142.04764" y1="208.2381" x2="148.04764" y2="216.2381" stroke="#000000" stroke-width="2" fill="none" id="svg_2193_10"/>
   <line x1="154.04764" y1="208.2381" x2="149.04764" y2="216.2381" stroke="#000000" stroke-width="2" fill="none" id="svg_2193_11"/>
   <text x="95" y="41.238" id="svg_2193_16" fill="#000000" stroke="#000000" stroke-width="0" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">A</text>
   <text x="149" y="40.238" id="svg_2193_17" fill="#000000" stroke="#000000" stroke-width="0" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">A</text>
   <text x="93.048" y="273.19" id="svg_2193_18" fill="#000000" stroke="#000000" stroke-width="0" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">R(A)</text>
   <text x="150.048" y="272.19" id="svg_2193_19" fill="#000000" stroke="#000000" stroke-width="0" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">R(A)</text>
  </g>
 </g>
</svg>

and I'll have to come back to this...
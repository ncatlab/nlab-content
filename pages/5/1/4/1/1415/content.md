### What this page is for ###

This Sandbox is specifically for mucking about with SVGs.  The point is that these pictures can get rather large (particularly if automatically generated - does anyone write their own?).  A Sandbox, such as [[Sandbox|this one]] is for trying things out.  Usually those are little things, such as getting the correct syntax for something, so if the Sandbox gets really big and takes ages to load and resubmit, it gets difficult to try out lots of little changes.  One SVG, such as my original one, can easily swamp the 'box.  However, as I've found out, getting SVGs to work in Instiki can take a little tweaking so this 'box is for that.

One shouldn't leave an SVG here for long.  I don't think that there's much to be learnt from looking through someone else's SVG code (unlike in the original [[Sandbox]] where it can be useful to scan through and see how something is done).  Rather, you should muck about with your SVG, get it right, and then transfer it across to the requisite page.

A reasonable rule would be that the author should delete it when they are finished with it, and that the maximum lifespan of a picture here is, say, 1 week.  To make this easier to police, please timestamp your SVGs.

Obviously as we play with these then we'll learn various strategies.  These should be added to the [[FAQ]] or [[HowTo]] pages as appropriate.  Maybe we should have a list of SVGs in the n-Lab so that people can find examples of what can be done and how to do it, this could be commented with what has had to be done to get it to work in Instiki.  If someone has a particularly nice example, or one they're particularly proud of, but doesn't really fit into an "honest" page on the n-Lab then may I suggest they put it on their userpage (I'll probably do that with the "map of manifolds" one since it doesn't really fit anywhere else).


##### Original import from the [[Sandbox]] #####

Testing tikzpicture to svg capability.

###### Timestamp: 2009-05-08 ######

(removed; see [revision 10](http://ncatlab.org/nlab/revision/Sandbox+>+SVG/10))

Not bad!  Thanks to Jacques, the sphere is fine now.  This picture is probably a little too big to leave in the sandbox so I'll remove it soon - just want to show off a little first!  For the original, see [Comparative Smootheology at Ottawa](http://www.math.ntnu.no/~stacey/Seminars/ottawa.html).


+-- {: .query}
Been a while since I thought about getting a good graphics engine here in inStiki, but these pictures have got me excited again. Right now I am thinking that the following procedure could work well:

* You draw a picture using your favourite method (TikZ, Inkscape, etc.)

* You export it as an svg file.

* You copy and paste this svg text into the nLab page you are editing.

* Now you click "Submit" as usual. 

* Here's the trick: the next time someone clicks "Edit page" in the nLab, the Instiki software is intelligent and displays the SVG text as a javascript "expand box". In other words, there's a little command in the text "Expand SVG code (+)" and if you click the (+), it expands all the code out. If you click "(-)", the code collapses again. This way we don't get large swathes of SVG code cluttering up the text area.

* Perhaps the software can be more advanced and remember if someone has altered any of the SVG segments of code. If not, it shouldn't be resubmitted when someone clicks "Submit",  otherwise it will make for slow uploads.

[[Bruce Bartlett]]

One method that would solve a lot of that would be to have the SVGs as external files that are then included at the appropriate point.  I don't know whether or not that is possible, though.

Another thing is that exported files can often contain a lot of "junk" (cafeful examination of my picture will reveal that it uses 5 decimal places; perhaps slightly over-accurate).  Some way of automatically trimming this down would be helpful.

I think it's okay to add another step into your scheme, between the export and copying into Instiki, but it needs to be an easy one, say a script that modifies things a little to be acceptable to Instiki.  However, what that needs to do will only become apparent with a little experimentation.

[[Andrew Stacey]]

Well, you can certainly upload files here in Instiki, and I think that method would be possible. But then we're back to the Fundamental Conundrum: 

_If we're going to start including files, you might as well export your graphic as a png file and include it the old-fashioned way._

It's the old problem: SVG and MathML have not been built so that one can use them both simultaneously (I think).

[[Bruce Bartlett]]


=--

Doing a quick LaTeX -> Inkscape -> SVG -> nLab test [[Bruce Bartlett]]: 

###### Timestamp: 2009-05-08 ######

(removed; see [revision 10](http://ncatlab.org/nlab/revision/Sandbox+>+SVG/10))

As you can see, the trouble with this method is that Inkscape is exporting the text as spline primitives... which takes up way too much space. I guess that just returns to the old problem: you can't mix MathML and SVG. Now I remember (I _knew_ there was some kind of nasty problem with this MathML, SVG and Instiki thing... and now 
I remember).  [[Bruce Bartlett]]

Ok, I'm giving it another go. Now I'm trying Andrew's method --- you do a diagram:

(removed; see [revision 10](http://ncatlab.org/nlab/revision/Sandbox+>+SVG/10)) 


_Mike_: Here is a little diagram produced from the following TikZ code:

    \begin{tikzpicture}[auto,scale=2]
      \node (A) at (0,0) {$A^2$};
      \node (B) at (2,0) {$\int B$};
      \node (C) at (1,1) {$\sum_0^\infty C$};
      \draw[->] (A) to node[swap] {$\phi$} (B);
      \draw[->] (A) to node {$\psi$} (C);
      \draw[->] (C) to node {$\theta$} (B);
      \draw[->] (1,0.5) to node {$\mu$} (1,0.3);
    \end{tikzpicture}

run through htlatex, and with the `<tspan>`s then manually replaced by the appropriate foreignObject tags:

(removed; see [revision 10](http://ncatlab.org/nlab/revision/Sandbox+>+SVG/10)) 

_Bruce_ : Hey, this is great Mike! For anyone reading this thread, who wants to contribute, don't forget about the [nForum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=20&page=1#Comment_95) page where we are discussing this stuff. 

_Toby_:  Here\'s the diagram again, but *without* the SVG code in the edit box, thanks to the magic of inclusions!

[[!include Inclusion Sandbox]]

(This is included from the new [[Inclusion Sandbox]].)

_Bruce_: The files I received from Olivier Binda, which includes a nice comprehensive test suite of how his patch to htlatex (which changes ordinary text in SVG into foreignobject tags) performs, are available here: [[LD_Svg_Tests_files.zip|LD@Svg@Tests_files:file]]

These three diagrams are testing re-use of SVG code.  The arrowheads are reused from diagram to diagram.  The first picture defines the arrowhead once and then reuses it for each of the arrows.  The second picture does not define the arrowhead so must get it from the first picture.  The third picture also does not define the arrowhead but refers to the arrowhead from the picture in the [[Inclusion Sandbox]].  As can be seen, it works.  One thing to test would be to have different arrowheads here and in the [[Inclusion Sandbox]] but with the same name and see which one gets used (my guess would be the definition closest above where it is used).

(removed; see [revision 12](http://ncatlab.org/nlab/revision/Sandbox+>+SVG/12)) 

Given that inclusions and references seem to work fine, it seems a reasonable idea to have a list of "standard" arrowheads.  Here's one such, loosely based on the types of arrowhead that the xy package considers as standard.

###### Date stamp: 5th June 2009

<svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="500" height="400">
<defs>
    <marker id="filledArrow" viewBox="0 0 10 10" refX="10" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="10" markerHeight="10"
	    orient="auto">
      <path d="M 0 0 L 10 5 L 0 10 z" />
    </marker>
    <marker id="basicArrow" viewBox="0 0 10 10" refX="10" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="10" markerHeight="10"
	    orient="auto">
      <path d="M 0 0 L 10 5 L 0 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="doubleArrow" viewBox="0 0 15 10" refX="10" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="15" markerHeight="10"
	    orient="auto">
      <path d="M 0 0 L 10 5 L 0 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 5 0 L 15 5 L 5 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="barArrow" viewBox="0 0 10 10" refX="10" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="10" markerHeight="10"
	    orient="auto">
      <path d="M 0 0 L 10 5 L 0 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 10 0 L 10 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="bardoubleArrow" viewBox="0 0 15 10" refX="10" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="15" markerHeight="10"
	    orient="auto">
      <path d="M 0 0 L 10 5 L 0 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 5 0 L 15 5 L 5 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 15 0 L 15 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="parenthesisArrow" viewBox="0 0 5 10" refX="5" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="5" markerHeight="10"
	    orient="auto">
      <path d="M 0 0 Q 10 5 0 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="reversebasicArrow" viewBox="0 0 10 10" refX="0" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="10" markerHeight="10"
	    orient="auto">
      <path d="M 10 0 L 0 5 L 10 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="reversedoubleArrow" viewBox="0 0 15 10" refX="5" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="15" markerHeight="10"
	    orient="auto">
      <path d="M 10 0 L 0 5 L 10 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 15 0 L 5 5 L 15 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="reversebarArrow" viewBox="0 0 10 10" refX="0" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="10" markerHeight="10"
	    orient="auto">
      <path d="M 10 0 L 0 5 L 10 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 0 0 L 0 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="reversebardoubleArrow" viewBox="0 0 15 10" refX="5" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="15" markerHeight="10"
	    orient="auto">
      <path d="M 10 0 L 0 5 L 10 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 15 0 L 5 5 L 15 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 0 0 L 0 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="reverseparenthesisArrow" viewBox="0 0 5 10" refX="0" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="5" markerHeight="10"
	    orient="auto">
      <path d="M 5 0 Q -5 5 5 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="slashArrow" viewBox="0 0 5 10" refX="2.5" refY="5" 
	    markerUnits="strokeWidth"
	    markerWidth="5" markerHeight="10"
	    orient="auto">
      <path d="M 5 0 L 0 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="doubleslashArrow" viewBox="0 0 10 10" refX="2.5" refY="5"
	    markerUnits="strokeWidth"
	    markerWidth="10" markerHeight="10"
	    orient="auto">
      <path d="M 0 0 L 5 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 5 0 L 10 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="crossArrow" viewBox="0 0 10 10" refX="5" refY="5"
	    markerUnits="strokeWidth"
	    markerWidth="10" markerHeight="10"
	    orient="auto">
      <path d="M 0 0 L 10 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 10 0 L 0 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="plusArrow" viewBox="0 0 10 10" refX="5" refY="5"
	    markerUnits="strokeWidth"
	    markerWidth="10" markerHeight="10"
	    orient="auto">
      <path d="M 5 0 L 5 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 0 5 L 10 5" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="vbarArrow" viewBox="0 0 5 10" refX="2.5" refY="5"
	    markerUnits="strokeWidth"
	    markerWidth="5" markerHeight="10"
	    orient="auto">
      <path d="M 2.5 0 L 2.5 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="doublevbarArrow" viewBox="0 0 10 10" refX="2.5" refY="5"
	    markerUnits="strokeWidth"
	    markerWidth="10" markerHeight="10"
	    orient="auto">
      <path d="M 2.5 0 L 2.5 10" fill="none" stroke="black" stroke-width="1" />
      <path d="M 7.5 0 L 7.5 10" fill="none" stroke="black" stroke-width="1" />
    </marker>
    <marker id="circleArrow" viewBox="0 0 10 10" refX="0.5" refY="5"
	    markerUnits="strokeWidth"
	    markerWidth="10" markerHeight="10"
	    orient="auto">
      <circle cx="5" cy="5" r="4.5" fill="none" stroke="black" stroke-width="1" />
    </marker>
</defs>
<path d="M 20 15 L 100 15 L 200 15" stroke="black" stroke-width="1" marker-start="url(#filledArrow)" marker-mid="url(#filledArrow)" marker-end="url(#filledArrow)" /><text x="220" y="25">filledArrow</text>
<path d="M 20 35 L 100 35 L 200 35" stroke="black" stroke-width="1" marker-start="url(#basicArrow)" marker-mid="url(#basicArrow)" marker-end="url(#basicArrow)" /><text x="220" y="45">basicArrow</text>
<path d="M 20 55 L 100 55 L 200 55" stroke="black" stroke-width="1" marker-start="url(#doubleArrow)" marker-mid="url(#doubleArrow)" marker-end="url(#doubleArrow)" /><text x="220" y="65">doubleArrow</text>
<path d="M 20 75 L 100 75 L 200 75" stroke="black" stroke-width="1" marker-start="url(#barArrow)" marker-mid="url(#barArrow)" marker-end="url(#barArrow)" /><text x="220" y="85">barArrow</text>
<path d="M 20 95 L 100 95 L 200 95" stroke="black" stroke-width="1" marker-start="url(#bardoubleArrow)" marker-mid="url(#bardoubleArrow)" marker-end="url(#bardoubleArrow)" /><text x="220" y="105">bardoubleArrow</text>
<path d="M 20 115 L 100 115 L 200 115" stroke="black" stroke-width="1" marker-start="url(#parenthesisArrow)" marker-mid="url(#parenthesisArrow)" marker-end="url(#parenthesisArrow)" /><text x="220" y="125">parenthesisArrow</text>
<path d="M 20 135 L 100 135 L 200 135" stroke="black" stroke-width="1" marker-start="url(#reversebasicArrow)" marker-mid="url(#reversebasicArrow)" marker-end="url(#reversebasicArrow)" /><text x="220" y="145">reversebasicArrow</text>
<path d="M 20 155 L 100 155 L 200 155" stroke="black" stroke-width="1" marker-start="url(#reversedoubleArrow)" marker-mid="url(#reversedoubleArrow)" marker-end="url(#reversedoubleArrow)" /><text x="220" y="165">reversedoubleArrow</text>
<path d="M 20 175 L 100 175 L 200 175" stroke="black" stroke-width="1" marker-start="url(#reversebarArrow)" marker-mid="url(#reversebarArrow)" marker-end="url(#reversebarArrow)" /><text x="220" y="185">reversebarArrow</text>
<path d="M 20 195 L 100 195 L 200 195" stroke="black" stroke-width="1" marker-start="url(#reversebardoubleArrow)" marker-mid="url(#reversebardoubleArrow)" marker-end="url(#reversebardoubleArrow)" /><text x="220" y="205">reversebardoubleArrow</text>
<path d="M 20 215 L 100 215 L 200 215" stroke="black" stroke-width="1" marker-start="url(#reverseparenthesisArrow)" marker-mid="url(#reverseparenthesisArrow)" marker-end="url(#reverseparenthesisArrow)" /><text x="220" y="225">reverseparenthesisArrow</text>
<path d="M 20 235 L 100 235 L 200 235" stroke="black" stroke-width="1" marker-start="url(#slashArrow)" marker-mid="url(#slashArrow)" marker-end="url(#slashArrow)" /><text x="220" y="245">slashArrow</text>
<path d="M 20 255 L 100 255 L 200 255" stroke="black" stroke-width="1" marker-start="url(#doubleslashArrow)" marker-mid="url(#doubleslashArrow)" marker-end="url(#doubleslashArrow)" /><text x="220" y="265">doubleslashArrow</text>
<path d="M 20 275 L 100 275 L 200 275" stroke="black" stroke-width="1" marker-start="url(#crossArrow)" marker-mid="url(#crossArrow)" marker-end="url(#crossArrow)" /><text x="220" y="285">crossArrow</text>
<path d="M 20 295 L 100 295 L 200 295" stroke="black" stroke-width="1" marker-start="url(#plusArrow)" marker-mid="url(#plusArrow)" marker-end="url(#plusArrow)" /><text x="220" y="305">plusArrow</text>
<path d="M 20 315 L 100 315 L 200 315" stroke="black" stroke-width="1" marker-start="url(#vbarArrow)" marker-mid="url(#vbarArrow)" marker-end="url(#vbarArrow)" /><text x="220" y="325">vbarArrow</text>
<path d="M 20 335 L 100 335 L 200 335" stroke="black" stroke-width="1" marker-start="url(#doublevbarArrow)" marker-mid="url(#doublevbarArrow)" marker-end="url(#doublevbarArrow)" /><text x="220" y="345">doublevbarArrow</text>
<path d="M 20 355 L 100 355 L 200 355" stroke="black" stroke-width="1" marker-start="url(#circleArrow)" marker-mid="url(#circleArrow)" marker-end="url(#circleArrow)" /><text x="220" y="365">circleArrow</text>
</svg>

What do people think?  Are there others that ought to be considered as "standard"?  Are these okay, or do they need tweaking?

Discussion on the [n-Forum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=31).

And just for Toby and Mike:

$$
\mathfrak{A}
\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="70" height="20">
<path d="M 5 10 L 35 10 L 65 10" marker-mid="url(#vbarArrow)" marker-end="url(#basicArrow)" stroke="black" stroke-width="1" />
</svg>
\end{svg}
\mathfrak{B}
$$

---

<svg width="21ex" height="21.6ex" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/2000/svg">
 <g>
  <title>Layer 1</title>
  <foreignObject x="4ex" y="4ex" width="2.5ex" height="2.8ex">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mstyle displaystyle="false">
     <mrow>
      <mspace width="0ex" height="1.8ex"/>
      <mi>A</mi>
     </mrow>
    </mstyle>
   </math>
  </foreignObject>
  <foreignObject x="14.5ex" y="4ex" width="2.5ex" height="2.8ex">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mstyle displaystyle="false">
     <mrow>
      <mspace width="0ex" height="1.8ex"/>
      <mi>B</mi>
     </mrow>
    </mstyle>
   </math>
  </foreignObject>
  <foreignObject x="4ex" y="14.8ex" width="2.5ex" height="2.8ex">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mstyle displaystyle="false">
     <mrow>
      <mspace width="0ex" height="1.8ex"/>
      <mi>C</mi>
     </mrow>
    </mstyle>
   </math>
  </foreignObject>
  <foreignObject x="14.5ex" y="14.8ex" width="2.5ex" height="2.8ex">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mstyle displaystyle="false">
     <mrow>
      <mspace width="0ex" height="1.8ex"/>
      <mi>D</mi>
     </mrow>
    </mstyle>
   </math>
  </foreignObject>
  <foreignObject x="9.5ex" y="2.6ex" width="2ex" height="2.8ex">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mstyle displaystyle="false">
     <mrow>
      <mrow>
       <mi>f</mi>
      </mrow>
     </mrow>
    </mstyle>
   </math>
  </foreignObject>
  <foreignObject x="3.25ex" y="9.8ex" width="2ex" height="2.8ex">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mstyle displaystyle="false">
     <mrow>
      <mrow>
       <mi>k</mi>
      </mrow>
     </mrow>
    </mstyle>
   </math>
  </foreignObject>
  <foreignObject x="15.75ex" y="9.8ex" width="2ex" height="2.2ex">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mstyle displaystyle="false">
     <mrow>
      <mrow>
       <mi>g</mi>
      </mrow>
     </mrow>
    </mstyle>
   </math>
  </foreignObject>
  <foreignObject x="9.5ex" y="17ex" width="2ex" height="2.8ex">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mstyle displaystyle="false">
     <mrow>
      <mrow>
       <mi>h</mi>
      </mrow>
     </mrow>
    </mstyle>
   </math>
  </foreignObject>
  <svg width="21ex" height="21.6ex" viewBox="0 0 21 21.6">
   <mask id="ClipB" maskUnits="userSpaceOnUse" maskContentUnits="userSpaceOnUse" x="0" y="0" width="21" height="21.6">
    <rect x="0" y="0" width="21" height="21.6" fill="white"/>
    <g transform="translate(14, 5.4) scale(0.1) rotate(0) translate(-10, -5)">
     <path d="m0,0l10,5l-10,5l10,0l0,-10z" fill="black"/>
    </g>
   </mask>
   <g transform="translate(14, 5.4) scale(0.1) rotate(0) translate(-10, -5)">
    <path d="m0,0l10,5l-10,5" fill="none" stroke="black"/>
   </g>
   <path d="m7,5.4l7,0" fill="none" stroke="black" stroke-width="0.1" mask="url(#ClipB)"/>
   <mask id="ClipC" maskUnits="userSpaceOnUse" maskContentUnits="userSpaceOnUse" x="0" y="0" width="21" height="21.6">
    <rect x="0" y="0" width="21" height="21.6" fill="white"/>
    <g transform="translate(5.25, 14.3) scale(0.1) rotate(90) translate(-10, -5)">
     <path d="m0,0l10,5l-10,5l10,0l0,-10z" fill="black"/>
    </g>
   </mask>
   <g transform="translate(5.25, 14.3) scale(0.1) rotate(90) translate(-10, -5)">
    <path d="m0,0l10,5l-10,5" fill="none" stroke="black"/>
   </g>
   <path d="m5.25,7.3l0,7" fill="none" stroke="black" stroke-width="0.1" mask="url(#ClipC)"/>
   <mask id="ClipD" maskUnits="userSpaceOnUse" maskContentUnits="userSpaceOnUse" x="0" y="0" width="21" height="21.6">
    <rect x="0" y="0" width="21" height="21.6" fill="white"/>
    <g transform="translate(15.75, 14.3) scale(0.1) rotate(90) translate(-10, -5)">
     <path d="m0,0l10,5l-10,5l10,0l0,-10z" fill="black"/>
    </g>
   </mask>
   <g transform="translate(15.75, 14.3) scale(0.1) rotate(90) translate(-10, -5)">
    <path d="m0,0l10,5l-10,5" fill="none" stroke="black"/>
   </g>
   <path d="m15.75,7.3l0,7" fill="none" stroke="black" stroke-width="0.1" mask="url(#ClipD)"/>
   <mask id="ClipE" maskUnits="userSpaceOnUse" maskContentUnits="userSpaceOnUse" x="0" y="0" width="21" height="21.6">
    <rect x="0" y="0" width="21" height="21.6" fill="white"/>
    <g transform="translate(14, 16.2) scale(0.1) rotate(0) translate(-10, -5)">
     <path d="m0,0l10,5l-10,5l10,0l0,-10z" fill="black"/>
    </g>
   </mask>
   <g transform="translate(14, 16.2) scale(0.1) rotate(0) translate(-10, -5)">
    <path d="m0,0l10,5l-10,5" fill="none" stroke="black"/>
   </g>
   <path d="m7,16.200001l7,0" fill="none" stroke="black" stroke-width="0.1" mask="url(#ClipE)"/>
  </svg>
 </g>
</svg>


category: meta

[[!redirects Sandbox > SVG]]
[[!redirects SVG Sandbox]]



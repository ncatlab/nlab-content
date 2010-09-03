
_Rod McGuire_

<!-- regular html comment --> 

xxxx < xxxx

math test: $A=B$. 

Start DIV test:

<div class="XE" json="json stuff" tex="tex stuff">math $A=B$ here</div>

end DIV test.

Div test with markdown="1" and an ending marked span in the kludge version.

<div class="DbE" json="json stuff" markdown="1">math $A=B$ here<span class="DB_end"/></div>

end div test.

Div test with markdown="1" and an without the ending kludge marked span.

<div class="DbE" json="json stuff" markdown="1">math $A=B$ here</div>

another math test: $A=B$.

stating SVG test

<svg width="640" height="480" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="13678">
 <g>
  <title>Layer 1</title>
  <g id="svg_13678_3">
   <line id="svg_13678_1" y2="161.5" x2="33.00116" y1="140.5" x1="0.00116" stroke-width="2" stroke="#000000" fill="none"/>
   <circle id="svg_13678_8" r="6.70703" cy="139.5" cx="11.00116" stroke-width="2" stroke="#000000" fill="#FF0000"/>
   <circle id="svg_13678_9" r="8.94531" cy="161.29999" cx="18.00116" stroke-width="2" stroke="#000000" fill="#FF0000"/>
   <rect fill="#0000ff" stroke="#000000" stroke-width="2" x="25.56784" y="137.25" width="13" height="13" id="svg_13678_2"/>
  </g>
 </g>
</svg>

zz

Ending svg test

auto inserted DBE div

<div class='DBE' markdown='1'
 json='{"id":"NEW","type":"Category","page":"[Rod McGuire]"}'>
 <div><span>{"id":"NEW","type":"Category","page":"[[Rod McGuire]]"}</span></div>
 <div markdown='1'><span>$NEW$ Category</span></div>
 <table><tr><td>id</td><td>NEW</td></tr><tr><td>type</td><td>Category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr></table>
 <span class='DBE'/>
</div>

and another one

<div class='DBE' markdown='1'
 json='{"id":"NEWNEW","type":"Category","page":"[[Rod McGuire]]"}'>
 <div markdown='1'>$NEWNEW$ Category</div>
 <table markdown='1'><tr><td>id</td><td>NEWNEW</td></tr><tr><td>type</td><td>Category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr></table>
 <span class='DBE'/>
</div>

The above example without the DIV wrapper. Internal DIV 1:

<div markdown='1'>$NEWNEW$ Category</div>

Internal TABLE 1:
<table markdown='1'><tr><td>id</td><td>NEWNEW</td></tr><tr><td>type</td><td>Category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr></table>

Internal TABLE 1 with an added row that has math.
<table markdown='1'><tr><td>id</td><td>NEWNEW</td></tr><tr><td>type</td><td>Category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr>
<tr><td>math</td><td>$3=5$</td></tr>
</table>


A test of a table inside a table inside of a table

<table markdown='1' id="tab0">
<tr><td>$a=b$</td><td>[[true]]</td></tr>
<tr><td>arrow</td>
 <td><table markdown='1' id="tab0-1">
      <tr><td>dir</td><td>$\to$</td></tr>
      <tr><td>full</td><td>[[true]]</td></tr>
      <tr><td>op</td><td><table markdown='1'>
       <tr><td>dir</td><td>$\leftarrow$</td></tr>
       </table></td></tr>
 </table></td></tr>
</table>

Make sure table captions work:

<table markdown='1'>
 <caption>$Set_*$ a [[category]]</caption>
 <tr><td>co product</td><td>a [[disjoint union]] where the argument's points are glued together</td></tr>
 <tr><td>initial object</td><td>a pointed singleton set</td></tr>
 <tr><td>has a zero</td><td>[[true]]</td></tr>
</table>
 
Test to make sure id attribute is retained. a DIV:

<div markdown='1' id="myDiv1">this div should have $id = myDiv1$</div>


A test to see if LaTex can appear in an internal link:

Try[[Rod McGuire|$Set_*$]] here.

Try using A tag with markdown=1: <a markdown='1' href="/nlab/show/Rod+McGuire">$Set_*$</a>. OK?

category: people

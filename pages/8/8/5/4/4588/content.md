
_Rod McGuire_

HTML comments only sometimes work

<!-- regular html comment --> 














xxxx < xxxx

math test: $A=B$. 

Div test with markdown="1" and an ending marked span in the kludge version.

<div class="DbE" json="json stuff" markdown="1">math $A=B$ here<span class="DB_end"/></div>

end div test.

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

Ending svg test

auto inserted DBE div

undefined

and another one

undefined

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
 <caption>$Set_*$ a [[category]] of [[pointed set]] objects</caption>
 <tr><td>id</td><td>Set_*</td></tr>
 <tr><td>type</td><td>[[category]]</td></tr>
 <tr><td>objects</td><td>[[pointed set|pointed sets]]</td></tr>
 <tr><td>initial object</td><td>a pointed singleton set</td></tr>
 <tr><td>product</td><td>a [[cartesian product]] where the point is the [[ordered pair|pair]] of the argument points</td></tr>
 <tr><td>co product</td><td>a [[disjoint union]] where the argument's points are glued together</td></tr>
 <tr><td>has a zero object</td><td>[[true]]</td></tr>
</table>
 
Test to make sure id attribute is retained. a DIV:

<div markdown='1' id="myDiv1">this div should have $id = myDiv1$</div>


A test to see if LaTex can appear in an internal link:

Try[[Rod McGuire|$Set_*$]] here.

Try using A tag with markdown=1: <a markdown='1' href="/nlab/show/Rod+McGuire">$Set_*$</a>. OK?

NEW FORMAT

<div class='DBE' markdown='1'
 id='%7B%22id%22%3A%22NEWone%22%2C%22type%22%3A%22Category%22%2C%22page%22%3A%22%5B%5BRod%20McGuire%5D%5D%22%7D'
 json='{"id":"NEWone","type":"Category","page":"[[Rod McGuire]]"}'><table markdown="1"><tr><td>id</td><td>NEWone</td></tr><tr><td>type</td><td>Category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr></table>
 <span class='DBE'/>
</div>

EXAMPLE test1

<div class='DBE' markdown='1'
 id='%7B%22id%22%3A%22test1%22%2C%22a%22%3A%22w%22%2C%22b%22%3A%7B%22c%22%3A%7B%22d%22%3A%22x%22%2C%22e%22%3A%22y%22%7D%2C%22f%22%3A%22z%22%7D%7D'
 json='{"id":"test1","a":"w","b":{"c":{"d":"x","e":"y"},"f":"z"}}'><table markdown="1"><tr><td>id</td><td>test1</td></tr><tr><td>a</td><td>w</td></tr><tr><td>b</td><td><table markdown="1"><tr><td>c</td><td><table markdown="1"><tr><td>d</td><td>x</td></tr><tr><td>e</td><td>y</td></tr></table>
 </td></tr><tr><td>f</td><td>z</td></tr></table>
 </td></tr></table>
 <span class='DBE'/>
</div>

The table inside EXAMPLE test1:

<table markdown="1"><tr><td>id</td><td>test1</td></tr><tr><td>a</td><td>w</td></tr><tr><td>b</td><td><table markdown="1"><tr><td>c</td><td><table markdown="1"><tr><td>d</td><td>x</td></tr><tr><td>e</td><td>y</td></tr></table>
 </td></tr><tr><td>f</td><td>z</td></tr></table>
 </td></tr></table>

<div class='DBE' markdown='1'
 id='%7B%22id%22%3A%22NEWx%22%2C%22type%22%3A%22category%22%2C%22page%22%3A%22%5B%5BRod%20McGuire%5D%5D%22%7D'
 json='{"id":"NEWx","type":"category","page":"[[Rod McGuire]]"}'><table markdown="1"><tr><td>id</td><td>NEWx</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr></table>
 <span class='DBE'/>
</div>

LATEST TESTS:

<div class='DBE' markdown='1'
 id='%7B%22id%22%3A%22NEW%22%2C%22type%22%3A%22category%22%2C%22page%22%3A%22%5B%5BRod%20McGuire%5D%5D%22%7D'
 json='{"id":"NEW","type":"category","page":"[[Rod McGuire]]"}'><table markdown="1"><tr><td>id</td><td>NEW</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr></table>
 <span class='DBE'/>
</div>

xx

<table class='DBE' markdown='1'
 id='{"id":"NEW","type":"category","page":"[[Rod+McGuire]]"}'><table markdown="1"><tr><td>id</td><td>NEW</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod+McGuire]]</td></tr></table>
 </table>
<span class='DBE'/>

cccc

<table class='DBE' markdown='1'
 id='{"id":"NEWxxx","type":"category","page":"[[Rod+McGuire]]"}'><table markdown="1"><tr><td>id</td><td>NEWxxx</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod+McGuire]]</td></tr></table>
 </table>
<span class='DBE'/><!-- span flags end of DBE table - don't remove -->




<table class='DBE' markdown='1'
 id='{"id":"xxxNEW","type":"category","page":"[[Rod+McGuire]]"}'><table markdown="1"><tr><td>id</td><td>xxxNEW</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod+McGuire]]</td></tr></table>
 </table>
<span class='DBE'/><!-- span flags end of DBE table - don't remove -->



<table class='DBE' markdown='1'
 id='{"id":"zzzNEW","type":"category","page":"[[Rod+McGuire]]"}'>
 <caption>Ungenerated DBE table</caption>
</table>
<span class='DBE'/><!-- span flags end of DBE table - don't remove -->

test if trailing multiline comments work

<table class='DBE' markdown='1'
 id='{"id":"xyzzzNEW","type":"category","page":"[[Rod+McGuire]]"}'>
 <caption>Ungenerated DBE table</caption>
</table>
<span class='DBE'/><!-- span flags end of DBE table - don't remove
 a = {a: 1, b: 2}
 -->

end test

category: people



1) abbreviate all special characters in TD - works. Use DQ in json.

<table class='DBE' markdown='1'
 id='{"id":"NEW","type":"category","page":"[[Rod McGuire]]","junkTest":"a &apos; b DQ c &lt; d > &amp; e"}'><tr><td>id</td><td>NEW</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr><tr><td>junkTest</td><td>a SQ b DQ c LB d RB AM e</td></tr></table>
<span class='DBE'/>

2) real SQ and DQ in text works. Abbr LB RB AM.

<table class='DBE' markdown='1'
 id='{"id":"NEW","type":"category","page":"[[Rod McGuire]]","junkTest":"a &apos; b DQ c &lt; d > &amp; e"}'><tr><td>id</td><td>NEW</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr><tr><td>junkTest</td><td>a ' b " c LB d RB AM e</td></tr></table>
<span class='DBE'/>

3) REXML doesn't like unescaped ampersand inside a TD. This conforms to standard.

<table class='DBE' markdown='1'
 id='{"id":"NEW","type":"category","page":"[[Rod McGuire]]","junkTest":"a &apos; b DQ c &lt; d > &amp; e"}'><tr><td>id</td><td>NEW</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr><tr><td>junkTest</td><td>a ' b " c LB d RB & e</td></tr></table>
<span class='DBE'/>

4) Here the ampersand in the td is escaped.

<table class='DBE' markdown='1'
 id='{"id":"NEW","type":"category","page":"[[Rod McGuire]]","junkTest":"a &apos; b DQ c &lt; d > &amp; e"}'><tr><td>id</td><td>NEW</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr><tr><td>junkTest</td><td>a ' b " c LB d RB &amp; e</td></tr></table>
<span class='DBE'/>

5) escaped ampersand and escaped brackets in td.

<table class='DBE' markdown='1'
 id='{"id":"NEW","type":"category","page":"[[Rod McGuire]]","junkTest":"a &apos; b DQ c &lt; d > &amp; e"}'><tr><td>id</td><td>NEW</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr><tr><td>junkTest</td><td>a ' b " c &lt; d > &amp; e</td></tr></table>
<span class='DBE'/>

6) escaped ampersand and unescaped brackets (for &lt;code>) in td. nLab seems to eat the space around the &lt;code> and the capital X appears small, almost lowercase.

<table class='DBE' markdown='1'
 id='{"id":"NEW","type":"category","page":"[[Rod McGuire]]","junkTest":"a &apos; b DQ c &lt; d > &amp; e"}'><tr><td>id</td><td>NEW</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr><tr><td>junkTest</td><td>a ' b " c <code>X</code> &amp; e</td></tr></table>
<span class='DBE'/>

99) as Generated with unescaped brackets in td text causes REXML to not contain error inside the offending table.

<table class='DBE' markdown='1'
 id='{"id":"NEW","type":"category","page":"[[Rod McGuire]]","junkTest":"a &apos; b \" c &lt; d > &amp; e"}'><tr><td>id</td><td>NEW</td></tr><tr><td>type</td><td>category</td></tr><tr><td>page</td><td>[[Rod McGuire]]</td></tr><tr><td>junkTest</td><td>a ' b " c < d > & e</td></tr></table>
<span class='DBE'/>

The END.

category: people

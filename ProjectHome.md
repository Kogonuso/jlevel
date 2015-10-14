/
  * 
  * @author Kogonuso<br />
  * @version 2.0<br />
  * @Since 27TH JANUARY 2013 BUT RELEASED TO THE PUBLIC ON 15TH MARCH, 2013<br /><br />
  * @Licence MIT-LICENCE
  * @contact info.jlevel@gmal.com
  * @webblog http://jlevel4java.blogspot.co.nz/
  * 
<h1>Brief description of JLevel 2.0</h1><br />
> JLevel 2.0 is a non- standard Java library that is changing the way Html is written inside java to remove all <br />
> rough appearances that developers have long wished could be changed.To the younger developers html tags inside <br />
> > java can be confusing and intimidating. So the aim of JLevel is to strip off all tagging operations of html inside<br />
> > java and to automate most commonly repeated html codes thus making working with html faster and fun. <br />

> Instead of tagging just call a method with familar name such as doctyte(...), html(...),body(...) table(...),form(...) etc.
> and get a well-formed-document, made possible by JLevel 2.0.<br /><br /><br />
> <h2>Before now we have been writing like this in java:<br />
<blockquote>String html = "<.html><.body style=\"color:blue;\">Tedious!!<.br/><.br/><./body><./html>"<br>
</h2>//ignore the dots (.) used to ensure that tags displayed<br /><br /><br />
<blockquote><h2>Now with <b>JLevel 2.0</b> in java we just write:<br />
</blockquote>String html = html(body( "color:blue;",t("easy, fast and fun!!"),br2));<br>
</h2><br /><br /><br /><br />
Please read the documentation to see what benefits you can derive from JLevel 2.0 and enjoy a free open Library from Kogonuso<br>
We will appreciate your feedback as we plan towards JLevel 3.0 that we will bring to you in the future.<br /><br /><br /></blockquote>

General note to all JLevel 2.0 users: <br />
<h1>Structure</h1> <br />
As you already know Java language has lots of reserved keyword and unfortunately some of these <br />
reserved words are the same as some of the attribute names used by html such as class, for, char etc.<br />
As a result of this obvious conflicts it is not possible to retain the names of these attributes as<br />
was the case with elements names in JLevel. So the solution that we could come up with is to end the <br />
name of every attribute variable and method with a $ sign. This decision was taken to ensure that  <br />
consistency is preserved with all JLevel codes inside Java. It would be pointed out that this style  <br />
could not be adopted for both attributes and elements variables and methods given that there is the  <br />
need to have a way to close the sets in the elements. Hence there are three possible opening  <br />
and one closing variables for the elements. The opening variables can start with c, o, or s. c  <br />
stands for a closed open set example cp for closed set p element. o stands for open set that cannot  <br />
automatically accept in-line css style for example op for an open p element that need to be closed. <br />
s stands for an open set that accepts in-line css style automatically  without the developer needing to  <br />
write style="..." but simply "..." eg. "color:red;" is automatically interpreted and completed by JLevel <br />
Example of this variable can be written like this sp for the p element. Lastly the fourth and last type <br />
of variable for the elements is starts with e which stands for end of the element. Example ep for end  <br />
element p. here is a full example of how this can be done: <br /> <br /><br />
cp,...,ep <br />
op,...ct,ep <br />
sp,...ct,ep <br />
<blockquote><br />
That said there are special variable that do not need to be like those described above and they are only  <br />
two kids of these variable and you will need them a lot during formating.They are: <br />
br up to br20 <br />
nbsp up nbsp30 <br />
<br />
This was in line with JLevel 1.0.0 but has become unnecessary with JLevel 2.0 which has automated these <br />
operations. The only variables that you can use are these two br and nbsp as explained above, every other  <br />
operation can be done by calling an appropriate method inside its parent and so on and JLevel 2.0 puts in the  <br />
bells and whistles . Let's see how operations have significantly changed to reduce how much code you need <br />
to write as well as reduce error and increase your productivity:  <br /> <br />
<pre>Instead of this:<br/> <ul><li><br>
cp,...,ep<br>
op,...ct,ep<br>
sp,...ct,ep<br>
<br>
<br>
Unknown end tag for </li><br>
<br>
<br>
<br>
Unknown end tag for </ul><br>
<br>
</pre></blockquote>

<pre>Do this:<br/> <ul><li><br>
p(,...)<br>
<br>
<br>
Unknown end tag for </li><br>
<br>
<br>
<br>
Unknown end tag for </ul><br>
<br>
</pre>
<br />
You get the same result and with less effort, less error....<br />

The other beautiful this that worth mentioning is that JLevel 2.0 provide shortcuts that are very handy<br />
such as login(), insertImage(...),addTextArea(...),all the inputTypes eg. inputRadio(...) etc,inlay(...) <br />
or emElementName(...) and allows you to embed css style as if you where writing on an external stylesheet. <br />
That is you can now do this:<br /><pre><br/><br/><br>
embedStyle(<br>
embody("font-size:large;"),<br>
inlay(".underline","text-decoration:none;"),<br>
inlay("a:hover","color:#AB160C;text-decoration:underline;"),<br>
inlay("a:visited","color:#AB160C;text-decoration:underline;"),<br>
inlay("ul","list-style-type:circle;"),<br>
inlay("#b","color:sienna;"),<br>
emp("color:yellow;")<br>
...<br>
),<br>
...</pre><br />
<blockquote>inside java and JLevel will understand it and apply the appropriate operations so that you get this:<br />
<br /><pre><br/><br>
...<br>
body{<br>
font-size:large;<br>
}<br>
.underline{<br>
text-decoration:none;<br>
}<br>
a:hover{<br>
color:#AB160C;text-decoration:underline;<br>
}<br>
a:visited{<br>
color:#AB160C;text-decoration:underline;<br>
}<br>
ul{<br>
list-style-type:circle;<br>
}<br>
#b{<br>
color:sienna;<br>
}<br>
p{<br>
color:yellow;<br>
}<br>
...</pre><br />
<p>To get the best of JLevel 2.0 that I cannot possibly present to you in this general structure section<br />
please read documentation of every method and variable carefully, but most importantly, check to be certain that the<br />
parameters that you are providing are correct. There mostly two different ways that parameters are accepted<br />
as an Array and as a String. It is a must that you called attribute method(s) when the required parameters are <br>
deemed arrays.So do not confuse this with specifying a String, especially when the parameters are more that two <br>
check to see that what you are providing it correct otherwise you will encounter error which is not a fault of  <br />
JLevel as it only has to work with what you provided.<br />
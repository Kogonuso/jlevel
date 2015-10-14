# Kogonuso JLevel 2.0 #
Kogonuso JLevel - a simple java library that has changed the way html can be written inside Java(tm) both application and Servlet.
It is a library that is more than your ordinary Html parser applications. It has automated all tagging operations of Html inside java, this means that you are no longer required to learn how to format html String when developing application that requires html in java or even when using Servlet technology to develop your websites. Just import JLevel 2.0 and turn all the tag elements that you have ever known into simple method call.

The best is there for you to discover as JLevel not only stripped off tagging in Java html , it has formulated series of shortcuts by abstracting redundant html codes that we have often repeatedly written saving you valuable time.
You will no longer dread including html as a formatting tool in your java application when you use JLevel 2.0.

Another important feature that JLevel 2.0 has made possible inside java is the ability to use css as if you are developing for the web. Just use JLevel’s css container method and embed unlimited css inside the same one container making it easy to maintain. It is certainly true that embedded document with embedded codes like css loads faster than documents that have link to an external file due to effect of round trip that the server and the client must go through to process the request. With JLevel 2.0, if you accept it use its saveAsJsp(...) and saveAsHtml(...) methods you will be glad you did as the page that you will get quality formatting and arrangement as described above made possible by JLevel. Most importantly, it is not twice as fast to format a document in Java application and Servlet as before. Imagine writing p("...") and you get a full well-formed paragraph text. Or what about this p("color:cyan;","...") for a paragraph with inline css style.

Please read the documentation included in the downloadable file to understand the re-engineering that JLevel 2.0 has undergone that has ultimately made JLevel 1.0.0 obsolete and therefore no longer available for download.

Enjoy this good library from Kogonuso!


SourceForge.net: https://sourceforge.net/projects/jlevelbeta/files/latest/download?source=dlp

Google.com: https://jlevel.googlecode.com/files/JLevel%202.0%20Full.rar



=

@author Kogonuso

@version 2.0

@Since 27TH JANUARY 2013 BUT RELEASED TO THE PUBLIC ON 15TH MARCH, 2013

@Licence MIT-LICENCE
@contact info.jlevel@gmal.com
@webblog http://jlevel4java.blogspot.co.nz/

Brief description of JLevel 2.0

JLevel 2.0 is a non- standard Java library that is changing the way Html is written inside java to remove all

rough appearances that developers have long wished could be changed.To the younger developers html tags inside

> java can be confusing and intimidating. So the aim of JLevel is to strip off all tagging operations of html inside

> java and to automate most commonly repeated html codes thus making working with html faster and fun.

Instead of tagging just call a method with familar name such as doctyte(...), html(...),body(...) table(...),form(...) etc. and get a well-formed-document, made possible by JLevel 2.0.

Before now we have been writing like this in java:

String html = "<.html><.body style=\"color:blue;\">Tedious!!<.br/><.br/><./body><./html>"
//ignore the dots (.) used to ensure that tags displayed

> Now with JLevel 2.0 in java we just write:

String html = html(body( "color:blue;",t("easy, fast and fun!!"),br2));

Please read the documentation to see what benefits you can derive from JLevel 2.0 and enjoy a free open Library from Kogonuso
We will appreciate your feedback as we plan towards JLevel 3.0 that we will bring to you in the future.

General note to all JLevel 2.0 users:

Structure

As you already know Java language has lots of reserved keyword and unfortunately some of these

reserved words are the same as some of the attribute names used by html such as class, for, char etc.

As a result of this obvious conflicts it is not possible to retain the names of these attributes as

was the case with elements names in JLevel. So the solution that we could come up with is to end the

name of every attribute variable and method with a $ sign. This decision was taken to ensure that

consistency is preserved with all JLevel codes inside Java. It would be pointed out that this style

could not be adopted for both attributes and elements variables and methods given that there is the

need to have a way to close the sets in the elements. Hence there are three possible opening

and one closing variables for the elements. The opening variables can start with c, o, or s. c

stands for a closed open set example cp for closed set p element. o stands for open set that cannot

automatically accept in-line css style for example op for an open p element that need to be closed.

s stands for an open set that accepts in-line css style automatically without the developer needing to

write style="..." but simply "..." eg. "color:red;" is automatically interpreted and completed by JLevel

Example of this variable can be written like this sp for the p element. Lastly the fourth and last type

of variable for the elements is starts with e which stands for end of the element. Example ep for end

element p. here is a full example of how this can be done:

cp,...,ep

op,...ct,ep

sp,...ct,ep

That said there are special variable that do not need to be like those described above and they are only

two kids of these variable and you will need them a lot during formating.They are:

br up to br20

nbsp up nbsp30

This was in line with JLevel 1.0.0 but has become unnecessary with JLevel 2.0 which has automated these

operations. The only variables that you can use are these two br and nbsp as explained above, every other

operation can be done by calling an appropriate method inside its parent and so on and JLevel 2.0 puts in the

bells and whistles . Let's see how operations have significantly changed to reduce how much code you need

to write as well as reduce error and increase your productivity:

Instead of this:

> cp,...,ep
> op,...ct,ep
> sp,...ct,ep

Do this:

> p(,...)

You get the same result and with less effort, less error....

The other beautiful this that worth mentioning is that JLevel 2.0 provide shortcuts that are very handy

such as login(), insertImage(...),addTextArea(...),all the inputTypes eg. inputRadio(...) etc,inlay(...)

or emElementName(...) and allows you to embed css style as if you where writing on an external stylesheet.

That is you can now do this:



embedStyle(
embody("font-size:large;"),
inlay(".underline","text-decoration:none;"),
inlay("a:hover","color:#AB160C;text-decoration:underline;"),
inlay("a:visited","color:#AB160C;text-decoration:underline;"),
inlay("ul","list-style-type:circle;"),
inlay("#b","color:sienna;"),
emp("color:yellow;")
...
),
...

inside java and JLevel will understand it and apply the appropriate operations so that you get this:


...
body{
font-size:large;
}
.underline{
text-decoration:none;
}
a:hover{
color:#AB160C;text-decoration:underline;
}
a:visited{
color:#AB160C;text-decoration:underline;
}
ul{
list-style-type:circle;
}
#b{
color:sienna;
}
p{
color:yellow;
}
...

To get the best of JLevel 2.0 that I cannot possibly present to you in this general structure section

please read documentation of every method and variable carefully, but most importantly, check to be certain that the

parameters that you are providing are correct. There mostly two different ways that parameters are accepted

as an Array and as a String. It is a must that you called attribute method(s) when the required parameters are
deemed arrays.So do not confuse this with specifying a String, especially when the parameters are more that two
check to see that what you are providing it correct otherwise you will encounter error which is not a fault of

JLevel as it only has to work with what you provided.

Enjoy this good library from Kogonuso!
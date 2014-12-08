# Design notebook for week ending December 7, 2014

2.5 hrs Friday.
## Description

I got my parser working as well as getting a "compiler" that takes a filename
and interprets it to work.  I also started to investigate how to deal with
multiple staves played at once in a song, like with a piano.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**
There's not much at this point, I've mostly got everything working.  I'd like to
extend the language a bit more so I can play more piano songs, like I mentioned
above.  I'd also like to clean up my code and polish everything into a final
product.

**What questions do you have for your critique partners? How can they best help
you?**
I'm not planning on adding any big features at this point.  Any comments of what
to add if I worked on this project again in the future would be nice.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**
I worked 5 hours this week.

## Post-critique summary
My reviewer thinks everything is going well and liked the composability of my
DSL.

My reviewer wondered why I split my IR between code in the IR directory and code
in the midi directory.  He also suggested I handle splitting tokens and removing
whitespace in the parser as opposed to the semantics.  He suggests using option
types to simplify my code and making sure I use descriptive names - `var gen  =
new Sugar` used as an example.

## Post-critique reflection
I'll try to take some of the suggestions into account while I clean up my code
this week.  The suggestion for table building is definitely a good one - I
figured I could make it cleaner but never got around to it.

I might try to put more parser-appropriate code into the parser instead of the
semantics.  I'm not incredibly comfortable with parsers, so I might hold off on
that due to fear of messing up my parser.  I agree my code could use better
layout in places.

I'll look into options.  I'm not incredibly used to using them, but I can
investigate it and see if I can clean my code up somewhat.

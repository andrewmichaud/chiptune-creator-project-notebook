# Design notebook for week ending November 30, 2014

## Description

I didn't work much this week because of break.  I worked on the parser this
week.  I wanted to get it to a point where I could actually parse music like I
wanted to at the beginning of the project.  It's almost in a working state, I
think.  I've defined note primitives, so the parser understands how those work.
Unfortunately, because you still need to put quotes around everything for the
parser to work, notes don't parse correctly.  I could mess with the note builder
to make it work, but I'd prefer to make the quotes unnecessary first, because I
don't really want them to be there.  I don't really have any useful images.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I need to get the parser working.  I think it's in a good enough state where it
can define things in terms of things that have already been defined correctly.
However, you need notes defined before you can build on them, and right now the
note parser isn't working, like I said.  I need to get that working and make
sure the parser as a whole works.  Then, you should be able to define and play
music.  At that point, I'll basically have a rough version of what I set out to
make.

**What questions do you have for your critique partners? How can they best help
you?**
I would ask about whether the syntax is clear or not, but it's a bit rough and I
didn't get a chance to smooth it out enough for proper testing.  You could try
playing around with it and seeing if you can give any useful feedback.  If not,
that's okay too.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I spent a bit over two hours this week.

## Post-critique summary

My critique partner liked the project.  The implementation seems good.  The
major concern was how easy input would be  - it currently seems repetitive.

## Post-critique reflection
I'm glad my partner liked my progress.  It might not be clear from my code (my
code isn't very clear), but the implementation should make things less
repetitive.  You can define as many building blocks as you want, so you should
never have to type the same thing out multiple times.  I currently provide a
wide range of note tones as building blocks, and I would like to put major
chords and other useful musical elements in as well.  That's coming along nicely
and I anticipate making music creation not repetitive at all.

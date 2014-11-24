# Design notebook for week ending November 23, 2014

## Description

I wasn't able to work a lot this week, which is partly due to work from other
classes and partly due to poor scheduling on my part.  I was able to work for
two hours.  I finally made using Array unnecessary in the Scala MIDI functions
in my code, which makes it a lot less obnoxious to create music.  I also worked
on the parser so I can actually create code files for my DSL.  I had to recreate
all of the work I did in class on Wednesday, because I lost all data on my
laptop at the end of the week and only recently got my laptop working again.  I
was able to knock out a very basic parser pretty quickly, and I'm hoping I can
get it running well very quickly, so I can actually start testing out how well
it works.

I realize my work for the week and this description are late.  I was under time
pressure from Algs and handled time badly this week (which is why I was under
time pressure from Algs).  I figured it was more worthwhile to spend some time
working on the project and turn this in later than turn in a notebook entry with
nothing in it.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I need to get the parser working.  The backend is running fine, but there is
currently no way to create code in a file and have my DSL parse it.  I would
like to get this working as quickly as possible.  I would also like to
investigate the visual representation of my DSL.  It would be nice for a user to
have, and I haven't investigated it at all yet.  I don't know how hard it will
be to do, either.

**What questions do you have for your critique partners? How can they best help
you?**

It's not a perfect emulation of the final product, but I would like to see what
people think of the Scala functions for creating songs.  Defining variables as
Notes or Chords or Sections is very similar to what I hope to do with the code
file, so I would like to see what my reviewers think, either when they review me
or when we do user testing in class.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

Unfortunately, I only worked for 2.5 hours this week on the project.  I hope to
not have to work alongside exam deadlines for the next couple of weeks.

## Post-critique summary
My reviewer was happy with my semantic engine, and said I just need to figure
out my parser and IR.  They don't have MIDI suggestions, but did suggest adding
some way to loop a sequence, with padding and duration specified.  They also
suggested some more premade sequences besides basic notes, to make it easier to
compose music.

## Post-critique reflection
I'm glad my reviewer agrees with my assessment of my progress.

I think the building block idea is a good one, and will be pretty simple.  I
think I'll prioritize getting parsing working, but it should be pretty quick to
get something like chords in.  I'd just have to dump some premade chords in a
file somewhere or add some default labels that will do the same thing.

I'm intrigued by the looping idea.  It could be nice to repeat a sequence.  I
could see this being useful when composing original music.  I'll keep this in
mind to look into later, depending on how fast I progress with my basic plan for
the DSL.

# Design notebook for week ending November 9, 2014

## Description

This week, I selected my language and started working on the backend to produce
the actual sounds.  I decided to go with Scala as my host language, because Java
has a seemingly good MIDI creation library.  I was hoping to use Go (because I
really like Go), but Scala should work just as well.

I was able to use some Linux utilities to create mp3 files from MIDI files.  So,
I can take the generated MIDI files, convert them, and see if they sound right.
I'd like to find some way to do this inside Scala/Java, but this'll work for
now.

I'm able to play some very simple notes in MIDI files.  I put some basic
functions to wrap the MIDI library functions.  I have a function to play an
arbitrary note, and a function to wrap up some of the boilerplate stuff that
(apparently) needs to be done to create MIDI files.  Next week, I'm hoping to
have some more wrappers to handle the rest of the MIDI library stuff, and to
make it easier to make full songs.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**
Right now, I need to figure out why all the notes I try to play play all at the
same time.  I think I just need to understand the MIDI library better, and I'll
figure out what's going on.

I also want to figure out how many more wrapping functions I'd like to make
around the MIDI library.  I can play individual notes, but it might be nice to
play several notes at once, or play rests, or some other things.  I'd also like
to put functions in to give more control over the speed of the song, and some
other things.  Right now I'm sticking with the values set by the example code I
started with.

**What questions do you have for your critique partners? How can they best help
you?**
What music creation functions would you see as useful for this project?  I'm not
really sure how much I'll want to extend my library wrapper/internal DSL before
I start working on the syntax for the actual language.  It'll be nice to get
some feedback and suggestions for what I might add.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**
I spent 1.25 hours in class on Wednesday, and two more hours on Sunday, for a
total of 3.25 hours.  I felt like I got a good start, but I'd like to get a
bit more in next week if I could.

## Post-critique summary
The concerns raised, as I understood it, were:
- wondering how exactly this would make music generation/ 8-bit music generation
  easier/better.
- possible concerns about the scope of the project.
- asked for a document summarizing the scope of the project

## Post-critique reflection
I can't really say whether this will make music generation easier, because I
don't have a lot of experience with music creation software.  I guess I'm mostly
hoping to make music generation easier for me personally.  I would also hope
that the syntax I choose for my language is fairly straightforward and easy to
use, and the visualizer makes it easy to see what your music is going to come
out like.

I feel confident about the scope of the project.  I already can produce notes.
Once I figure out how to make them not play all at the same time, I should be
able to produce songs in Scala pretty easily.  I don't know how hard the parsing
will be, but I can't imagine it will be incredibly difficult to get something
working by the end of the project.

I'll try to put a document in with the scope for my reviewers.

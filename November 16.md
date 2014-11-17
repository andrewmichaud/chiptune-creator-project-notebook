# Design notebook for week ending November 16, 2014

## Description
I worked in class for an hour on Wednesday, experimenting with a simpler way of
making MIDI work in Java.  I tried to transcribe some sheet music and make it
work.  Later in the week, I got chords and notes working nicely.  Today, I added
sections, which can contain other sections and notes and chords.  This made it a
lot nicer to define variables for arbitrarily-sized parts of the song, and made
transcribing a lot nicer.  I'd like to leverage these elements when making my
parser and external DSL, because they represent a lot of what I was hoping to do
in this assignment as far as abstraction goes.

I was able to transcribe an entire song, and it sounds great, so I'm pretty
happy.  I have an early state of that song in the repo as a picture
(composability.png), and you can check the code in examples.scala for the full
code for the song I transcribed.

The one design change I made was using strings instead of case classes for tones
and note times.  I wanted to use case classes because I wanted to have something
like enums or constants, (like Note(D2, Quarter)).  It turned out that was
really hard, so instead I made the constructors take strings and convert them
using functions with cases that replaced the case classes.  This is a bit
nicer, and as a side benefit means I don't have a few dozen compiled .class
files lying around.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**
I'd like to get rid of Array in my code.  Both Chords and Sections take arrays
of things (because Chords are made of a bunch of notes, and Sections of a bunch
of something).  I'd like to do something similar to a varargs function in C, so
the array doesn't have to be manually written.  I should also probably start on
the parser and syntax for my external DSL.  I think the backend's mostly in
place, and I can add more functions to the backend if I need to later.

**What questions do you have for your critique partners? How can they best help
you?**
How easy does this syntax look?  Could you transcribe some sheet music in this
way?  Could you write a new song this way?  What would you want changed?  What
seems obnoxious or annoying?

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**
1 hour in class, 5 hours outside class.

## Post-critique summary
Summary of pressing issues:
 - Figure out exporting to MIDI, possibly exporting directly to MP3.
 - Figure out input and IR, and target audience.
 - Go would have been really cool

Summary of questions:
 - Would love to see simplified input.
 - Maybe wrap notes up in sequences?

Final thoughts:
 - Enjoyed summary
 - Different instruments would be awesome.

## Post-critique reflection
Right now, I'm letting Java's MIDI synthesizers play the sounds directly.  I'd
like to export to MIDI at some point, but I figure that's not a top priority.
Exporting to MP3 seems very difficult, due to how MIDI works and what the
library has, so I'll put that aside for now too.

I'm planning to investigate the input next, and the IR as well.

I think my target audience is people with a weak background in either music or
computer science.  I plan to make the syntax as simple as I can - basically just
describing notes or sequences of notes - so it isn't hard to use even with
little experience.  It will require knowing what C3, C4, C2, etc. are or at
least being able to figure it out through experimentation, though.

I plan on making the input very simple.  You will have to have all the notes
there, but I want to (and should be able to, with the section functionality I
added) let you say things like "PARTB = C3 (PARTBA) D4 E4".  This will make it
easy to describe repeated parts of a song and not have to type them multiple
times.  They should stack, too, so you can say:
FOO = A3 B1
BAR = BAZ FOO C2
BARAGE = BAR BAR BAR C3
SONG = BARAGE BARAGE BARAGE FOO
I can do this within Scala, I'll just need to do it in the parser.

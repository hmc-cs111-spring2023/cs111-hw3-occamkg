# Free project 1

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

There are many interfaces and softwares for designing presentations and many
people use these softwares to create products to clearly and visually
communicate their ideas.
However, these presentations have a basic structure that limits the ability to
effectively communicate ideas.
A language that expands the abilities of presentation creators to allow them to
create more dynamic elements could make presentations more engaging and clear.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Currently, presentations are almost always given as a set of slides arranged in
a temporally linear way.
Transitions between slides are usually less smooth than an animation and more
similar to turning a page where all the information from one slide is lost on
the next unless the user deliberately copies and pastes it, making
presentations lose a sense of fluidity.
Additionally, the most interactive parts of slide presentations are usually
videos and even those can often not display well in a presentation.
Thus, there is a need to create a way to design presentations that are more
fluid and interactive.
Ideally, this DSL would allow people to easily create presentations that aren't
constrained by the traditional "slide" format and offer more options for
interactivity.

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL could allow users to more freely define the way their desired components
work than the traditional presentation UI can.
It is also more focused than a broader language built for display like HTML/CSS.
This narrower focus can help the user better understand the limits of the
presentation space and can help them explore these limits.
Thus, it is more manageable to novices than a full blown language, but also
offers more options than a presentation UI.

### Why you?

_What excites you about this idea? How did you come up with it?_

Presentations always seem like a vital part of communication and I just feel like PowerPoint, Google Slides, Beamer, etc. have a very bland structure
compared to what is possible.
Looking at the capabilities of HTML/CSS/JavaScript in terms of visually
displaying information and how they can be interactive inspired me to expand my
opinions about what a presentation could be.

### Domain

_Describe the project's domain in five words._

Interactive and fluid presentation design

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

For this language, there could be different types of components that the user
can add to their presentation.
These components could then be controlled by key frames that would be triggered
by a clicker for the output presentation.
In the language, the user could decide any of a number of behaviors that they
could apply to an object at each keyframe.
These could go beyond the traditional visible/not visible to include
translations, scalings, color changes, and other property changes.
To visualize the programs, a visual representation of the presentation could be
displayed to the user adjacent to their code with the ability to move through
the key frames.

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program is actually run, it could output a presentation file (maybe
HTML) that could then be saved and used for a presentation.
This could possibly have issues with conversion, but most of it should be seen
in the program beforehand by the visualizer.
If there are issues with components and how they function, the errors could be
output to the user when they are detected as the user is programming them.

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to place components in organized locations (centered,
justified, on a grid, etc.) vertically and horizontally.
It should also be easy to place components in more free spots possibly by using
cursor input, and in relative spots (i.e. aligning with other components).

It should be easy to group objects together so they can be modified together by
the user and also so they can have grouped behaviors for the output
presentation.

It should be easy to change behavior of objects over time (visibility, scaling,
position, color?, etc.).

It should be easy to include interactive components (like buttons), but how they
interact with other components should be handled by another broader language.

It should be difficult to use web sources (like databases) from within the
program since it seems like a generally bad practice to have data that is not
concrete (i.e. different from day to day) used for presentations, but there
could be cases in which that is useful, so maybe it shouldn't be impossible.

It should be impossible to create non-visual/auditory outputs since that is
beyond the goal of presentations.

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Beamer is an internal DSL in TeX that offers a range of capabilities for making
presentations, but it is severely limited by themes and it is difficult to
individually modify components beyond basic properties.
UIs like PowerPoint offer more options for manipulating individual components,
but they are still constrained to the strict slide deck format.
I was not able to find any presentation options that offered non-slide based
designs and interactive capabilities possibly because the slide ideas have
worked so far and are a standard that many people don't think needs changing.

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I would say most of this project would be trying to make it intuitive to make
presentations with different capabilities, so a lot of the time would be spent
on designing the different aspect of the **language**.
I would guess it would be about 70% **language** and 30% **systems**.

### Scope

_How big an idea is this? How ambitious is this project?_

One thing I like about this idea is that it has a lot of different features
that can be added to make it more of an ambitious project, but it can also be
more simple if I want it to be.
To have it compete with currently used software would be ambitious, but whatever
I could produce in this class, I could continually build off of it after.

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

Benefits:
* It's scalable: I can start with a few components and capabilities of
positioning, etc. and immediately test the DSL
* It's something I strongly think could be improved with not too much effort
* The languages I'm probably most familiar with are web design languages which
could come in handy for designing this DSL

Drawbacks:
* I'm not sure how much broader need there is for this DSL
* People that create presentations come from a broad range of backgrounds, so it
would be difficult to account for all the features people could want
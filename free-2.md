# Free project 2

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

Modern composers often want to work with current technologies to make unique
ways of controlling sound (instruments).
Oftentimes, however, they have limited programming experience, so the barrier
of entry causes their interesting ideas to remain unrealized.
A language that has a more limited vocabulary geared toward instrument creation
could be the perfect tool for these composers.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Currently, for a composer to create an electronic instrument with their desired
inputs and resulting outputs, they can use a program like Arduino's C++-like
language to handle inputs and convert them to data and then a program like
Cycling '74's Max language to convert the data to the desired audio.
This requires learning two languages and circuitry which can be a lot for a
composer to try since it is somewhat out of their domain.
Ideally, after designing an applicable DSL, composers could clearly define what
inputs they want and how those directly correspond to audio outputs.
From there, it could show how the user could setup their circuit and give them
the code they need to upload to the board making the overall process more
contained and less confusing.

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

I think a DSL is appropriate because it would be more constrained to the
composers' domain making it more intuitive to make the desired instruments.
It also doesn't need the full functionality of a general purpose language
because it only has one type of output (audio).
A DSL would effectively address the composers' needs because it would make it
more intuitive and simple to make the instruments they desire.

### Why you?

_What excites you about this idea? How did you come up with it?_

I've worked a lot with audio processing in interesting ways and have even made
a sort of "instrument" myself with ultrasonic sensors as inputs, so I would
love to see where this project could go.
In a composition class in high school, I remember my teacher saying that one of
his composer friends had made a glove that could be used as an instrument and
he had a lot of interesting ideas of his own that he wished he could make.
He had worked with Max before, but thought that learning circuitry and
programming the circuits would be too complex for him to make the things he
wanted.
That whole interaction is what led me to reach this solution of using a DSL.

### Domain

_Describe the project's domain in five words._

Designing unconventional electronic instruments easily

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

The programmer could define what kind of inputs they want by either choosing
from a list of predefined sensors or by expressing what the nature of the
inputs are (e.g. data type, refresh rate, noise, etc.).
Next they could give functions for how to process this data into what they want.
Finally, they could define what the processing output relates to auditorily
(e.g. gain, audio file, effect, pitch, etc.).

This would be intuitive because from what I've observed of the composers I know,
they typically thing of instruments in terms of how different inputs affect the
auditory outputs of the instrument.

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs, it would upload appropriate code to a connected
microcontroller so the program could be used on the device.
It could also have a built-in simulation that would allow user input through
value sliders or input fields without the need for the entire circuit and
hardware components.
Runtime errors could include data mismatch, infinite loops, and other common
program errors that could be reported similar to other programming languages.
One key error that could cause problems would be getting the outputs "stuck on"
which could make for an unpleasant experience, so it would be important to also
have an easy way to stop the program immediately.

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to make a way for any mechanical input to result in an
auditory output.
Everything else should be impossible or at least difficult since the domain of
this language is pretty much completely constrained to this structure.

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Most musical instrument design software I can find is completely digital
relying on only computer inputs or completely physical without actually using
code for the production of the sound at all.
The closest thing I know of is Max which has a large range of auditory effects
it can manipulate, but it requires the inputs to somehow be given to the
computer first, making it more challenging to make your own unique input methods.
I do, however, like Max's programming style which is very visual and makes it
more intuitive for those less familiar with code.

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think there would be a large need to make this intuitive for composers, so it
would require thoughtful **language** decisions, but it would also be a bit
challenging to interface it with existing programs, so the **systems**
requirement would be high as well.
With that in mind, I'd guess it would be around 50% **language** and 50%
**systems** possibly leaning more toward the **systems** side.

### Scope

_How big an idea is this? How ambitious is this project?_

This does seem like a rather large project since it deals with defining inputs
and outputs that can have a large range of structures.
However, common basic inputs and outputs would not be too challenging to add and
as long as the language allows for the user to define other IO structures, it
could still be useful.
The simulation part may also be difficult to create, but also may not be
necessary although helpful.

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

Benefits:
* It has a lot of domain-specific features that make it well suited for a DSL
* I am familiar with the domain as well as how to make and program circuits, so
it fits my expertise well
* It could strengthen my skills in creating something highly adaptable for the user

Drawbacks:
* It may be a bit large of a problem to tackle since it deals with designing
things that no one has thought of before
* It may be difficult to find domain experts to get feedback from at HMC
* Relatively, there aren't many avant-garde composers that want to design their own instruments, so this may not be too useful

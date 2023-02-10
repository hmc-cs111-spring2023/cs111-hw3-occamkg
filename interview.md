# Interview project

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

Printed circuit boards (PCBs) offer a way for engineers to programmatically
control physical devices in all sorts of objects from things as simple as
flashlights to things as complex as fully autonomous robots.
However, designing these boards can be a bit challenging and unintuitive with a
steep learning curve.
Thus, a language that could more intuitively show how the programs work with
their hardware in real time could ease the development process for programmers.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

The primary goal of this project would be to allow a PCB programmer to simulate
how their program interacts with their hardware all within the programming
interface.
Currently, PCB programmers need to prototype the circuit they are designing and
plug in a programmable prototyping board and upload the code they write in order
to test it.
Some drawbacks of this method are that it takes a while to test each time,
sometimes programmers don't want to carry around an entire prototype when
working with their code, and sometimes the users don't even have all the
necessary components to create the prototype when they're programming.
This DSL would allow the programmer to get more immediate feedback on what they
are writing and ease the debugging experience significantly.

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL is appropriate because firstly, the users typically are already
programmers if they are attempting to program a PCB, and secondly, it could
build from the already existing functionality of PCB programming languages
without the need for an entirely new general language.
It addresses the need by offering ways for the user to control inputs and
observe outputs for real-time simulated hardware.

### Why you?

_What excites you about this idea? How did you come up with it?_

I interviewed an engineering friend who talked about their troubles with
learning how to design PCBs and they mentioned that it was difficult to get
started since there were so many different parts that each require decisions
before you can even start prototyping.
They also mentioned that some of the things they had liked in programs they
tried out include the debugging capabilities that output register values in real
time as well as some more visual debuggers.

This interests me because I have also worked with PCB design and find all the
separate parts difficult to navigate and oftentimes inconvenient.
Funnily enough, I had actually come up with a similar idea as a potential other
project before I did the interview.

### Domain

_Describe the project's domain in five words._

Interactively linking PCBs and code

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

In addition to the code they write for their microchip, the user could define
interactions between pin outputs and inputs or simply put probes on the pins.
Additionally, it could visually display pin readouts which could further be
displayed as hardware component outputs (i.e. light brightness, servo rotation,
etc.) with behavior defined by the user.
For inputs, there could be a way to input values in the visualization and
observe the response.

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

Ideally, when the program runs, the user would see a visual representation of
their device and interact with different inputs directly as the program runs.
If the user incorrectly defines a device (beyond reasonable constraints), the
device and the corresponding pin(s) it is connected to could be highlighted in
the visualization and it could display the error message when it is clicked.

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to define devices that can be connected to pins and what their
simulated representation would be.
It should also be easy to define a general circuit and put virtual "probes"
anywhere on the circuit.
Finally, it should be easy to define inputs and allow real-time changes of the
inputs.

It should be impossible to create looping structures and recursive behaviors
since those are not really properties of the input/output hardware components
and are more from the PCB program which is separate.

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are Arduino simulation programs, but they are typically constrained to
only showing circuits with pre-defined components.
I believe it would be immensely helpful if it could be more open-ended allowing
the user to define only the parts of the components that are necessary for the
simulation which would require a lot less code maintenance, but also allow for
predefined modules that could be shared between users (like libraries).

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think a lot of the time would be spent on the **systems** aspect because it would
require designing a way to simulate how PCB code interacts with the pins.
Thus, I'd guess 80% **system**, 20% **language**.

### Scope

_How big an idea is this? How ambitious is this project?_

This is a fairly ambitious project since it requires lots of knowledge of many
different hardware components, but at the root of the problem, there are a
finite amount of input and output pin types, so I guess those could just be what
the language

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

Benefits:
* The product could help save time for many PCB programmers
* I would be interested and invested in creating this DSL

Drawbacks:
* It would be challenging to get it to a level where it is helpful and not too
limiting in comparison to the traditional PCB programming techniques.

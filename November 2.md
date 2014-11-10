# Design notebook for week ending November 2, 2014

## Description

This week, we only filled out the language design for the assignment, as well as
discussing our plans for future work. We got a late start to the assignment and
were a little unclear on the time expectations, but we plan to work a significant
portion of tomorrow. Our major work so far is narrowing down the idea of "IQ" in
our project, and discussing with each other what we want from our game and how
that informs our language design. We also looked at a possible game engine for
our project.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Right now, the biggest question that I have is how to design a language
which is easily understood and easy to use in order to implement AI, but also
provides enough flexibility and creativity for the user that they can make
their own unique and creative programs. Much of this lies not just in the
language design, but in the design of the different game units in order to give
them meaningful interactions. While it is hard to predict, it is still important
to have a good understanding of how the units will behave and how games might
play out in order to make a well-informed language design from the beginning.

**What questions do you have for your critique partners? How can they best help
you?**

If you were new to a RTS-style game, what would you think as the fundamental choices
or actions of a character that you would expect to see? What do you think of as
"basic" to this kind of a game? Is there anything you would be very surprised to see?
What kinds of interactions would annoy you?

**How much time did you spend on the project this week? If you're working in a

team, how did you share the labor?**
As stated above, we were a little fuzzy about the time requirements, and so as
of now I only worked betwwen 2 and 2.5 hours on the project this week. However,
we plan to work a significant amount of time on Monday in order to off-set this.

## Post-critique summary
_Note_: I forgot about this until I was writing my notebook entry for November 9, but figured this was still worth
writing. The big take-aways from the critique were that the language design has to be very careful, and that we need
to make sure we don't spend too much time on the game engine itself.
## Post-critique reflection
The really big thing I had to think about after the critique was the balance of how much we would let the user say
while designing their AI. Ari had a good point that we don't want our assumptions about what are good conditionals
to use and smart actions to take to overly restrict a user's creativity. After all, the point of this game
is to reward creativity as much as possible. At the same time, there are dual reasons for wanting to limit the
syntax. One is that we simply can't make the language too big, or we won't be able to write code for it all.
Since we have to implement the AI to perform all the actions the user writes, it rapidly becomes infeasible to give
them too many choices. Second, limitation breeds creativity. This is where balance becomes very important. With too
few choices, nobody is able to use their own cleverness and originality because the syntax doesn't give them the
appropriate tools. With too many choices, you don't have to be clever or original in order to make something good.

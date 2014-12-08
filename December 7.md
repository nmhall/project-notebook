# Design notebook for week ending December 7, 2014

## Description

This week was primarily focused on getting semantics for IQ restrictions. This was
surprisingly hard. I put a lot of thought into the balance between keeping a
grammar that stayed modular, and making rules that lent themselves nicely to
the semantic processing that we wanted. In the end, I'm not super happy with where
we ended up, and think there is still too much redundancy in the grammar. However,
this is at least balanced out by the fact that the generated AST contains more
generality, since the labels assigned to the rules during parsing do not have to
match the actual rules within the grammar. Probably more important is that it is
now very easy to semantically determine whether the IQ limits have been violated,
since we distinguish between rules given to each of the three classes. Like I said,
I was very torn about this because on one hand, these rules contain the same meaning
and should therefore be the same. On the other, they serve different purposes, and
creating different rules lends some differentiation of the three AI classes into the
grammar, for better or for worse. In the end, I think I probably made the right
decisions with respect to making a working semantics and an easily-interpreted AST,
but the purist in me wishes there had been a more elegant way to do things. Also,
this took way more time than I anticipated, for both stupid get-Python-to-work
reasons and for the amount of time it took me to figure out how to make semantics
nice without butchering the grammar even more than I did. The AST is now in pretty
good shape, and even though it looks like we won't actually go through the process
of writing JSON to a separate file and trying to interpret it in the actual Spring
AI, I think that I did take care to make sure the AST is of a form that could be
interpreted if we did follow through on that avenue. Labelling rules to produce
dictionary-like structures seems to add some regularity to what is otherwise a pretty
confusing Grako-produced thing.

I also spent some time thinking about AI implementatin for a final demo. While
targeting seems to be an extremely simple process of just picking the enemy out of
a list of enemies to shoot, movement is made more complicated by the fact that we
have two categories (formation and movement) that effect where a unit wants to go.
Movement in Spring seems to be a matter of picking a point and assigning a move
order for that point, and the engine determines pathing and such. It seems like the
answer for movement is to have a function which takes in the given orders (group
up, move toward enemies, etc.) and picks a point which represents the best compromise
between all of those things. If we pick a point, then having the unit start to move
toward it (recognizing that we can change that on a frequent basis) is easy. The real
issue is picking a point which balances the differing things we want the unit to do,
but I think we can do at least a good approximation of that for our demo.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I think the most pressing concern now is creating a couple good sample AIs that a
person might actually write in our language, and implementing them in Spring so that
we can show people how our language works, and then what that looks like in an actual
AI within the game. For this, the only significant barrier that seems to be in place
right now is that of point selection for movement around the map, but I'm confident
that we can do at least a very good approximation of a solution to that.

**What questions do you have for your critique partners? How can they best help
you?**

If you were going to write a simple AI that illustrated the different things you
can have your units do, what might you write? There aren't stellar descriptions
of what you can say and how to say it right now, but hopefully you know the basics
at least and can give us an idea of what might be the most illustrative examples for
a demo. The only major change to the syntax is that default, per user feedback, is
no longer required when adding rules for a category.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I probably spent 11+ hours on the project this week, with a large portion of that
being planning and implementing the semantics for IQ enforcement. I focused on the
grammar while Alex did some awesome work with the AI file, and I then also did some
planning for movement for AIs and the demo.

## Post-critique summary

## Post-critique reflection

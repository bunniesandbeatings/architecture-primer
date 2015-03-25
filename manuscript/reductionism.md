Reductionism
------------

Reductions are not metaphors
============================

Metaphors tend to fail under pressure. Given a metaphor for object oriented design, such as "A class is like a
blueprint, so you might have a blueprint for a car" you can be forgiven for spending much of your career modelling real
world objects.

Unlike the metaphor, the reduction is a proven and sound set of rules that are know to work well. The reduction is not
always perfect, but dogmatic application of the reduction is at the very least, dependable.

This book presents a reduction that when used dogmatically, also prepares you to make informed, pragmatic decisions
about its rules.

The "Real world object as a model" metaphor does not edify programmers in the art of producing scalable systems which
other developers can reason about. It gives you a way of understanding noun-verb interactions in an object, and then
does you a disservice when you try to apply it to scalable architectures.

The reduction in this book does no such disservice. If you used it dogmattically alongside 'Clean Code' for the rest of your life, you would
always build maintainable code. When you are comfortable with it, you can start to use your own judgement as to when to
apply it or modify it.

Precursors
==========

Two great software reductions that are already widely known are 'Clean Code' and 'SOLID'.

The 'Clean Code' reduction talks about how you write code at the object, method and variable level. It describes self documenting code which reduces cognitive overhead for the next consumer of your work. It helps you reason about much of the minutiae where you will spend most of your time focused on actual lines of code.

-- example
-- resource not for cc-bob

'SOLID' is a reduction which simplifies reasoning about inheritance and object design. When followed, it removes
surprises for the next programmer.

-- example
-- resource note for poodr-sandy

Encapsulation
=============

An encapsulation lets you wrap a cognitive load into a simpler element.

Reasoning about change
======================

Encapsulating state and a reason for it to change is at the center of the modular reduction. Causes for state to change
introduce system complexity. --- details

The modular reduction states that:

Given a system has dependencies.
And that a change to dependency means, at the least, that dependants need to be checked for side effects (from the change)
Then developers and teams need a clear mechanism for identifying affected artifacts.

Circular or tangled dependencies are hard to reason about
=========================================================

-- graph

Trees are easy to reason about
==============================


Trees are not sufficient to model dependency structures
=======================================================

Directed acyclic graphs are sufficient
======================================

-- Dependency inversion makes it possible to avoid cycles

DAG nodes are all trees
=======================

All edges entering a node are a tree - cause for change
All edges leaving a node are a tree - affected nodes


Nesting DAGs lets you encapsulate subsystems
============================================

Subsystems are components are modules. Hence, modular architechture.

Encapsulating a subsystem hides its complexity and surfaces a simpler cognitive load for the consumer.


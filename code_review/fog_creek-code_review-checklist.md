
# Guidelines for both the reviewer and the submitter:

# General


- [ ] Does the code work? Does it perform its intended function, the logic is
correct etc.
- [ ] Is all the code easily understood?
- [ ] Does it conform to your agreed coding conventions? These will usually
cover location of braces, variable and function names, line length,
indentations, formatting, and comments.
- [ ] Is there any redundant or duplicate code?
- [ ] Is the code as modular as possible?
- [ ] Can any global variables be replaced?
- [ ] Is there any commented out code?
- [ ] Do loops have a set length and correct termination conditions?
- [ ] Can any of the code be replaced with library functions?
- [ ] Can any logging or debugging code be removed?

# Security

- [ ] Are all data inputs checked (for the correct type, length, format,
  and range) and encoded?
- [ ] Where third-party utilities are used, are returning errors being
  caught?
- [ ]  Are output values checked and encoded?
- [ ]  Are invalid parameter values handled?

# Documentation

- [ ] Do comments exist and describe the intent of the code?
- [ ] Are all functions commented?
- [ ] Is any unusual behavior or edge-case handling described?
- [ ] Is the use and function of third-party libraries documented?
- [ ] Are data structures and units of measurement explained?
- [ ] Is there any incomplete code? If so, should it be removed or flagged
  with a suitable marker like ‘TODO’?

# Testing

- [ ] Is the code testable? i.e. don’t add too many or hide
  dependencies, unable to initialize objects, test frameworks can use
  methods etc.
- [ ] Do tests exist and are they comprehensive? i.e. has at least your
  agreed on code coverage.
- [ ] Do unit tests actually test that the code is performing the intended
  functionality?
- [ ] Are arrays checked for ‘out-of-bound’ errors?
- [ ] Could any test code be replaced with the use of an existing API?



# Guidelines for the Reviewer:


- [ ] Is this a good solution regardless of my own preferences to solve
    the problem (there is more than one way to do it)
- [ ] If I am not happy with a particular piece of code,
    can I match it with one the guidelines listed at the top of this document ?
- [ ] Have I provided an example re-implementation code for the piece
    I don't particularly agree ?
- [ ] Have I only provided constructive feedback?
- [ ] Are my concerns enough to 'block' this code to be merged?
- [ ] Have I thanked the submitter for their efforts ?


# Attribution

This template came verbatim from the [Fog Creek blog post with a Code Review
Checklist](http://blog.fogcreek.com/increase-defect-detection-with-our-code-review-checklist-example/)
and was the inspiration for the software_dev_templates_and_checklists
effort.  Please, read the blog post to understand the motivation for
this checklist as well as understanding how to use it.

# Additional reading:

http://kevinlondon.com/2015/05/05/code-review-best-practices.html

    On mindset

    As developers, we are responsible for making both working and maintainable
    code. It can be easy to defer the second part because of pressure to
    deliver working code. Refactoring does not change functionality by
    design, so don’t let suggested changes discourage you. Improving
    the maintainability of the code can be just as important as fixing
    the line of code that caused the bug.

    In addition, please keep an open mind during code reviews.
    This is something I think everyone struggles with.
    I can get defensive in code reviews too, because it can feel personal when
    someone says code you wrote could be better.

    If the reviewer makes a suggestion, and I don’t have a clear answer as to
    why the suggestion should not be implemented, I’ll usually make the change.
    If the reviewer is asking a question about a line of code, it may mean that
    it would confuse others in the future.
    In addition, making the changes can help reveal
    larger architectural issues or bugs.


https://news.ycombinator.com/item?id=9517892

    If the reviewer makes a suggestion,
    and I don’t have a clear answer as to why the suggestion should not be
    implemented, I’ll usually make the change

    This I feel is bad. Code reviews are usually between peers so you
    shouldn't be afraid to seek out clarification where possible.
    You shouldn't be making edits to code that goes in production
    without clearly understanding why.

    The other thing that wasn't mentioned, that I think is important,
    is to not act as a blocker for code reviews unless its absolutely necessary.
    Lots of engineers take on the attitude that they're going to "gate" code they
    don't agree with by with holding their +1 and bogging down the review with
    questions and all sorts of runarounds till its what they want.
    this is a bad attitude to have, even when you're dealing
    with Junior engineers.

    I'm generally going to +1 something unless I fundamentally disagree with it
    or think its going to break things in production. What I do, though, is
    leave lots of comments with questions/suggestions and mention it in the +1
    with (see comments).

    This builds trust on teams, and stops things getting personal, especially
    with people who aren't very good at dealing with criticism, even
    in something as banal as a CR. On a team that works well together,
    teammates will see those comments, think about them and make
    thoughtful responses, especially once they understand that you're not
    trying to get in their way. Giving the +1 gives them the freedom to
    consider your suggestions without being irritated that their PR is
    being blocked. They feel like they're in control not you.

    In rare exceptions, someone will brush off my questions and merge ... which
    means that next time, I get to be tougher on the review and specifically ask
    for responses before the code can be merged, because they've degraded the
    implicit team trust. Usually repeat offenders are assholes, and assholes
    generally don't last on healthy teams.

# How well are we doing ?

https://biterg.io/dashboards/e3e205eb-cfb7-4086-b7df-adbb2d93f42d/ng/#/

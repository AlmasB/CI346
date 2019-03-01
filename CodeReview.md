## Effective review practices

* Any person's (regardless of status and experience) code must be reviewed.
Any person should also have the chance to review.
* Automate as much as possible: e.g. code must pass all tests and static checks before review.
* Review time 60-90 minutes.
* Up to 400 lines of code.
* Use checklists to help authors know what is being reviewed.

## What to review (Examples)

* Consistency / code guidelines. Ideally through automation.
* Presence of tests for new code. Ideally through automation.
* Purpose of change / new code (particularly concerning new API).
* Is the code maintainable, readable?
* Does the code follow appropriate design, whether idiomatically, or architecture-wise?

## How to provide feedback

* Keep your ego out of reviews: do not think "I would've done this in a better way".
Instead suggest (don't enforce either) changes, justifying why these changes are more suitable.
* Critique the code, not the author.
* Ensure you have the right tone, textual feedback is likely to be more direct and blunt
compared to verbal.
* Leave positive comments, sometimes it's OK to let negligible things pass.
* Avoid judgements, such as: "this will fail", "this is wrong".
Instead ask questions: "I think this may fail because X. Can you confirm?".
* Indicate what response you are expecting from the author, e.g. a reply, a bug fix, API change.

## How to accept feedback

* Treat reviews as a learning practice. Others might suggest
approaches you don't know or haven't tried.
* Provide responses to every comment (if appropriate).
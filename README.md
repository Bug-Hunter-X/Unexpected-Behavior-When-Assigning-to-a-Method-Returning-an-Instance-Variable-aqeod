# Ruby Bug: Unexpected Assignment Behavior

This repository demonstrates a subtle but important aspect of Ruby's behavior when assigning values to methods that act as accessors to instance variables.  Direct assignment to such methods does not modify the instance variable's value if there's no corresponding setter method.

## Bug Description

The `bug.rb` file shows that attempting to directly assign a new value to the `value` method (which is an accessor for `@value`) does not modify the instance variable. This leads to unexpected behavior where the value remains unchanged despite the assignment.

## Solution

The `bugSolution.rb` file presents a solution by explicitly creating a setter method (`value=`) that modifies the `@value` instance variable. This ensures correct modification behavior.

## How to Reproduce

1. Clone this repository.
2. Run `bug.rb`. Observe that the final output is still 20, not 30.
3. Run `bugSolution.rb`. Observe that the final output is now 30, reflecting the change.
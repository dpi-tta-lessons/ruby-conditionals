# Ruby Conditionals

> "To be, or not to be, that is the question."
>
> Hamlet (Shakespeare)

## Goal

By the end of this lesson you'll understand how to use booleans, `if`/`else` statements and the difference between *assignment* (`=`) and *equivalence* (`==`) operators to control the flow of your programs.

<div class="alert alert-info">
  <ul>
    <li><a href="https://www.youtube.com/watch?v=adibHGN4yz8" target="_blank">Tech Meeting with Amanda</a></li>
    <li><a href="https://www.youtube.com/watch?v=pRjJ463qq0w" target="_blank">Tech Meeting with Benny</a></li>
  </ul>
</div>

## Even or Odd?

Let's start with a real problem: how do we check if a number is even or odd?

```ruby
n = 7

if n.even?
  puts "#{n} is even!"
else
  puts "#{n} is odd!"
end
```
{: .repl }

This is your first example of a conditional statement. Ruby decides which branch of code to run based on whether `n.even?` is `true` or `false`.

## What is a Conditional?

A conditional in programming is a way to "make decisions". It lets your code run different instructions depending on whether something is `true` or `false`. You can think of it like a fork in the road:

- `if` this is *true*, do one thing
- `else` do another thing

## Anatomy of an `if` Statement

The basic form looks like this:

```ruby
if condition
  # code that runs if condition is true
else
  # code that runs if condition is false
end
```

In this code `condition` is a boolean (`true` or `false`) value.

<aside class="tip">
  Every <code>if</code> requires a matching <code>end</code>. Don't forget! It is a very common source of bugs.
</aside>

## Multiple Conditions

You can chain multiple conditions with `if`/`elsif`/`else`/`end`.

```ruby
the_temp = rand(100)

pp the_temp

if the_temp > 75
  pp "It's hot today."
elsif the_temp > 32
  pp "It's a nice day."
else
  pp "Brrr, too cold!"
end
```
{: .repl }

<aside class="tip">
  Ruby checks conditions top to bottom and runs the first one that matches. If none match, else runs as the fallback.
</aside>

<aside class="tip">
  Indent code within each branch by two spaces. This especially helps if you have multiple nested <code>if</code> statements.
</aside>

Consider this program. What do you expect it to print?

```ruby
n = 15

if n < 12
  s = "first part"
elsif n > 20
  s = "second part"
elsif n < 18
  s = "third part"
else
  s = "fourth part"
end

pp "It picked the " + s
```
{: .repl }

## "Truthy" vs "Falsy"

Most objects in Ruby are *truthy*, even `0`, `""`, and `[]`. Only `false` and `nil` are *falsy*.

<!-- TODO: example repl? -->

## Comparisons

We'll mostly use expressions after `if` that return either `true` or `false`. There are a lot of operators that are designed to do this; we've seen Integer's `.odd?` and `.even?` methods, but there are a lot more.

```ruby
5 > 3     # is 5 greater than 3?
5 < 2     # is 5 less than 2?
5 == 5    # does 5 equal 5?
5 != 3    # is 5 not equal to 3?
5 >= 5    # is 5 greater than or equal to 5?
5 <= 4    # is 5 less than or equal to 4?
```
{: .repl }

## Equivalence and Assignment Operators

`=` is the *assignment* operator. It *assigns* a value to a variable.

<!-- eql? and equal? -->
`==` is the *equivalence* operator. It checks if the values are equal.

Consider this program. What will this program print?

```ruby
n = "giraffe"

if n == "Giraffe"
  s = "first branch"
elsif n != "giraffe"
  s = "second branch"
else
  s = "third branch"
end

p "It picked the " + s
```
{: .repl }

<aside class="tip">
  Since "giraffe" is lowercase, the final else branch runs.
</aside>

## Quiz

- What does `=` do in Ruby?
- It assigns a value to a variable.
  - ✅ Correct!
- It checks if two values are equal.
  - ❌ That’s `==`.
{: .choose_best #assignment_vs_equivalence answer="1"}

Wrap-Up

- Conditionals let Ruby “choose a path” based on whether something is true or false.
- Use `if`/`elsif`/`else`/`end` to handle multiple branches.
- Remember: `=` assigns, `==` compares.
- Ruby considers everything "truthy" except `false` and `nil`.

## Project: Conditionals

In this project, you'll practice writing conditionals that handle different scenarios, including debugging common mistakes like forgetting end or mixing up `=` and `==`. This project includes automated tests, so click this link to get started <https://github.com/dpi-tta-projects/ruby-conditionals/fork>, fork the repository and create a codespace.

<aside class="warning">
  In order to get credit for completing this project you'll need to open the assignment link from canvas to generate an access token.
</aside>

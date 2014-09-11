# Object Lateral *Ruby* Style Guide

This document describes appropriate Ruby coding style across Object Lateral
projects. Please refer to the primary Style Guide for general principles which
also apply to Ruby.

## Hashes

Use Ruby 1.9-style hashes when possible.

Good:

```
attrs = {
  name: "Joe Blow",
  age: 27
}
```

Bad:

```
attrs = {
  "name" => "Joe Blow",
  "age" => 27
}
```

The hashrocket style is acceptible when the hash's keys must not be symbols.

Good:

```
statuses = {
  1 => "new",
  2 => "pending",
  3 => "complete"
}
```


## Blocks

Which block syntax to use depends on the purpose of the block of code. If the
block of code's purpose is to have a side-effect, use `do end` style.

Good:

```
users.each do |user|
  user.update :age, user.age + 1
end
```

Bad:

```
users.each { |user| user.update :age, user.age + 1 }
```

If the block of code's purpose is to transform some data for further use
(most often when chaining), use the `{}` style.

Good:

```
users.map { |user| user.name.upcase }
```

Bad:

```
users.map do |user|
  user.name.upcase
end
```

## Parentheses

Omit parentheses unless the language requires it, e.g. – when method chaining.

Good:

```
Ticket.where title: "help me out"
Ticket.where(title: "help me out").limit 10
```
```
def my_method arg1, arg2
  # ...
end
```

Bad:

```
Ticket.where(title: "help me out")
Ticket.where(title: "help me out").limit(10)
```

```
def my_method(arg1, arg2)
  # ...
end
```

# Object Lateral Style Guide

The purpose of these documents is to define what is appropriate coding style
across Object Lateral projects. General principles are described in this
document, while language-specific principles reside appropriately named files.

Language-specific principles trump general principles in the case of a conflict.

## Indentation

Indent code blocks using **2** whitespace characters (soft tabs). Remove hard
tabs from files that have them.

## White Space

Do not include any white spaces at the end of lines. Blank lines should have no
white space characters at all. It is recommended to integrate this into your
text editor before write.

Include a white space between assignments and after commas in arguments lists
and arrays.

Good:

```
test = [1, 2, 3]
User.authenticate("joe@blow.com", "test1234")
```

Bad:

```
test=[1,2,3]
User.authenticate("joe@blow.com","test1234")
```

Do not include extra whitespaces between before function arguments.

Good:

```
def hello(first_name, last_name)
```

Bad:

```
def hello( first_name, last_name )
```

## Blank Lines

Include one blank line between significant code blocks. Significant code blocks
include: class/modules, function/method definitions, conditionals.

Good:

```
def method1
  # ...
end

def method2
  # ...
end
```

Bad:

```
def method1
  # ...
end
def method2
  # ...
end
```

Do not include blank lines between nested code blocks.

Good:

```
if x == 1
  y.each do |z|
    if y > z
      puts z * x
    end
  end
end
```

Bad:

```
if x == 1

  y.each do |z|

    if y > z
      puts z * x
    end

  end

end
```


## String Literals

All string literals should be wrapped in double quotes. This allows for easy use
of string interpolation in languages that support it. Escape `"` characters
inside strings or use `'` where appropriate.

Good:

```
"how now brown cow"
"They saw \"The Wizard of Oz\""
"They saw 'The Wizard of Oz'"
```

Bad:

```
'how now brown cow'
'They saw "The Wizard of Oz"'
'They saw "The Wizard of Oz"'
```

## Curly Braces

Use "east-coast" curly braces not "west-coast" curly braces.

Good:

```
if (1 == 1) {
  // do something
} else {
  // do something else
}

```

Bad:

```
if (1 == 1)
{
  // do something
}
else
{
  // do something else
}
```

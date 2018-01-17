# WebDevBoK - The WebDev Book of Knowledge

## Purpose

To do their job and to do it effectively Web Developers are required to 
be familiar with multiple technologies, languages, libraries, tools, 
frameworks, processes, and procedures. Memorizing information with this
breadth, complexity, and sheer volume of information is a daunting task.

The purpose of this repo is to collect, organize, and document this 
information in a way that makes it easy to find and use. In other words,
to make this information readily available and actionable so you don't 
have to memorize it.

As you might expect this information is categorized and indexed to make
it easy to find. At the highest level categorization centers on the
major elements of the WebDev's normal workflow. Namely, design,
development, operations, and project management.

## Design

## Development

### Javascript

#### Truthy & Falsey Values

A value is truthy if it converts to true when evaluated in a boolean context.
For example, the number 1 is truthy because, 1 evaluates to true. 

Here’s the list of all of the falsy values:
- Boolean value false
- null type
- undefined type
- number 0
- empty string ""
- odd value NaN (stands for "not a number", check out the NaN MDN article)

Essentially, if it's not in the list of falsy values, then it's truthy!

### Array Copy vs. Reference

#### Rationale
Javascript assignment of one object to another merely assigns the reference
associated with the original object to another. This means that both 
variables reference the same physical object. This is generally 
desirable for operations such as passing variables as parameters to
functions. However, sometimes you really want a copy of the array so
the original array is preserved.

A relatively simple way to make a copy is to use `JSON.stringify` and
`JSON.parse` to create a copy of the array.

#### Example
```
const newArray = JSON.parse(JSON.stringify(currentArray));
```

### Source Code Control

#### Git

## Operations

### Managing Environment Variables
## Project Management


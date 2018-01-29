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

## Development Environment

### Linux

The following assumes that a CentOS/Fedora/RHEL distro. These commands may
not work in other distros such as Debnian or ArchLinux.

#### Basic Environment

The following packages are useful for working in a Linux environment and 
are independent from any particular set of development languages or tools.
For the sake of brevity `sudo` has not been specified in the installation
command, but may be required when installing under a user id other than
`root`.

| Package           | Installation               | Purpose                                    |
|:------------------|:---------------------------|:-------------------------------------------|
| Fedora EPEL repo  | `yum install epel-release` | Fedora EPEL repos and third party packages |
| Update yum package catalog | `yum update`      |                                            |
| Bash Autocomplete | `yum install bash-completion bash-completion-extras` | Enable recognition of [TAB] character to autocomplete command line commands |

## Design

## Development

### Javascript

#### Functions

##### Return

Functions always return some value upon exit. Even if there is no `return` 
statement. When there's no `return` statement a value of `undefined` is
implicitly returned. 

This is why you'll see a value of `undefined` in the 
browser console when you execute a `console.log` statement. This function
doesn't execute a return so you'll see both the message you have requested it
to log, plus `undefined`.

#### Scope

There are three types of scope. `Global scope` refers to variable defined outside
all functions in the Javascript file. `Function scope` refers to variables
defined inside a function. Variables that are part of the `global scope` are
available to all functions in the Javascript file, while those that are part of
`function scope` are available only to the function they were defined in and any
functions contained or nested within that function.

ES6 introduced a new type of scope called `Block scope'. *_TBD_*.

When trying to access an identifier, the JavaScript Engine will begin looking
for the identifier within the scope of the current function. If it isn't found
then the Engine steps out to the next outer function and reapeats the search.
the process is repeated through all outer functions until the global scope
is reached.

##### Hoisting

Before any Javascript is executed all function definitions are `hoisted` to the
top of their containing scope. This is what allows a function to be called
ahead of its definition in a file. However, variable assignments are not
hoisted!

A best practice is to define functions before they are referenced and to define
variables at the highest point in their containing scope. This ensures that the
way the code looks and the sequence in which the code executes are the same.
This can save considerable confusion and bugs since nothing is hidden from the
webdev.

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

##### Workflows

## Libraries

### jQuery

#### Selectors

- `$('tag')`
- `$('.class')`
- `$('#id')`

## Operations

### Managing Environment Variables

## Project Management


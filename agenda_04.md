# Agenda

_Any fool can write code that a computer can understand. Good programmers write code that humans can understand._ - Martin Fowler

Code Golf - solve a specific problem in as few lines of code as possible.

Things to think about while golfing:
 - What does your language of choice do well (with respect to code golf)?
 - What does your language of choice do poorly (with respect to code golf)?
 - Did you ever hit a point where your code becomes 'unreadable'?
 - Is there such a thing as 'the best solution' to a problem?
 - How do you determine if/when a particular solution is elegant?

# The Problem

Here is a simple ASCII art snowman:

    _===_
    (.,.)
    ( : )
    ( : )

Let's make him some friends. This will be the general pattern for our ASCII art snowpeople:

     HHHHH
     HHHHH
    X(LNR)Y
    X(TTT)Y
     (BBB)

The leading spaces and the parentheses are always the same for all snowpeople. The different letters represent sections of the pattern that can individually change. Each section has exactly four presets for what ASCII characters can fill it.
By mixing and matching these presets for all eight sections, we can make a variety of snowpeople. 

## All Presets

<sup>(Notice that spaces are put on otherwise empty lines so the section shape is always correct.)</sup>

#### H is for Hat

1. Straw Hat
```
_===_
```
2. Mexican Hat
```
 ___ 
.....
```
3. Fez
```
 _  
/_\ 
```

4. [Russian Hat](http://en.wikipedia.org/wiki/Ushanka)
```
 ___ 
(_*_)
```

#### N is for Nose/Mouth

1. Normal `,`

2. Dot `.`

3. Line `_`

4. None  ` `

#### L is for Left Eye

1. Dot `.`

2. Bigger Dot `o`

3. Biggest Dot `O`

4. Closed `-`

#### R is for Right Eye

(Same list as left eye.)

#### X is for Left Arm

1. Normal Arm
```
<
```

1. Upwards Arm
```
\
```

2. Downwards Arm
```
/
```

3. None
```
 
```

#### Y is for Right Arm

1. Normal Arm
```
>
```

2. Upwards Arm

```
/
```

3. Downwards Arm

```
\
```

1. None
```
 
```

#### T is for Torso

1. Buttons <code> : </code>

2. Vest `] [`

3. Inward Arms `> <`

4. None <code>   </code>

#### B is for Base

1. Buttons <code> : </code>

2. Feet `" "`

3. Flat `___`

4. None <code>   </code>

### Challenge

Write a program that takes in an eight character string (via stdin or command line) in the format `HNLRXYTB`, where each letter is a digit from 1 to 4 that denotes which preset to use for the corresponding section of the snowperson. Print the full snowperson to stdout.

For example, the input `11114411` is the snowman at the top of the page. (First `1`: he has a straw hat, second `1`: he has a normal nose, etc.)

Another example, the snowperson for input `33232124`:

       _
      /_\
    \(o_O)
     (] [)>
     (   )

### Details
- Any amounts and combinations of leading/trailing spaces and leading/trailing newlines are allowed as long as...
    - the snowperson has all their sections arranged correctly with respect to one another, and
    - there are never more than 64 total whitespace characters (the general pattern is only 7&times;5, so you probably won't hit this limit).

    You don't need to print rows/columns of the pattern if they only contain whitespace. e.g. the empty line of the straw hat is not required.

- You must use the ordering of the parts as they are given above.

- Instead of a program, you may write a function that takes the digit string as an argument. The output should be printed normally or returned as a string.
- You may treat the input as an integer instead of a string if preferred.

## Food
Catering from [Creole Soul Café](http://creolesoulcafe.com/index.html) on East Jefferson St.

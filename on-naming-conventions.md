## Naming and differentiation of categorical identifiers
The Breakfast Post<sup>[1](#footnotes)</sup> made an excellent laborous study, poring over about 500,000 lines of code across nearly 2000 source files of SML code, on the anarchy of *Standard ML*'s guidelines on naming and separating with the capitalization rules the different aspects of the language, namely `variable`s, `structure`s,
`signature`s, `functor`s and `exception`s. They drew from these conclusions of a standardized convention through **argumentum ad popularum**, by apppealing to the wide adoption of each guideline between the most prominent projects programmed in SML. This argumentation could be compared to Common Lisp's still-born standardization process, which had the more popular implementations blackmailing their concerns with threats of backing down from the project. I think this fails to see the variance on ergonomics between text input from layout to layout. My concerns apply to Ocaml's general guidelines as well.

### Ergonomics
To start with, I had to take a closer look at a **US/GB QWERTY** -layout, since I
have never had to use one in my entire life, and the very first thing I notice is
that I can already see the non-issue of reaching towards the hyphen-underscore (`-` */* `_`)
key, which is located in the number row, to the right of 0. It is a **lot** easier
than in **SV QWERTY** which has the `-` */* ` _`-key where the `?` */* ` /`-key
would be located in a standard **US QWERTY**; and where the `!` */* ` §`-key lies in the
**FR AZERTY.**

I did some purely subjective experiments to compare if it's as easy as it looks and I
quickly came to the conclusion, that having the underscore, where it's easily pushed by 
one of the more dominant fingers, is a lot better than a location, than a key reached with
with a pinky finger. After all, throghout this I have the other (left) hand's
pinky holding the Shift down.

This is a simple fact of *ergonomics* being a huge matter for the rest of the
world, at least for the **DE QWERTZ** and the **SV QWERTY** (which is used all
throghout the Fennoscandia!) users. Both of these layouts have the
`-` */* `_` located right next to the right-hand Shift.

I understand why these things wouldn't matter for the native English-speaking,
or the French-speaking programming world, since you have your underscore
accesible, with a simple keychord of Shift+8. A character, that is fairly simple
to reach from the homerow, with having the ability to use your eg. middle-finger
extended forward, is definetly not something a programmer would find themselves
straining to type. Now compare this to the concept of *Emacs pinky*, a repetitive
strain injury said to be caused by having to curl your pinkies repeatedly to
hold Ctrl/Meta/Alt/Shift while chording the keys <sup>[2](#footnotes)</sup>

### snake_case
I can't emphasize how much I've come to abhor `snake_case` and it's variants. 
Underscores in general too. For most, Lisp's parenthesis-leaden syntax is an
abomination, while some might accept it as a neccesary evil for the efficient
metaprogramming facilities. For me, though, the fact that there are no other 
delimiters or special characters to worry about than a parenthesis and a hyphen<sup>[3](#footnotes)</sup>
acts as a leveler of a certain sort.

(This is what specifically attracted me to Scheme the first time
I actually tried typing it out, rathen than moan about being *Lost In a Sea of
Parens*. Even the naming convention, `kebab-case`, is pure bliss!
Not having to keep a finger on guard duty, ie. sitting on top of Shift, can k
quite liberating.)

While SML and Ocaml don't allow hyphen-delimited names due to the lexer, snake_case is still
avoidable

### camelCase and DromedaryCase
I simply resist the practice of delimiting words with underscores in names, so I'll resort to
`camelCase` and `DromedaryCase` (or more derogatorily `PascalCase`) when needed. I know it's against
the Standard-library's conventions on SML and the suggested guidelines for Ocaml, but mostly
I'm programming on my own. If I had to collaborate and add to someone else's project, I would of course
follow the convention set forth in it. Otherwise others will have to conform to my convention and
I'm highly opionated, as evidenced by this, on the  matter.

#### Footnotes
1. [Naming conventions in Standard ML, The Breakfast Post](https://thebreakfastpost.com/2016/06/11/naming-conventions-in-standard-ml/)
2. [Emacs Pinky, C2 Wiki](http://wiki.c2.com/?EmacsPinky)
3. *Scheme does utilize the question mark convention on predicates, but it is convenient addition to the syntax compared to Common Lisp's `-p`-suffix.*

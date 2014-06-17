---
layout: presentation
year: 2014
title: User Interfaces
instructors:
 - Seifu
---
<section markdown="block">
### What are we talking about?

Whenever we write code, we have some user in mind who will interact with it via some an interface.

How do you interact with (your own? someone elses?) software?
</section>

<section markdown="block">
What broad kinds of interfaces are there?

What kinds of users are there?
</section>

<section markdown="block">
No interface:

- Click program icon

- Type name, press ENTER

</section>

<section markdown="block">
Command line interface (CLI):

- Arguments passed after program name
  - `ls -lh`
  - `tar -czvvf my_new_tar_file.tgz ./*`

- Interactive UI
  - `fdisk`

- Special cases:
  - servers
  - supercomputers

</section>

<section markdown="block">
What makes CLI software easy/hard to use?
<section markdown="block">
Take the next ten minutes and explore `cat` and `grep` then explain what they do.
Were they easy to use?
</section>
</section>

<section markdown="block">
Graphical user interface (GUI):

- Common operating systems
  - Windows, OS X, Gnome/KDE/XFCE for linux
- Most commercial or consumer-targeted software
  - Office
  - Photoshop
  - Firefox
- Special cases:
  - Websites
  - Touch screens

</section>

<section markdown="block">
What makes GUI software easy/hard to use?

<section markdown ="block">
With the people around you:
Compare some interfaces, e.g. Yahoo & Google, Notepad & Word
</section>
</section>

<section markdown="block">
Simple software should have a simple interface.
Should complex software have a complex interface?
</section>

<section markdown="block">
Creating simple interfaces for complex software is hard!
Broad principles:

- Know your users and what they know
- Exploit familiar interface patterns
- Exploit psychology and culture

</section>

<section markdown="block">
Know your users.  Are they:

- Kids or adults
- One time or long term users
- Novices or experienced programmers

</section>

<section markdown="block">
Know your users (cont.)

- Make common things easy
- Create basic/advanced alternative interfaces [Examples?]
- Create customizable interfaces [Examples?]

</section>

<section markdown="block">
Exploit familiar interface patterns

- What does flipping a switch do?
- What does turning a dial do?
- Swiping? Ctrl + V? Clicking an 'X'?
[What are some more examples of ingrained controls?]

</section>

<section markdown="block">
Exploit familiar interface patterns (cont.)

- Command line tools: reuse familiar flags!
List as many flags as you know from our course so far. 9 common flags come to mind.

</section>

<section markdown="block">
Exploit psychology and culture

- If you step into an unfamiliar room, where do you look first for the light switch?
- How do you choose whether to push or pull a door?
- If something is flashing red, what does that mean? Other colors?

</section>

<section markdown="block">
Exploit psychology (cont.)

- Put things where people will naturally look for them
  - Controls near the thing they control
- Group related things
- Hide confusing/misleading options
- Use good documentation/pop up messages to target subtle or misleading controls

</section>

<section markdown="block">
Having many controls that are poorly organized can obscure the useful ones
Having excessive documentation for things that are obvious or unnecessary for the user can obscure the useful information
</section>

<section markdown="block">
When you don't know how to make something better, find some guinea pigs!
Ask *them* what they expect to happen when they use your software.
</section>

<section markdown="block">

- `python -m http.server 8000`
- [Curses Textbox](curses_textbox.py)
- [Curses Dungeon Creator](curses_dungeon_maker.py)
- [TKinter Nibbles](tkinterNibbles.py)

</section>

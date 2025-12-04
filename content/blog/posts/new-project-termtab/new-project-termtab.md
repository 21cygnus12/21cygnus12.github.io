+++
date = '2025-11-04T21:54:05-08:00'
draft = false
title = 'new project: termtab'
+++
### the root of the problem
i hate my mouse, especially on my laptop. because of this, i'm always trying to
minimize my need to use it.
### the problem
i've been playing guitar for years, and i often find myself wanting to
transcribe things i've learned to avoid having to start from scratch if i
forget anything. in an effort to fix this, i purchased a copy of guitar pro and
have been using that ever since. my main issues with guitar pro are:
- complete lack of linux support (i don't want to have to use wine)
- proprietary software and file formats
- cost (~$70)
- design heavily favors mouse usage

all of these factors combined led me to want to fix the problems myself.
### my solution
i started designing my own program. it would be an open source terminal
interface that uses vim motions. i also wanted everything to be
plaintext-based. originally, i planned to make a neovim plugin that would
streamline the parsing, formatting, editing, and exporting of as many guitar
tablature formats as possible. this would make things much easier to develop
since neovim would handle all of the user input and configuration for me.
however, i eventually settled on making my own app using rust's ratatui crate.
this would allow me to create my own file handling and structured layout, but
mainly i just really like using rust over something like lua. additionally, i
came up with the idea to create my own tab format that's expressive enough to
clearly represent rhythms while only using unicode.

{{< image src="/images/old-tab.png" alt="old-tab.png" position="center" >}}

above is an example of "ascii tab" i found on the wikipedia page of the same
name. although it's in plaintext, which is nice, so much information is
missing. what's the time signature? in what rhythm should the notes be played?
these problems are what i set out to solve.

{{< image src="/images/new-tab.png" alt="new-tab.png" position="center" >}}

now look at *this* image. 

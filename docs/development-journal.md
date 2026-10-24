# Motivation for this project

Music fascinates me, particularly bass. I wanna be able to take any song, figure out the notes used in composition, and play around with it on different instruments. 

# Core Data Structure

When I was first thinking about this project, I thought I'd need multiple sources of data involving the bass guitar's strings, frets and tuning for the app to identy a music note and use it. So either nested arrays, or multiple variables storing each piece. Fortunately, after some research I figured the **MIDI numbers could be used to identify pitch**. Each string and each fret on the bass will produce certain pitch when played - and these change with the bass guitar's tuning. The same can be said for any other intrument I might add to the app in future.

To expand on this idea, I don't even need an array full of all possible MIDI numbers mapped to each fret. I can simply use a number equivalent to an instrument's amount of inputs (mainly, a standard bass guitar has 4 strings) and then run some calculations when frets are selected too. For example, let's say open E string returns MIDI number 1; selecting fret 2 on the E string will return MIDI number 3. 

This whole setup for the main data structure avoids unnecessary duplication and looks tidier. No need to run calculations on 5 different variables when MIDI number can be the only one that derives other numbers from calculations.

# My approach to testing

As much as I'd love to sound like a rockstar and say that this project is following test-driven development (TDD), I'd rather admit that this is an exploratory project. I'm still figuring a lot of stuff out, including what features or behaviour I even want. I'll do what I can with testing, and I'd love to explore it further, but yes I'm basically winging it to an extent.
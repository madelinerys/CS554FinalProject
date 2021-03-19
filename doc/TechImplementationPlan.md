# Technical Implementation Plan, CS-554 Final Project

## Group Tempest

## Group members

#### Kyle Bernardes CWID 10412644
#### Mahima Chandan CWID 10467889
#### Dale Pippert CWID 10469880
#### Madeline Rys CWID 10416134

## Project Overview

Falling under the broad classification of *gamification [1]*, our project is __Topic Tempest__.

Topic Tempest is a subset of a Jeopardy!-like game [2]. Unlike Jeopardy!, the board holds *questions* which
players must *answer* by typing into a text box on their browser screen [3]. Topics can be anything,
but our intent is to target the game towards learning and professional training environments. Apart
from actual game play, users may be given permission to enter their own topics and questions from
their field of interest.

## Planned Course Technologies
This section lists technologies covered in course lectures that are planned
for use by our group.

***React***. Client side will be built using Facebook React framework. React is an excellent choice
for this project, because the notion of *state* is first-class and central to its existence, and in game play,
understanding and modeling the *state*, *actions*, and *events* that cause state transitions,
is just *everything* important.

***Bootstrap***. Client side layout will be a responsive design using Bootstrap grid layout
along with some Bootstrap controls.

***Firebase Authentication***. Our app will authenticate users using Firebase Authentication.

## Planned Independent Technologies
This section lists technologies that were not covered in course lectures, that we plan
to investigate and make use of.

***Firebase Realtime Database***. Another separate and distinct product under the Google Firebase umbrella.
We will use this to keep the game state (as represented by your browser screen) across players in sync,
as well as using it for the general purpose application data store.

***Screen reader***. We intend to explore use of screen reader technology (text-to-speech) within
the client-side application. Our plan is to make use of this for speaking questions to the
players, as well as providing guidance, status, and control information during game play. We
believe leveraging this type of assistive technology within our platform, is both course-relevant
and compelling in terms of application accessibility.

<hr/>

[1] Wikipedia defines gamification as *the strategic attempt to enhance systems, services, organisations
and activities in order to create similar experiences to those experienced when playing games, in
order to motivate and engage users.*

[2] https://en.wikipedia.org/wiki/Jeopardy!. (N.B. And with special tribute to longtime-host Alex Trebek,
who recently passed.)

[3] In Jeopardy!, the board holds *answers*, and players must respond with (e.g.) "What is.." as a leader
to their proposed *question*.

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

## Notes

[1] Wikipedia defines gamification as *the strategic attempt to enhance systems, services, organisations
and activities in order to create similar experiences to those experienced when playing games, in
order to motivate and engage users.*

[2] https://en.wikipedia.org/wiki/Jeopardy!. (N.B. And with special tribute to longtime-host Alex Trebek,
who recently passed.)

[3] In Jeopardy!, the board holds *answers*, and players must respond with (e.g.) "What is.." as a leader
to their proposed *question*.

<hr/>
</hr/>

## Application architecture

1. UI is a *single page application (SPA)*. All references in here to words like *page* or *screen* are
therefore logical in nature and not to be taken literally.

## Authentication

1. Users must be authenticated in order to play.

1. Authentication must include functionality for both Sign up (new user)
and Sign in (existing user).

1. Login screen once authenticated takes you to game screen.

1. Authentication must support native (Tempest username/password).

1. Authentication must support at least one third-party identity provider (Google, Facebook,
Twitter, GitHub, Amazon, etc.).

1. Support provided for changing your password only time-permitting.

## Game play

1. Game play occurs on game screen.

1. Game play will start once a configured number of players have joined.

1. Player is blocked on game screen until set number of players have joined.

1. Host is automated and enters instructions in the host guidance text area control.

1. Screen reader is used to speak host guidance.

1. Host decides order of play amongst players.

1. Host will decide who goes first.

1. Each question/answer pair is considered a *round*.

1. Player's turn appears in Player text box.

1. Player has 5 seconds on clock to make a selection by clicking a square on board.

1. Clock counts down until player clicks an available board square, or clock reaches 0.

1. Question pops up in *non-modal* box (so that player can type while question is active).

1. Screen reader assists by reading the question aloud.

1. Clock starts at :15 seconds once question pops up.

1. Clock counts down until at least one player *submits*.

1. Clock pauses count down, but does not erase, when player submits. 

1. Player enters answer by typing in Answer box and pressing Enter (or &lt;Enter&gt; key).
 
## Upload Topics and Questions

A feature of the system is to allow users to upload topics and questions. Requirements follow.

1. An authenticated user is presented an option to create a new topic or search and edit
an existing topic.

1. No capability is provided through UI for users to delete a topic.

1. No capability is provided through the UI for users to change the name of a topic.

1. Users can browse the list of questions and answers for a topic and make changes such
as adding another answer to a question, changing the wording of a question, deleting a
question that is a duplicate or not longer wanted, or adding a question and (possibly multiple)
answers to the question.

1. Case and punctuation insensitive. 

1. Batch upload of topics and questions/answers is not supported by UI.

## Work Breakdown

<table>
<tbody>
<tr>
  <th>Item</th><th>Developer</th>
</tr>

<tr>
  <td>Authentication. Sign up/Sign in. At least one third-party identity provider (eg Google/Facebook/Twitter etc.)
supported in addition to Tempest itself.</td><td></td>
</tr>

<tr>
  <td>Upload topics and questions. Includes creation of new topics, batch upload, and one-off entry
and editing of topics and question/answer. Questions may have more than one correct answer.</td><td></td>
</tr>

<tr>
  <td>Authentication including Sign in or Sign up, AuthCookie, middleware validation, logout</td><td></td>
</tr>

<tr>
  <td>Preparation of topics with questions/answers and loading same into database.</td><td></td>
</tr>

<tr>
  <td>API to betting lines including database storage</td><td>Dale</td>
</tr>

<tr>
  <td>API to game results (scores) including database storage</td><td>Dale</td>
</tr>
</tbody>
</table>



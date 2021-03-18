Hello CodePath! This repo contains the game with the optional features!

# Pre-work - _Memory Game_

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program.

Submitted by: **Jason Zhang**

Time spent: **5** hours spent in total


Link to Project: https://glitch.com/edit/#!/shorthaired-glaze-suggestion?path=README.md%3A45%3A47


## Required Functionality

The following **required** functionality is complete:

- [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
- [x] "Start" button toggles between "Start" and "Stop" when clicked.
- [x] Game buttons each light up and play a sound when clicked.
- [x] Computer plays back sequence of clues including sound and visual cue for each button
- [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess.
- [x] User wins the game after guessing a complete pattern
- [ ] User loses the game after an incorrect guess

The following **optional** features are implemented:

- [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
- [x] Buttons use a pitch (frequency) other than the ones in the tutorial
- [x] More than 4 functional game buttons
- [x] Playback speeds up on each turn
- [x] Computer picks a different pattern each time the game is played
- [x] Player only loses after 3 mistakes (instead of on the first mistake)
- [x] Game button appearance change goes beyond color (e.g. add an image)
- [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
- [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:
![](your-link-here)


the gifs below shows the light and memory game with additional features.
the link below is the link to all the gifs

https://imgur.com/a/9Sz8NMu

the first two gifs below is the winning playthrough with a randomized pattern of 8 buttons.

![Alt Text](https://i.imgur.com/qAetuGm.gif)
![Alt Text](https://i.imgur.com/KeNgpW1.gif)

the next gif shows what happens when you go past three strikes for mistakes and lose

![Alt Text](https://i.imgur.com/7xptlZ6.gif)

the next gif shows what happens in this game when you press start/stop

![Alt Text](https://i.imgur.com/RL9MC2D.gif)

## Reflection Questions

1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.

W3 website

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)

A challenge was really just keeping track of all the different parts of the parts(the html, the javascript,
and the css files) of the webpage. In order to keep track of everything, I took out paper and pen, and organized
all parts of the three files into groups based on their functions. Basically, I created a table where the
columns are the html components and each column contains the corresponding javascript functions and css styles.
This not only helped organizing my thoughts but also let me see the big picture more easily. I actually had to
create that table while I was trying to have the buttons display images instead of just changing the background
colors of the buttons. I had the images disappear at the start of the game, but I could not make it reappear
after clicking. I thought I had somehow messed up the entire structure of the program because every function
depends on another and that one function may have changed the entire output of the button functions.  
After making the chart and poring through every function, I could not find the problem. This, embarrassingly
enough, took me way over an hour until I finally found the problem. It was not a problem with the structure
of my code though funnily enough I found a different problem(The other problem was if the game hasn’t
started yet and the player clicks on any button then the alert “Game over. You lost” will pop up.
The cause was because I had still set gamePlaying to true which should have been false for the
stopGame function). The problem was that I had set the image as hidden since I was following the functions
shown in the given tutorial. However, hidden images are unclickable! That’s why the images won’t show up even
after clicking the buttons. Honestly, when I found that out, I thought I had wasted so much time for something
so simple. I only overcame this problem by complete brute force and then finding out of the opacity style.
Based on the documentation, I had thought the display style was the only one that was unclickable because
the display element makes whatever html picked to be not visible and not take any space. On the other hand,
I thought the visibility style was clickable because it just makes the html element not visible but still
takes up space(I somehow assumed that not taking up space meant just being invisible)! Evidently, that was
not the case and the opacity style of css came and saved the day.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words)

My first question is if there is a way of calling other functions after certain functions run.
I was curious after trying to implement timer but to no avail since I wanted the timer to be called
after everything is done yet everything seems to run at the same time? Another question is
that(I could be wrong) what I currently did seems to just be pure HTML, CSS, and Javascript.
The only link I see on the Glitch project is to style.css which is just regular css I believe.
However, I heard of other popular frameworks such as Bootstraps and am wondering if those frameworks
look nicer/are more user-friendly/ are easier for programming? Generally what makes these frameworks
more popular?
Another question: Since this tutorial is all front-end and I only got a small taste of web development,
how will the backend be incorporated into the frontend? An example would be if a button is pressed on
the frontend, how will that action be transferred to the backend for whatever function that button is
supposed to do?

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words)

If I had a few more hours, I will definitely try to figure out how to implement the timer.
I wrote the call to the timer function below the code logic for playClueSequence so that it was
supposed to be run after the for loop of clue sequence is done. However, the timer runs at the same time
as the for loop which results in a shorter time for guessing the longer the clue playback is.
Another issue with the timer was that the same timer function is called! What that means is that if
the timer stops at 3 seconds after the first guess, the timer for the second guess will start at 3
instead of the original starting time like 5 seconds! As the game goes on, the timer function’s starting
time will get shorter and shorter. I am still wondering if it’s possible to create copies of functions in
javascript so each call of the timer function will be a new version 
and the time variable that keeps track of the timer will be new each time.

Another feature that I thought would be cool is instead of a set number of patterns,
the game will go on as long as possible until the player loses. That means a player can
theoretically play infinitely if the player remembers every pattern. The game can start with a
randomized pattern array with only one button element in it. If the player guesses right, then
another random button element will be added into the array. This will keep going on until the player loses.
A scoreboard can be set up to keep track of the longest record in the game.

## License

    Copyright [YOUR NAME]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

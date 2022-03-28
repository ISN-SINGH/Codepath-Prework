# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program.

Submitted by: Ishan Singh

Time spent: 5 hours spent in total

Link to project: https://glitch.com/edit/#!/acoustic-daffy-plantain

## Required Functionality

The following **required** functionality is complete:

* [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [x] "Start" button toggles between "Start" and "Stop" when clicked.
* [x] Game buttons each light up and play a sound when clicked.
* [x] Computer plays back sequence of clues including sound and visual cue for each button
* [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess.
* [x] User wins the game after guessing a complete pattern
* [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [x] Buttons use a pitch (frequency) other than the ones in the tutorial
* [ ] More than 4 functional game buttons
* [ ] Playback speeds up on each turn
* [x] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [x] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:
![](https://recordit.co/DSffMO8a6G)
![](https://recordit.co/SxMbPD2L00)
![](https://recordit.co/OKosqrDKvP)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.
https://developer.mozilla.org/en-US/docs/Web/API/setTimeout
https://developer.mozilla.org/en-US/docs/Web/API/clearTimeout
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)
One challenge I faced was in trying to implement a limited amount of time for each turn.
I was at first thinking that I should learn how to use setInterval() and call playClueSequence() only if the player finished entering
their sequence within some time and if not, they lose. This solution required a lot of restructuring of the code and I wanted something more
concise. My thought was that if I'm having to rewrite startGame(), which is the root of the functionality, I may have to rewrite functions it calls and this could lead to a lot of unnecessary work.
I overcame this by breaking down the task into smaller parts. I realized that if the player lost if they didn't do certain things
within a time limit, why not just put loseGame() on a timeout? Then I could add a new countdown for each turn of the player that corresponded to longer turns. This required me to only add one line to playClueSequence()
and a few more conditions to guess(). I also needed to set the right amount of time for each level. I solved this by simply play-testing my game and gathering data. On average I only needed the amount of time it took for
the website to display the current clue sequence for me to enter it. I decided to set the time limit as the time it took to display the sequence and one extra second.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words)
One burning question I had was: How could I implement a graphical countdown timer that showed the user how much remaining time they had for their turn? I looked into it a little and it requires learning Scalable
Vector Graphics but that only gave me more questions: What are SVG's limitations? Can SVG be used to animate objects like paragraph text/buttons or does it have its own objects? I also had questions about how I could
make a website more interactive with a user. What ways other than buttons/hyperlinks allow a user to interact with a site? I think that making a website more interactive and less static
would be best for UX. I want to know how web developers balance interactivity and simplicity in website design.

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words)
There are websites that can play animations or hold still depending on how much you've scrolled on the page. This feature has always fascinated me and it would be one thing I would try to implement. If a user has played
the memory game multiple times, they could scroll down and fancy animations would tell them their gameplay stats (average time spent on turn, # of wins, # of losses, etc). I would also implement a graphical countdown timer using
SVG and keep the timer at a spot where the user can be aware of their time remaining as they play. Lastly, I would change the game so that in the beginning the user could enter the number of buttons they want to play the memory game with
(up to 8) and the layout of the website would change accordingly with more/less buttons. The clue sequence chosen would increase its possibilities to all buttons the user chose to have and the sounds played when pressing each button would
change based on how many buttons there are.

## Interview Recording URL Link

[My 5-minute Interview Recording](https://youtu.be/Fnnuo2IA_Sw)


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

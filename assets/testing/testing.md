# Testing
[Go back to the main README.md file](README.md)
[Go to the Plant Memory live project here!](https://josefinekihlstrom.github.io/Plant-Memory/)

## Automated Testing
- [W3C CSS Validation](https://jigsaw.w3.org/css-validator/)
    - This project passed the W3C CSS Validator without any remarks. 14th November - 2020
- [W3C Markup Validation](https://validator.w3.org/)
    - This project passed the W3C Markup Validator without any remarks. 14th November - 2020
- [JSHint](https://jshint.com/)
    - This project was validated with JSHint validator on 14th November 2020 with
        - 20 warnings
        - One undefined variable
        - Two unused variables

## Manual testing
All manual tests were done in the following browsers:
- Firefox
- Google Chrome
- Microsoft Edge

1. Open a new browser and verify that the content is loaded correctly.

2. Memory game section:
    - Click on the 'Start The Game' overlay and the overlay disappears correctly.
    - Timer is starting after overlay is removed.
    - When clicking the first card, sound effect fires and the card stays flipped.
    - When clicking the second card, second card flips and sound effect fires:
        - If match: Both cards stays flipped and a sound effect fires. Moves counter adds one.
        - It no match: Both cards unflip and sound effect fires. Moves counter adds one.
    - When clicking on a third card before unmatched cards unflip, the board is locked.
    - When clicking on the first card after it's already been clicked, it still counts as first card and does
    not affect when the second card getting clicked.
    - When clicking on the second card after it's already been clicked, it still counts as second card and
    checkMatch function fires as normal.
    - When all cards are matched, timer stops, winning sound effect fires and 'Congratulations' overlay covers the memory game.

3. Menu section:
    - When replay icon is clicked the page reloads and 'Start The Game' overlay appears.
        - Verified by pressing the 'Start The Game' overlay that the cards are being reshuffled.
        - If a round has been played and finished before clicking the replay button, the time stamp from the last
        round appears in the menu section under the timer.
    - When clicking on the speaker icon the background music starts playing and the icon changes to a speaker playing sound.
        - When clicking the speaker icon again the music stops and the icon changes back to the initial state.
        - When background music is playing, the other sound effects aren't negatively affected.
        - When finishing the game while background music is playing, the background music stops correctly and
        icon changes back to initial state.
        - When clicking the speaker icon when game is finished and background music has turned off, background
        music starts playing again and icon is changed to speaker playing sound.
    - When clicking the questionmark the 'How to play' modal pops up.
        - When modal is showing, verify that by clicking the 'X' symbol the modal closes.
        - When modal is showing, verify that by clicking the 'Close' button the modal closes.
        - If game is started and questionmark icon is clicked, the timer continnues to run when modal pops up.

### Bugs found while testing manually
1. When matching a pair right after a previous match, the match sound effect would not fire a second time.
    - This was solved by putting the match sound effect to a current time of 0 when being executed.

2. When the game has been started and the question mark icon is clicked and modal pops up, the timer does not stop.
This function of stopping the timer when modal is showing does not exist in this version of the game due to lack
of time to develop it. This is added to the 'Features left to implement' section in the README.md file.

## User testing
The user testing is based on the user stories from the README.md file.

**I want to play a game...**

1. **..that is fun.**
    - Memory is a classic game that most of us know how to play. The confirmation of getting a matching pair
    makes this game both fun and enjoyable during playing.

2. **..that is easy to navigate through.**
    - Clear instructions on how to start the game with the large play ucon and text right under it.
    - Large buttons with clear text that describes the buttons purposes before clicking them.
    - The design of the icons reflect the meaning behind them.

3. **..that doesn't require compeeting agianst the clock.**
    - The timer function only shows the time that has passed since starting the game.

4. **..that has a nice and clean design.**
    - The page layout has a good balance between the different features to highlight where the major focus
    is going to be, but also doesn't hide other functions to make it hard to find them.
    - Contrast between the text and background and with generous space between the different sections and 
    functions.
    - The color scheme is soft for the eyes to look at, with a minimum of color choises as not to overwhelm the player.

5. **..that doesn't play too loud and stressing audio effects on everything I click.**
    - The sound effects are chosen with the intention of not distracting the player too mutch during playing.
    - The volume is set on the sound effects to not be too loud when playing the game.
    - Sound effects are only added to the main events to the game such as:
        - The card is flipping
        - The card is matching
        - The game is finished
    - The background music is optional to use and can at any time be turned off.

6. **..that I can see what my previous score was.**
    - When replaying the game you can se your previous score in the menu section, right under the timer.

7. **..that I can come back to and play to get my mind off something. With a mindfulness aspect.**
    - This user storie can be referenced with the answears from point number 3-5.

8. **..that I can play to practise my memory skills.**
    - The images used for the memory cards are carefully chosen with a few colors each which makes them easy 
    to interpret and memorize while playing.

9. **..that I can play at night with a darker theme.**
    - With the theme buttons the player can choose what color scheme they want to use when playing the game.
    - The darker theme is more suitable for playing with in darker enviorments because the contrasts are not 
    as strong and thus not as strenuous for the eyes to look at.


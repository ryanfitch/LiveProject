Live Project.  Text-based Horror!
==========================
A text based choose your own adventure game group project.  

### Introduction:
A basic version of this game was originally written in Python by one jr dev team... then another jr dev team took the Python code and rewrote it to operate the same way in JavaScript and jQuery.  My team's mission was to take the existing code and improve on the overall experience of the game by improving the flow of text on the screen, styling the overall appearance to fit the mood of the game, and also add buttons to correspond with the game play story.  

### Technologies Used:
* Programming Languages:  JavaScript, jQuery, HTML5/CSS3
* Framework: Bootstrap
* IDE: SublimeText 2
* Methodologies: Agile/Scrum

### Challenges:
There were many challenges with this project but most of the tasks were straight forward and easy to complete.  The hardest task (which ended up being a huge problem to tackle) was how to take the existing code and add two buttons which could get used over and over again in the story and have them behave properly.  It turns out when you re-use certain event listeners like a button click event, the event listeners can start to pile up causing many things to trigger at once. 

### Solutions:
Dealing with the button behavior in jQuery was an interesting problem to solve.  I tried every every trick in the book I could think of from unbinding and rebinding the element, to turning the listener event off and then back on, to making it a one event listener in hopes that it's current state wouldn't be saved moving from story line to story line.  Unfortunately, none of these fixed the problem.  

I took the problem to a meet up and asked some respected senior developer friends what they recommended.  They all tried to help, experimenting with different ways to handle the click event but nothing was working.  Their advice was to rewrite the code from scratch changing the structure of the game.  This was tempting to do since I knew the code structure wasn't ideal for the way this game was structured, but I was focused on trying everything I could think of to fix these strange behaving buttons before re-writing the code and restructuring everything. 

After I pondered on this button problem for a little while, an usual work-around idea came to mind.  jQuery was stacking event listeners to the same button element... I didn't want to add new buttons to every decision point to the story, but maybe I could trick jQuery to think it was assigning event listeners to different elements instead... so basically, it would refer to an unique instance of the button which corresponded to a certain part of the story.  So I created a bunch of button element class names (over 50 class names!) to correspond with each part of the story.  Luckily, that did the trick and the buttons started to behave as expected.  




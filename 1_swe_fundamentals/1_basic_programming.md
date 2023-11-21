# MODULE ONE: Basic Programming

## Learning Objectives

- [x] Learn to manipulate files and directory structures using the command line.
- [x] Learn to track changes to my code using Git version control.
- [x] Learn to write small programs using Python:
    - [x] Execute Python code in two different ways
    - [x] Make a plan using problem decomposition and experimentation
    - [x] Describe and use variables
    - [x] Describe and use conditionals
    - [x] Describe and use lists
    - [x] Describe and use dictionaries
    - [x] Describe and use loops to go through collections
    - [x] Describe and use methods & functions
    - [x] Describe and use classes
    - [x] Build programs using all of the above!

## Projects

These are my projects for this module (starred projects involved a recorded challenge with coach feedback):
- [Playing With Git](https://github.com/NatalieJClark/playing-with-git)
- [Command Line & Git Challenge](https://github.com/NatalieJClark/cmd_line_git_challenge)  ⭐️ 
    - <a href=#1-command-line--git-challenge>Challenge recording & feedback</a> 👀 
- [Python Foundations](https://github.com/NatalieJClark/python_foundations)  ⭐️
    - <a href="#2-python-fundamentals-chapter-one-challenge">Chapter 1 challenge recording & feedback</a> 👀 
    - <a href="#3-python-fundamentals-chapter-two-challenge">Chapter 2 challenge recording & feedback</a> 👀 

## Challenge Recording & Feedback

#### 1. Command Line & Git Challenge

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1DITpdQXKl4AnW6n3ULGQJYbLm2RoCQ6x)

> #### Feedback from Neil Studd (Makers Coach)
> Hi Natalie, I've reviewed your command line Git challenge from Friday afternoon. First things first, your output (the commits, the files and their contents) was 100% perfect - this already puts you into the upper echelons of people who complete this challenge!

> It was good to see you using techniques to help save you time and avoid typos, including pressing tab to complete file/folder names, and copying/pasting chunks of message text from the curriculum (rather than risk making mistakes by typing them out by hand).

> Your Git usage was also splendid, I was particularly impressed (when doing your first git push) that you remembered there was a much easier way to set the upstream branch than the way that the command line was telling you.

> Your precision for adding multiple files with git add lib/code.rb spec/code_spec.rb was very impressive! It was probably unnecessary in this instance - step 23 specifically said "add everything else", so a simple git add -A (to add all files) would have been enough here. However we often warn people away from using git add -A unnecessarily, as you might end up adding more files than you meant to, so you made a good clean choice here!

> One small note on these submissions - they're not designed to be a test! You're allowed to refer back to your notes at any time; I think you might have been doing this at a couple of points, but I spotted a few points where you said "...I think?" where this should be a prompt to refer back to your notes, rather than guessing. But on every occasion, you thought correctly, so there are no complaints from me here :)


#### 2. Python Fundamentals Chapter One Challenge

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1DITpdQXKl4AnW6n3ULGQJYbLm2RoCQ6x)

> #### Feedback from Neil Studd (Makers Coach)
> Hi Natalie, I've reviewed your Chapter 1 submission. I promise that I'm not kidding when I say that this is one of the best submissions that I've seen for this group - you demonstrated a couple of really key things which others have missed.

> Firstly, you took the time to make your own notes first, to check your own understanding and to work out your inputs/outputs/etc. You created something that's very similar to a "design recipe" - this is a concept which we're going to formally introduce you to in the next module (Golden Square), so you are already thinking in this way!

> Secondly, you ran the pytest tests multiple times, to check the impact of your latest changes. Most people just run them once at the start, and once at the end, but by regularly running them you're able to see whether your code is doing what you expect, and (similar to the drills) see what's still failing. This is a development mindset called Test Driven Development, again we're formally introducing it next week in Golden Square - I can see you're going to be well ahead of the curve here!

> I see what you mean in terms of your code looking "different" to others - your use of if/elif/else was absolutely fine given what you've learned so far. You could have avoided the need for all the elifs by using the "or" keyword to do it all on a single line - i.e. if "!" in password or "@" in password or "$" in password etc. If you watch the Pytest workshop video from yesterday lunchtime (which you definitely should!) then you'll see another approach (which involves storing all of the special characters in a single string or list, and then only needing to check it once) but all of these are examples of refactoring, which we lightly touched upon at the end of chapter 1, but refactoring is the 3rd of the 4 concepts that we teach in the upcoming Golden Square module - so you're already demonstrating 75% of the behaviours that we're hoping to guide people towards next week. This is great to see and you should be really pleased with how your day went yesterday!


#### 3. Python Fundamentals Chapter Two Challenge

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1DITpdQXKl4AnW6n3ULGQJYbLm2RoCQ6x)

> #### Feedback from Eddie Andress (Makers Coach)
> Here's some feedback on your chapter 2 challenge 🙂
> 
> **Headline: nice work!**
>
> *Foundational Points*  
> This is a list of points a that are worthwhile to explore whilst learning the foundations of programming in Python. They're not exhaustive, by any means, but they are a solid foundation upon which you can build deeper comprehension.  
> 🟢 I saw you use built-in Python methods when appropriate (e.g. #any,  #count)  
> 🟢 I saw you make good use of control flow  
> 🟢 I saw you use correct, legal Python syntax
> 
> *Use of Conditionals*  
> 🟢 I saw you use good conditional flow  
> 🟢 I saw you use logical operators to express conditions
> 
> *Code Readability and Accessibility*  
> 🟢 I saw you use consistent and correct indentation
> 🟢 I saw you use descriptive variable names  
> 🟢 I saw you adhere to DRY principals (Don't Repeat Yourself)
> 
> *Debugging*  
> 🟢 I saw you Regularly run tests while coding to check implementation  
> 🟢 I saw you read error messages to identify problems in the code  
> 🟢 I saw you use stacktraces to focus your attention on the source of the error  
:white_circle: I didn't see you use visibility tools like printing or debuggers to discover more about problematic code - BUT I don't you needed to do this.  
> 🟢 I saw you consistently make informed and considered changes to resolve problems
> 
> *Summary*
> Overall I think you did some really nice work here. The planning you did at the start, referring to the Python docs as needed, was great and it meant you were able to implement your solution with little fuss.
>
> A few more specific points...
> - It was great to see you use "any" combined with list comprehension to make a really neat password validation method
> - Seems like you're picking up Python syntax really well
> - I would have liked to see you start by running the tests and then using the first failing test as a guide... but it was great that you did start to use the tests in this way after you had implemented the first method ("add").
> - It was also great that you paused at the end of the challenge to think about whether there was any refactoring to be done.
>
> Great work! :)

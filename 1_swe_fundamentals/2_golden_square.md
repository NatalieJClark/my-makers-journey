# MODULE TWO: Golden Square

## Learning Objectives

- [x] Learn to test-drive programs with multiple classes.
- [x] Learn to break programs up into classes.
- [x] Learn to debug your programs.
- [x] Learn to build software as a pair.
- [x] Learn to explain why test-driving, object-oriented design, debugging, and pairing are powerful practices for software engineers.

## Projects

These are my projects for this module (starred projects involved a recorded challenge with coach feedback):
- [Pytest Practise](https://github.com/NatalieJClark/pytest_practice)
- [TDD and Design of Single Function Programs](https://github.com/NatalieJClark/tdd-and-designing-single-function-programs)  ⭐️ 
    - <a href=#1-design-and-test-drive-a-single-function-to-do-program>Challenge recording & feedback</a> 👀
- [Debugging Single Function Programs](https://github.com/NatalieJClark/debugging-single-function-programs)
- [TDD and Design of Single Class Programs](https://github.com/NatalieJClark/tdd-and-designing-single-class-programs)  ⭐️
    - <a href=#2-design-and-test-drive-a-single-class-music-tracker-program>Challenge recording & feedback</a> 👀  
- [Debugging Single Class Programs](https://github.com/NatalieJClark/debugging-single-class-programs)
- Test driving multi-class programs:
    - [Multi Class Music Library](https://github.com/NatalieJClark/music-library)
    - [Multi Class Diary](https://github.com/NatalieJClark/multi-class-diary)
    - [Multi Class To Do](https://github.com/NatalieJClark/multi-class-to-do)
- Designing multi-class programs:
    - [Multi Class Task Tracker](https://github.com/NatalieJClark/multi-class-task-tracker)  

## Challenge Recording & Feedback

#### 1. Design and Test Drive a Single Function "To Do" Program

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1kB9lD91LWhyiBVawerLoZQ2PWkOe9YA9)

> #### Feedback from Neil Studd (Makers Coach)
> Hi Natalie, I've reviewed your first Golden Square challenge (test driving a TODO method). I was very impressed with your process and your output; there are a lot of notes below, but only because I know that you will welcome the feedback, not because it's intended to be overly critical!
>
> **The really good stuff:**  
> - Your up-front thought and design process (with a small caveat, below!)
> - The way you tightly followed the TDD loop (also with a small caveat, below!)
> - Implementing a test which required exception handling - and remembering how to do it! It would have been very easy to skip that test as "too hard" or "not important", when it's neither of those things :slightly_smiling_face:
> - Stopping to consider refactoring at the end  
> 
> With that in mind, here are some small areas to watch in the future. Note that I would say the majority of people fall into these same traps!
>
> **1. "Simplest possible code"**  
> When you've got a failing TDD test, the idea is to write the simplest possible code which could make that test pass. There were a couple of places where you skipped slightly too far ahead, though it's completely understandable, because you were going directly to the ultimate solution. EG:
> - At 17min in the video - you implemented the exception handling, when you should have just returned an `Exception` for EVERY input. (Your test would pass, and then your next test would illustrate why that wasn't the optimal solution.)
> - At 22min in the video - you implemented your `return "#TODO" in text` check, when you should just have written `return True` . (Your test would pass, and then your next test would illustrate why that wasn't the optional solution.)
> 
> This is a difficult habit to get into, but it'll prove useful when you're working with larger systems, when "just jumping to the correct code" isn't necessarily quick or easy.
>
> **2. Considering your edge cases**  
> When planning, you wrote down `Assume TODO can appear anywhere in the given string` - but then your tests didn't verify this! You had one which checked `#TODO` at the beginning of the string, but nothing with `#TODO` in the middle or end of the string. Given your chosen implementation, these would have just worked anyway, but it's nice to have the tests there, to protect you in the future. (Somebody might come along with a "better" way to do the check, which might only work if the text is at the beginning of the string - it's good to have the tests as a safety net  
>
> It's good that you had `check_todo("")` (with exception handling) but what about a null value - `check_todo(None)` would currently fail with a different exception.  
>
> Finally (and this is really pedantic and only because I'm a tester) - do you only want to return True if it says `#TODO`? At the moment, for instance, `#TODOS` will return True, as will anybody who writes the word `#TODOMONDO` (because they're a big fan of Romania's 2007 Eurovision entry).  
>
> All of this is to say... when you think you've written all the tests you could possibly need, take a pause and consider whether there might be anything else :slightly_smiling_face:


#### 2. Design and Test Drive a Single Class "Music Tracker" Program

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1kB9lD91LWhyiBVawerLoZQ2PWkOe9YA9)

> #### Feedback from Neil Studd (Makers Coach)
> Good morning Natalie!  
> I've reviewed your second Golden Square submission (Music Tracker) and I'm genuinely impressed by what I saw here. This is a calm and confident completion of the exercise, demonstrating both solid coding and process skills. If this were a coding challenge in an interview situation, you'd definitely be through to the next phase!  
> **Things which were really good:**
> - All of your design process, including taking the time to rethink your variable names a few times, so that they felt natural.
> - Remembering the concept of side effects - lots of people forget about this!
> - Considering your edge cases. Though as a tester, I'd always suggest more - I think if you added new test cases for each of these, you might find that they're doing unexpected things right now:
>     - `music_tracker.add(None)`
>     - `music_tracker.add(3)`
>     - `music_tracker.add([""])`
> - Protecting your instance variable - while things are never "truly" private in Python, by doing this you're indicating that you don't intend for the variable to be accessed directly.
> - Yay for remembering "simplest possible code" to pass the first test - `return []`
> I honestly don't have any negatives! I've got a few suggestions for things that you might choose to do differently, for instance if you wanted to revisit later to make enhancements:  
> - At the moment you're just storing track name. If I add "Hallelujah", was I listening to Jeff Buckley, Leona Lewis or Paramore? You might decide that you'd just add this to the string e.g. `add("Paramore - Hallelujah")` but you might alternatively consider storing the data in a more complex format, so that you can capture artist and title.
> - At the moment your `list_listened()` method literally just prints out the raw list. To a typical end user, this might not be very user-friendly - effectively you're exposing them to the internals of the system, when they just want you to print them a nice list back. Could you maybe consider modifying the method (and the tests!) to return something nicer, eg:  
> ```
> You have listened to the following songs:
> Track 1
> Track 2
> Track 3
> ```
> All in all, you deserve a gold star for this one, so here it is -> :star:

# MODULE FOUR: Web Applications

## Learning Objectives

- [x] Explain how HTTP requests and responses work at a high level
- [x] Write integration tests for a web application
- [x] Implement web routes using a lightweight web framework
- [x] Follow a debugging process for a web application

## Projects
These are my projects for this module (starred projects involved a recorded challenge with coach feedback):
- [Hello Web Project](https://github.com/NatalieJClark/hello-web-project/blob/main/README.md) ⭐️
    - <a href=#1-test-driving-routes>Challenge recording</a> 👀
- [Music Web App](https://github.com/NatalieJClark/music-web-app) ⭐️
    - <a href=#2-test-driving-routes-with-databases>Challenge recording & feedback</a> 👀
- [Music Web App HTML](https://github.com/NatalieJClark/music-web-app-html) ⭐️
    - <a href=#3-using-links-to-send-get-requests>Challenge recording & feedback</a> 👀 ◀︎◀︎◀︎  Check out my end of module project! 🚀

## Challenge Recording & Feedback

#### 1. Test Driving Routes

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1djE4r_-FDWtyjFuV9yy0lJefA5QMip8D)

#### 2. Test Driving Routes with Databases

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1djE4r_-FDWtyjFuV9yy0lJefA5QMip8D)

> #### Feedback from Neil Studd (Makers Coach)
> Hi Natalie, I've reviewed your second submission from the Web module (test driving including a database). Really well done on this one - there are a lot of different parts to the challenge, and you excelled at never losing track of what test/code you needed to work on next.
>
> The list of positives is pretty much the same as I always give you!
> - Planning / recipe design
> - Test driven process incl. method names and documentation
> - Remembering where you were in the "stack" during your implementation loop / remembering what you have to do next
> - Reading what the pytest errors tell you
> - Refactoring
>
> Just one tiny thing to note, which I'd observed when you were doing your recipe near the beginning and lifting some SQL code from a previous exercise: you've got some places in your code where your string values are being stored in the database as VARCHAR(255) (which is "text, but limited to 255 characters") and some which are TEXT (which is "text, but with no realistic upper limit") (I think it's actually capped at 1GB). There's no noticeable performance difference in using this, but it means that - for example - the system allows artist names with more than 255 characters. It's simply a design decision to consider, whether you want somebody to be able to have a band name with more than 255 characters. (And on the other hand: if you think you don't need an upper limit, what if somebody were to post a 1,000,000 character band name to your database? would you want that?)
> 
> It's a minor point at this stage though, and I'm almost certainly only highlighting it because my background is in testing and trying to break things :smile:

#### 3. Using Links To Send GET Requests

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1djE4r_-FDWtyjFuV9yy0lJefA5QMip8D)

> #### Feedback from Neil Studd (Makers Coach)
> Morning Natalie! I've just gone through your final challenge submission from the Web module!
> 
> Honestly at this point my feedback must seem repetitive because your process continues to be immaculate, so these are just a few edited highlights:
>
> - When encountering errors (especially unexpected ones), reviewing them for yourself in a web browser to see what was happening
> - You knew what errors you were expecting to see, and you immediately noticed when a different error was occurring (e.g. methhods typo)
> - When you were getting the "resolves to 4 list elements" failure in your Playwright code - you genuinely solved that faster than I would have!
> - Finishing the video by sanity-checking the site again in a browser
>
> I hope you found the Playwright stuff fun - we spend weeks looking at it on the Quality Engineering course, because it gets a lot more complicated than that, especially as the webpage complexity increases.
>
> Semantically I might have done the final test differently, although I appreciate that you were following the albums page example that Kay had done. Your (and Kay's) final test is technically what we call a "scenario test" or a "journey test": you're performing a series of actions to walk through a website in the same way that a user would.
>
> What this means is, technically clicking the Taylor Swift link, waiting for the Taylor Swift page to load, and checking the text on the page is actually unnecessary: you already know that the `/artists/<id>` page renders correctly, because that's what your previous test did. This isn't a problem, but in a test suite for a large application - let's imagine you were doing this 1000 times - these extra page loads can add up to a lot of extra time running the tests.
>
> In case you're curious, here's how I might have done the same test in the Quality Engineering course (though to reiterate, you did exactly what we expected of you!):
``` python
# NB I've skipped the db seed / goto steps
link_text = page.locator("text='Taylor Swift'")
a_tag = link_text.locator("xpath=..") # This means "get the parent element", i.e. it finds the <a> tag
expect(a_tag).to_have_attribute("href", "/artists/3")
```
> You're right, that code is uglier than what you've got! But it will probably run half a second faster, because you don't need to click the link, wait for the server to request the artist data from the database, and render the template. And you can safely do this because your `test_get_artist_with_id` test is already giving you the confidence that the link will work when clicked.
>
> Anyway I definitely got carried away with feedback there, because I saw the opportunity to make a developer into a better tester, which is a chance I'll always take!

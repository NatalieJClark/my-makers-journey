# MODULE THREE: Databases

## Learning Objectives

- [x] Design a database schema with at least two tables from a specification, including a one-to-many relationship between two tables, and create the schema in a database using SQL.
- [x] Use SQL to query a database to read data from one table or resulting of a join, create new records, update and delete.
- [x] Integrate a relational database to a program by test-driving classes which implement CRUD methods to send SQL queries to a database.
- [x] Explain how your program communicates with the database by creating a sequence diagram.

## Projects
These are my projects for this module (starred projects involved a recorded challenge with coach feedback):
- [Book Store Database](https://github.com/NatalieJClark/book-store-database)  ⭐️ 
    - <a href=#1-design-and-test-drive-model-and-repository-classes>Challenge recording & feedback</a> 👀
- Diagramming my Book Store Database Application  ⭐️ 
    - <a href=#2-diagramming-a-database-application>Challenge recording & diagram</a> 👀
- [Student Directory Table](https://github.com/NatalieJClark/student-directory-table)
- [Movies Directory Table](https://github.com/NatalieJClark/movies-directory-table)
- [Recipe Directory Database](https://github.com/NatalieJClark/recipe-directory-database)
- [Student Directory Two Tables](https://github.com/NatalieJClark/student-directory-two-tables)
- [Social Network Database](https://github.com/NatalieJClark/social-network-database)
- [Music Library Database](https://github.com/NatalieJClark/music-library-database) ⭐️  ◀︎◀︎◀︎  Check out my end of module project! 🚀
    - <a href=#3-test-drive-repository-class-methods-to-insert-delete-and-update>Challenge recording & feedback</a> 👀

## Challenge Recording & Feedback

#### 1. Design and Test Drive Model and Repository Classes

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1aRsaxHB6pmVlBQxWwPlbHnwA1DzLdTKO)

> #### Feedback from Neil Studd (Makers Coach)
> Morning Natalie, I've just reviewed your Python submission from yesterday.
> 
> I've got nothing but praise for you here. There were a couple of moments where I thought you might have slipped up (e.g. having your `__repr__` method returning the string in a format which was different to what it said in the challenge) but you caught these yourself - primarily because you are continuing to follow excellent process.
> 
> **Things I especially liked:**
> - EXCELLENT selection of tests, and using them to follow a strict TDD loop
> - Following what Pytest errors are telling you, especially when it's not necessarily obvious, e.g. when you were getting a list of dictionaries back from the db
> - Predicting what you expected to happen when running pytest, i.e. was it going to pass or fail (and getting it right!)
> - Using autocomplete (in terminal and vscode) to reduce unnecessary typing
> - Taking time to consider refactoring at the end

#### 2. Diagramming a Database Application

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1aRsaxHB6pmVlBQxWwPlbHnwA1DzLdTKO)

<img width="1155" alt="image" src="https://github.com/NatalieJClark/my-makers-journey/assets/107806810/3226c025-0ea2-4611-8208-d3701d45409c">

#### 3. Test-drive Repository Class Methods to INSERT, DELETE and UPDATE.

#### [📽️ See challenge recording](https://drive.google.com/drive/folders/1aRsaxHB6pmVlBQxWwPlbHnwA1DzLdTKO)

> #### Feedback from Neil Studd (Makers Coach)
> Hi, here's some feedback on your database create/delete challenge!
>
> Firstly (and this is almost a given at this point) your process is splendid - you're adhering to strict TDD in a way that I wish we could infuse into everybody! Plus you're continuing to write minimal, clean code and check afterwards for refactoring, which is everything that we're hoping for at this stage.
>
> In terms of potential room for improvement, I'd highlight that you only designed the "happy path" for create/delete (i.e. what if everything goes correctly). But there are other situations which you might consider adding tests (and code) for, to help make your code more robust:
> - What if someone tries to delete an album ID which doesn't exist (e.g. .delete(99))? Would you expect it to return an error, or to just silently do nothing? (What does it do at the moment if you try this?)
> - Ditto for validating your .create method, as there are plenty of places where bad data could cause errors - e.g. what if someone tries to create an album where year = "a"?
(I haven't reviewed any other challenge 3s yet, but I can almost guarantee that 95% of others won't have done this either.)
> 
> Finally, to put you out of your misery with breaking a string across multiple lines like that - the way that you indicate this in Python is by using a backslash to say "this string continues on the next line".
```shell
"INSERT INTO albums (title, release_year, artist_id) \
VALUES (%s, %s, %s)"
```
> All in all, excellent again though :trophy:

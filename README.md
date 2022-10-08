W09D03

# **How does the Internet Work?**

First, we start with the front end. The front end is inputed and sends what it is looking for to routing. Routing then tells the back end, what the front end needed. Backend then checks with the database to find what that need was. Then it is sent back to the then front end through routing.

# **What do HTML, CSS, and JavaScript do?**

HTML, CSS, and JavaScript all work together to make a website function properly while looking good. HTML creates the base for the webstie with the text and division of classes and id's. CSS creates the style of the website including colors, placement, and other creative elements. Javascript allows any functionality of a website including working buttons, inputs, or any other user oriented actions.

# **What is the Difference Between Backend and Frontend?**

Frontend is what the user sees or anything a user can interact with. Backend is what the user doesn't see but is necessary to allow the user to do what they want to do or to allow a website to fulfil it's purpose. 


W10D01

# **What do the HTTP Status Codes represent?**

- 100-199 is informational
- 200-299 is successful
- 300-399 is Redirection 
- 400-499 is Client Error
- 500-599 is Server Error

# **What are the Primary HTTP Verbs and what do they mean?**

- Get, requests a specified resource, retrieves data.
- Post, creates a resource on the server.
- Put, replaces a resource with what was requested. 
- Delete, deletes the specified resource. 

W11D01

I found a resource that explains each restful action as one of the seven dwarfs from snow white and it helped me understand each one a little better.
[7 Restful Actions Dwarfs](https://medium.com/@carolineglass89/rails-and-the-seven-restful-routes-838e3e5e85d9)

# **Explain what Index does.**

Index holds all of our existing subjects.

Index is "Doc" because it holds all of the knowledge of all of our disney movies, it's the wise action.

Dwarf example:
``` js
def index
@disney_movies = DisneyMovie.all
render :index
end
```

# **Explain what New does.**

New allows a user to add a new subject but does not add this new subject to the database.

New is "Sleepy" because new only displays a form that allows to add a new disney_movie but doesn't do the hard part of adding to the database, the lazy action.

Dwarf example:
``` js
def new
@disney_movie = DisneyMovie.new
render :new
end
```

# **Explain what Create does.**

Create takes the new subject that added to "New" and adds it to the database while also showing the user the new subject.

Create is "Happy" because create welcomes the new disney movie and happily adds it to the database while also taking the extra step and redirects it to show the user the disney_movie, the nice and helpful action.

Dwarf example:
``` js
def create
@disney_movie = DisneyMovie.create(disney_movie_params)
redirect_to disney_movie_path(@disney_movie)
end
```

# **Explain what Show Routes does.**

Show takes a subject out of an index and puts it on its own page. 

Show is "Sneezy" because the individual movie doesnt want to get lost in the index with the other movies so it asks for a whole page for itself, its the show off action, gets a lot of attention, like a sneeze.

Dwarf example: 
``` js
def show
@disney_movie = DisneyMovie.find(params[:id])
render :show
```

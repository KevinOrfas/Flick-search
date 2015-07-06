#Flickr Service for search and show images based on title and description of the image

The project is organized into small modules. The main.js defines the event handlers for the buttons of the gallery, the links in the pager, and the search.

Each module is defined using an Immediately-Invoked Function Expression, allowing us to create private variables and methods and to avoid polluting the global scope.

###The Utility Module

It defines only two methods: extend and buildUrl.

The extend method is used to merge the properties of two or more objects into one (the first parameter).
The buildUrl method is used to create a valid URL containing a query string, starting from a URL and an object of names and values to use in the query string.

###The Gallery Module

The gallery module defines a Gallery object exposed in the global scope. Its constructor accepts three parameters: the list of the photos (i.e. an array containing the URLs of the photos) belonging to the gallery, the DOM element that will show the image in its natural size and a caption of the photo(hardcoded till further developement). This object defines the ability to show the previous  or next method image, or to create the list of thumbnails.

###The Flickr Module

The Flickr module is the core of our application, because it defines the code that uses the Flickr API.


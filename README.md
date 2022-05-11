# LiveProject Introduction

For the last two weeks in the Tech Academy's Front-End Developer Bootcamp is the Live Project, where other Web Developers and I contributed to a Lifestyle Website, each of us adding in our own sections. The goal was that each section had a particular interest as the focus, mine was the Martial Art of Brazilian Jiu-Jitsu. 

We had to constantly improve the site, making it more responsive, dynamic, and asthetic based on feature requests. It was a good oppurtunity to hone my skills and achieve a specific desired result. There was a varying degrees of difficulty in the requests needed. Making software for others required good testing of features before commiting and working with resources available. It instilled good team developement habits such as having good Version Control, testing constantly, and good clear communication.

It was a good opportunity to drill and refine skills of a good Developer, making software simple, reliable, and efficient.

Technologies involved in the Live Project and to create the site:

- HTML 5
- CSS 3
- JavaScript
- Boostrap 5
- Azure Dev Ops
- Git
- Axios - JS Library

Below is some examples of features implemented.

## Stories
- [Responsive Site (Mobile-Friendly)](#responsive-site-mobile-friendly)
- [Pop-Up Contact Form](#pop-up-contact-form)
- [Dark Mode](#dark-mode)
- [Connecting an API](#open-movie-database-api)

## Responsive Site (Mobile-Friendly)

This was achieved using Bootstrap 5. Designing the site around Bootstraps Grid system made having a responsive site much easier from the start. It was a good lesson in development, which is to set-up a good base early on, as this was something I implemented later in the project.

![Responsive Site - The Gentle Art ](https://user-images.githubusercontent.com/98543446/164914903-bcd058eb-0c7d-4662-90eb-f24bdbd78f95.gif)



## Pop-Up Contact Form

This was also achieved using Bootstap 5. Each field was required except for the messages section. The form works and is connected via Formspree.io to an email.


### Form Validation

![Dynamic Form](https://user-images.githubusercontent.com/98543446/164915169-28feaf14-e664-484b-8167-45dc083ce69d.gif)



### Form Access
The form can be accessed from two places, the Nav Bar or the Contact Button below. This design made for an improved user experience.

![Contact Button](https://user-images.githubusercontent.com/98543446/164915682-80d4b395-7751-45ae-be50-735d33046372.gif)


## Animation

This animation was made using CSS rule @keyframes. 

![The Gentle Art - Animation](https://user-images.githubusercontent.com/98543446/166086462-6c6b0fd8-8480-4561-88f4-2cea6c9dadf9.gif)


## Dark Mode

This was done using HTML and JavaScript. It required a good understanding of bootstrap classes and targeting elements. I had to target individual elements and style each accordingly. End result was  a button which gives the site a dark mode and light mode. 

![The Gentle Art - Dark Mode (7)](https://user-images.githubusercontent.com/98543446/166086849-74320d97-bc28-41e7-aad7-cf820d94600d.gif)


## Open Movie Database API

This was done primarily with JS and Axios a JS Library, used to make HTTP Requests. It was a good challenge in that I had to first retrive user input, which required use of class, events handlers and an array. 
```
/* Getting User Input*/

  /* Creates an array from elements with class name */
  var movies = document.getElementsByClassName("movies");

  /* Goes through array assigning 'click' event to each element, and function to run when clicked. */
  for (i = 0; i < movies.length; i++) {
    movies[i].addEventListener('click', movieChoice);
  }

```
The user click, triggered a funciton which sent a request Axios to the API, along with the user input.

```
/* Request/Response with Axios - JS Library, used to make HTTP Requests */
    axios.request(options)
      /*'.then' runs function when response a success */
      .then(function(response){
      /* Variable to store 'data' portion of response*/
      var moviedata = response.data;
      /* Call function that will input information into webpage */
      inputFunction(moviedata);
      })
      /*'.catch' runs function when response a failure/error */
      .catch(function(error) {
        console.error(error);
      });

```
Following the documentation I then retrieved the film info and outputted desired fields into a 'response' card on the webpage. It is hidden by default but appears when there is a response from the API.
```
  /* Displays response into Webpage */
      function inputFunction(moviedata) {
        document.getElementById("display-response").classList.remove("visually-hidden");
        document.getElementById("title").innerHTML = moviedata.Title;
        document.getElementById("plot").innerHTML = "<h6> Plot: </h6>" + moviedata.Plot;
        document.getElementById("director").innerHTML = "<h6> Directed by: </h6>" + moviedata.Director;
        document.getElementById("release-date").innerHTML = "<h6> Released: </h6>" + moviedata.Released;
        document.getElementById("actors").innerHTML = "<h6> Starring: </h6>"  + moviedata.Actors;
        document.getElementById("poster").setAttribute("src", moviedata.Poster);    
      }
  }
```

Resulting in a fully dynamic card as a response below the movie selection, which fills dynamically with movie info. 

![The Gentle Art - API](https://user-images.githubusercontent.com/98543446/166086922-0cb17718-b952-4d48-8bb7-13fed2f52813.gif)





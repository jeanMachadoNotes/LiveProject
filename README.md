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

Below is some examples of features implemented.

## Stories
- [Responsive Site (Mobile-Friendly)](#responsive-site-mobile-friendly)
- [Pop-Up Contact Form](#pop-up-contact-form)

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


```
<!-- Button to Open the Modal -->
        
          <div class="container-fluid mb-5 p-3 bg-light ">
            <div class="row">
              <div class="col">
                <p id="Contact" class="text-center fs-2 mb-4">Find out how to get signed-up and started!</p>
              </div>
            </div>
            <div class="row">
              <div class="col m-3 mb-4">
                <button type="button" class="btn btn-primary position-absolute start-50 translate-middle px-4 py-2 fs-4" data-bs-toggle="modal" data-bs-target="#myModal">
                  Contact Us
                </button>
              </div>
            </div>
          </div>


          

          <!-- The Modal -->
          <div class="modal " id="myModal">
            <div class="modal-dialog">
              <div class="modal-content">

                <!-- Modal Header -->
                <div class="modal-header">
                  <h4 class="modal-title">Contact Form</h4>
                  <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
                </div>

                <!--Modal body -->
                <div class="modal-body">

                  <form action="https://formspree.io/f/xpzbygdq" method="POST">
                      <div class="mb-3">
                        <label for="firstname" class="form-label">First Name</label>
                        <input type="text" class="form-control" id="firstname" aria-describedby="firstnameinfo" name="First Name" required>
                      </div>
                      <div class="mb-3">
                        <label for="lastname" class="form-label">Last Name</label>
                        <input type="text" class="form-control" id="lastname" aria-describedby="lastnameinfo" name="Last Name" required>
                      </div>
                      <div class="mb-3">
                        <label for="exampleInputEmail1" class="form-label">Email address</label>
                        <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" name="Email" required>
                        <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
                      </div>
                      <div class="mb-3">
                        <label for="message" class="form-label">Message</label>
                        <textarea class="form-control" aria-label="message" placeholder="Your message, question..." name="Message"></textarea>
                      </div>
                      <div class="mb-3 form-check">
                        <input type="checkbox" class="form-check-input" id="exampleCheck1" required>
                        <label class="form-check-label" for="exampleCheck1">I am not a robot</label>
                      </div>
                    <button type="submit" class="btn btn-primary">Submit</button>
                    <button type="button" class="btn btn-danger" data-bs-dismiss="modal">Close</button>
                    </form>
                </div>  
              </div>
            </div>
          </div>
```








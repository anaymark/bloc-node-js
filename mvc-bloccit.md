# For each question below, answer which part of MCV should be responsible for it:

* model-brain of the app, data related logic, interaction with database(CRUD), communicates with controller, in some frameworks updates the view directly. 

*view-the end user UI and usually consists of HTML/CSS. Communicates with controller and can be passed dynamic values from the controller. Can be as simple as barebones of HTML/CSS or dynamic JS.

* controller-gets data from model and passes data to the view, process requests(GET, POST, PUT, DELETE). 

## A method that pulls the last 10 topics.

* The controller interacts with the model by sending a get requests for the database queries. Thus, the controller is responsible for pulling the last 10 topics by initiating the model to read from the database and return the data to the controller to be sent and displayed by the view to the browser and the end user. 

## A representation of the upvotes on a post.

* The representation of upvotes is stored in the database and retrieved through the controller and model, but the actual viewed representation is displayed by the view layer of the application to the browser.

## Logic that parses params coming from the client.

* The view layer is responsible for receiving user interaction from the client and passing this to the model through some kind of routing in the controller. The model is the layer that parses the params and will have the logic to respond to the client requests. 


# Write a user story with acceptance criteria for a feature that involves moderating content on Bloccit.

# As a user, I want to be able to report an inappropriate post on a given topic, so I can prevent abusive/offensive/racist content that is defined by the sites user agreement.

Acceptance criteria:

* While logged in and visiting a posts page for topics and a posts page within a topic, I see a link to report a post which leads to have an administrator approve the blacklisting of a post based on site criteria.



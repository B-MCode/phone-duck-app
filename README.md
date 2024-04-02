'

# phone-duck-app
School Project in teams of two

# tools : 
JWT, Express, Nodemon, Mongo DB, Node.js, Socket



The assignment description (Optional reading, technical requirements below)
The subsidiary Phone Duck inc. to the company Budget Ducklings, which handles the development of new software for people who have encountered unwanted situations in traffic, recently heard about a moose migration that had stopped travelers past Hudiksvall.

Gertrude, a traveler stuck in traffic, who is a big fan of chat applications submitted a proposal to Phone Duck inc. which meant that vulnerable people in local traffic could connect to different chat channels based on interest. The idea was that there is a main channel that sends out emergency stoppage messages, and another channel that advertises new channels that users have created to amuse themselves while waiting for traffic to clear.

Demarcation
This is a backend course and does not require a functioning frontend application. At the beginning of the course, you had the opportunity to think about what it would look like, which can facilitate the testing of the application. If the backend can be run according to the requirements only with thunderclient, postman or similar tools, the task is approved.

In the case of higher ratings, sockets are expected to be used. However, it should also be emphasized here that there is not expected to be a finished frontend to illustrate the socket solutions in a finished product, but rather as shorter script solutions in javascript that illustrate data communication between socket and server.

Technical requirements
Students develop a backend service that can store information about chats and chat channels as described below. Note that the data is expected to be stored in a database but that this does not need to be reported in the video recording.

Terminology
Advertised channels refer to channels previously sent out via a PUT request and are available via the channel api, see details below. Each advertised channel must have a theme set by the creator of the channel.

Emergency channel refers to a unique (only one) channel that is created at startup and holds all emergency messages sent.

Endpoints
The backend must contain at least the following working endpoints. Each endpoint is described as "[http method] - url <-- expected result when called".

[GET] - http://address:port/ducks/api/channel/ <-- retrieves a list of advertised channels. See VG criteria for requirements for a higher rating.

[GET] - http://adress:port/ducks/api/channel/:id <-- retrieves the content of an identified channel that has been previously advertised, this refers to messages that have been sent in the channel. See VG criteria for requirements for a higher rating.

[PUT] - http://address:port/ducks/api/channel/ <-- creates a new channel. Theme (header) of the channel must be sent as part of the http body, preferably as part of a json object.

[POST] - http://address:port/ducks/api/channel/:id <-- sends out a new message to an identified channel that has been previously advertised. The content of a message should be at least sender and content.

[DELETE] - http://address:port/ducks/api/channel/:id <-- deletes an identified channel previously advertised. See the VG reviews for requirements for a higher rating.

[GET] - http://adress:port/ducks/api/broadcast/ <-- retrieves a list of all events that have been broadcast, e.g. elk migration, traffic accidents, etc. See VG criteria for requirements for a higher rating.

[POST] - http://address:port/ducks/api/broadcast/ <-- creates a new emergency event. This call should require a valid JWT token.


# JsServerlessGame-PoC
This repo serves as a **Proof of Concept** for a multiplayer game using [PeerJS](https://peerjs.com) and [Github Pages](https://pages.github.com).

To try the game out you can do so [here](https://carlosganhao.github.io/JsServerlessGame-PoC/)

### The Concept
The idea is very simple, in order to make a serveless peer to peer multiplayer game, we use [PeerJS](https://peerjs.com) to brokerage the Peer connections, keeping all the connection logic client-side. Then using [Github Pages](https://pages.github.com) we host the static html page, and since all the connections reside in client-side javascript, we can make games or other apps, mostly for free.

### The Concrete Implementation
In this repo we made a very basic version of Rock, Paper, Scissors, using the previously mentioned tools and API's, and also using [JQuery](https://jquery.com) to speed up development.

What happens in the code is very simple, we have a text saying what is our ID, this id is provided to us by the PeerJS servers, then we have an input field to put another Peer's ID into. Then we connect both Peers and each time one of the play buttons gets clicked, a message is sent to the other player with information about what was played, and once both have played, we check both plays and determine who won and who lost.

### Shortcommings
One of the most obvious downsides to this implementation is that a little knowledge of javascript could lead to the game becoming rigged, since the player can read what is being played by the other player and play accordingly. 

It needs to be seen how this could be fixed but some ideas are obfuscating the code and maybe encrypting the messages coming in and out.

### Future Work
It is definitely possible to implement more complex games with this concept, but something worth looking into is if it is possible to use front-end API's and frameworks that render to native HTML to ease development of such a project, and also to make said project look better and more responsive.

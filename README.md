# CS230-OperatingPlatforms

Project Summary

The Gaming Room is a game development company that wanted to expand their existing Android game, Draw It or Lose It, into a web-based, multi-platform application. The software needed to support multiple teams and players within a single game session, enforce unique naming for games and teams, ensure only one game instance ran in memory at a time, and deliver a consistent experience across Windows, Mac, Linux, and mobile operating systems. The design document I produced outlined the system architecture, platform evaluation, domain model, and development environment recommendations to guide both the client and the development team through the build.


Reflection

What did you do particularly well in developing this documentation?

The domain model and class diagram were the strongest parts of the document. I clearly mapped the relationships between the Game, Team, and Player entities and articulated how the Singleton pattern would prevent multiple game instances from running simultaneously. That section gave the development team a concrete, unambiguous starting point rather than leaving architecture decisions to interpretation during implementation.

What about the process of working through a design document did you find helpful when developing the code?

Working through the design document before writing any code forced early decisions about structure. Defining the class hierarchy on paper first meant that when I moved into the Java implementation, the relationships between Game, Team, and Player were already settled. That eliminated a category of confusion that often surfaces mid-development, where you realize two components have responsibilities that conflict or overlap in ways that are expensive to untangle.

If you could choose one part of your work on these documents to revise, what would you pick? How would you improve it?

I would revise the platform comparison section. While it covered the major operating systems and evaluated server-side options adequately, the mobile considerations were thinner than they should have been given that the client's original product was an Android app. A stronger revision would include a more detailed breakdown of cross-platform development frameworks and a clearer recommendation for how the mobile client should interface with the server layer.

How did you interpret the user's needs and implement them into your software design? Why is it so important to consider the user's needs when designing?

The client's core needs came down to scalability, uniqueness enforcement, and platform reach. I translated those into specific technical constraints: the Singleton pattern addressed the single-instance requirement, an iterator pattern supported traversal of game and team collections without exposing internal structure, and the recommendation for a RESTful server architecture addressed cross-platform delivery. Centering user needs matters because a technically elegant system that misses what the client actually requires delivers no real value. Design decisions made without grounding in user needs tend to optimize for the wrong things.

How did you approach designing software? What techniques or strategies would you use in the future to analyze and design a similar software application?

I started by identifying the functional and nonfunctional requirements separately, then moved into domain modeling before touching any implementation detail. In the future I would continue using that sequence and add more structured stakeholder questioning earlier in the process. Getting explicit sign-off on requirements before producing the design document would reduce the chance of building detailed documentation around assumptions that the client would later revise. I would also incorporate iterative feedback checkpoints rather than treating the design document as a single deliverable.


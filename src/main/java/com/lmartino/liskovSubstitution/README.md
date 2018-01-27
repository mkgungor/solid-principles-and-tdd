### Liskov Substitution Principle (Subtyping and inheritance)
![alt text](https://lostechies.com/derickbailey/files/2011/03/LiskovSubtitutionPrinciple_52BB5162.jpg)

Functions that use references to base classes must be able to use objects of derived classes without knowing it
Child classes should never break the parent class type definitions. It's in strong relation with Open Closed Principle.
In fact a violation of LSP is a latent violation of OCP.
In other words, a subclass should override the parent class methods in a way that does not break 
functionality from a client's point of view.

*Real World situation:* If you cook youserlf a stew, you'd only put things in there that were edible
because you want to eat the stew without asking yourself anytime 'is this edible'.
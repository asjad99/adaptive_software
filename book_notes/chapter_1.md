### Background - About the book 



- books is about  decisions about the program design process (provides wisdom on Avoid Programming Yourself into a Corner)

- specifically it address additive programming which is about program organization strategies that maintain flexibility. 

- it investigates the construction of computational systems so that they can be easily adapted to changing requirements. in simple terms we learn, how to add functionality to an existing program without breaking it.

- Idea (unclear):  *there are advantages to being able to treat code as data, to treat data as code, and to bundle smallish amounts of code and related data together rather than organizing code and data separately as monolithic chunks. The most flexible kind of data is a record structure that can contain not only “primitive data items” such as numbers and characters but also references to executable code, such as a function. The most powerful kind of code constructs other code that has been bundled with just the right amount of curated data; such a bundle is not just a “function pointer” but a closure (in a functional language) or an object (in an object-oriented language).*

- ideas about generic functions, treating data as code, functions returning functions are intriguing. 

  

### Chapter 1 

- systems typically cannot evolve gracefully to cater for revised problem definitions. i.e be robust in the face of changes in requirements.
- PO: examples of internet and cities are bad? 
- Assumptions made during the design and construction of a program may reduce the possible future extensions of the program. **make just-in-time decisions based on the environment that the program is running in**
- Seperation of concerns: the parts that we combine to make a system must sharply separate concerns. i.e individual pieces combine with minimal unintended interactions.
- Keep them simple and make em <u>general</u>. General pertains to the kind of inputs/outputs the system accepts Example a part that accepts a wider range of inputs than is strictly necessary for the problem at hand will have a wider applicability than one that doesn't. outputs on the other hand should be small and well defined.  (Postel's law” in honor of Internet pioneer Jon Postel)
- The principal cost of software is the time spent by programmers over the lifetime of the product, including maintenance and adaptations that are needed for changing requirements. Designs that minimize rewriting and refactoring reduce the overall costs to the incremental additions rather than complete rewrites. In other words, long-term costs are additive rather than multiplicative.



**Architecture of computation**

- *parti*: an organizing principle for the design. The *parti* is usually a sketch of the geometric arrangement of parts. The *parti* may also embody abstract ideas, such as the division into “served spaces” and “servant spaces,
- At small scale the *parti* may be an abstract algorithm and data-structure description. <u>In larger systems it is an abstract composition of phases and parallel branches of a computation. In even larger systems it is an allocation of capabilities to logical (or even physical) locales.</u> 
- <u>The architectural *parti* should be sufficiently complete to allow the creation of models that can be used for analysis and criticism. The skeleton plan of a program should be adequate for analysis and criticism, but it should also be executable, for experiment and for debugging. Just as an architect must fill in the *parti* to realize the structure being designed, a programmer must elaborate the plan to realize the computational system required.</u>



**Smart parts for flexibility**

- A central problem in system engineering is the establishment of interfaces that allow the interconnection of components so that the functions of those components can be combined to build compound functions.
- a priori specification become progressively more difficult as the complexity of the system increases. 
- Our software systems are built with large numbers of custom-made highly specialized parts. The difficulty of specifying software components is <u>exacerbated by the individualized nature of the components.</u>
- Takes example of biology which constructs systems of enormous complexity without very large specifications, where every cell is a decedent of single zygote with same genetic endowment. 
- and conclude: **If our software components were simpler or more general they would have simpler specifications.** If the components were able to **adapt themselves to their surroundings**, the precision of their specification would be less important.
- Traditionally, software systems are built around an imperative model, in which there is a hierarchy of control built into the structure. The individual pieces are assumed to be dumb actors that do what they are told. This makes adaptation very difficult, since all changes must be reflected in the entire control structure. In social systems, we are well aware of the problems with strict power structures and centralized command. But our software follows this flawed model. We can do better: making the parts smarter and individually responsible streamlines adaptation, since only those parts directly affected by a change need to respond. 



**Body plans**

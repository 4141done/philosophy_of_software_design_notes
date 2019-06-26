
# A Philosophy of Software Design
Notes on A Philosophy of Software Design by John Ousterhout

## Chapther 2: The Nature of Complexity
  > Complexity is anything related to the structure of a software system that makes it hard to understand and modify the system.
### Symptoms of Complexity
#### Change amplification
 A seemingly simple change requires code changes in multiple places
#### Cognitive load
 How much a developer needs to know in order to complete a certain task
> Sometimes an approach that requires more lines of code is actually simpler because it reduces cognitive load
#### Unknown unknowns
What code needs to be modified, and what knowledge is required to do the modification is unknowable.
### Causes of complexity
#### dependencies
A given piece of code that cannot be understood or modified in isolation
#### obscurity
Important information is not obvious. IE a variable name that is too generic or a storing units in a variable without making it clear what the units are.
### Complexity is incremental
> Complexity comes about because hundreds or thousands of small dependencies and obscurities build up over time.
### My Thoughts
This information jives with my experience in working on very new and very old codebases as well as working with teams and solo.  The very old codebases seemed to be slow or difficult to modify but it was hard to put your finger on why.  This supports the "many small lapses" statement at the end of this chapter.

With newer codebases or in companies with stricter gating on the types of fixes/changers that are allowed I noticed this feeling less even on older codebases.

Likewise I have worked solo on codebases written entirely by me and felt great even though looking back at some of that code it didn't fit the definition of "clean and simple".  It had low cognitive load because I had the entire system in my head along with all the dependencies.  Likewise there was no obscurity because I knew exactly what I meant with most of what I did.  I would bet that if I revisted that code now with several years elapsed I would have a much more difficult time working with it as I would have lost all that knowledge.

## Chapter 3: Working Code Isn't Enough (Strategic vs. Tactical Programming)
### Tactical Programming
The main focus is to get the thing working.  It makes it easy to tell yourself that it's ok to add that bit of complexity because you'll be able to finish.
> This is how systems get complicated.
#### The tactical tornado developer
Tactical to the extreme, gets a lot done, but often leaves behind systems that are very hard to work with/understand.  Often well recognized by business.
### Strategic Programming
> Working code isn't enough.  Most code is written by extending existing code, so your most important job as a developer is to facilitate those future extensions.
### How much to invest?
10-20% more ish.  You'll make up the lost time in continued productivity
### My thoughts
I've seen this play out.  I've seen the tactical tornado and I have also seen the difference in codebases where companies really encouraged a tactical approach when some did not.

Especially as a manager of a lead developer it's very easy to convince yourself to make those tradeoffs because you're experiencing the organizational pressure firsthand.  In those roles it should be one of your primary focuses to resist that.

Of course you want to have a balance and being overly strategic can lead to overengineered codebases.  The author's general suggestion of 10-20% more care up front suggests the need for that balance.

## Chapter 4: Modules Should Be Deep

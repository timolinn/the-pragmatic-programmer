# The Pragmatic Engineer

- [The Pragmatic Engineer](#the-pragmatic-engineer)
  - [Chapter 1 - The Pragmatic Philosophy](#chapter-1---the-pragmatic-philosophy)
  - [Chapter 2 - A Pragmatic Approach](#chapter-2---a-pragmatic-approach)
    - [The Essence of Good Design](#the-essence-of-good-design)
    - [Orthogonality](#orthogonality)
    - [Reversibility](#reversibility)
    - [Tracer Bullets](#tracer-bullets)
    - [Prototypes](#prototypes)
    - [Domain Language](#domain-language)
    - [Estimating](#estimating)
  - [Chapter 3 - The Basic Tools](#chapter-3---the-basic-tools)
    - [Psychology of Debugging](#psychology-of-debugging)
  - [Chapter 4 - Pragmatic Paranoia](#chapter-4---pragmatic-paranoia)
  - [Chapter 5 - Bend, or Break](#chapter-5---bend-or-break)
    - [Decoupling](#decoupling)
    - [Juggling the real world](#juggling-the-real-world)
    - [Transforming Programming](#transforming-programming)
    - [Inheritance Tax](#inheritance-tax)
  - [Chapter 6 - Concurrency](#chapter-6---concurrency)
  - [Chapter 7 - While you are coding](#chapter-7---while-you-are-coding)
    - [Password Anti patterns](#password-anti-patterns)
    - [Naming things](#naming-things)

## Chapter 1 - The Pragmatic Philosophy

What distinguishes Pragmatic Programmers? We feel it’s an attitude, a style, a philosophy of approaching problems and their solutions. They think beyond the immediate problem, placing it in its larger context and seeking out the bigger picture. After all, without this larger context, how can you be pragmatic? How can you make intelligent compromises and informed decisions?

- We can be proud of our abilities, but we must own up to our shortcomings—our ignorance and our mistakes
- Don't be afraid to admit ignorance or error or mistakes. Try to offer solutions
- Provide Options, Don’t Make Lame Excuses
- Think! About Your Work. Constantly be thinking, critiquing your work in real time
- Care About Your Craft
- When you find yourself saying, “I don’t know,” be sure to follow it up with “—but I’ll find out.”
- Don’t leave “broken windows’’ (bad designs, wrong decisions, or poor code) unrepaired. Fix each one as soon as it is discovered. If there is insufficient time to fix it properly, then board it up. Neglect accelerates software rot faster than any other factor.
- Like the soldiers in [The Stone Soup Story](https://en.wikipedia.org/wiki/Stone_Soup), be a catalyst for change. However, be as objective as you can be when you try to catalyze a change.
- Constantly review what’s happening around you, not just what you personally are doing. Remember the big picture.
- Let your users and stakeholders participate in deciding what is good enough software. Great software today is often preferable to the fantasy of perfect software tomorrow. If you give your users something to play with early, their feedback will often lead you to a better eventual solution.
- Don’t spoil a perfectly good program by overembellishment and overrefinement. Move on, and let your code stand in its own right for a while. It may not be perfect. Don’t worry: it could never be perfect.

> An investment in knowledge always pays the best interest - Benjamin Franklin

- Your knowledge and experience are your most important day-to-day professional assets. Unfortunately, they’re expiring assets
- Your ability to learn new things is your most important strategic asset
- Your knowledge portfolio is all the facts you know in computing, the application domain you work in, and all your experience.
- Building Your Knowledge Portfolio:
  - Invest regularly - Just as in financial investing, you must invest in your knowledge portfolio regularly, even if it’s just a small amount.
  - Diversify - The more different things you know, the more valuable you are. As a baseline, you need to know the ins and outs of the particular technology you are working with currently. But don’t stop there. And don't forget the non-technical areas.
  - Manage risk - Technology exists along a spectrum from risky, potentially high-reward to low-risk, low-reward standards. Don’t put all your technical eggs in one basket.
  - Buy low, sell high - Learning an emerging technology before it becomes popular can be just as hard as finding an undervalued stock, but the payoff can be just as rewarding
  - Review and rebalance - This is a very dynamic industry. That hot technology you started investigating last month might be stone cold by now.

    > The most important of all is - __Invest Regularly in Your Knowledge Portfolio__

- Some suggestions on how to go about acquiring knowledge
  - Learn a new language each year
  - Read a technical book each month
  - Read non-technical books too
  - Take classes - online or offline
  - Participate in local user groups and meetups - be active in these groups
  - Experiment with different environments - Windows, Linux, vim etc.
  - Stay current by reading news and posts online on different technology

- When someone asks you something you have no idea what it is, take it as a challenge, don't rest until you find the answer.
- Time spent waiting for doctors and dentists can be a great opportunity to catch up on your reading - but be sure to bring your own e-reader with you, or you might find yourself thumbing through a dog eared 1973 article about Papua New Guinea
- Critically Analyze What You Read and Hear. Beware of zealots who insists there dogma is the only way to go. Beware of commercialism, the first hit from your web search is not necessarily the best result, someone could have paid to put it there.

> A good idea is an orphan without effective communication.

- Know your Audience
- You’re communicating only if you’re conveying what you mean to convey—just talking isn’t enough. To do that, you need to understand the needs, interests, and capabilities of your audience.
- Plan what you want to say. Write an outline. Refine it until it communicates exactly what you want to say to your audience
- Be a listener, encourage people to talk by asking questions.
- Get back to people. do your best to respond to emails, voicemails, chats etc. "I'll get back to you later" can buy you sometime if you need it.

> It is both what you say and The way you say it.

- Pragmatic programmers embrace documentation. Keep documentation as close as possible--in the code itself.
- It is easy to produce good documentation from comments in source code.

> It is recommended to add comments to modules and exported functions.

- Add comments to capture engineering trade-offs, why decisions were made, other alternatives that were discarded, etc.

## Chapter 2 - A Pragmatic Approach

### The Essence of Good Design

- Good design is easier to change than bad design.
- A thing is well designed if it adapts to people who use it.
- In code, adapting means changing; So apply the ETC principle; __EASIER TO CHANGE__. This is not a rule but a simple guide.
- internalizing good engineering principles takes time and practice, be patient make notes about current situations and decisions then give yourself feedback when the code changes.
- `DRY` is not just about code - code is a tiny part - `DRY` is more about avoiding duplication of __Knowledge and Intent__.
- Not all code duplication is knowledge duplication
- Inter-developer duplication is the hardest to discover or fix eg. same functionality written in different places by different developer. The best way to deal with this is to encourage frequent communication between developers.
- Foster an environment where it’s easier to find and reuse existing stuff than to write it yourself. If it isn’t easy, people won’t do it.
- Make a point of reading other peoples code and documentation, formally or informally-- you're learning from them.

### Orthogonality

- Commonly known as decoupling/modular/layered systems by developers.
- Two or more things are orthogonal if changes in one do not affect any of the others.
- Design components that are self-contained: independent, and with a single well-defined purpose are said to be orthogonal.
- Orthogonality increases productivity by guaranteeing changes are localized, and so development time and testing time are reduced. It also promotes reuse.
- Look for opportunities to improve your code structurally or to make it more orthogonal. This process is called __Refactoring__
- Eliminate Effects Between Unrelated Things
- Every time you write code you run the risk of reducing the orthogonality of your application. Unless you constantly monitor not just what you are doing but also the larger context of the application, you might unintentionally duplicate functionality in some other module, or express existing knowledge twice.
- To maintain orthogonality, write shy code -- modules that don't reveal anything unnecessary to other modules and don't rely on other modules implementations.
- Avoid global data.
- Duplicate code is a symptom of structural problem.
- Get into the habit of being constantly critical of your code.
- An orthogonally designed and implemented system is easier to test.
- Look for opportunities to improve your code structurally or to make it more orthogonal. This process is called __Refactoring__
- In summary, Orthogonality is reducing the interdependency among a system's components.

### Reversibility

> Nothing is more dangerous than an idea if it’s the only one you have.
> ➤ Emil-Auguste Chartier (Alain), Propos sur la religion, 1938

- There are no final decisions. Critical decisions can be irreversible or at great expense. eg. Vendor lock in for a database
- Technology have evolved over the years, web today is not same web as we used to know it years ago. Investing in flexible architecture for testing, deployment, vendor integration is crucial to tackle the volatility of technologies today.
- Forgo Following Fads

### Tracer Bullets

- Tracer bullets are loaded at intervals alongside regular ammunition. When they’re fired, their phosphorus ignites and leaves a pyrotechnic trail from the gun to whatever they hit. If the tracers are hitting the target, then so are the regular bullets. Soldiers use these tracer rounds to refine their aim: it’s pragmatic, real-time feedback under actual conditions. That same principle applies to projects, particularly when you’re building something that hasn’t been built before
- Like a PoC but non-disposable. The goal is connect the components end-to-end to get a feedback on where we are with the target.
- In the face of vague requirements, large number of unknowns the classic response is to specify the system to death. One big calculation up front, then shoot and hope. Pragmatic programmers prefer the tracer bullet approach.
- Look for the important requirements, the ones that define the system. Look for the areas where you have doubts, and where you see the biggest risks. Then prioritize your development so that these are the first areas you code.
- Tracer code is not disposable: you write it for keeps. It contains all the error checking, structuring, documentation, and self-checking that any piece of production code has. It simply is not fully functional
- Pros
  - Users get to see something working early
  - Developers build a structure to work in
  - You have an integration platform
  - You have something to demonstrate
  - You have a better feel for progress
- Prototyping generates disposable code. Tracer code is lean but complete, and forms part of the skeleton of the final system. Think of prototyping as the reconnaissance and intelligence gathering that
- In summary Tracer code is a lean way to develop a system by starting very small, and evolving towards the target iteratively.

### Prototypes

- Prototyping is a learning experience. Its value lies not in the code produced, but in the lessons learned. That’s really the point of prototyping.
- Anything that carries risk. Anything that hasn’t been tried before, or that is absolutely critical to the final system
- When building a prototype ignore: correctness (use dummy data), robustness (skip unimportant error checking), completeness, and style.
- Prototypes gloss over details, and focus in on specific aspects of the system being considered, so you may want to implement them using a high-level scripting language
- Here are some -specific areas you may want to look for in the architectural prototype:
  • Are the responsibilities of the major areas well defined and appropriate?
  • Are the collaborations between major components well defined?
  • Is coupling minimized?
  • Can you identify potential sources of duplication?
  • Are interface definitions and constraints acceptable?
  • Does every module have an access path to the data it needs during execution? Does it have that access when it needs it?
- Before you embark on any code-based prototyping, make sure that everyone understands that you are writing disposable code.

### Domain Language

- Pragmatic Programmers go to the next level by also using vocabulary, syntax, semantics of the domain to write a program and not just the programming language. eg. RSpec, Ansible, Phoenix

### Estimating

- By learning to estimate, and by developing this skill to the point where you have an intuitive feel for the magnitudes of things, you will be able to show an apparent magical ability to determine the feasibility of a project
- The context of which the estimate is asked is important. Are they looking a highly accurate time or just a ballpark figure?
- Look for someone that has done it in the past and draw from their experience. It must not be exact, something similar is already helpful
- Build a rough-and-ready mental model. You may find that making a variant of the solution will be more beneficial and take shorter time
- Break the model into components, describe how they interact. You will find how each component contribute to the overall model. Simply identify parameters
- Assign each parameter a value and workout which ones have the most impact on the result and concentrate on getting them about right.
- Calculate your answer. Keep track of it to see how close or off you were when the project delivered.
- When an estimate turns out wrong, don’t just shrug and walk away—find out why
- Give a range a values not a single answer
- Estimate the project on iteration basis, refinement at the end of each iteration will determine the number of iterations, what can be included in each iteration.
- Estimates given at the coffee machine will (like the coffee) come back to haunt you.

## Chapter 3 - The Basic Tools

- Tools amplify your talent. The better your tools, and the better you know how to use them, the more productive you can be. Start with a basic set of generally applicable tools.
- Don't make the mistake of choosing a single power tool and staying in the comfort of it's cozy interface. Keep the basic tool set sharp and ready to use.
- Spend time mastering your tools, you’ll be surprised to discover your fingers moving over the keyboard, manipulating text without conscious thought.
- As Pragmatic Programmers, our base material isn’t wood or iron, it’s knowledge.
- The best way to store knowledge is plain text. HTTP, SMTP, IMAP are all plain text based. Meaningful plain text is self describing. Think Unix Philosophy
- Every woodworker needs a good, solid, reliable workbench, somewhere to hold work pieces at a convenient height while they’re being shaped. The command shell is the workbench of programmers manipulating text files.
- GUI interfaces are great, but they do not necessary let you do everything a shell does. They are great for simple straight forward tasks of course but if you do all your work in GUI you are missing out on the full capabilities of your environment. Because you won’t be able to automate common tasks, or use the full power of the tools available to you.
- A benefit of GUIs is WYSIWYG—what you see is what you get. The disadvantage is WYSIAYG—what you see is all you get.
- In the same way that a woodworker will customize their workspace, a developer should customize their shell.
- Work towards being fluent in your text editing (IDEs), it eliminates having to thinking about it. Instead you can focus on your programming and it will also save you a lot of time. a 4% increase in your text editing efficiency can save you a week in a year.
- Whenever you find yourself doing some repetitive task, get into the habit of thinking "there must be a better way to do this". Then find it.

> CHALLENGE: lose the trackpad/mouse for week, you'll find things you can do without pointing. Learn how to do it. Keep notes of key sequences you learn.

- On growing and extending your IDE with extensions, if you cannot find an extension that does what you want, write one.
- Knowing you can roll back to a previous state using a VCS is one thing, but can you actually do it? Are your commit well defined enough that rolling back is easy and straightforward?
- Put all your local configs and preferences in VCS. Including installed apps.
- Thought Experiment: Spill a cup of tea on your PC. Buy a new one how long will it take you to restore your new machine to the state of the other one?

### Psychology of Debugging

- Debugging is a sensitive, emotional subject for many developers. Instead of attacking it as a puzzle to be solved, you may encounter denial, finger pointing, lame excuses, or just plain apathy.
- It doesn’t really matter whether the bug is your fault or someone else’s. It is still your problem. Fix the problem, Not the blame.
- A debugging mindset means to step back a pace and actually think about what could be causing the symptoms. Don't panic and keep your ego in check.
- Always try to discover the root cause of a problem, not just this particular appearance of it.
- Write a failing test before fixing the code.
- Read the error message.
- Logging and tracing. Debuggers and a stack trace can only tell you the state and how you get there respectively, but they typically will not tell you what you were doing before you got there. That is where logs/tracing comes into play.
- **Rubber Ducking**: A very simple but particularly useful technique for finding the cause of a problem is simply to explain it to someone else. The other person should look over your shoulder at the screen, and nod his or her head constantly (like a rubber duck bobbing up and down in a bathtub).

## Chapter 4 - Pragmatic Paranoia

- YOU CAN'T WRITE PERFECT SOFTWARE: Accept it as an axiom of life. Embrace it. Celebrate it. Because perfect software doesn’t exist.
- Software engineering is mostly a team effort, so we are trained to code defensively: We use assertions to detect bad data, and distrust data from potential attackers or trolls. We check for consistency, put constraints on database columns, and generally feel pretty good about ourselves. But Pragmatic Programmers take this a step further. They don’t trust themselves, either.
- Knowing that no one writes perfect code, including themselves, Pragmatic Programmers build in defenses against their own mistakes.
- Over the millennia, humans have developed techniques to deal with fellow humans. Contracts are one of these techniques that can be applied when dealing with computers.
- Contracts define your rights and responsibilities as well as those of the other party. In addition there is an agreement concerning repercussions if either party fails to abide by the contract.
- Design with Contract
- Clients and Servers must agree on rights and responsibilities.
- Dead Programs Tell No Lies: we want to ensure that we do no damage while we’re working the bugs out. So we try to check things often and terminate the program if things go awry.
- Assertive programming: describes an easy method of checking along the way—write code that actively verifies your assumptions.
- Whenever you find yourself thinking “but of course that could never happen,” add code to check it.
- The function or object that allocates a resource should be responsible for de-allocating it--finish what you start.
- For anything that you create that takes up a finite resource, consider how to balance it--eg. if you are logging to a database how about a process to expire them after sometime?
- Because Pragmatic Programmers trust no one, including ourselves, we feel that it is always a good idea to build code that actually checks that resources are indeed freed appropriately.

> Don't Outrun your headlights---Take small steps always

- As pragmatic programmers we know we can't really see too far in the future, so we follow a rule: __Take Small Steps--Always__.
- Always take small, deliberate steps, checking for feedback and adjusting before proceeding. Consider that the rate of feedback is your speed limit. You never take on a step or a task that’s “too big.
- Note that feedbacks can be unit tests, user demo and conversations etc.
- Any task that requires "fortune telling" is too big. You're fortune telling if your estimate is months in the future, guessing users future needs, guessing technology availability, plan future maintenance.
- Much of the time, tomorrow looks a lot like today. But don’t count on it.

## Chapter 5 - Bend, or Break

### Decoupling

- Coupling is the enemy of change, because it links together things that must change in parallel. This makes change more difficult
- Some symptoms of coupling:
  - Wacky dependencies between unrelated modules or libraries
  - “Simple” changes to one module that propagate through unrelated modules in the system or break stuff elsewhere in the system
  - Developers who are afraid to change code because they aren’t sure what might be affected
  - Meetings where everyone has to attend because no one is sure who will be affected by a change
- The principle of "Tell, Don't Ask" (TDA) states that: you shouldn’t make decisions based on the internal state of an object and then update that object. Doing so totally destroys the benefits of encapsulation and, in doing so, spreads the knowledge of the implementation throughout the code. Basically, tell the object what to do, don't ask it for something and do something on it based on its internal details.
- When you want to access something, try not to chain methods, don't have more than one `.`. Unless the things you're chaining are really, really unlikely to change. eg. std libraries

> Globally accessible data is an insidious source of coupling between application components.

- Avoid global data, including singletons, external resources--make sure you always wrap these resources behind code that you control.
- If It’s Important Enough to Be Global, Wrap It in an API.

### Juggling the real world

- These days computers are expected to fit into our messy world, writing applications that respond to events regardless of the source will work better in the real world.
- Four strategies for writing applications that will work better in the real world:
  - Finite state machines
  - The Observer pattern
  - Pub/Sub
  - Reactive Programming and Streams
- A state machine is basically just a specification of how to handle events. It consists of a set of states, one of which is the current state. For each state, we list the events that are significant to that state. For each of those events, we define the new current state of the system. State machines are underused by developers, and we’d like to encourage you to look for opportunities to apply them.
- In the observer pattern we have a source of events, called the observable and a list of clients, the observers, who are interested in those events. The observer pattern has a problem: because each of the observers has to register with the observable, it introduces coupling. It can also introduce performance bottlenecks, since the notifier has to process registered functions synchronously.
- Publish/Subscribe (pubsub) generalizes the observer pattern, at the same time solving the problems of coupling and performance.
- If you’ve ever used a spreadsheet, then you’ll be familiar with reactive programming. If a cell contains a formula which refers to a second cell, then updating that second cell causes the first to update as well.

### Transforming Programming

- All programs transform data, converting an input into an output. And yet when we think about design, we rarely think about creating transformations. Instead we worry about classes and modules, data structures and algorithms, languages and frameworks.
- Programming Is About Code, But Programs Are About Data
- A top down approach to finding transformation is with the requirements, determining its inputs and outputs.
- Thinking in transformations and applying the philosophy data pipelining
- Don't Hoard State, Pass It Around

### Inheritance Tax

> You wanted a banana but what you got was a gorilla holding the banana and the entire jungle. ➤ Joe Armstrong

- Inheritance is coupling. Not only is the child class coupled to the parent, the parent’s parent, and so on, but the code that uses the child is also coupled to all the ancestors
- Don't pay Inheritance tax use these alternatives:
  - Interfaces and protocols
  - Delegation
  - Mixins and traits
- Prefer Interfaces to Express Polymorphism
- Use Mixins to Share Functionality
- Parameterize Your App Using External Configuration
- Static configuration is good, but configuration as a service is better.
- Configuration as a service: storing configuration behind a service API:
  - Multiple applications can share configuration information, with authentication and access control limiting what each can see.
  - Configuration changes can be made globally.
  - The configuration data can be maintained via a specialized UI.
  - The configuration data becomes dynamic.
- The idea that we should have to stop and restart an application to change a single parameter is hopelessly out of touch with modern realities. Whatever form it takes, configuration data drives the runtime behavior of an application. When configuration values change, there’s no need to rebuild the code.

## Chapter 6 - Concurrency

- Concurrency is when the execution of two or more pieces of code act as if they run at the same time. Parallelism is when they do run at the same time
- Analyze application workflow as part of the design to identify opportunities of what can be done at the same time. This can be easily done with an activity diagram
- Shared state is incorrect state.
- A semaphore is simply a thing that only one person can own at a time.
- A lot of attention is given to shared memory as a source of concurrency problems, but in fact the problems can pop up anywhere where your application code shares mutable resources: files, databases, external services, and so on
- Random Failures Are Often Concurrency Issues
- Concurrency in a shared resource environment is difficult, and managing it yourself is fraught with challenges.
- Use Actors For Concurrency Without Shared State
- In the actor model, there’s no need to write any code to handle concurrency, as there is no shared state.
- Use Blackboards to Coordinate Workflow
- Messaging systems can be like blackboards.

## Chapter 7 - While you are coding

- Coding is not mechanical, there are decisions to be made every minute—decisions that require careful thought and judgment if the resulting program is to enjoy a long, accurate, and productive life.
- Listen to your lizard brain: pay attention to that nervous or queasy feeling your brain might be trying to tell you something.
- On the says coding feels like some uphill task, resist the urge to soldier on instead think about the code, perhaps your brain is trying to tell you that task is harder than it should be or the design is wrong or you should be solving a different problem.
-  Give yourself a little time and space to let your brain organize itself. Stop thinking about the code, and do something that is fairly mindless for a while, away from a keyboard. Take a walk, have lunch, chat with someone. Maybe sleep on it. Let the ideas percolate up through the layers of your brain on their own: you can’t force it. If that’s not working, try externalizing the issue.
- Learning to listen to your gut when coding is an important skill to foster. But it applies to the bigger picture are well. Sometimes a design just feels wrong, or some requirement makes you feel uneasy. Stop and analyze these feelings. If you’re in a supportive environment, express them out loud
- For code you write that others will call, the basic principles of good modularization and of hiding implementation behind small, well-documented interfaces can all help
- Avoid programming by coincidence, program against documented interfaces and not just of some behavior that could change or is incorrect
- Program deliberately:
  - be aware of what you are doing
  - can you explain the code in detail to a junior engineer? if not you might be relying on a coincidence
  - don't use tech you don't fully grasp or build an application you don't fully understand
  - plan
  - don't depend on assumptions, always assume the worst
  - document your assumptions
  - don't just test your code, test your assumptions
  - don't be  a slave to history, don't let existing code determine your future code
- Estimate the Order of Your Algorithms and Test Your Estimates
-  Rather than construction, software is more like gardening—it is more organic than concrete. You plant many things in a garden according to an initial plan and conditions. Some thrive, others are destined to end up as compost
- The gardening metaphor is much closer to the realities of software development. Perhaps a certain routine has grown too large, or is trying to accomplish too much—it needs to be split into two. Things that don’t work out as planned need to be weeded or pruned.
- Refactoring is a disciplined technique for restructuring an existing body of code, altering its internal structure without changing its external behavior.
- refactoring is a day-to-day activity, taking low-risk small steps, like weeding and raking
- Reasons to refactor:
  - Duplication
  - Non-orthogonal design
  - Outdated knowledge
  - Usage
  - Performance
  - The tests pass
- Time pressure is often used as an excuse for not refactoring. But this excuse just doesn’t hold up: fail to refactor now, and there’ll be a far greater time investment to fix the problem down the road—when there are more dependencies to reckon with
- Refactor Early, Refactor Often
- Refactoring tips:
  - Don’t try to refactor and add functionality at the same time
  - Make sure you have good tests before you begin refactoring.  Run the tests as often as possible. That way you will know quickly if your changes have broken anything.
  - Take short, deliberate steps.  Refactoring often involves making many localized changes that result in a larger-scale change. If you keep your steps small, and test after each step, you will avoid prolonged debugging
- Testable code is good code.
- Before writing code, thinking about how to test the code you are about to write is a good way discover useful insight that reduces coupling
- A Test Is the First User of Your Code
- By all means practice TDD. But, if you do, don’t forget to stop every now and then and look at the big picture. It is easy to become seduced by the green "tests passed" message, writing lots of code that doesn’t actually get you closer to a solution.
- Build End-to-End, Not Top-Down or Bottom Up: The only way to build software is incrementally. Build small pieces of end-to-end functionality, learning about the problem as you go. Apply this learning as you continue to flesh out the code, involve the customer at each step, and have them guide the process.
- Test Your Software, or Your Users Will
- Use Property-Based Tests to Validate Your Assumptions
- Pragmatic Programmers have a healthy amount of paranoia
- Basic security principles:
  - 1. Minimize Attack Surface Area
  - 2. Principle of Least Privilege
  - 3. Secure Defaults
  - 4. Encrypt Sensitive Data
  - 5. Maintain Security Updates

### Password Anti patterns
- Do not restrict password length to less than 64 characters. NIST recommends 256 as a good maximum length.
- Do not truncate the user’s chosen password.
- Do not restrict special characters such as []();&%$# or /. If special characters in your password will compromise your system, you have bigger problems. The NIST says to accept all printing ASCII characters, space, and Unicode.
- Do not provide password hints to unauthenticated users, or prompt for specific types of information (e.g., “what was the name of your first pet?”).
- Do not disable the paste function in the browser. Crippling the functionality of the browser and password managers does not make your system more secure, in fact it drives users to create simpler, shorter passwords that are much easier to compromise. Both the NIST in the US and the National Cyber Security Centre in the UK specifically require verifiers to allow paste functionality for this reason.
- Do not impose other composition rules. For example, do not mandate any particular mix of upper and lower case, numerics, or special characters, or prohibit repeating characters, and so on.
- Do not arbitrarily require users to change their passwords after some length of time. Only do this for a valid reason (e.g., if there has been a breach).
- In summary; You want to encourage long, random passwords with a high degree of entropy. Putting artificial constraints limits entropy and encourages bad password habits, leaving your user’s accounts vulnerable to takeover

### Naming things

> There are two hard things in computer science: cache invalidation, naming things and off-by-one errors.

- Honor the culture. ie. follow the convention of naming certain things in you programming language. eg. in C `i` is used in loops for index
- Every project has its own vocabulary: jargon words that have a special meaning to the team.  It’s important that everyone on the team knows what these words mean, and that they use them consistently.
- Have a project glossary, listing the terms that have special meaning to the team. This is an informal document, possibly maintained on a wiki, possibly just index cards on a wall somewhere.

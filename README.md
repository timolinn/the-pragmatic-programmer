# The Pragmatic Engineer

## Chapter 1 - The Pragmatic Philosophy

What distinguishes Pragmatic Programmers? We feel it’s an attitude, a style, a philosophy of approaching problems and their solutions. They think beyond the immediate problem, placing it in its larger context and seeking out the bigger picture. After all, without this larger context, how can you be pragmatic? How can you make intelligent compromises and informed decisions?

- We can be proud of our abilities, but we must own up to our shortcomings—our ignorance and our mistakes
- Don't be afraid to admit ignorance or error or mistakes. Try to offer solutions
- Provide Options, Don’t Make Lame Excuses
- Think! About Your Work. Constantly be thinking, critiquing your work in real time
- Care About Your Craft
- When you find yourself saying, “I don’t know,” be sure to follow it up with “—but I’ll find out.”
- Don’t leave “broken windows’’ (bad designs, wrong decisions, or poor code) unrepaired. Fix each one as soon as it is discovered. If there is insufficient time to fix it properly, then board it up. Neglect accelerates software rot faster than any other factor.
- Like the soldiers in "The Stone Soup Story", be a catalyst for change. However, be as objective as you can be when you try to catalyze a change.
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

## Pragmatic Paranoia

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
- Any task that requires "fortune telling" is too big.
- Much of the time, tomorrow looks a lot like today. But don’t count on it.

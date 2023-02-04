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
- Critically Analyze What You Read and Hear. Beware of zealots who insists there dogma is the only way to go. Beware of commercialism, the first hit from your web search is not neccessarily the best result, someone could have paid to put it there.

> A good idea is an orphan without effective communication.

- Know your Audience
- You’re communicating only if you’re conveying what you mean to convey—just talking isn’t enough. To do that, you need to understand the needs, interests, and capabilities of your audience.
- Plan what you want to say. Write an outline. Refine it until it commmunicates exactly what you want to say to your audience
- Be a listener, encourage people to talk by asking questions.
- Get back to people. do your best to respond to emails, voicemails, chats etc. "I'll get back to you later" can buy you sometime if you need it.

> It is both what you say and The way you say it.

- Pragmatic programmers embrace documentation. Keep documentation as close as possible--in the code itself.
- It is easy to produce good documentation from comments in source code.

> It is recommended to add comments to modules and exported functions.

- Add comments to capture engineering trade-offs, why decisions were made, other alternatives that were discarded, etc.

## Chapter 2 - A Pragmatic Approach

#### The Essence of Good Design

- Good design is easier to change than bad design.
- A thing is well designed if it adapts to people who use it.
- In code, adapting means changing; So apply the ETC principle; __EASIER TO CHANGE__. This is not a rule but a simple guide.
- internalizing good engineering preinciples takes time and practice, be patient make notes about current situations and decisions then give yourself feedaback when the code changes.
- `DRY` is not just about code - code is a tiny part - `DRY` is more about avoiding duplication of __Knowledge and Intent__.
- Not all code duplication is knowledge duplication
- Interdeveloper deuplication is the hardest to discover or fix. THe best way to deal with this is to encourage frquent communication between developers.
- Make a point of reading other peoples code and documentation, formally or informally-- you're learning from them.

#### Orthogonality

- Two or more things are orthogonal if changes in one do not affect any of the others.
- Design components that are self-contained: independent, and with a single well-defined prupose
- Orthogonality increases productivity by guaranteeing changes are localized, and so development time and testing time are reduced. It also promotes reuse.
- To maintain orthogonality, write shy code -- modules that don't reveal anything unnecessary to other modules and don't rely on other modules implementations.
- Avoid global data.
- Duplicate code is a symptom of structural problem.
- Get into the habit of being constantly critical of your code.
Lokk for opportunities to improve you code structuaally or to make it more orthogonal. This process is called __Refactoring__

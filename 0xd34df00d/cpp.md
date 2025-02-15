# Cognitive load in C++

I was looking at my RSS reader the other day and noticed that I have somewhat three hundred unread articles under the "C++" tag. I haven't read a single article about the language since last summer, and I feel great!

I've been using C++ for 20 years for now, that's almost two-thirds of my life. Most of my experience lies in dealing with the darkest corners of the language (such as undefined behaviours of all sorts). It's not a reusable experience, and it's kind of creepy to throw it all away now.

Like, can you imagine, the token `||` has a different meaning in `requires ((!P<T> || !Q<T>))` and in `requires (!(P<T> || Q<T>))`. The first is the constraint disjunction, the second is the good-old logical OR operator, and they behave differently.

You can't allocate space for a trivial type and just `memcpy` a set of bytes there without extra effort - that won't start the lifetime of an object. This was the case before C++20. It was fixed in C++20, but the cognitive load of the language has only increased.

Cognitive load is constantly growing, even though things got fixed. I should know what was fixed, when it was fixed, and what it was like before. I am a professional after all. Sure, C++ is good at legacy support, which also means that you **will face** that legacy. For example, last month a colleague of mine asked me about some behaviour in C++03. `🤯`

There were 20 ways of initialization. Uniform initialization syntax has been added. Now we have 21 ways of initialization. By the way, does anyone remember the rules for selecting constructors from the initializer list? Something about implicit conversion with the least loss of information, _but if_ the value is known statically, then... `🤯`

**This increased cognitive load is not caused by a business task at hand. It is not an intrinsic complexity of the domain. It is just there due to historical reasons** (_extraneous cognitive load_).

I had to come up with some rules. Like, if that line of code is not as obvious and I have to remember the standard, I better not write it that way. The standard is somewhat 1500 pages long, by the way.

**By no means I am trying to blame C++.** I love the language. It's just that I am tired now.

[Readable version](https://minds.md/0xd34df00d/cpp)

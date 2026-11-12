---
notebook:
tags:
---
okay, so a bit of context. back when i was studying at college, i was trying to optimize my learning process as much as possible, and i ended up discovering Anki and spaced-repetition as a concept. i ended up using Anki for quite a while and it did help me. i loved the concept... but i didn't like the app. it had me conflicted. on one hand, it allowed me to properly review the content from my classes (among other stuff), but on the other it had way too many quirks and complicated ways of handling things that i wasn't a fan of (in particular, the UX leaves a lot to be desired, although it has marginally improved in recent years). ended up churning from Anki and just abandoning the practice of spaced repetition altogether.

after some time, i ended up reading this article recommended by Justin Skycak https://lelouch.dev/blog/you-are-probably-not-dumb/ . 
the tldr is that knowledge has prerrequisites, and if you don't have them, you won't fully understand what you are trying to learn in the first place. and that was one of my annoyances with Anki. 
as i kept reviewing stuff (especially pre-made decks) Anki assumes all knowledge is in the same layer of understanding. it assumes that each flashcard is independent from the others, and that makes it difficult to actually progress while trying to learn a particular topic. 
Justin Skycak (the guy from Math Academy) ended up implementing spaced-repetition + prerrequisite graphs for math learning, and there i ended up seeing we could extend the concept more generally. one of the things Math Academy made me realize is that if we combine spaced-repetition (i.e. when we should review a card) with prerrequisite graphs (i.e. we keep unlocking new knowledge as we learn the prerrequisites), we can learn things more clearly and in a more structured way.

that's where my "bet" goes. i want something like Anki, but with the option to create a graph of prerrequisites (e.g. you can't learn Y until you properly learn X). that's Armin. among other stuff, i also tried to fix some of the annoyances i had with Anki and make it as intuitive as possible to use. this is a non-exhaustive list of the things i worked on for this app:

- UI polish of the interface. i tried to make it as intuitive as possible.
- MCP server for letting agents read, edit and manage cards and decks. in particular, the MCP server is very useful for creating flashcards from any existing content you have. just point your agent to a resource (e.g. a pdf) and it will take its content and transform it into a deck with flashcards with its prerrequisites graph already created.
- Anki-compatibility with caveats. the app supports bringing your existing Anki decks for most decks out there, but we currently don't support custom Anki cards.
- graph view that shows all your flashcards. in here, you can create a graph of prerrequisites and further structure your decks.
- "concept cards". they work more like exercises. you provide the template of an exercise (e.g. how to calculate a derivative) and an agent creates variations of that same type of exercise while changing the details (like the values).

we also have a paid plan for creating way more flashcards and use "concept" cards, but i built the free plan with generous limits so you can test the app without any issue. to be honest, i want the app to be as flexible as possible, and most people will probably only need the free plan. but hey, if you find it too tight, please hit me up and i'll see how i can improve the experience for everyone.

the app is open source and MIT-licensed. you can find it here https://github.com/andy-spike/armin

as for the rest, it is the same you would expect from a spaced-repetition flashcard app. 
please try it out and tell me what you think of it!
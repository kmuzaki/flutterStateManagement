# Differences between Ephemeral State and an App State

Technically, there isn't a clear-cut as to what is considered an ephemeral state and an app state, but from what I've observed from the two projects, which are obvious by looking at the code structure, there are one or two things to note.

## Ephemeral state

Even the word itself, *ephemeral*, which means *lasting or used for only a short period of time* according to the Oxford Dictionary, should give an idea of how this works.
An ephemeral state is a state that is contained in a single widget. Thus, no other widgets besides the widget that contained said state could change/edit, or access it.
Meaning that it is not necessary to implement some advanced state management techniques. In analogy terms, it's like containing protected properties within that class only, or a variable that is contained in only one function.

## App state

In short, it is a state that is NOT ephemeral or temporary. It's persistent. It is a state that can be accessed across other aspects or widgets within the app. Sometimes it is called a shared state. Technically, you can use setState() to manage this state. In an analogy, it's like an ephemeral state's analogy, but you have set getter/setter methods to those protected properties so that they can be accessed by other classes.

## The advantage of App state
The advantages of App state, in the context of larger Flutter applications, especially when dealing with user authentication, shopping carts, and other app-wide state needs, are as follows:
1. Persistence (Because it'll retain some important data you need to save)
2. Better performance (Prevents unnecessary widget rebuilds across the app)
3. Consistency management (Because all data that you need is contained within a single location)
4. Easier authentication (So that widgets that depend on the user's credentials could update correspondently if the user logs out, and then a new user logs in)

## References:
https://docs.flutter.dev/data-and-backend/state-mgmt/ephemeral-vs-app
https://chatgpt.com/share/68d3ab58-f034-8010-a96c-973380e2fc72

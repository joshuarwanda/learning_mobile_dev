# Project Notes
Now we get into the meaty bits. \
Previous notes were mostly theory and setup, All notes here henceforth shall be what I learn while building projects.\
## State
What is state?\
- **State** is basically data that is saved by you client and rendered in the UI when it changes.
- **Stateful widgets** are widgets that contain information that is mutable and can change while the app is running, **Stateless** widgets cannot contain mutable information.\
- In Flutter, Everything is basically a widget
- !! In Flutter, It is best practice to use Stateless widgets as much as possible over stateful widgets.
- `late` keyword in dart 'promises' to assign a value to a variable before it is used, e.g a text field to be entered by a user before a button is clicked.
- Stateful widgets come with two predefined functions, `initState` and `dispose`: 
- `initState` - Initializes variables when the app is ran
- `dispose` - discards variables when the app is terminated

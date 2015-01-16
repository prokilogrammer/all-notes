# Implementation Basics

## Architecture
Here are the cores classes in Ace:

1. _Editor_: Main entry point for API; Handles user input (keyboard, mouse); Holds on to the VirtualRenderer and EditSession objects. It has APIs to programatically perform everything from selecting text, copy-paste, find & replace to configuring behaviors (Ex: auto-pairing special characters/auto-indentation), goto line, navigate cursor anywhere on screen, etc

2. _VirtualRenderer_: Drawing class. Draws everything.
	2.1. _Layers_: Holds controls for Text, Cursor, Selection

3. _EditSession_: Keeps track of state relating to the document. Stores things like Selection, Cursor Position, Scroll Position, UndoManager, Language etc. Almost all of the APIs exposed by EditSession is wrapped and exposed by Editor also. 

4. _Document_: Holds the text (array of strings) of the document. Text and keyboard events bubble up from Document to Editor via EditSession where they are handled. Has APIs to add/get/remove lines from the text, undo or applyDeltas.

5. _TextMode_: Defines language specific functionality like Syntax Highlighting, Auto-indentation rules etc.

6. _Range_: It is like a rectange within the text area. It is specified by row-column number of top left and bottom right points. It has APIs to perform range intersection, grab text within a range, collapse a range of rows etc. Because ranges are defined by col, row pair, we can have a range starting with arbitrary column and still work.

7. _Tokenizer_: This class takes a set of highlighting rules and creates a tokenizer out of it.
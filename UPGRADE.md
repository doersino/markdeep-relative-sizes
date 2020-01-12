*(Really just a note to self.)*

Whenever a new version of Markdeep is released, perform the following steps:

1. Download https://casual-effects.com/markdeep/⟨OLD⟩/markdeep.js and https://casual-effects.com/markdeep/⟨NEW⟩/markdeep.js, where `⟨OLD⟩` and `⟨NEW⟩` are the *most recent supported version* and the *new version*, respectively.
2. Check if any of the non-relatively defined sizes in the included stylesheets have changed or new ones have been added. Use a visual diff tool for this, e.g. FileMerge.
3. Copy the folder `⟨OLD⟩/` to `⟨NEW⟩/` and perform the required changes in the new copy.
4. **Don't forget to change the version number in the comment at the top of the file.**

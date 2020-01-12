# markdeep-relative-sizes

The stylesheet `relativize.css`, which is provided for different Markdeep versions, "relativizes" sizes: It overrides sizes/lengths defined in terms of `px`, `pt` etc. in the stylesheets that are automatically applied by Markdeep with lenghts defined in terms of `rem`. This enables scaling the entire document simply by adjusting the `<html>` element's font size – exactly what's required to enable

* fullscreen presentations via https://github.com/doersino/markdeep-slides,
* adjustable base font sizes in https://github.com/doersino/markdeep-thesis,
* and more!

The conversion rule is simple: `⟨N⟩px` ⟼ `calc(⟨N⟩rem / var(--rf))`, where `--rf` is the base font size the original `px` measurements are assumed to be relative to. In fact, `--rf` is the browser default, `16px`. (Note that I would've preferred to define `--rf: calc(1rem / 16px)` and then use it like `calc(⟨N⟩px * var(--rf))`, but `calc` disappointingly, yet understandably, can't deal with "rem per pixel" units in current browsers.)

When applied to a standard Markdeep document, this stylesheet is designed *not to yield any visual changes* (unless you change the root font size from its `16px` default, that is).

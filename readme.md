# Sam's Enhance Example

This is an example project intended entirely for personal use while I play around with [Enhance](https://enhance.dev/).

## Auto-formatting

The official Enhance docs recommend using es6-string-html and literally-html for syntax highlighting and formatting. I've found that the latter doesn't work on Windows, so, after scouring the internet for a solution, I found [this discussion for on the Lit repository](https://github.com/lit/lit/discussions/4033) with recommends using Prettier via ESLint with a the Lit plugin.

The only thing that wasn't working was formatting on save. This worked for everything outside the template literals, but not for the HTML inside. Since the ESLint/Prettier fixes were still working when I triggered them manually, I added the following to my VS Code settings to trigger them on save:

```
"editor.codeActionsOnSave": {
	"source.fixAll.eslint": true
}
```

# Create a extensions.json file

In order to suggest extensions to other users in a repository project,
you can put a `extensions.json` in your project in the `.vscode` folder.

The structure of the file is:

```json
{
// See https://go.microsoft.com/fwlink/?LinkId=827846
// for the documentation about the extensions.json format
 "recommendations": [
  "owner.extension-name"
 ]
}
```

I could not find a way to do this automatically from Visual Studio Code.

From this template file, you can suggest packages by going to:

<https://marketplace.visualstudio.com/>

And searching for the extension(s) you want to recommend to anyone working with your repository.

Then go to the individual page for the extension you want to recommend and copying and pasting the value listed in `Unique Identifier` on the right side of the page, or you can copy and paste it from the `Installation` field, leaving out the `ext install` .

The format for the extension name is owner.package and usually is listed in between double quotes.  For more than one, use a , after each extension.

If a user is using GitHub and VSCode, they will get a message from the taskbar saying they have extension recommendations

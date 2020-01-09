# Editorial -> Working Copy
Shortcut to sync repositories between Working Copy and Editorial.

## Requirements
1. [Editorial](https://omz-software.com/editorial/)
2. [Working Copy](https://workingcopyapp.com/)
3. [Scriptable](https://scriptable.app/)<sup>[1](#footnote)</sup>
4. Shortcuts app

## Install
Get the shortcut at [https://www.icloud.com/shortcuts/25a24d5dbb634567bfef2667e903a6d6](https://www.icloud.com/shortcuts/25a24d5dbb634567bfef2667e903a6d6).

Follow the instructions in the Import Questions to install the necessary Editorial workflow. You can also see [this file](/workflow_link.md) to copy and paste the workflow on your iPhone or iPad to install the workflow.

## Usage
1. Run the *shortcut* without any input in order to select a repository to sync from Working Copy to Editorial. All of the files will be copied to a folder with the name of the repository.
2. Run the Editorial -> Working Copy *workflow* from within Editorial to sync the current* folder back to Working Copy. You will be able to select the repository to sync to.

## Optional configuration
1. The export from Editorial can be configured to use the current directory or to choose a directory every time. Only immediate subdirectories of Editorial's local document root are supported.

![workflow options](/workflow_options.jpeg)

2. Which file extensions are considered to be binary can be configured. To do so, edit the list in the shortcut, as well as the list in the Editorial workflow.

![shortcut options](/shortcut_options.jpg)

## How it works
Folders and files are converted to and from JSON inorder to pass them between Editorial and the shortcut. Text files are passed as text, while binary files are b64encoded and decoded.

---
<a name="footnote">1.</a> Scriptable is needed to get the relative paths of the files in the Working Copy repo. Thanks to [@palmin](https://twitter.com/palmin) for suggesting this. The latest version of Scriptable is needed to run the inline script included in the shortcut .

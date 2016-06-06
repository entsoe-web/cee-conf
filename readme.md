# ENTSO-E CEE Conference

This is the mini website for the CEE Regional Conference 2016. Use this repo to edit and publish website content.

## Getting Started - The structure
The main folders you will be interested in are as follows:

```
.
├── _events
├── _data
├── _sections
```

### _data
- [__speakers.csv__](_data/speakers.csv) - this csv file is used to populate the speakers boxes on the home page. It is independent of what's in each event.

### _sections
This folder includes the files for each section (horizontal row) of the homepage.

They include the following metadata:

```
---
title: agenda
order: 2
fill: 'fill-grey'
---
```

All content between the `---` and `---` is known as the front matter. This is where we define the metadata.

`title:` This is used for the nav bar and the section title.

`order:` The sections are shown on the home page in order. If you wish to reorder them you will need to change this. It will only accept numbers.

`fill:` This allows you to set the background colour of a row. The only option for now is `fill-grey` or nothing.

**The main one you will need to edit is [_sections/intro.md](_sections/intro.md). You will need to edit this to fix the copy at the top of page.**


### _events
This folder includes the files for each section of the homepage.

They include the following metadata:

```
---
title: "My amazing title"
time: 09.30 - 10.40
moderator: Jaroslavas Neverovičius
speakers:
  - Rokas Masiulis
  - Arvils Ašerādens
  - ...
type: panel/break
---
```

All content between the `---` and `---` is known as the front matter. This is where we define the metadata.

Each event will be ordered by the time. It is important to the time in the following format: __HH.MM__.

`speakers:` Each name must be on a new line with __2 spaces__ from the left and proceeded with a dash (-) and another space and the name of the person. Use existing events as templates.

`type:` This influences whether a link is put in the agenda to the event or not. Using break will mean the link will not be shown. Look at the [01_registration.md](_events/01_registration.md) to see this in action.


# How to edit & update
You have two options when updating the site:

1. Edit files directly online here at github
2. Edit files offline in Sublime Text and then push changes to github

## Offline Editing
__The very first time complete these steps__

1. Open github on your machine.
2. Click the plus in the top left. __Choose Clone__ ![](readme_pics/01_clone.png)
3. Search for entsoe-web ![](readme_pics/03_clone.png)
4. Select the `entsoe-web/cee-conf`
5. Select the folder to clone to, it will automatically create a folder called `baltic-conf` below your chosen one. ![](readme_pics/04_clone.png)
6. You will then be presented with this screen showing the change history.![](readme_pics/05_clone.png)

__Not the first time?__

1. Open github
2. Click `entsoe-web/cee-conf` on the left.
3. you will see the screen with all the changes ![](readme_pics/05_clone.png)
5. __Click sync before you do any work!__ __IMPORTANT!!!__

__Open Sublime Text__
1. File -> Open Folder...
2. Navigate to the folder you have cloned `baltic-conf` into eg. `D:\CBR\GitHub\baltic-conf`
3. On the left you should see a list of files that are located in the `baltic-conf` folder. IF this is not there go to `View -> Side Bar -> Show Side Bar`.
4. Select the file on the left you wish to edit.
5. For instance to edit the closing speechs - [_events/closing_speech.md](_events/closing_speech.md). Click the carrot beside "_events" and then "closing_speeches.md"
6. You will be presented with a grey screen to edit on: ![](readme_pics/07_sublime.png)
7. If it's not grey make sure Markdown or Markdon GFM or MultiMarkdown is shown in the bottom right. To do so click on the bottom right -> MarkdownEditing -> Select one of the above. ![](readme_pics/08_sublime.png)

## Online Editing
1. Go to the repo [github.com/entsoe-web/cee-conf/](https://github.com/entsoe-web/cee-conf/)
2. Find the file you wish to edit.
3. Maybe you want to edit the closing speeches - [_events/closing_speech.md](_events/closing_speech.md)
4. Select the edit button in the top right.
5. OR [Edit _events/closing_speech.md](https://github.com/entsoe-web/cee-conf/edit/gh-pages/_events/closing_speech.md)
6. When you are done with making changes, make sure to comment on what changes you made in the commit box at the bottom of the page.
7. Add your content to the closing speeches and press save or <kbd>Ctrl</kbd>+<kbd>S</kbd>.

## Go back to github app
1. Go back to the github app.
2. You will now see that at the top of the baltic-conf page, `Changes` will have a blue circle beside it.
3. Click Changes on the top bar.
4. You will see a list of the changes you've made.
5. If you're happy, scroll to the bottom of the page.
6. Enter a summary exlpaining the edits you've made.
7. Click `Commit to gh-pages`
8. Next you should click sync.


# Learning Markdown in GitHub


## Headings: 
add # (number sign) to create heading - # heading 1, ## heading 2 ....###### heading 6 is the lowest

### Heading Best Practices:
- always put a space between the nunber signs and heading name e.g: # Heading name
- put blank lines before adn after a heading for compatibility


## Styling text:
- **Bold**:  ** **
- *Italic*: * *
- ~~Strikethrough~~: ~~ ~~
- **Bold _and nested_ italic**: ** ** and _ _
- ***All bold and italic***: *** ***
- <sub>Subscript</sub>: <sub> </sub>
- <sup>Superscript</sup>: <sup> </sup>


## Quoting text:
You can quote text with a >.

Text that is not a quote

> Text that is a quote


## Quoting code:
You can call out code or a command within a sentence with single backticks. The text within the backticks will not be formatted. You can also press the Command+E (Mac) or Ctrl+E (Windows/Linux) keyboard shortcut to insert the backticks for a code block within a line of Markdown.

Use `git status` to list all new or modified files that haven't yet been committed.
Rendered inline code block

To format code or text into its own distinct block, use triple backticks.

Some basic Git commands are:
```
git status
git add
git commit
```


## Supported color models
In issues, pull requests, and discussions, you can call out colors within a sentence by using backticks. A supported color model within backticks will display a visualization of the color.

The background color should be `#ffffff` for light mode and `#0d1117` for dark mode.

Here are the currently supported color models.

Color	Syntax	Example	Output
HEX	`#RRGGBB`	`#0969DA`	Rendered supported color model in HEX format.
RGB	`rgb(R,G,B)`	`rgb(9, 105, 218)`	Rendered supported color model in RGB format.
HSL	`hsl(H,S,L)`	`hsl(212, 92%, 45%)`	Rendered supported color model in HSL format.


## Links:
You can create an inline link by wrapping link text in brackets [ ], and then wrapping the URL in parentheses ( ). You can also use the keyboard shortcut Command+K to create a link. When you have text selected, you can paste a URL from your clipboard to automatically create a link from the selection.

You can also create a Markdown hyperlink by highlighting the text and using the keyboard shortcut Command+V. If you'd like to replace the text with the link, use the keyboard shortcut Command+Shift+V.

This site was built using [GitHub Pages](https://pages.github.com/).


## Section Links:
You can link directly to a section in a rendered file by hovering over the section heading to expose the link.


## Relative links
You can define relative links and image paths in your rendered files to help readers navigate to other files in your repository.

A relative link is a link that is relative to the current file. For example, if you have a README file in root of your repository, and you have another file in docs/CONTRIBUTING.md, the relative link to CONTRIBUTING.md in your README might look like this:

[Contribution guidelines for this project](docs/CONTRIBUTING.md)
GitHub will automatically transform your relative link or image path based on whatever branch you're currently on, so that the link or path always works. The path of the link will be relative to the current file. Links starting with / will be relative to the repository root. You can use all relative link operands, such as ./ and ../.

Relative links are easier for users who clone your repository. Absolute links may not work in clones of your repository - we recommend using relative links to refer to other files within your repository.


## Images
You can display an image by adding ! and wrapping the alt text in [ ]. Then wrap the link for the image in parentheses ().

![This is an image](https://myoctocat.com/assets/images/base-octocat.svg)


## Paragraph:
to create paragraphs, use a blank line to separate one or more line of text.

### Paragraph Best Practices:
Don't put table or spaces in front of your paragraph
Keep left lines aligned

## Line Breaks
add (<br>) to end a line.

### Line Break Best Practices
use two or more spaces

## List:
You can make an unordered list by preceding one or more lines of text with -, *, or +.

- George Washington
* John Adams
+ Thomas Jefferson
Rendered unordered list

To order your list, precede each line with a number.

1. James Madison
2. James Monroe
3. John Quincy Adams
Rendered ordered list

Nested Lists
You can create a nested list by indenting one or more list items below another item.

To create a nested list using the web editor on GitHub or a text editor that uses a monospaced font, like Visual Studio Code, you can align your list visually. Type space characters in front of your nested list item, until the list marker character (- or *) lies directly below the first character of the text in the item above it.

1. First list item
   - First nested list item
     - Second nested list item
Note: In the web-based editor, you can indent or dedent one or more lines of text by first highlighting the desired lines and then using Tab or Shift+Tab respectively.

Nested list with alignment highlighted

List with two levels of nested items

To create a nested list in the comment editor on GitHub, which doesn't use a monospaced font, you can look at the list item immediately above the nested list and count the number of characters that appear before the content of the item. Then type that number of space characters in front of the nested list item.

In this example, you could add a nested list item under the list item 100. First list item by indenting the nested list item a minimum of five spaces, since there are five characters (100. ) before First list item.

100. First list item
     - First nested list item
List with a nested list item

You can create multiple levels of nested lists using the same method. For example, because the first nested list item has seven characters (␣␣␣␣␣-␣) before the nested list content First nested list item, you would need to indent the second nested list item by seven spaces.

100. First list item
     - First nested list item
       - Second nested list item
List with two levels of nested items

## Code Blocks:
code blocks are normally indented four spaces or one tab

## Task List

To create a task list, preface list items with a hyphen and space followed by [ ]. To mark a task as complete, use [x].

- [x] #739
- [ tesr] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete :tada:
Rendered task list

If a task list item description begins with a parenthesis, you'll need to escape it with \:

- [ ] \(Optional) Open a followup issue

For more information, see "About task lists."

## Mentioning people and teams
You can mention a person or team on GitHub by typing @ plus their username or team name. This will trigger a notification and bring their attention to the conversation. People will also receive a notification if you edit a comment to mention their username or team name. For more information about notifications, see "About notifications."

Note: A person will only be notified about a mention if the person has read access to the repository and, if the repository is owned by an organization, the person is a member of the organization.

@github/support What do you think about these updates?

Rendered @mention

When you mention a parent team, members of its child teams also receive notifications, simplifying communication with multiple groups of people. For more information, see "About teams."

Typing an @ symbol will bring up a list of people or teams on a project. The list filters as you type, so once you find the name of the person or team you are looking for, you can use the arrow keys to select it and press either tab or enter to complete the name. For teams, enter the @organization/team-name and all members of that team will get subscribed to the conversation.

The autocomplete results are restricted to repository collaborators and any other participants on the thread.

## Referencing issues and pull requests
You can bring up a list of suggested issues and pull requests within the repository by typing #. Type the issue or pull request number or title to filter the list, and then press either tab or enter to complete the highlighted result.

## Referencing external resources
If custom autolink references are configured for a repository, then references to external resources, like a JIRA issue or Zendesk ticket, convert into shortened links. To know which autolinks are available in your repository, contact someone with admin permissions to the repository.

## Uploading assets
You can upload assets like images by dragging and dropping, selecting from a file browser, or pasting. You can upload assets to issues, pull requests, comments, and .md files in your repository.

## Using emoji
You can add emoji to your writing by typing :EMOJICODE:.

@octocat :+1: This PR looks great - it's ready to merge! :shipit:

Rendered emoji

Typing : will bring up a list of suggested emoji. The list will filter as you type, so once you find the emoji you're looking for, press Tab or Enter to complete the highlighted result.

## Paragraph:
You can create a new paragraph by leaving a blank line between lines of text.

## Footnotes:
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].  

You can also use words, to fit your writing style more closely[^note].

[^1]: My reference.
[^2]: Every new line should be prefixed with 2 spaces.  
  This allows you to have a footnote with multiple lines.
[^note]:
    Named footnotes will still render with numbers instead of the text but allow easier identification and linking.  
    This footnote also has been made with a different syntax using 4 spaces for new lines.


## Hiding content with comments
You can tell GitHub to hide content from the rendered Markdown by placing the content in an HTML comment.

<!-- This content will not appear in the rendered Markdown -->

## Ignoring Markdown formatting
You can tell GitHub to ignore (or escape) Markdown formatting by using \ before the Markdown character.

Let's rename \*our-new-project\* to \*our-old-project\*.


## Disabling Markdown rendering
When viewing a Markdown file, you can click <>  at the top of the file to disable Markdown rendering and view the file's source instead.



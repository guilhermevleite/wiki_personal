# Markdown

## - Header Tags:

Use # as H1 tag:

> # H1 Tag
> ## H2 Tag
> ###### H6 Tag

---

## - Horizontal Rules:

Use three or more of these to create a rule:

> Hyphens \--- 
> Asterisks \*** 
> Underscores \___ 

---

## - Text Formating:

* Bold:
> \**bold\** also \__bold\__ 
> **This** is important 

* Italic:
> \*italic\* also \_italic_  
> *This* also is important

---

## Hyperlink:
> \[Hyperlink\](https://www.google.com.br)  
> [Hyperlink](https://www.google.com.br)  
> It should also be automatic: https://www.google.com

---

## Blockquotes:
> \> This will be quoted

---

## Inline code:
> I think you should use an  
> '<addr>' element here instead.  
> '<addr>' Test1
> '<addr>' Test2
> `<addr>` Test3
> "<addr>" Test4

---

## Lists:

> Use \* or \- for unsorted lists

> * Unordered
> * One
> * Two
>   * Two.One
>     * Two.One.One

> Use X. for orderef lists, change X with the numeration

> 1. Ordered
> 2. One
> 3. Two
>    4. Two_One 
>       5. Two_One_One

---

## Images:

!\[Github Logo](/images/logo.png)  
![Google Logo](https://i.imgur.com/jCxpBrW.jpg)

# Github Markdown

---

Ignore markdown by placing a \ before the markdown symbol: \*\*Not Bold\*\*.  

## - Syntax:
'''python
def test(param)
    # Identation need to be four spaces
    print("Hell on earth!")
    var status = 666
'''

Task list:
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

If you include a task list in the first comment of an Issue, you will get a handy progress indicator in your issue list. It also works in Pull Requests!

Tables:
First row is separated with - and the columns with |
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

SHA ref:
You can link to a commit using it's SHA-1 Hash
16c999e8c71134401a78d4d46435517b2271d6ac
mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac

Issues ref:
To link a Issue within the same repo
#1
mojombo#1
mojombo/github-flavored-markdown#1

User ref:
@lupins to notify that person to come and look at this

Strikethrough:
Any words within two ~ will be ~~crossed out~~.

Emoji:
Yes! :feelsgood: :octocat:
Complete list: https://www.webpagefx.com/tools/emoji-cheat-sheet/

Sources:

https://guides.github.com/features/mastering-markdown/


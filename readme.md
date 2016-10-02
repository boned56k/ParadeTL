ParadeBuster translation project
===================


This project is the in-progress translation of the output of arc_converter + wolftrans.

----------


Contributing
-------------

Clone this repository and begin modifying the translation text files. I've added an example of a before and after below. Once you have completed some translations, submit a github pull request (pull request guide: https://help.github.com/articles/creating-a-pull-request/). I will merge it into the main branch after quality checking it ASAP.


I don't know shit about Git
-------------
OK
1) https://git-scm.com/download
2) use the green clone with HTTPS button in top right
3) do some translations
4) use this guide maybe http://rogerdudler.github.io/git-guide/
5) **finally** create a pull request https://help.github.com/articles/creating-a-pull-request/

How do I apply the translation patch?
-------------
It is complicated. 
1) Get and use Arc_Converter
2) Get Ruby (https://www.ruby-lang.org/)
3) Follow the guide here (https://github.com/mathewv/wolftrans)
4) Copy contents of this repository into the location you think makes sense
5) Follow the guide in step 3 **again** and then maybe enjoy the results?

OR

Just wait for the patched version on your favorite forums.

Examples
-------------

Some original strings contain metadata characters and we need to make sure they do not get replaced.
Here is an example of what you will see in the translation patch **.txt** files.

> **Before:**

> \> BEGIN STRING
「鉄機都ロンボーン」ではアイテムや武器を消費して
\\\c\[3]武器を強化できる\\\c\[0]工房を利用できます。
>\> CONTEXT COMMONEVENT:348/184/Message < UNTRANSLATED

>\> END STRING

The bold text is the added translation. It is very bad but it will work for this example. You do not need to remove the "**< UNTRANSLATED**" part of the metadata. Note that the weird **\\\c[3]** stuff is still in-tact. The game engine does stuff like replace it with an item or player name so keep it in the translation.
> **After:**

> \> BEGIN STRING
「鉄機都ロンボーン」ではアイテムや武器を消費して
\\\c\[3]武器を強化できる\\\c\[0]工房を利用できます。
>\> CONTEXT COMMONEVENT:348/184/Message < UNTRANSLATED
> **Putting items in 「Iron machine Metropolitan Ronbon」workshop**
> **\\\c\[3] will allow you to strengthen them \\\c\[0] **
>\> END STRING


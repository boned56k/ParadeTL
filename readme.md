ParadeBuster translation project
===================


This project is the in-progress translation of the output of arc_converter + wolftrans.

----------
![Example](http://i.imgur.com/QIUMZKN.png)

Contributing
-------------

Find a .txt file that needs some translations and then do the following:
![Howto](http://i.imgur.com/R1JG2QZ.png)
Just do one .txt file at a time and submit your changes. Git is really great at resolving any conflicts and showing other people what has been done.


How to translate
-------------

Some original strings contain metadata characters and we need to make sure they do not get replaced.
Here is an example of what you will see in the translation patch **.txt** files.

**Leave the following alone:**  
  **\> BEGIN STRING**  
  **\> CONTEXT** ... **< UNTRANSLATED**  
  **\> END STRING**  
  
> **Before:**

> \> BEGIN STRING  
>「鉄機都ロンボーン」ではアイテムや武器を消費して  
>\\\c\[3]武器を強化できる\\\c\[0]工房を利用できます。  
>\> CONTEXT COMMONEVENT:348/184/Message < UNTRANSLATED  

>\> END STRING

The bold text is the added translation. It is very bad but it will work for this example. Note that the weird **\\\c[3]** stuff is still in-tact. The game engine needs it so stay in the translation for name or item text replacement.
> **After:**

> \> BEGIN STRING  
>「鉄機都ロンボーン」ではアイテムや武器を消費して  
>\\\c\[3]武器を強化できる\\\c\[0]工房を利用できます。  
>\> CONTEXT COMMONEVENT:348/184/Message < UNTRANSLATED  
> **Putting items in 「Iron machine Metropolitan Ronbon」workshop**  
> **\\\c\[3] will allow you to strengthen them \\\c\[0]**  
>\> END STRING


I will not accept pull requests for terrible translations like mine in the example above.
-------------


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


Why should I contribute?
-------------

This repository is open/free as in freedom. If you don't like it's direction, you can clone/fork it and do whatever you want with it. That means anything done here will be a contribution to the end purpose of delivering a translation patch for the game. Don't worry about your effort clashing with somebody else's. That is what git is for; resolving conflicts easily and showing progress.

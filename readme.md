jQuery UI Modal Login Form
==========================

----------


This is a phpbb 3 mod that pretty much just loads :

`jQuery 1.8.2`

`jQuery UI 1.9.0`

Into overall header of the Prosilver Style. That is not all it does though.

The main function of this mod is to replace the standard login link with a button that fire a pop up / modal
login form.

![alt text](https://raw.github.com/randomessence/jqueryUIloginphpbb3mod/master/contrib/examples/form.png)

This is a html form styled by jQueryUI. **It has potential**. 

So in terms of phpbb 3 edits, the mod is minor. What is does is add the potential to many things such as:

**Style :** many things can be styled and managed using the exisisting Framework. make us of the icon sets, ccs and range of the many themes available.

**Create :** Make use of the many plugins and widgets that jqueryUI comes bundled with. An example of this is the accordian spoiler bbcode i have already created. simple javascript snippets can be made to do some cool stuff.

##Theme Changing

with the release of v1.1.0 you can manually enter a value in the acp for the theme folder containing the .css

![](https://raw.github.com/randomessence/jqueryUIloginphpbb3mod/master/contrib/examples/acp.png)

This works on a simple principle. You are specifiying the name of the theme folder located in the `js/jqueryui/css/` directory. There are 25 theme folders included ( all the default ones ) . 

All the included CSS files are generically named as `jquery-ui.css` and not `jquery-ui-1.9.0.custom.css`. You need to create your custom theme, download, unzip and rename the css of your choosing (minified or not) to `jquery-ui.css` then upload your folder to the previously stated directory. If your theme folder containging your `jqueryu-ui.css` is named `myfancytheme` then then value you would enter in the ACP/General/Board Settings page would be: myfancytheme

**Theme Folders included:**

- base
- black-tie
- blitzer
- cupertino
- dark-hive
- dot-luv
- eggplant
- excite-bike
- flick
- hot-sneaks
- humanity
- le-frog
- mint-choc
- overcast
- pepper-grinder
- redmond
- smoothness
- south-street
- start
- sunny
- swanky-purse
- trontastic
- ui-darkness
- ui-lightness
- vader

**For Previews or to roll your own theme go here**

[http://jqueryui.com/themeroller/](http://jqueryui.com/themeroller/)

##CSS

in each theme folder there is a jquery-ui.css

This CSS relates to the padding of the buttons when styling out LOGIN/LOGOUT link.

`/*button text element */`

`.ui-button-text-only .ui-button-text { padding: .4em 1em; }`

i use (and will update the css files soon)

`.ui-button-text-only .ui-button-text { padding: .3em 1em; }`

This CSS relates to tooltip thingies if there is a conflict

```css
.ui-tooltip {
	padding:8px;
	position:absolute;
	z-index:9999;
	-o-box-shadow: 0 0 5px #aaa;
	-moz-box-shadow: 0 0 5px #aaa;
	-webkit-box-shadow: 0 0 5px #aaa;
	box-shadow: 0 0 5px #aaa;
}
```


##Addons

Since this mod loads jquery Ui into Style we can use it for other cool stuff as well. 

##Accordion Spoilers

**With the use of 2 special and custom bbcodes we can create jQuery UI spoilers using the Accordian feature.**

**Example**

`[accspoiler=Secret Stuff]some text[/accspoiler]`

**Usage**

`[accspoiler={TEXT1}]{TEXT2}[/accspoiler]`

**HTML Replace**

```
<div>
<div class="accordion">
<h1><a href="#">{TEXT1}</a></h1>
<div>
{TEXT2}
</div>
</div>
</div>
```

**HelpLine**

`[accspoiler=Title goes here]spoiler text goes here[/accspoiler]`

![alt text](https://raw.github.com/randomessence/jqueryUIloginphpbb3mod/master/contrib/examples/spoiler1.png)

![alt text](https://raw.github.com/randomessence/jqueryUIloginphpbb3mod/master/contrib/examples/spoiler2.png)

**The second BBcode allows to create the full accordion functionality within a phpbb 3 post buy adding extra spoilers.**

**Example**

`[accspoiler=Part 1]some text [accextra=Part 2]some more text[/accextra][/accspoiler]`

**Usage**

`[accextra={TEXT1}]{TEXT2}[/accextra]`

**HTML Replace**

```
</div>
<h1><a href="#">{TEXT1}</a></h1>
<div>
{TEXT2}
```

**Helpline**

 `[accspoiler=] [accspoiler=Title goes here}]spoiler text goes here[/accspoiler]  [/accspoiler]`

![alt text](https://raw.github.com/randomessence/jqueryUIloginphpbb3mod/master/contrib/examples/extra1.png)

![alt text](https://raw.github.com/randomessence/jqueryUIloginphpbb3mod/master/contrib/examples/extra2.png)

**And this is what they look like together in a single post.**

![alt text](https://raw.github.com/randomessence/jqueryUIloginphpbb3mod/master/contrib/examples/full.png)
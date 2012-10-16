
BBCODE

Since the jqueryui framework is loaded onto you board with this mod you can use it for loads of other stuff. here i am going to use it to create an accordion/spoiler type displaye using 2 bbcodes

Usage

[accspoiler={TEXT1}]{TEXT2}[/accspoiler]

HTML Replace

<div>
<div class="accordion">
<h1><a href="#">{TEXT1}</a></h1>
<div>
{TEXT2}
</div>
</div>
</div>

HelpLine

[accspoiler=Title goes here}]spoiler text goes here[/accspoiler]

----------------------

Now to have layers (the full accordion type thing) you use the next bbcode inside the [accspoiler=][/accspoiler].

[accextra={TEXT1}]{TEXT2}[/accextra]

</div>
<h1><a href="#">{TEXT1}</a></h1>
<div>
{TEXT2}

Helpline

 [accspoiler=] [accspoiler=Title goes here}]spoiler text goes here[/accspoiler]  [/accspoiler]
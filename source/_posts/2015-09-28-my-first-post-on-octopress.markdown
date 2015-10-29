---
layout: post
title: "My First Post On Octopress"
date: 2015-09-28 17:46:20 -0400
comments: true
categories: Flatiron School
---

Spatial metaphors permeate our thoughts and language. 

Analyzing a common phrase will proove this point. 
<blockquote>“the meeting is <b>AT</b> 3”. </blockquote>
3 pm is not a physical place, but we use the word <b>AT</b> to describe our relation to it. 

The idea of language and space are inexplicably tied together and are integral for us to be able to communicate with one another. Take for example this Ghanaian commercial from 2009 for Blink Wireless: 

<video width="320" height="240" controls>
  <source src="../images/blink_sd.mp4" type="video/mp4">
</video> 

The idea of spatial metaphors goes back hundreds of years. For instance, this sonnet written by Shakespeare emphasizes the difference between he and the woman he desires by describing the two distinctly different spaces they inhabit: 

<blockquote>
To Jade<br>
Sweet Jade, by whom my transient hopes are dash’d,<br>
To whom persistent fools attend in constant thrall,<br>
Woulds’t not enmesh me in thy web,<br>
That I may browse the fairest form of all?<br>
<b>And tho’ an object not of thy class</b>,<br>
Whose primitive root excites no deference,<br>
Still dare I hope, as Time doth pass,<br>
Thy hidden attributes to reference.<br>
Such vain collections of idle loons<br>
Do dote upon thy treasur’d face,<br>
<b>Shall I then be class’d with these poltroons</b>,<br>
<b>And, tarr’d by their methods, invite disgrace?</b><br>
<br>
Spring me, sweeting, from this fever’d trap,<br>
Or cast me forth to roam the global map.
</blockquote>

Here, the speaker is comparing two Objects, one of great beauty and the other disgraced. The specificity of the language that Shakespeare uses helps to shed light on what each object represents. 

OOP uses physical metaphors to help us interact with abstract ideas. 

Defining our classes and methods with concise, impactful language gives our Objects dynamic meaning and helps the programmer to communicate their intent. 

```ruby
def player_stats(name)
 game_hash.each do |key, value|
   value.each do |k, v|
     v.each do |stuff, more_stuff|
       if stuff == name
         return more_stuff
       end
     end
   end
 end
end
```

If someone unfamiliar with the code were to look at this method, it would be hard to see what the data any of the iterations were operating on. 

After learning to define my methods more clearly the code came out something like this: 

```ruby
def player_stats(player_name)
  player = find_player(player_name)
  player.delete(:player_name)
  player
end
```

Refactoring my code had a similiar affect on my CLI Hangman game. 

My initial outline of the application charged the Game class to be responsible for the Player's guesses. However, while refactoring I began to think that a separate Player class should be responsible for the guess. After all, when describing my intent in an english sentence I would say, “The <b>player</b> guesses the <b>letter</b> that will be printed in the <b>game</b>.” 

I anticipate that as the cohort moves forward with MVC, naming classes will become critical the creating concise descriptive code. In the future, I would love to start a database of synonyms and the etymology for commonly used method and class names. This database would serve as an extremely helpful tool towards choosing exactly the right word for the Object and/or process that I am trying to describe. I eagerly await the challenge ahead to get better at naming in my code. 


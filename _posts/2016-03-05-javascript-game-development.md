---
layout: post
title: JavaScript Game Development — Where to Start?
published: true
date: 2016-03-05
tags:
  - JavaScript
  - Web Development
  - Game Development
---
This is the question that I have asked myself this morning. The JavaScript ecosystem is huge. But today I decided to experiment with something new, how about making something simple and fun — *oh I know a game*.

![A slightly more advanced version of Pong](/assets/uploads/pong.gif "A slightly more advanced version of Pong")

Usually before evaluating any technology choice it’s a good to have requirements in place to pick the right tool for the job (or the shiniest tool for the job). *Do you have requirements*, you ask, yes — Pong. I want to start with a simple prototype of Pong, because I have 0 game development experience (actually, not true I did build BlackJack, Tic-Tac-Toe and Rock Paper Scissors Spock Lizard games in Ruby).

### Unity?

The biggest player in the indie game development scene is [Unity](https://unity3d.com/unity), they offer an end-to-end tooling for the next AAA and indie game makers. But learning C# is not something that I have planned as my next learning topic. It looks like Unity also supports UnityScript which is like JavaScript but [not exactly](http://wiki.unity3d.com/index.php/UnityScript_versus_JavaScript). From my brief exposure to Unity feels a little too heavy handed, I just want to experiment.

### Elm?

![Use Reactive programming you must Yoda meme](/assets/uploads/reactive-programming.jpg)

Another option that I have considered is [Elm](http://elm-lang.org/), it’s an intriguing compile-to-javascript language that promises *0 runtime exceptions*. Some of the example do feature games: [Mario](http://elm-lang.org/examples/mario), [Adventure (Zelda)](http://elm-lang.org/examples/adventure), [Pong ](http://elm-lang.org/examples/pong)and others.

In addition Tobias Hermann offers many praises for the [functional approach to game programming](https://github.com/Dobiasd/articles/blob/master/switching_from_imperative_to_functional_programming_with_games_in_Elm.md) in Elm. It’s also been that inspiration to things like [Redux](http://redux.js.org/). The Elm language is very interesting and I want to come back to it, but it looks like currently there is no set “Game Engine” or any other support library in Elm — everything is do-it-yourself.

### JavaScript?

![I have no idea what I'm doing must blame javascript dog at computer meme](/assets/uploads/blame-javascript.jpg "JavaScript the best language")

*Ok, ok so what about vanilla JavaScript you ask*. Unsurprisingly JavaScript has many libraries and game engines to choose from, [HTML5 Game Engines](http://html5gameengine.com/) and this [Github Wiki](https://github.com/bebraw/jswiki/wiki/Game-Engines) offer some choices. Did I mention choices, oh so many choices. After some research, primarily reading Reddit threads (yes, I know) and looking at the websites of the most popular frameworks (judging-a-frameworks-by-its-homepage™) I am considering these 3, no, 5 game frameworks:

1. [Phaser ](http://phaser.io/)—“A fast, fun and free open source HTML5 game framework”, looks like it has many features, ooh Opal support.
2. [Pixi.js](http://www.pixijs.com/) — “2D webGL renderer with canvas fallback”, its fast?!
3. [Create.js ](http://createjs.com/)— “A suite of JavaScript libraries and tools designed for working with HTML5”, not just games.
4. [Crafty.js](http://craftyjs.com/) —“A flexible framework for Javascript games”, looks small maybe simple too.
5. [gameQuery ](http://gamequeryjs.com/)— “Javascript game engine for jQuery”, looks unmaintained and has a nice SteetFighter demo (unplayable) but hey, it’s jQuery.
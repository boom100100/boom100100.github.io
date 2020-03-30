---
layout: post
title:      "Blackjack CLI Final Project"
date:       2020-03-29 22:15:57 -0400
permalink:  blackjack_cli_final_project
---


Everyone wants to beat the house. Few games in a casino create an environment where that is remotely likely to happen.

But there *is* Blackjack.

With the right training, a player can understand when the odds are in their favor and make a gamble that truely pays off. A player wants to start with a bet that matches their chances of winning, and make it to the end of the hand without busting. Once their part is done, it's good for a player to know if the house is likely to overtake them.

Ideally, the player can figure out the best atrategy before ever stepping into a casino.

Enter Blackjack CLI.

My app is an attempt at simulating the rules and environment of a blackjack table. A user can practice with as many decks of cards as they choose. This is useful because blackjack tables often have more than one deck of cards to thwart card counters. An ongoing running count helps the player keep track of where they are in understanding their odds of winning so that the player can hone the ability to calculate their chances. And multiple computer players create a competitive environment where one player's victory may create an unexpected loss.

Not only is there gaming functionality, but there is also a scraper that takes music and ambiance tracks from a few websites and presents them as an auditory experience that resembles a real casino. Distractions are an important part of the experience, and they can help a player hone razor-sharp focus that will allow making the best possible decisions.

The structure of the project hinges on a separation between controlling the music and playing the game. The scraper for the music is its own concern, while the music controller is elsewhere. The scraper only runs when there are no music tracks in the designated folders.

The game concern manages the components of the game: the players and the cards. The players and the cards are also separate from the game, while also belonging to it. Since there are three types of players (the dealer, the human player, and the computer players), they each require different functionality. While it's possible to have different numbers of decks of cards in play, the players at the table aren't so flexible.

In the spirit of a real casino, the successful player finds that they are punished. An angry dealer kicks out the human player if the player manages to turn the initial investment of 500 chips into over 1 million chips. But not without awarding the player's winnings first.

An aspiring blackjack professional has much to learn and a good deal of money to save from using this app.

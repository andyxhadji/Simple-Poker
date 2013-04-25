Simple-Poker (Java)
===================

One player simple poker, gives you a hand, option to draw a new card, and then evaluates your hand.

HOW TO USE:

Run the program, and it'll show you your cards and ask you to keep or
redraw each one. After you do that, it will display your new hand and 
tell you its evaluation. Then you will be prompted to play again.

To test the program, use the makeHand() method in the Game class. You
can use it to set each card's rank and suit. You also must uncomment
"this.makeHand();" in the play() method.

GameTest class:

This class instantiates the Game class and calls game.play().


Game class:

This class is responsible for instantiating the Deck and PLayer classes
It calls methods in Deck to fill and shuffle it, and then calls a method
in Player to draw from the Deck. The hand is sorted and then it prompts
redraws. Then the hand is sorted again before it is evaluated, to make
evaluation easier. The evaluate() method evaluates the hand, starting 
from royal flush all the way down to highest card. Then the user is
asked if they want to play again.


Card class:

The Card class keeps track of the suit and rank of each card. It also
has a compareTo class so that I can use Arrays.sort() to sort the hand.


Player class:

The Player class has two methods. One is a draw method which returns 
the hand, and the other is a redraw method which returns the next card
the deck.


Deck class:

The Deck class is responsible for filling the deck with 52 Card objects.
It shuffles by taking two random numbers from the size of the deck and 
switching those two card. It does this 2000 times, but it can be changed
by changing SHUFFLE_EXCHANGES in the constructor. Method deal() returns
a hand of 5 cards. redeal() returns the next card in the deck. The 
position of the counter must be refreshed everytime the deck is redealed,
solved by refreshDeckPosition().

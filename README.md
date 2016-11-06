# Math Problems
This repostiory contains a bunch of math problems and their solutions in plain English. I will try to include the source for each problem. Sources might be erroneous or not original.

PRs are welcome.

## Probability and Statistics

1. Find the probability of obtaining four of a kind in an ordinary five-card poker hand. [Ash, Basic Probability Theory]

2. Three balls are dropped into three boxes. Find the probability that exactly one box will be empty. [Ash, Basic Probability Theory]

3. Find the probability of obtaining the A K Q J 10 of at least one suit in a 13-card bridge hand. That is, the probability that the A K Q J 10 of spades, or of hearts, and so on.

## Algorithms and Data Structures


# Solutions

## Probability and Statistics

### 1.

(13)(48) / (52 choose 5)

There are (52 choose 5) distinct poker hands (without regard to order). To obtain four of a kind,

(a) choose the face value to appear four times (13 choices: A, K, Q, ..., 2)

(b) choose the fifth card (52 - 4 = 48 remaing cards to choose from)

Thus *p* = (13)(48) / (52 choose 5)

### 2.

2/3

There are (3 choose 2) ways to choose two non-empty boxes. Now select which box of those two to contain just one (rather than two) balls. Thus *p* = (2) / (3 choose 2) = 2/3

### 3.

(4(47 choose 8) - 6(42 choose 3)) / (52 choose 13)

The number of ways to draw a 13-card bridge hand from a 52-card deck is (52 choose 13). Now, given that the five A K Q J 10 of spades are all in the hand, select 8 of the remaining 47 cards. Thus the probability of drawing the A K Q J 10 of spades in a 13-card bridge hand is (47 choose 8) / (52 choose 13).

Now recall that there are 4 suits in a standard 52-card deck. The probability of drawing the A K Q J 10 of spades or the A K Q J 10 of hearts is thus

(47 choose 8) / (52 choose 13) + (47 choose 8) / (52 choose 13)

= 2(47 choose 8) / (52 choose 13)

However, this does not account for the 13-card hand in which both the A K Q J 10 of spades and the A K Q J 10 of hearts are drawn. Given the fact that those 10 cards are already in the hand, select 3 from the remaining 42 cards to be the remainder cards in the hand. Thus, probability of drawing the A K Q J 10 of either suit, but not both, is (2(47 choose 8) - (42 choose 3)) / (52 choose 13).

It is possible to generalize this problem to all 4 suits. There are 4 different suits, and 6 different unordered pairs of suits. Thus the probability of drawing the A K Q J 10 of any suit is (4(47 choose 8) - 6(42 choose 3)) / (52 choose 13)

## Algorithms and Data Structures

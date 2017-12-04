## Seeding

A brief review of the few build-a-puzzle posts shows that there are two approaches to providing puzzles — seeding and building from scratch.

Strangely, seeding in these examples seems to be done on a unique basis; that is, if a puzzle is provided, it is only used once.

However, if an entire puzzle is rotated, say, it plays as though it were a completely new puzzle. Likewise, if the symbols are switched, again it plays as though new.

My original, seat-of-the-pants calculation was that one puzzle seed could be altered to provide hundreds of thousands of actual puzzles.

## Replication

Gordon Royle at the Minimum Sudoku page details these types of alteration to replicate the original puzzle so that it plays as though it were a different puzzle:

    Barring mistakes, these are guaranteed to be mathematically inequivalent in that no two of them can be translated to each other by any combination of the following operations:

    - Permutations of the 9 symbols,
    - Transposing the matrix (that is, exchanging rows and columns),
    - Permuting (i.e., rearranging) rows within a single block,
    - Permuting (i.e., rearranging) columns within a single block,
    - Permuting the blocks row-wise,
    - Permuting the blocks column-wise.

    This collection of operations forms a group of order

    9! x 6^8 x 2
    = 362,880 x 1,679,616 x 2
    = 609,499,054,080 x 2
    = 1,218,998,108,160

    Note: although not immediately apparent, rotations and reflections are already included in the above list because they can be expressed as combinations of these operations.

http://staffhome.ecm.uwa.edu.au/~00013890/sudokumin.php

## A practical example

The author of “a top selling Sudoku game on the iOS app store,” badweasel, explains his process in an answer on Stack Exchange’s Game Development site.

He notes:

    I call them seed puzzles and here's what I mean. The numbers in a sudoku game are really just tokens. Instead of being the numbers 1-9 they could be colors or symbols or letters. So my seed puzzles are not numbers, they are the letters a-i. Each seed puzzle gets changed on the fly to make a playable puzzle:

    - Randomize the numbers/tokens. When I turn the letters a-i back to into the numbers 1-9 the lookup table is randomized. Meaning that a isn't always 1. That alone creates about 300,000 variations on each puzzle.
    - Rotate the puzzle by 90, 180 or 270 degrees. That adds 4 more variations. [Note: this **adds** 3 more variations, not 4.]
    - Flop the puzzle horizontally, vertically, or both. That adds 4 more variations. [Again, this add 3 more variations, not 4.]

    Each seed puzzle therefore can create 5,806,080 variations. I've tested this in the field with real players. People do not know they're essentially playing the same puzzle. It's impossible actually.  

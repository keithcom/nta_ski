nta_ski
=======

Example NuPIC model to learn the classic text based skiing game

This is a simple example program that is trying to teach a NuPIC HTM how to play the classic text based skiing game.  It starts by feeding the model 1000 lines of perfect positions in a ramdomly generated ski slope.  A slope line consists of 80 characters with two trees as boundaries and the skier (hopefully) in the middle.

              |              H               |                              
            Tree           Skier           Tree

The slope line is encoded as three integer values to pass into the model: the left tree position, the skier position, and the right tree position.

Given the current ski slope line, we ask the model to predict the next skier position.  If the position is greater than the current value, the skier is moved to right one space.  If the position is less than the current value, the skier is moved to the left one space.  Otherwise, the skier position is left alone.

How far can your AI ski before it crashes into the trees?


Credits

The ski game code is based on:
https://github.com/codycollier/ski

And the NuPIC model code is based on the hotgym example at:
https://github.com/numenta/nupic

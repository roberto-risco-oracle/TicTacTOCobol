# Tic Tac ToCOBOL

This is just a version of Tic Tac Toe in COBOL. Based on the project from  ShaunLawrie/TicTacTOBOL
 😜  

For instructions on how to build and run this see [How to Play](https://github.com/BasiliusCarver/TicTacTOBOL#how-to-play) at the bottom of the readme.  

I forked this project to make some experiments on AI automatic translation, aiming to modernize mainframe codebases in Cobol to modern languages that allow to take those workloads to the Cloud. 

Using a file to define win conditions wasn't a very efficient way to do it but but the author wanted to do some basic file operations to see how it worked. Using REDEFINE and breaking the functionality into more paragraphs could massively simplify this version.  

Another version of Tic Tac Toe is at this [blog post on torquingwetstrainers](https://torquingwetstrainers.wordpress.com/2010/01/13/tic-tac-toe-cobol/) which coudl be a lot easier to read than this as it doesn't use a full screen display, colors or a computer opponent.  

You can compile COBOL in freeform with `cobc -free` which relaxes [the old punchcard column enforcement](https://en.wikipedia.org/wiki/Computer_programming_in_the_punched_card_era) so you don't have to start every line with at least 7 spaces to leave room for the punchcard margin but I wrote mine in the old format.  

## Example
![Example Game](./TicTacTOBOL.gif)
[cool-retro-term](https://github.com/Swordfish90/cool-retro-term) was used for this ^

## Features
 - A terrible opponent that just picks random available squares
 - ASCII graphics

## Future Enhancements
 - Blockchain
 - AI
 - Raytracing
 - Webscale

## How to Play
### Online
> **Warning**  
> This no longer works online as they've taken away the STDIN tab on tpcg.io :(  d

Here's a version that kind of works but you have to make all the move choices ahead of time in the STDIN tab. I quickly hacked together a version that works without a real terminal display or file operations so I could run it online http://tpcg.io/28wFoKOu.  
Before you click "execute" paste some input into the STDIN tab e.g.
```
a1
a2
a3
b1
b2
b3
c1
c2
c3
```
### Locally
This one uses a proper terminal display output and looks more like the gif above.  
1. Install a cobol compiler  
`sudo apt install open-cobol`  
2. Compile the COBOL file  
`cobc -W -x -o TicTacTOBOL TicTacTOBOL.cbl`  
3. Run the executable  
`./TicTacTOBOL`  
4. Play the game

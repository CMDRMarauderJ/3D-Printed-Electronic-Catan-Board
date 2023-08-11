# Electronic-Catan-Board
3D printed catan board with electric dice roller, tile rolled LEDs, boardsetup, saveboard, game stats.

Finally Completed! If you can say a project is ever really completed. At least now in a finished playable product.

It all started when I had a nice new 3D Printer and wanted to do something with it. I was watching an episode of Corridor Crew on you tube when they started talking about a 3D Printed Catan board they were working on. I like Catan and I thought that would be a good project to work on.

  As I was planning this my flatmate mentioned that it would be cool if it could have LEDs and light up the squares on a dice roll. The more we talked about it the more I got excited about this idea and the more I realised that it was just outside of my skill level to achieve. Which is the best place to be in my opinion as it would mean I would challenge myself and learn new things. 12 months later I have a finished board.

I started this board having a few things in mind I wanted to get out of it:
	Firstly, that it would have an electronic dice and that the resource square would light up on the roll of the dice.
	That it would be flexible to play either a 2-4 player board or a 5-6 player board.
	That it could have some statistics shown at the end of the game.
	I wanted the board to be able to generate a random board itself but within the rules of Catan board layouts.
	That it could be transportable.

  I started out printing and painting all the board pieces and player pieces. Then made some cases to transport these pieces in. This taught me a lot on using Tinkercad and how to modify other people’s 3d designs for my needs.

  I then designed a layout of how the board would look and function. It was to have a 5-6 player hexagonal layout with 6 player boxes around the game board. These will be on hinges to lift and secure to a lid for transport and storage. When the game board is in 2-4 player mode, I will simply have additional water pieces that I can use to shrink the board down in size. 

  ![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/56b3ee21-7e96-4827-ae8a-00e4dc986c67)

  The board would have mounting bases for all the game board pieces so I could surface mount the LEDs and would give the light more room to diffuse. The resource pieces would also need a transparent surround that would light up on the dice roll. I found transparent PLA filament was very good for this and chose green to give the board a grassy field look. 6 player boxes would sit around the board that would have a LED for turn indication, space for all the player pieces, a 3d printed resource cost's card, and some space for longest road, largest army and last game winner trophies. These would be hinged onto the playfield board and could sit up 90deg so a lid could attach to them somehow. This would make the whole thing smaller in size and protected for storage and transport.

![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/a9cc878d-ef17-4526-aa87-0663eb3773ea)

  I started out making a wood base of ply for the main game board and the player Box’s. I used an acrylic panel for the playfield for mounting the LEDs, I just needed make space for under the board for all the wiring. On testing I found that 1 LED would not be enough to light up a resource pieces and that 3 spaced out was pretty good. So, I purchased a whole bunch of 10mm addressable LEDs for the board and got to work on wiring and soldering them. This was a mistake as it took me a full week at 6 hrs a night wiring this up. If I had to do it again, I would definitely find a quicker way of doing this, perhaps LED rings that you can get from Amazon.

![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/c3d9df53-696e-4f3e-a76e-a87d826d426e)

![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/975daedb-473c-433c-91ed-1edd902480b2)

  You can see in these pictures I had done my measurements wrong and had not accounted for the water pieces when cutting the acrylic. At this stage the board and the acrylic were already made to measurement, and I was not going to redo them. The water pieces still barley fitted into the game base, so it still worked. But now it is going to make it difficult if and when I need to lift the acrylic panel to get to the wiring should I need to in the future once these base pieces are glued down.
  When that was done, I put together the board, and wired up all the player boxes. You can see here that I have used terminal blocks. My mistake was that I used cheap AWG14 %70 copper cable on this. I needed the 2mm cable to get the board as slim and as light as I could, but the nasty %70 copper strands are constantly breaking off the Arduino and the terminal blocks, shortening my cables and making me have to constantly fault find. I imagine someday I am going to have to take it apart and rewire the entire thing. I think bootlaces on the cable ends could help but probably won’t eliminate the problem. Lesson learned not to cheap out on the cable!

![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/9619142b-5bc8-4061-b82b-cb13c5d2af2f)

![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/3647000a-2bae-4d64-ab60-8f7dcdc3b793)

![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/bb648e81-0b16-4617-8d9d-98e1f99366f6)	![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/a58591f4-333e-4680-a045-189745516fe3)

![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/869a0e5b-90c9-43d7-84a3-aca2e5c3447e)

  Once I had a wired-up board done it was onto the coding. I had played with an Arduino once before, using it to do some logic for a home ventilation system I put in my house. But it was very simple and nothing like what I was about to get myself into. I watched a lot of videos and poured through a lot of forums, but I managed to learn all that I needed to achieve what I wanted in the end.
  Each player had a 128 x 64 OLED screen, this was to display some dice animations and other information during the setup phase. I also wanted to see if I could get some game statistics at the end of the game to show up. I started out with an Arduino UNO, but after a while needed to upgrade to a Mega after I started to add in graphics and basic animations. I now know more about the coding by the end of it that I new in the beginning. After learning a few tricks to reduce my code and the memory required for the animations, I think if I overhauled my code, I could get it to fit onto a UNO again. My code really is quite amateur, and I know now that I have done a lot of it the hard and long way. But it’s at a stage where it is working and seems stable. I have a little more skill in it now than when I started but I really don’t have the motivation to go through and overhaul it and retest. If someone ever wanted to pay me a ridiculous amount of money to build another board, I might look at doing that, but I’m just happy its working for now.

  The program evolved a bit as I was coding and testing and finding this that I wanted to add. There will even likely be things I will change or add to the program as I play it more and get suggestions from my friends.
This is its function for now:
  When you power up the board the first step is for each of the players playing to pick which player box they will be using. Once the first player has pressed their button, all other players have 10 seconds to press the button in front of them. The program then locks these players in as being the ‘active’ players and will generate a random resource layout in either a regular size board, or large board for the 5-6 player expansion depending on how many players there are.
  Then the board will light up the LEDs to indicate what the tile resources are that it has created. It is up to the players now to place the resource pieces onto the board as indicated by the colours on the LEDs. The Ports are also indicated by a single LED. Only 2 LEDs are slightly different on the small size board from the expansion board. I have just drawn a small arrow on the board to indicate the relocation of the port square.

![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/6a7ae36e-ade3-4cb1-b864-3b386ba6298b)
 
  After the ports and the resources are placed and player can hold down the button for 3 seconds to advance the program. Next is the layout of the dice roll tokens. As per the rules the tokens are placed in a specific order starting at anyone of the corners of the board and spiralling inward to the centre of the board skipping any deserts. The randomly selects one of these corners and lights it red. Then each next tile in the sequence lights up and spirals into the centre to indicate the sequence. This repeats until you lay out the tokens and press any button for 3 seconds.

![image](https://github.com/CMDRMarauderJ/Electronic-Catan-Board/assets/77212927/6ad5301e-3ab2-450c-acaa-cf10aa0e2709)

  This completes the setup stage and moves onto starting the game. Here I have put in a little title animation and some music, just to jazz up the experience.
After that finishes, the program randomly selects the starting player from all the ‘active’ players that pressed their button at the start of the setup. The player Box LED’s light up in a spinning motion, like a ‘wheel of fortune’ slowly getting slower until it stops on a player.
Then moves into gameplay. The player who’s turn it is has their LED lit up green and can press the button to roll the dice. A dice roll animation plays, then randomly selects two numbers from a 6-sided dice and adds them together, displaying the result. The corresponding tile(s) on the board then flash 3 times to indicate the resources that the dice number landed on. These light up only the surround of the tile piece. The players LED remains green, and no other players button is active until the current turn player presses their button to advance to the next player. The player to the lefts LED then lights up green and they then have the ability to roll. This continues until the game is over.
The 5-6 player expansion has a slightly different sequence to this to account for the ‘Settler 2’ rule. Where the 3rd player to the left of the active player has the ability to do some building after the players turn if they wish. I have accounted for this by lighting up Settler 2’s LED orange while Settler 1 is having there turn. When Settler 1 is finished they can press their button to pass play onto Settler 2. The next player to roll’s LED then turns orange but cannot roll the dice until Settler 2 presses their button to indicate they are done. It repeats like this until the game ends.
When the winner is determined, play can be ended by the winner holding their button down for a few seconds. This then cycles between two sets of statistics. One showing a bar graph of the number of times each dice roll came up, and another showing a bar graph on how much each resource came up.


  As any good programmer does, I copied a lot of my code from other people’s code I found here on GitHub and other places. I learned a lot from these user’s code and am very grateful with everyone willing to put up these repositories for people to freely use.
  A lot of my starting code and initial structure came from jareddilley’s SMART-Catan-game-board that I found on GitHub here. https://github.com/jareddilley. His code for his catan board is simple and elegant, which is very far off my finished product. But this was a launchpad to build my code from. His code for the random board setup is fantastic and took me weeks to figure out how it even worked when I started out, I could never have figured this out without finding his code.
  My code for the dice roll mostly came from Nelson Bowers catan dice I found on YouTube here https://www.youtube.com/watch?v=biL6dSZkcWw&ab_channel=NelsonBowers
Most other code was created by my amateur self, or adapting other solutions for my needs the best I could. I pulled from loads of different how-to’s, beginners guides and forums from the Arduino community.

Anyways hope this helps anyone else trying to get their own project off the ground or inspires someone to build from this and perhaps make something better! If it does, I’d been extremely keen on hearing from you. I will try to do a video of the whole thing in a few weeks and put it up on YouTube.

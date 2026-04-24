## Mastermind for a Xilinx FPGA

I wrote a program in Verilog for a Xilinx FPGA that was essentially the game of Mastermind, where there is a pseudo-randomly generated pattern and you have 10 guesses to determine the pattern,
and each guess will show the number of correct options in the correct spaces and the number of correct options in the incorrect spaces. As stated this was written in Verilog for the Xilinx FPGA.
All the code was written by hand by myself. This project was written using a rather complex state machine as the design restrictions on this specific FPGA were 4 buttons and 16 switches, so there 
was a bit of knowledge on how to play required. Essentially you had one state machine keeping track of the current guess and another keeping track of the current button input.


One challenge of this was setting up that array memory system so a player could return to previous guesses and see how they were scored to make informed guesses on further attempts. 
This was essentially solved by having each switch refer to a turn, and by having only that switch set you could see what that guess was, and how it was scored.
This unfortunately required execution knowledge of the player, but once understood, I think it worked quite nicely.

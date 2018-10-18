# Pong-Breaker
To do List
1.	Game logic
•	Game logic includes the physics, maths, and code logic put in place to create the game. Ball velocity and paddle movement code will be included here.
•	Ball Class should have at least: sprite, xVelocity (speed at which the ball moves on the X axis), yVelocity (speed at which the ball moves on the Y axis), bounding box (collision detection, xPosition, yPosition (xVelocity and yVelocity will determine xPosition and yPosition of the ball sprite). The ball should have a constant movement speed, but the direction should change when it collides with an object (brick, paddle, or other ball)
•	Paddle Class should have at least: sprite, xPosition, yPosition, code to move the paddle on the X axis only. When we test the game logic, we can test the paddle movement using touch controls, but accelerometer controls will move the paddle in the final version and should be implemented as early as possible for balance purposes.
•	Brick class should have at least: sprite, xPos, yPos, and points associated to the brick. If the ball hits a brick, then the player receives the associated points. The brick is then destroyed and the ball’s momentum inverts.
•	Powerups will also have a class of their own. This will likely be a superclass/subclass situation where the specific powerups are children of a parent class that determines when powerups spawn. 
•	Besides the obvious classes, we will also need to implement victory/defeat conditions, brick layouts for different levels, etc. in a GameManager class.
•	AI for the computer player needs to be implemented in logic code. 
2.	Game design
•	Design of the game will involve the creation or referencing of visual assets (sprites, animations), audio assets (sound effects, music) and other effects (screen shake, etc.)
•	The design of the game will be directly related to the feedback to the user since it is what they see once they start the game. 
•	UI design is a part of the game’s design and should not be taken lightly. A graphical user interface to select a level would make sense, with a ‘tap to start’ screen when the player begins. Menus, buttons, sliders, etc. will be part of the UI.
•	The design of the game will relate to how all objects interact in real time to the user. E.g. ball hits paddle, then propels the opposite direction and hits a brick, the brick breaks, and the ball is sent in the opposite direction again, until all bricks are broken, or the ball misses the paddle.
•	Victory condition: all bricks broken AND playerScore > rivalScore
•	Defeat condition: Ball falls past the paddle 3 times OR (all bricks broken AND playerScore < rivalScore)
•	These are just ideas for ending the game. It could be time-based and the player with the most points at the end of the time limit wins, as another example.
3.	Connectivity
•	For simplicity’s sake it might be best to implement multiplayer using a Bluetooth connection as opposed to actual networking.
•	In this case, one device will act as the server and the other device connects to it as the client.
•	Being able to see the other player’s paddle and ball movements in real time might prove difficult.

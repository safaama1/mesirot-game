# Mesirot Game :large_blue_circle: 
The game consists of two or more participants and a [`ball`](https://github.com/safaama1/Mesirot-Game/blob/main/Ball.java) , which is implemented in Java using multithreading and a GUI.<br/>
All the participants in the game stand in a circle and face the other participants. One of them holds the ball in his hand and must throw it to one of the other participants of his choice. The participant who received the ball passes it to another participant (or to the participant from whom he received the ball, depending on his choice) and so on. The person who fails to catch a thrown ball is eliminated from the game, and the person who remains last is declared the winner.<br/>
The game starts with an initial number of [`player`](https://github.com/safaama1/Mesirot-Game/blob/main/Player.java)s (the number is set in the constructor), one player is randomly selected to start passing the ball, and each time one player is randomly selected to pass the ball.<br/>
The number of players is determined before the game starts, as well as the playing time.<br/>

<br/>

_On the attached picture you can see the ball in flight from number 8 to number 2 (the simulator shows the thrower in green and the receiver in red)._

<br/>

![](image/MesirotGame.png)
<br/>

_The [video](https://github.com/safaama1/Mesirot-Game/tree/main/video) folder also contains a video of the simulator in action_.

<br/>

Each player runs on their own **_thread_** and is active for a set amount of time, which is determined when they are created. The player's activity time is a random variable determined by a lottery according to a normal distribution, which gives the mean and variance of the activity time.<br/>
The mean and variance are parameters of the game that are set in the [`Game`](https://github.com/safaama1/Mesirot-Game/blob/main/Game.java) constructor.<br/>
Also in the king of the game, more players are added to the game. The parameters that determine the arrival time of a new player are set in the [`Game`](https://github.com/safaama1/Mesirot-Game/blob/main/Game.java) constructor and are: the mean and variance of the arrival time of a new player.<br/>
The difference between player arrival times is a random variable drawn according to a normal distribution when the mean and variance are given and constant throughout the game.<br/>
Each player has a unique name. The name is a serial number based on the order of entry into the game.<br/>

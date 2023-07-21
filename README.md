# #Summary
<hr>
This project has finally tested my ability to be able to work hours in a row and to be able to publish something finished and with optimized performance thanks to better programming techniques.

## #Project goals

- Building a PC game with *unique* gameplay
- Building a PC game with simple and effective design, to test and improve my skills as designer
- Building a PC game with complex technical structure under the surface, to test and improve my skills as a game programmer
- Building a PC game as optimized as possible, putting before design, after performance and than art


## #Specifications

    - 2 weeks ( 5h / day )
    - Unique Parkour Game
    - Developed in Unreal Engine
    - Textures made in Quixel Mixer


# #Game design
<hr>
The game is inspired by games I played when I was younger like Minecraft Parkour, Crash Bandicoot and a little bit of titan fall 2. 
- I love giving the player the chance to decide 
- I wanted to challenge myself with new things
- Monotony is boring
Because of this, I realized this idea:

## #Game Idea
The player finds himself on a hill (an island) surrounded by an infinite low land (an ocean) and must find a way to escape but if he touches the land, he dies. To avoid dying, he uses his gun to shoot and create obstacles for him to jump over with a fast and easy to control movement.

## #Unique Points

- The *player decides* where to go, not the game. The player creates rooms with different types of obstacles inside
- Each room may contain different obstacles from the previous room, so the player always faces new challenges
- The player evaluates whether or not to take debuffs to obtain other advantages such as a better position to jump
- *** video of graybox and empty rooms (Alpha) ***
  
# #Game design Details

## #Rooms and obstacles
<hr>
- *** video ***
- This Room contains a series of platforms that slowly descend one after another. The player's aim is to be able to climb and reach the top (each platform has a waiting timer that increases based on its own ID. In this way they don't all descend together but sequentially).
- *** video ***
- This Room contains a number of pillars. The pillars are standing still and the player aims to climb high to have an advantage in the next Room.
- *** video ***
- When the player touches the platforms of this Room, after 0.3 seconds he is thrown up. The goal is to reach the top pillar and take a short break before continuing to the next level. It is difficult because to get a good result the player has to jump almost at the same time as the impulse is given. (If the impulse were applied immediately he could not make the jump, because he would never touch a solid surface due to the box collider)
- *** video ***
- When the player enters this level, his gun stops working for 5 seconds. For this reason he is forced to jump on platforms that are destroyed when touched. The player's goal is not to finish the platforms before the gun reactivates.
- *** video ***
- When the player touches the wall, the number of possible jumps is increased to 5. This way he can wall jump without abusing it. Here he must learn how to manage them, too. After he stops touching one of the walls they wait 0.3 seconds and the number of max jumps goes back to 2 (it doesn't make sense in theory, but this way the feeling of the movement is better - whatch with and without delay of 0.3s -). 

## #Movement
<hr>
- **Image here**
- I wanted to make a custom movement system that allowed for more accurate jumping on platforms. This required tweaking how fast the character falls when jumping and allowing the player to have a better experience.
- **Image here**
- This first movement is activated when the player enters a "Wall Jump" room and allows the player to be lighter and faster, helping him to reach distant obstacles. (Disabled when the player exits the room)
- **Image here**
- This second movement is turned on by default and features higher gravity and jumps. This way the player is more accurate and can't cross half the room and jump over all the obstacles.

## #Debuff
<hr>
- **Image**
- Mele and EvilMele (EM) are scattered around the map. Debuffs are applied only when the player picks up an EM.
- EM is a real enemy and should be avoided. The player must constantly think about whether to choose a path even if it will lead him to encounter a debuff.
<hr>
All 3 possible effects:
- **video**
- The player starts sliding, thanks to the change of friction with the ground. This increases the difficulty of the player who has to jump continuously to get back on the platform and not fall.
- **video**
- After 0.5 seconds, the gravity starts changing every 1-2.5 seconds randomly (min 0.6, max 2.1) forcing the player to have to wait and take a small break or risk and have to constantly adapt to a new movement. (By picking up an apple in flight, the gravity could increase and the player could fall. Those 0.5 seconds of waiting are an advantage and a way to avoid making the player die and create too much frustration).
- **video**
- The player loses one HP.


# #Problems and how I solved

## #Extra Jump
<hr>
Within levels, obstacles spawn randomly. this means that there is a very rare chance that they will all spawn in a corner making it impossible for the player to continue.

- This could have been fixed with an extra jump to reach distant locations
- Every time the player collects 5 "Mele" he gets a HP that he can trade for extra jumps. This way the abuse of the triple jump is avoided.
- This skill must be used in a one jump combo, immediately afterwards. The player cannot save himself at the last minute, but must think about it before jumping.
## #score and quest
<hr>
**Img**
There is a score and record counter in the game UI. The player has two ways to increase points:
- Collect apples, each apple awards one point
- Reach a required position. Reaching this position you get 1000 points instantly. In this way the player is encouraged to go where the game asks, to score more points faster.

# #What would I have done
<hr>
 If I had more resources, I would have liked to make the game even more unique and communicate with the player more efficiently.
- For the first point, I would have made each room take the most unique and important features of other games and have obstacles, music, sounds and art inspired by those games (Example: super mario).
- For the second point, I would have liked better particle effects, sounds, models and textures to communicate different moods to the player.

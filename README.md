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
    - Unique Parkur Game
    - Developed in Unreal Egine
    - Texures made in Quixel Mixer


# #Game design
<hr>
The game is inspired by games I played when I was younger like Minecraft Parkour, Crash Bandicoot and a little bit of titan fall 2. 
I love giving the player the chance to decide and I wanted to challenge myself with new things and I hate monotony, so I realized this idea:

## #Game Idea
The player finds himself on a hill (an island) surrounded by an infinite low land (an ocean) and must find a way to escape but if he touches the land, he dies. To avoid dying, he uses his gun to shoot and create obstacles for him to jump over with a fast and easy to control movement.

## #Unique Points

- The *player decides* where to go, not the game. The player creates rooms with different types of obstacles inside
- Each room may contain different obstacles from the previous room, so the player always faces new challenges
- The player evaluates whether or not to take debuffs to obtain other advantages such as a better position to jump
- *** video of graybox and empty rooms (Alpha) ***
# #Game design Details

<hr>
## #Rooms and obstacles
- *** video ***
- This Room contains a series of platforms that slowly descend one after another. The player's aim is to be able to climb and reach the top (each platform has a waiting timer that increases based on its own ID. In this way they don't all descend together but sequentially).
- *** video ***
- This Room contains a number of pillars. The pillars are standing still and the player aims to climb high to have an advantage in the next Room.
- *** video ***
- When the player touches the platforms of this Room, after 0.3 seconds he is thrown up. The goal is to reach the top pillar and take a short break before continuing to the next level. It is difficult because to get a good result the player has to jump almost at the same time as the impulse is given. (If the impulse were applied immediately he could not make the jump, because he would never touch a solid surface due to the box collider)
- *** video ***
- When the player enters this level, his gun stops working for 5 seconds. In this reason he is forced to jump on platforms that are destroyed when touched. The player's goal is not to finish the platforms before the gun reactivates.
- *** video ***
- When the player touches the wall, the number of possible jumps is increased to 5. This way he can wall jump without abusing it. Here too he must learn to manage them. After he stops touching one of the walls they wait 0.3 seconds and the number of max jumps goes back to 2 (it doesn't make sense in theory, but this way the feeling of the movement is better - whatch with and without delay of 0.3s -). 

## #movement

- **Image here**
- I wanted to make a custom movement system that allowed for more accurate jumping on platforms. This required tweaking how fast the character falls when jumping and allowing the player to have a better experience.
- **Image here**
- This first movement is activated when the player enters a "Wall Jump" room and allows the player to be lighter and faster, helping him to reach distant obstacles. (Disabled when the player exits the room)
- **Image here**
- This second movement is turned on by default and features higher gravity and jumps. This way the player is more accurate and can't cross half the room and jump over all the obstacles.

## #debuff

## #Problems and how I solved

### #Extra Jump

### #score and quest

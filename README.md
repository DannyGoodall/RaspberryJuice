# RaspberryJuice

A Bukkit plugin which implements the Minecraft Pi Socket API.

# PythondsMinecraft

A Bukkit plugin which implements Minecraft server from 1.15.1 version
PythondsMinecraft replace id  block numbers ant entity type numbers by MATERIAL, BLOCKDATA and ENTITY names
it implements all the RaspberryJuice - mcpi commands and more ... with specific BlockData

for an exhaustive list and PYTHON EXAMPLES see : http://pinet.rouviere.free.fr/description_mcse/tutoriel_utilisation_mcse__librairie_python.html -> Tutoriel utilisation mcse 

## Commands

### A lot of RaspberryJuice Commands supported are "traduced" in PythondsMinecraft

### some of the RaspberryJuice Extra commands on entity still present but not tested

 - player.pollChatPosts - get events back for posts to the chat for the player
 - player.clearEvents - clear events for the player

 - entity.pollChatPosts - get events back for posts to the chat for an entity
 - entity.clearEvents - clear events for this entity

###  PythondsMinecraft Commands supported
1) Add Blocks Methods - Minecraft Class
------------------------------------------------
- world.setBlock 
- world.setBlocks 
- world.setBlockAge : Material block of  BlockData type Ageable
- world.setBlockBisected : Material block of  BlockData type  Bisected
- world.setBlockDir : Material block of  BlockData type BlockData
- world.SetBlockDistrib : Material block of  BlockData type Dispenser -  version 3.0 and more
- world.setBlockLevel : Material block of  BlockData type  Levelled
- world.setBlockMultiFace : Material block of  BlockData type  MultipleFacing 
- world.setBlockOrient : Material block of  BlockData type  Orientable
- wordl.setBlockPower :  Material block of  BlockData type Powerable - version 3.0 and more
- world.setBlockRotat : Material block of  BlockData type Rotatable
- world.setBlockSapl : Material block of  BlockData type Sapling 
- world.setBlockWithData : set a block with his Blockdata !!! - version 3.0 and more
- world.setBed : Material block of  BlockData type  BED 
- world.setChest : Material block of  BlockData type Chest 
- world.setDoor : Material block of  BlockData type Door 
- world.setEntonnoir : Material block of  BlockData type Hooper - version 3.0 and more
- world.setFence : Material block of  BlockData type  Fence 
- world.setFurnace : Material block of  BlockData type  Furnace 
- world.setGate : Material block of  BlockData type  Gate 
- world.setGindstone :  Material block of  BlockData type Gindstone - version 3.0 and more
- world.setOberver : Material block of  BlockData type Observer - version 3.0 and more
- world.setPane : Material block of  BlockData type stained glass pane
- world.setRail : Material block of  BlockData type rail - version 3.0 and more
- world.setSign : Material block of  BlockData type  Sign (wall or stand)
- world.setSlab : Material block of  BlockData type Slab 
- world.setStairs : Material block of  BlockData type  Stair
- world.setSwitch :  Material block of  BlockData type Switch - version 3.0 and more
- world.setTrapDoor : Material block of  BlockData type TrapDoor
- world.setWall :  Material block of  BlockData type Wall - version 3.0 and more

2) Informations on Blocks Methods - Minecraft Class
----------------------------------------------------
- world.getBlock 
- world.getBlockWithData : Get block and BlockData at X,Y,Z
- world.getHeight 


3) Adding entities (Mobs) Methods - Minecraft Class
----------------------------------------------------
- world.spawnEntity
- world.spawnCat 
- world.spawnHorse 
- world.spawnParrot 
- sworld.pawnRabbit 
- world.spawnWolf 


3) Gestion of entities (Mobs) Methods - Minecraft Class
----------------------------------------------------
- world.getEntityTypes
- world.getEntities 
- world.removeEntities 
- world.removeEntity 
- world.setCustomName 

4) Players Methods - Minecraft Class
-------------------------------------------
- world.getPlayerEntityId 
- world.etPlayerEntityIds 

5) Chat Methods - Minecraft Class
-------------------------------------------
- world.postToChat

6) Player Gestion -  Player Class
------------------------------------------------
- player.getDirection 
- player.getEntities :
- player.getPitch 
- player.getPos 
- player.getRotation 
- player.getTilePos 
- player.pollBlockHits :
- player.pollProjectileHits 
- player.removeEntities 
- player.setDirection 
- player.setPos 
- player.setPich 
- player.setRotation doesn't- Pb with Bukkit version 15.1.1
- player.setTilePos

6) Entity (Mobs) Gestion - Entity clss
------------------------------------------------
- entity.getEntities 
- entity.getDirection 
- entity.getName 
- entity.getPos 
- entity.getPitch 
- entity.pollBlockHits 
- entity.PollProjectileHits :
- entity.getRotation 
- entity.getTilePos 
- entity.removeEntities 
- entity.setDirection 
- entity.setPos 
- ntity.setPitch :
- entity.setRotation doesn't- Pb with Bukkit version 15.1.1
- entity.setTilePos


6) Event Gestion - Event clss
------------------------------------------------
- events.pollBlockHits
- events.PollProjectileHits 

 
 see Python examples on [http://pinet.rouviere.free.fr/description_mcse/tutoriel_utilisation_mcse__librairie_python.html


## Config

Modify config.yml:

 - port: 4711 - the default tcp port can be changed in config.yml
 - location: RELATIVE - determine whether locations are RELATIVE to the spawn point (default like pi) or ABSOLUTE
 - hitclick: RIGHT - determine whether hit events are triggered by LEFT clicks, RIGHT clicks or BOTH 

## Libraries

To use the extra features an modded version of the java and python libraries that were originally supplied by Mojang with the Pi is required, [github.com/zhuowei/RaspberryJuice/tree/master/src/main/resources/mcpi](https://github.com/zhuowei/RaspberryJuice/tree/master/src/main/resources/mcpi).  

You only need the modded libraries to use the extra features, the original libraries supplied with Minecraft Pi edition still work, you just wont be able to use the extra features


To use the PythondsMinecraft plugin, the python mcse library is required : 
[RaspberryJuice/src/pythondsminecraft_src/vxxx/mcse/](https://github.com/sprouviere/RaspberryJuice/tree/master/src/pythondsminecraft_src)
then choose the version of the mcse which depends on the PythondsMinecraft version ie the Minecraft server version

## Build

To build RaspberryJuice, [download and install Maven](https://maven.apache.org/install.html), clone the repository, run `mvn package':

```
git clone https://github.com/zhuowei/RaspberryJuice
cd RaspberryJuice
mvn package
```

##  RaspberryJuice Version history

 - 1.12 - getEntities, removeEntities, pollProjectileHits, events calls by player and entity
 - 1.11 - spawnEntity, setDirection, setRotation, setPitch
 - 1.10.1 - bug fixes
 - 1.10 - left, right, both hit clicks added to config.yml & fixed minor hit events bug
 - 1.9.1 - minor change to improve connection reset
 - 1.9 - relative and absolute positions added to config.yml
 - 1.8 - minecraft version 1.9.2 compatibility
 - 1.7 - added pollChatPosts() & block update performance improvements
 - 1.6 - added getPlayerId(playerName), getDirection, getRotation, getPitch
 - 1.5 - entity functions
 - 1.4.2 - bug fixes
 - 1.4 - bug fixes, port specified in config.yml
 - 1.3 - getHeight, multiplayer, getBlocks
 - 1.2 - added world.getBlockWithData
 - 1.1.1 - block hit events
 - 1.1 - Initial release


##  Pythondsminecraft Version history

 - 2.1 - Initial release for Minecraft server 1.15.1 and later
 - 3.0 - Release for Minecraft server 1.16.1 and later


## Contributors

 - [zhuowei](https://github.com/zhuowei)
 - [martinohanlon](https://github.com/martinohanlon)
 - [jclaggett](https://github.com/jclaggett)
 - [opticyclic](https://github.com/opticyclic)
 - [timcu](https://www.triptera.com.au/wordpress/)
 - [pxai](https://github.com/pxai)
 - [RonTang](https://github.com/RonTang)
 - [Marcinosoft](https://github.com/Marcinosoft)
 - [sprouviere](https://github.com/sprouviere)
 

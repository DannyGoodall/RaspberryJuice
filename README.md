# RaspberryJuice

A Bukkit plugin which implements the Minecraft Pi Socket API.

# PythondsMinecraft

A Bukkit plugin which implements Minecraft server from 1.15.1 version
PythondsMinecraft replace id  block numbers ant entity type numbers by MATERIAL, BLOCKDATA and ENTITY names
it implements all the RaspberryJuice - mcpi commands and more ... with specific BlockData

for an exhaustive list see : http://pinet.rouviere.free.fr/description_mcse/tutoriel_utilisation_mcse__librairie_python.html


## Commands

###  RaspberryJuice Commands supported

 - world.get/setBlock
 - world.getBlockWithData
 - world.setBlocks
 - world.getPlayerIds
 - world.getBlocks
 - chat.post
 - events.clear
 - events.block.hits
 - player.getTile
 - player.setTile
 - player.getPos
 - player.setPos
 - world.getHeight
 - entity.getTile
 - entity.setTile
 - entity.getPos
 - entity.setPos

### RaspberryJuice Commands that can't be supported

 - Camera angles

### RaspberryJuice Extra commands

 - getBlocks(x1,y1,z1,x2,y2,z2) implemented
 - getDirection, getRotation, getPitch functions - get the 'direction' players and entities are facing
 - setDirection, setRotation, setPitch functions - set the 'direction' players and entities are facing
 - getPlayerId(playerName) - get the entity of a player by name
 - pollChatPosts() - get events back for posts to the chat
 - setSign(x,y,z,block type id,data,line1,line2,line3,line4)
   - Wall signs (id=68 or block.SIGN_WALL.id) require data for facing direction 2=north, 3=south, 4=west, 5=east
   - Standing signs (id=63 or block.SIGN_STANDING.id) require data for facing rotation (0-15) 0=south, 4=west, 8=north, 12=east
 - spawnEntity(x,y,z,entity) - creates an entity and returns its entity id. see entity.py for list.
 - getEntityTypes - returns all the entities supported by the server.
 - entity.getName(id) - get a player name for entity id. Reverse of getPlayerId(playerName)
 - getEntities - get all currently loaded entities list by optional entity type id
 - removeEntity - removes entity with specified id
 - removeEntities - removes all currently loaded entities by optional entity type id
 - entity.getEntities - get currently loaded entities list near specified entity by optional entity type id
 - entity.removeEntities - removes currently loaded entities near specified entity, by optional entity type id
 - player.getEntities - get currently loaded entities list near specified player entity id by optional entity type id
 - player.removeEntities - removes currently loaded entities near specified player entity id, by optional entity type id
 - events.pollProjectileHits - get events back of arrow hit
 - player.pollProjectileHits - get events back of arrow hit for the player
 - player.pollBlockHits - get block hits for the player
 - player.pollChatPosts - get events back for posts to the chat for the player
 - player.clearEvents - clear events for the player
 - entity.pollProjectileHits - get events back of arrow hit for an entity
 - entity.pollBlockHits - get block hits for an entity
 - entity.pollChatPosts - get events back for posts to the chat for an entity
 - entity.clearEvents - clear events for this entity
 
Note - extra features are NOT guaranteed to be maintained in future releases, particularly if updates are made to the original Pi API which replace the functionality

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


- world.getBlock 
- world.getBlockWithData : Get block and BlockData at X,Y,Z
- world.getHeight 
- world.getEntityTypes
- world.getEntities 
- world.removeEntity 
- world.removeEntities 
- world.setCustomName 
- world.spawnEntity 
- world.spawnCat 
- world.spawnHorse 
- world.spawnParrot 
- sworld.pawnRabbit 
- world.spawnWolf 
- world.getPlayerEntityId 
- world.etPlayerEntityIds 
- world.postToChat

- player.getDirection 
- player.getEntities :
- player.getPitch 
- player.getPos 
- player.getRotation 
- player.pollBlockHits :
- player.pollProjectileHits 
- player.removeEntities 
- player.getTilePos 
- player.setDirection 
- player.setPos 
- player.setPich 
- player.setRotation doesn't- Pb with Bukkit version 15.1.1
- player.setTilePos

- entity.getEntities 
- entity.getDirection 
- entity.getName 
- entity.getPos 
- entity.getPitch 
- entity.getRotation -entity.getTilePos 
- entity.pollBlockHits 
- entity.PollProjectileHits :
- ntity.removeEntities 
- ntity.setDirection 
- entity.setPos 
- ntity.setPitch :
- entity.setRotation doesn't- Pb with Bukkit version 15.1.1
- entity.setTilePos

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
 

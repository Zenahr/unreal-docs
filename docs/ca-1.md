---
id: ca-1
title: Clickable Actors (Part 1) - GameMode & PlayerController
sidebar_label: Clickable Actors (Part 1)
---

## Goal

Sometimes we would like to interact with our game objects via click events. This is useful for many things, such as product configurators, 3d menus or if you'd like to make a elaborate settings menu but don't want to mess with UMG/Slate for the UI.

## Setup

1. Create a new Player Controller Blueprint
2. Under _Mouse Interface_ inside the _Details_ panel enable the following options:
- Show Mouse Cursor
- Enable Click Events
- Enable Mouse Over Events

For convinience sake let's enable touch screen support too:
- Enable Touch Events
- Enable Touch Over Events

Now create a new GameMode Blueprint.

We need to specify the new Player Controller as our _Player Controller Class_ inside the _Classes_ panel found in the _Details_ panel.
Also we need to override the GameMode inside our _World Settings_ for our current level.

Make sure your level has a _Player Start_.
You should now be able to move around and see the Mouse Cursor when playing the game.

# Deactivating Movement by Mouse Cursor (Posessing a static Camera Actor)

You might have noticed that you can move freely at the moment. This might not be intended. For our purposes we'd like to decouple the character movement from the mouse input.

# Setting Up A Static Camera Actor

1. Add a Camera Actor to the level
2. Pilot the and position it to the place you want it to be.
3. Rename the Camera to "Cam" (optional)
4. Open the Level Blueprint

5. Get Player Controller
6. Drag a _Set View Target with Blend_ node out of the value socket of your Get Player Controller node
7. Chain the _Set View Target with Blend_ node to the _Event BeginPlay_ node.
8. Pull your "Cam" actor from the _World Outline_ into the Level Blueprint. This creates a reference to your "Cam" actor. (You should see a "from persistent level" text showing up under the Node)
9. Plug your _Cam_ actor reference into the _New View Target_ socket of the _Set View Target with Blend_ node.
10. Compile & Save

Now we have set up the control side of things. Next up is setting up Click Events.
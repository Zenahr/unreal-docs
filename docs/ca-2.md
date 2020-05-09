---
id: ca-2
title: Setting Up Click Events
sidebar_label: Setting Up Click Events
---

# Introduction

We want to fire off events by clicking on actors in our scene. This is how to accomplish it: 

# Setup

1. Create a new Blueprint.
2. Add a mesh component to it.
3. With the mesh component selected, click on _On Clicked_ inside the _Events_ category on the _Details_ panel.
4. Feel free to add _On Begin Cursor Over_ and _On End Cursor Over_ events as well.

This adds Events to the _Event Graph_ of your Blueprint.
Open up the _Event Graph_ to customize the Events.

To check wether the events get triggered or not, simply chain a _Print String_ node to your Events

5. Place your Blueprint Actor into the scene.
6. Play and click on the Actor.
7. You should now see your log message displayed in the upper-left corner of your viewport.
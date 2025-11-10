---
layout: post
title:  "Off The Grid"
thumbnail: "/assets/img/off_the_grid/cover.webp"
date:   2025-10-22 16:59:24 +0200
categories: project professional
releasedate: 10/08/24
website: https://gameoffthegrid.com/
websitesteam: https://store.steampowered.com/app/3659280/Off_The_Grid/
websiteepic: https://store.epicgames.com/en-US/p/off-the-grid-7e3cc5
tools:  [Unreal Engine 5, Visual Studio, Perforce, Jira/Confluence]
permalink: "/:title/"
imgpath: "/assets/img/off_the_grid/"
videopath: "/assets/video/OffTheGridSteamLaunchTrailer.mp4"
professional: true
---

Off The Grid is an extraction battle royal third person shooter.
It's main distinctive feature are the cyberlimbs, arms and legs that can be changed during the game to gain different abilities, and the jetpack of the player, giving a lot of movement freedom.

I started as a Junior Gameplay Programmer in May 2022, as the (then) sole programmer on the Cyberlimbs team.
Initially I worked on prototype limbs, based on basic designs from the cyberlimbs game designers.
All of them were quite basic but still viable for playtesting in our internal playtests.
A few examples of these were:
  - Sticky Goo Arm: A field of "magnetic" liquid, slowing down enemies caught in it.
  - Micro Missiles Arm: Missiles that can be fired in an arc around obstacles
  - Mortar Legs: Indirect fire from your legs, aimed via a in-world arc

All of these would change over time, mostly keeping their original purpose but improving their viability and refining their design.

Later on  I was asked to taker over the implementation of a prototype vehicle, a 4 seater(driver, 2 passengers and 1 top turret gunner).
This was done with and on top of the experimental UE5 Chaos vehicle plugin(for general vehicle simulation).  
I worked on the driving, camera, turret and partial implementation of VFX/SFX (so almost everything :)).  
The vehicle feature was cancelled later on, the plans for the map changed and the jetpack was made more prominent.

As part of the ongoing cyberlimb improvements I created a propgation system, used for liquids and gases.  
It's using a 3D grid of points that are sampled via different collision traces plus additional logic, similar to voxels but just using points.  
This was used mainly for the aforementioned Sticky Goo Arm(now the goo can spread dynamically through the world, along surfaces) and the Toxic Smoke Arm(shooting a projectile exploding in a big gas volume, where the gas is spreading outwards through openings and along walls).  
This allows these effects to adjust dynamically to its surroundings and (potentially) create some unique situations.

Over my three years I was promoted from Junior to regular and later Senior Gameplay Programmer, at some point being responsible for the implementations of all cyberlimbs, although more programmers were joining the team soon after.
I worked on 11+ limbs(not all of them made it to release) as well as base code for limbs, such as their recharging mechanics or asset memory management.  

The list of limbs I worked on in a major capacity(these are the internal names, I never got used to the ingame names):
  - Sticky Goo Arm: As described above
  - Micro Missiles Arm: Allows locking on to enemies in line of sight and firing several homing missiles at locked on targets
  - Jump Boost Legs: Jump far and high, to reach ledges/floors or to escape
  - Mortar Legs: Select 3 targets on a tablet showing the game map and start shooting projectiles from your leg, in a mortar like fashion
  - Super Sprint Legs: Gain increased sprint speed as well as leave a trail behind when sprinting, allowing anyone else to also gain the increased sprint speed
  - Toxic Smoke Arm: As described above
  - Katana Arm: Dash forward and swing/stab the sword blade from inside your arm
  - Spider Mine Arm: Shoot/Place mines that explode when an enemy runs into the laser triggers
  - Assault Drone: Spawn a companion drone that follows you and shoots at your enemies
  - Cloak Arm: Place a cloaking device that spawns a cloaking area, making you near invisible when standing still or moving slowly. Actions such as shooting interrupt the cloak for a brief amount of time.
  - Kinetic Shield: Open your arm up to activate an energy shield, blocking bullet and explosion damage.

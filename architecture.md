# Jumpman Plumber Game

### Software Architecture Document (SAD)
Version 0.1 

## Revision History

| Date    | Version   | Description   | Author   |
|:-------:|:---------:|:-------------:|:-------------:|
| 2/29/19 | 0.1       | First Draft   |  RunTimeTerror |

## Table of Contents

1. Introduction
    
    1. Purpose

        1. SAD

        2. Game

2. Overview
    
    1. Key Terms

    2. Representation
    
    3. Framework

3. Architectural Goals

    1. Standards
       
    2. Constraints
    
    
## Introduction

**Purpose**


This document is designed to explain the software design of Jumpman Plumber
and its architecture. It will give an overview of the various systems
that Jumpman Plumber utilizes and define features that are novel to Jumpman Plumber. 
It will also provide key terms that will be useful to the user as they play our Java game. 

## Overview

**Key Terms**

This section defines some terminology that is useful when speaking
about video game design and our game, Jumpman Plumber

- *Administrators (admins)* - Also known as sysadmin, a person who is responsible for the upkeep, configuration, and reliable operation of computer systems
- *Animation* - A collection of images that are displayed in an order to 
express movement
- *Animator* - A system that displays images in a certain order to 
form an animation. The system is a finite state machine that is defined by the
core logic
- *Bitmap* - A picture created on a visual display unit where each pixel corresponds to one or more bits in memory, the number of bits per pixel determining the number of available colors
- *Bug* - An unwanted and unintended property of a program or piece of hardware, especially one that causes it to malfunction. E.g. "There's a bug in the editor: it writes things out backward." The identification and removal of bugs in a program is called "debugging".
- *Collider* - A theoretical area where a game object exists and can
be interacted with by other game objects or the mechanics
- *Controller* - A means of control over the console or PC on which the game is played. In Jumpman Plumber's case, we use the keyboard to navigate throughout the game.
- *Double Jump* - Being able to jump (once) while already in the air and not in contact with anything. The player must then typically touch the ground before being able to mid-air jump again
- *Emulator* - A software program that is designed to replicate the software and hardware of a video game console on more-modern computers and other devices. Emulators typically include the ability to load software images of cartridges and other similar hardware-based game distribution methods from the earlier hardware generations, in addition to more-traditional software images.
- *Game Character* - A character in a video game or role playing game who is controlled or controllable by a player
- *Game Engine* - The code on which a game runs. There are different subsets of engines such as physics engines and graphics engines
- *Game Loop* - The main procedure of the game, where all higher level
systems are called from
- *Game Object* - A theoretical representation of an object in the game.
All interactive elements in the game stem from this concept.
- *Game Over* - 1.  The end of the game.
2.  The failure screen shown at a game loss.
- *High Level Systems* - Broad systems in the architecture that govern many
small functions and utilities. These are the Animator, Mechanics, Core Logic, Input and Ouput.
- *Input* - The keyboard/joystick events that come from the user
- *Jump* - A basic move where the player jumps vertically
- *Level* - A section or part of a game. Most games are so large that they are broken up into levels, so only one portion of the game needs to load at one time. To complete a game level, a gamer usually needs to meet specific goals or perform a specific task to advance to the next level.
- *Life* - One or multiple chances that a player has to retry a task after failing. Losing all of one's lives is usually a loss condition and may force the player to start over.
- *Mechanics* - A System that dictates the possible outcomes in the game via a set of clearly defined rules.
It is analogous to the way that Physics dictate the possible outcomes in the 
real world. Note that the system does not define each individual outcome,
it only defines what can happen from event to event.
- *Output* - The Graphical User Interface (GUI) for the game. Here, the screen with
two fighters on it along with some other information about the state of the game
- *Rendering* - Drawing elements on a screen with pixel math
- *Sprite Sheet* - An array of images that are equal in pixel area
that are displayed frame-wise to form an animation
- *Finite State Machine* - A system that has a clearly defined set of
states that are mutually exclusive and can be transitioned to only from 
certain other states by a clearly defined set of actions. A very important
concept that is essential to the Animation, Core Logic and I/O 
- *Upgrade* - A way to make the given item, character, etc. more powerful.


**Representation**

This section describes the three ways in which we will talk about SUMOH.


The first will be the user-facing or Front-End view. A view of the software
that is Abstracted from every system except the input and output. This view
is helpful when making design decisions that will impact user experience.


The Second will be the system-facing or Back-End view. This view examines
the interactions between high level systems in the code and the results of 
those interactions. This view is essential for understanding the design and implementation
of large-scale features in the game.

The final view will be the code-facing or low-level view. This view is at the unit level
and examines the way in which individual code elements perform their tasks and their input and
output. This view is essential for testing and optimization.

**Framework**

This section explains the framework that SUMOH is modeled after.

## Architectural Goals

**Standards**

This sections describes the requirements that SUMOH must satisfy to be considered viable
software

**Restraints**

This section describes the limitations that the developers of SUMOH are bound by 


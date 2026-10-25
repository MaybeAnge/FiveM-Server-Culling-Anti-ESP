# FiveM-Server-Culling-Anti-ESP

<p align="center">
  <a href="https://youtu.be/SEYKExYM3Es">
    <img src="https://img.youtube.com/vi/SEYKExYM3Es/0.jpg" alt="Vidéo YouTube" width="480"/>
  </a>
</p>

<p align="center">
  <a href="https://imnotcheating.eu/">
    <img src="https://imnotcheating.eu/assets/images/ImNotCheatingBanner.png" alt="Vidéo YouTube" width="480"/>
  </a>
</p>

# Overview
This video presents a server culling system for FiveM that goes after the root of the ESP problem: player data is simply no longer sent to the client unless it has a legitimate reason to see it.
No code is provided. The technique used is deliberately kept private.

For the demonstration, I rebuilt a working ESP using FiveM’s DrawText function. It displays player information such as name, position and distance through walls, just like a classic cheat ESP would. It serves as the reference for the video: first the ESP running without protection, then the same ESP running with the protection enabled.

# How It Works
Whatever the cheat, an ESP needs a source of information. It reads what the game has already loaded: the players present in the client’s memory, along with their positions and data.
This system acts before that step. When a player is not supposed to be visible to you, the server stops sending you any data about them. They no longer exist in your memory, so there is nothing left to read, display or exploit, even for a very advanced ESP that scans RAM.

# What Makes It Effective
The visibility check is based on the camera, not on the character. It is calculated from what your camera can actually see, so if you lean your camera out of a wall corner to look at a player, they appear exactly as they would in the normal game. The system also anticipates movement: it predicts both the player’s trajectory and your camera’s, so a player is loaded just before becoming visible and never pops in suddenly in front of you. A short grace period after losing sight prevents flickering when you move the camera quickly, and visibility stays consistent between players, so if A can see B, both are properly synchronized without desync or invisible players at close range. All checks are spread over time and limited to players within range, which keeps performance under control.

# Result
On the test bench, the ESP is cut off: players behind walls no longer show up. The system is designed to counter the ESPs of black market cheats such as Keyser, Susano, Omerta Software, Vanity and many others, because they all rely on the same thing: reading, from memory, data that the server sent them. Since the server no longer sends that data, the cheat has nothing left to display, regardless of the technology it uses to read it.

Cheaters pay a fortune for software that is completely useless the moment the server stops feeding it data. I didn’t just counter your ESP, I made it blind. Every cheat on the market, no matter what technology it uses, just got humiliated. 🔥

Maybe Ange,<br>
ImNotCheating.

<p align="center">
  <a href="https://imnotcheating.eu/">
    <img src="https://imnotcheating.eu/assets/images/ImNotCheatingLogo.png" alt="Vidéo YouTube" width="480"/>
  </a>
</p>

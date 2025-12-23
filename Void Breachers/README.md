# Void Breachers

> [!TIP]
> - 2 Lvl: Many Bots outside the Spaceship, 1 Boss bot inside the Spaceship.
> - As the Player fights and wins over the Boss Bot/ Player, they will get a Genome Drive which will save them from the toxic gases and come out of the Enemy Spaceship.
> - Refer [Foundation Galactic Frontier](https://play.google.com/store/apps/details?id=com.games.foundation) for 3D Game angle UI style in 2D, Combat mode, Spaceship style 

---

🚀 Game: VOID BREACHERS

Tagline: Gravity is a Luxury. Dominate the Void.

The Year is 2142. Factions wage war in Earth's orbital debris field. The prize is the HELIX STATION, the last source of oxygen and fuel. You are a BREACHER, an elite soldier equipped for high-speed, zero-gravity warfare. Your jetpack is your life; your weapons are your key to survival. With only 3 Remote-Link Lives, every move counts.

---

🎮 CORE GAME LOOP

1. DEPLOY: Choose a game mode and load into the lobby/spawn ship.
2. THRUST & GRAPPLE: Use omnidirectional jetpack thrusters and a grappling hook to navigate the 3D battlefield of derelict ships and the Helix Station.
3. FIGHT & MANAGE: Engage in fast-paced combat using a Plasma Gun (breaks shields) and Railgun (deals final damage). Manage your Fuel and Health.
4. RESUPPLY: Dock at Supply Stations on the map to refill Fuel, Health, and Ammo. You are vulnerable while docking.
5. COMPLETE OBJECTIVE: Fight for your team's win condition (destroy enemy base, get most kills).
6. SURVIVE OR PERISH: You have 3 lives. Lose them all, and you're out for the match.

---

⚙️ KEY SYSTEMS

1. Movement (Zero-G Physics)

· Omnidirectional Jetpack: Move in full 360 degrees. A blue Fuel bar depletes with use. Zero fuel leaves you drifting helplessly until it recharges.
· Zero-G Drift: Release thrusters to drift on momentum, conserving fuel and becoming a harder target.
· Grappling Hook: Swing around debris for speed or pull yourself toward/away from enemies or objectives.

2. Combat & Survival

· Two-Weapon Meta:
  · Plasma Gun: Fast-firing, breaks enemy energy shields.
  · Railgun: Slow-firing, high-impact. Effective against unshielded targets for final hits.
· Health System: You can survive 2 hits. A 3rd hit eliminates one of your lives. Health can only be restored by docking at a Supply Station.
· Permadeath: Each player has 3 Remote-Link Lives per match. After the 3rd death, the player is eliminated permanently for that round.

3. Resupply & Safe Zones

· Supply Stations: Scattered static docks on the map. Docking refills Health, Fuel, and Ammo.
· Critical Vulnerability: You cannot shoot or be shot while docked. Teammates must provide cover.

---

🏆 GAME MODES & OBJECTIVES

Your notes outline three primary competitive modes. All are team-based (e.g., 2v2, 3v3, up to 5v5).

Mode Attacker Goal Defender Goal Win Condition
DESTROY THE MOTHERSHIP Destroy the enemy team's Spaceship (Mobile Base). It has 5 Hull Points (weak spots). Protect your own Spaceship. Attackers win if they destroy the enemy ship. Defenders win if time runs out or they eliminate all attackers.
ASSAULT THE STATION Destroy the enemy team's Space Station. It has 10 Structural Weak Points. Protect the Helix Station. Attackers win by destroying all 10 weak points.
ANNIHILATION Eliminate the opposing team. Eliminate the opposing team. Team with the most total kills when time expires wins.

How it works: In Destroy the Mothership and Assault the Station, both teams have the same objective simultaneously. You must attack the enemy base while desperately defending your own.

---

🕹️ PLAYER MODES

1. Multiplayer (Primary Mode)

· Lobby System: Create/Join rooms globally.
· Room Settings: Room owner can set team size (1v1 to 5v5), map, and mode.
· Matchmaking: "Play Online" to join a random room or "Join by Username" for private matches.

2. Single Player with Bots

· Practice & Offline Play: Play any mode (1v1, 2v2, etc.) populated with AI bots.
· Bot Difficulty: Adjustable settings (Easy, Medium, Hard).

3. Training Section

A dedicated area to master mechanics without pressure:

· Shooting Range: Stationary and moving targets. Practice the Plasma/Railgun combo.
· Mobility Course: An obstacle course of debris and rings to master jetpack thruster control, drifting, and grappling.
· Combat Simulator: Fight against dummy enemies that don't shoot back.

---

📊 PROGRESSION & REWARDS

- In-Match Progression: Perform actions (kills, assists, objective damage) to earn points for temporary in-match upgrades (e.g., faster fuel recharge, stronger shields for one life).

- Cosmetic Unlocks: Earn credits from matches to buy skins for your Breacher, jetpack trails, weapon camos, and victory emotes.
- Ranked Mode (Future): A competitive ladder for the Multiplayer mode with seasonal rewards.

---

🎯 NEXT STEPS FOR DEVELOPMENT (Your Unity Project)

This structure is now clean and focused. Your immediate next steps should be:

1. Finalize Core Design: Lock this document as your "Version 1.0" design.

2. Start Prototyping in Unity (Ubuntu):
   - Week 1-2: Build the Zero-G Movement Prototype. Create a player capsule with Rigidbody, script the jetpack thrusters, fuel bar, and basic grappling hook. This is your most critical system.
   - Week 3-4: Build the Combat Prototype. Add the two weapon types with different fire rates and the shield/health damage system.
   - Week 5-6: Build a Single Test Map & One Game Mode. Create a small space arena with one Supply Station and implement the "Annihilation" (most kills) mode first—it's the simplest.
   - Week 7-8: Integate UI, Polish, and Bots. Add health/fuel UI, a basic main menu, and simple AI bots for your Single Player mode.



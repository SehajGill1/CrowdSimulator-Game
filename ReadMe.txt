CS 4332.001 – Crowd Simulator (Assignment 3)
Name: Sehaj Gill
NetID: ssg190004
Submission Date: 4/22/25
Platform: Windows 11, AMD Radeon(TM) Graphics
Unity Version: 6000.0.34f1

Description:
This project is a crowd simulation game built in Unity where over 25 NPCs walk around the map on their own. They randomly pick places to go, walk there using AI pathfinding, and then go idle after every 6 stops. The player can move around in first-person and throw grenades, which cause nearby NPCs to run away in fear. NPCs also avoid bumping into the player and obstacles like cylinders placed around the scene. They have smooth animations for walking, running, and stopping, which makes the whole simulation feel more realistic and alive.


Features Implemented:
- First-person character with keyboard/mouse control  
- Grenade throwing system (G key)  
- Explosion effect with Particle System  
- NPCs with NavMeshAgent and Animator  
- 6-goal wander behavior (looping with idle in between)  
- Fleeing behavior from grenade (with animation + rerouting)  
- Obstacle and player avoidance (10+ cylinders, distance-based logic)  
- Fully implemented idle state: NPCs stop all movement and animation for 4 seconds after each wander cycle

Assets Used:
- All assets provided in the CrowdStarter package
- No external assets downloaded

Challenges Faced:
- Ensuring NPCs actually stop movement during idle (solved with 'agent.isStopped', 'ResetPath()', and animation fixes)
- Preventing NPCs from clipping through obstacles when fleeing (solved using 'NavMesh.SamplePosition()' for safe rerouting)
- Syncing Animator states with velocity and state flags to clearly distinguish idle vs walk vs run

Demo Video:
https://youtu.be/KLUhb2CU6PA

To Play:
1. Press Play in Unity.
2. Use "WASD" + (mouse) to move and look around.
3. Press "G" to throw a grenade.
4. Observe NPCs as they wander, flee, and idle around the map.


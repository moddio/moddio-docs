# Run On: Local vs. Server

In Moddio, scripts can be set to **Run On** either the **Local** side (client) or the **Server** side. This choice determines **where** and **how** your code executes, which can affect performance, security, and gameplay synchronization.

---

## Local Scripts

**What They Are**  
- Local scripts run **on the client**—which is typically the player’s computer or device.  
**When to Use Them**  
  - **UI Interactions & Effects**: Animations, interface elements, and any visual updates that don’t affect the entire game world.  
  - **Immediate Feedback**: Quick client-side responses to user input (e.g., highlighting a button, playing a sound).  
  - **Non-Critical Checks**: Light calculations or checks that don’t need authoritative confirmation from the server.  

**Pros**  
1. **Fast Response**: Minimal latency, since you don’t wait for the server to confirm each interaction.  
2. **Reduced Server Load**: Frees up server resources by handling small tasks locally.

**Cons**  
1. **Not Authoritative**: Changes made locally can be overridden or invalidated if the server has different logic.  
2. **Easy to Exploit** (in some contexts): If your game is competitive, purely local checks can be vulnerable to cheats or manipulation.

---

## Server Scripts

**What They Are**  
- Server scripts run on the **Moddio server** (or host authority in a P2P context).  
**When to Use Them**  
  - **Authoritative Game Logic**: Health calculations, item creation, or major world changes that affect **all players**.  
  - **Security & Anti-Cheat**: Ensuring only valid moves or actions are accepted, preventing cheating.  
  - **Global State**: Anything that must remain consistent across the entire multiplayer session (e.g., scoreboard, spawning enemies).  

**Pros**  
1. **Authoritative & Secure**: Harder for players to tamper with server-side logic.  
2. **Reliable Synchronization**: The server can broadcast updates to every client, keeping everyone in sync.

**Cons**  
1. **Higher Latency**: Player actions must travel to the server, so real-time feedback can feel slower.  
2. **Increased Server Load**: Complex calculations on the server can impact performance for all players.

---

## Choosing Local or Server

1. **Is the Logic Critical to All Players?**  
   - If yes, **Server** scripts ensure consistent, cheat-resistant behavior.  
   - If no, **Local** can be faster for client-side visuals or simple interactions.
2. **Does It Affect Game State or Shared Resources?**  
   - For awarding points, managing inventory, or spawning entities for everyone, prefer the **Server**.  
   - For showing an animated UI or a personal effect (like a local sound), go **Local**.
3. **Performance vs. Security**  
   - **Local** scripts reduce server load but can be less secure.  
   - **Server** scripts add overhead but prevent unauthorized changes.
4. **Hybrid Approaches**  
   - Use **Local** for instant feedback or visuals, then **Server** to validate and update game-wide data.  
   - This balance offers responsive gameplay without sacrificing security.


## 🔗 Continue Learning
- **[Triggers →](using-scripts/script-editor/triggers.md)**
- **[Actions →](using-scripts/script-editor/actions.md)**
- **[Unit Scripts →](using-scripts/script-editor/unit_scripts.md)**
- **[Item Scripts →](using-scripts/script-editor/item_scripts.md)**
- **[Projectile Scripts →](using-scripts/script-editor/projectile_scripts.md)**

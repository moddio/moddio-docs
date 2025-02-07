---
# Beginner's Guide to Modd.io Map Editor

**Modd.io** is a platform for creating and sharing multiplayer online games. This guide covers the essentials of designing game worlds using the map editor.

---
## **Interface Overview**

<div style="text-align: center;">
  <img 
    src="Imgs/map_editor.PNG"
    alt="Modd.io Map Editor"
    title="Modd.io Map Editor"
    style="width: 12000px; height: auto;" />
</div>


The editor interface includes these key components (visual layout reference):
- **Canvas (Center)**: Your main workspace for designing the map.
- **Toolbar (Top)**: Access tools like Cursor, Stamp Brush, and Layers.
- **Properties Panel (Right)**: Edit settings for selected objects/tiles (e.g., size, collision).
- **Tile Palette (Bottom Right)**: Choose tiles to paint onto layers.
- **Layer Selector (Top Left)**: Switch between layers (e.g., Floor, Walls).

---

## **Core Tools & Shortcuts**
### **Editing Tools**
| Tool | Shortcut | Function |
|------|----------|----------|
| **Cursor** | `C` | Select/move objects or regions. |
| **Entities** | `A` | Place interactive objects (e.g., spawn points, items). |
| **Stamp Brush** | `B` | Paint tiles (LMB) or copy/paste (RMB) on the active layer. |
| **Eraser** | `E` | Remove tiles from the active layer. |
| **Bucket Fill** | `F` | Fill connected areas with the selected tile. |
| **Region** | `R` | Define gameplay zones (e.g., team bases). |

### **Actions**
| Action | Shortcut |
|--------|----------|
| Undo | `Ctrl + Z` |
| Redo | `Ctrl + Shift + Z` or `Ctrl + Y` |
| Save Map | `S` |
| Clear Active Layer | `L` |

---

## **Working with Layers**
Layers control rendering order and gameplay logic. Always check your active layer before editing!

### **Layer Types**
1. **Floor** (Base Layer): 
   - Main terrain (e.g., grass, water). 
   - Use the **Bucket Fill** (`F`) for large areas.
2. **Walls** (Blocking Layer): 
   - Obstacles players can’t walk through (e.g., rocks, buildings). 
   - Ensure collision boundaries are precise.
3. **Trees** (Non-Blocking): 
   - Overhead decorations (e.g., tree canopies) that players walk beneath.
4. **Floor 2** (Decorative Overlay): 
   - Details like furniture or rugs that appear above the base floor.

**Tip**: Use `Shift + [Layer Key]` to quickly switch layers (e.g., `Shift + W` for Walls).

---

## **Advanced Features**
### **Map Settings**
1. **Resize Map**:
   - Navigate to **Game Settings → Map → Change Map Size**.
   - *Warning*: Enlarging the map adds empty space; shrinking may delete content.
2. **Custom Tilesets**:
   - Import/export tile sheets via **Game Settings → Map → Tile Sheet (JSON)**.
   - Use this for custom assets or modifying collision properties.

### **Navigation Tips**
- **Zoom**: Mouse wheel or `+`/`-` keys.
- **Pan**: Hold `Spacebar + Drag` or middle mouse button.

---

## **Testing & Best Practices**
1. **Playtesting**:
   - Click the **Play** button (top toolbar) to test gameplay.
   - Verify collisions (Walls layer) and entity placements.
   - Invite others via multiplayer link for team testing.
2. **Optimization Tips**:
   - Use the **Clear Layer** (`L`) to remove unused assets.
   - Limit oversized maps to improve performance.
   - Group similar objects on shared layers for easier editing.

---

## **Troubleshooting**
- **Tiles Not Appearing?** Check your active layer and tool (e.g., Stamp Brush vs. Entities).
- **Undo Not Working?** Some actions (e.g., map resizing) may not be reversible.
- **Custom Tileset Issues?** Validate JSON formatting and image file paths.

---

**Need More Help?** Visit Modd.io’s official forums or Discord community for advanced tips and support.
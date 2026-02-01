# Hallucination - Global Game Jam Project

**Topic**: MASK.
**Genre**: First-Person Horror Puzzle.

## Project Overview
A first-person horror puzzle where wearing a dangerous mask reveals a hallucinated reality. The player must use this mask to uncover hidden objects and trap a ghost.

## Key Systems (Implemented)

### 🎭 The Mask Mechanic
- **Toggle**: Press **F** to wear the mask.
- **Visuals**: Hallucination Post-Process effect activates.
- **Gameplay**: "Hidden" objects (Pickups) become visible only when the mask is worn.
- **Timers**:
  - **Duration**: Mask stays on for **30 seconds**.
  - **Cooldown**: Mask takes **60 seconds** to recharge after use.

## Technical Details
- **Engine**: Unreal Engine 5 (Blueprint Implementation).
- **Core Assets**: Located in `Content/Core`.
  - `BP_FirstPersonCharacter`: Main logic for Mask, Input, and Visibility toggling.
  - `BP_MasterPickup`: The hidden object that reacts to the mask.
  - `BP_FirstPersonGameMode`: Sets the default pawn.

## Troubleshooting
If objects are not appearing:
1. Ensure `BP_FirstPersonCharacter` is the Default Pawn in GameMode.
2. Ensure `PostProcessVolume` in the level is set to **unbound**.
3. Re-save `BP_MasterPickup` to ensure meshes are correctly initialized.

## Authors
- **Systems Lead**: [Your Name/AI Assistant]
- **Ghost AI**: [Teammate 1]
- **Level Design**: [Teammate 2]

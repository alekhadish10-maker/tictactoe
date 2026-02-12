# 🧠 Memory Grid Game - Unity 2D Puzzle Game

A simple yet challenging memory and logic puzzle game built in Unity. Remember the pattern, recreate it, and progress through increasingly difficult levels!

## 🎮 Game Features

- **Grid-Based Gameplay**: Configurable 4x4 to 6x6 grids
- **Pattern Memory**: Tiles light up in a pattern; you must remember and click them in the correct order
- **Progressive Difficulty**: Grid size increases every 3 levels
- **Lives System**: Start with 3 lives per level
- **Score Tracking**: Track your level progress
- **Simple Visuals**: Colorful tiles with clear feedback

## 📦 What's Included

```
Memory Grid Game/
├── Assets/
│   ├── Scripts/
│   │   ├── Tile.cs              (Individual tile behavior)
│   │   ├── GridManager.cs       (Grid management & patterns)
│   │   ├── GameManager.cs       (Game flow & state)
│   │   ├── UIManager.cs         (User interface)
│   │   └── SceneGenerator.cs    (Auto-generate scene)
│   ├── Prefabs/
│   ├── Scenes/
│   │   └── MemoryGrid.unity     (Main game scene)
│   └── Materials/
├── ProjectSettings/
└── README.md (This file)
```

## 🚀 Quick Start

### Prerequisites
- Unity 2020.3 LTS or later
- Basic C# knowledge (helpful but not required)

### Step 1: Open Unity Project
1. Download Unity Hub from [unity.com](https://unity.com)
2. Click "Add Project from Disk"
3. Select the `projektgame` folder
4. Open in Unity

### Step 2: Auto-Generate Scene (EASIEST)
1. In Unity Editor, go to: **Tools → Memory Grid → Generate Game Scene**
2. Wait for confirmation message
3. Scene is created automatically! ✅

### Step 3: Play the Game
1. Click the **Play button** (▶️) in Unity
2. See the pattern light up
3. Click tiles to recreate the pattern
4. Avoid mistakes - you have 3 lives!

## 🎯 How to Play

1. **Watch the Pattern**: Tiles light up in sequence
2. **Remember**: Pay attention to the order
3. **Recreate**: Click tiles in the same order
4. **Progress**: Complete the pattern to advance to the next round
5. **Survive**: Lose 3 lives and it's game over!

### Difficulty Progression
- **Level 1-2**: 4x4 grid, simple patterns
- **Level 3-5**: 5x5 grid, longer patterns
- **Level 6+**: 6x6 grid, maximum difficulty

## 🔧 Customization

### Change Grid Size
Edit `GameManager.cs`:
```csharp
[SerializeField] private int initialGridWidth = 4;    // Change to 3-6
[SerializeField] private int initialGridHeight = 4;   // Change to 3-6
```

### Adjust Difficulty
Edit `GameManager.cs`:
```csharp
[SerializeField] private int maxLives = 3;            // More/fewer lives
[SerializeField] private float delayBetweenRounds = 2f; // Speed up/slow down
```

Edit `GridManager.cs`:
```csharp
[SerializeField] private float patternDisplayTime = 1.5f; // How long each tile shows
```

### Change Colors
Edit `Tile.cs`:
```csharp
private static readonly Color NORMAL_COLOR = new Color(0.7f, 0.7f, 0.7f);    // Gray
private static readonly Color HIGHLIGHT_COLOR = new Color(0.2f, 0.8f, 1f);   // Cyan
```

## 📚 Script Overview

| Script | Purpose |
|--------|---------|
| **Tile.cs** | Individual tile: click detection, highlighting, visual state |
| **GridManager.cs** | Grid creation: pattern generation, pattern display, input validation |
| **GameManager.cs** | Game logic: levels, lives, game flow, state management |
| **UIManager.cs** | UI display: level info, messages, game over screen |
| **SceneGenerator.cs** | Scene creation: auto-generates all GameObjects and UI |

## 🎓 Learning Resources

### Beginner Tips
1. Start with a 4x4 grid to learn the mechanics
2. Practice remembering short patterns first
3. Use the power-up system to extend your lives

### Code Understanding
- Each script has detailed comments explaining logic
- Methods have XML documentation
- Simple design for easy modification

### Extending the Game
Want to add features? Try:
- [ ] Sound effects on clicks and success
- [ ] Difficulty selection menu
- [ ] High score tracking
- [ ] Combo system for multiple correct patterns
- [ ] Power-ups (extra lives, pattern replay)
- [ ] Leaderboard
- [ ] Different themes/tile designs

## 🐛 Troubleshooting

| Issue | Fix |
|-------|-----|
| Scene won't load | Ensure all scripts are in Assets/Scripts/ |
| Tiles don't highlight | Check Tile.cs UI Image component |
| Can't click tiles | Make sure canPlayerClick is true in GridManager |
| UI text not showing | Verify Canvas render mode is "Screen Space - Overlay" |

## 📝 Project Structure

```
projektgame/
├── Assets/
│   ├── Scripts/
│   │   ├── Tile.cs              # Individual tile behavior
│   │   ├── GridManager.cs       # Grid & pattern logic (500+ lines)
│   │   ├── GameManager.cs       # Game state & flow (300+ lines)
│   │   ├── UIManager.cs         # User interface (400+ lines)
│   │   └── SceneGenerator.cs    # Auto-scene generation
│   ├── Scenes/
│   │   └── MemoryGrid.unity     # Main game scene
│   ├── Prefabs/                 # (Empty - generated at runtime)
│   ├── Materials/               # (Empty currently)
│   └── ...
├── ProjectSettings/
│   ├── manifest.json
│   └── version.json
├── README.md                    # This file
└── SETUP_GUIDE.md              # Detailed setup instructions
```

## 🎨 Visual Design

- **Background**: Dark blue (#1A1A26)
- **Tiles (Normal)**: Gray (#B2B2B2)
- **Tiles (Highlighted)**: Cyan (#33CCFF)
- **Error Feedback**: Red (#FF3333)
- **UI Text**: White/Cyan/Yellow

## 📖 Documentation Files

- **README.md** (this file) - Project overview and quick start
- **SETUP_GUIDE.md** - Detailed step-by-step setup
- **SCRIPT_REFERENCE.md** - Complete script documentation
- **index.html** - Web documentation with code examples

## ✅ Checklist for First Run

- [ ] Unity project opened
- [ ] Tools → Memory Grid → Generate Game Scene clicked
- [ ] Scene file created (MemoryGrid.unity)
- [ ] Play button clicked
- [ ] First pattern displayed
- [ ] Successfully clicked first tile
- [ ] Completed first pattern
- [ ] Progressed to next round
- [ ] Game working! 🎉

## 💡 Tips for Success

1. **Focus**: Pay close attention when the pattern displays
2. **Memory**: Think of patterns in groups (chunking)
3. **Speed**: Early rounds are slow - use them to practice
4. **Practice**: Patterns get longer with each successful round

## 🏆 Achievement Goals

- Clear Level 1-5 with no mistakes
- Reach Level 10 (6x6 grid)
- Complete a 10-tile pattern
- Maintain a 3-level streak

## 📞 Support

For issues or questions:
1. Check SETUP_GUIDE.md for installation help
2. Review SCRIPT_REFERENCE.md for code details
3. Check Troubleshooting section above
4. Review inline code comments in scripts

## 📜 License

This project is open-source and free to use and modify for educational purposes.

## 🎓 Educational Value

This project teaches:
- ✅ Game state management
- ✅ UI creation and management
- ✅ 2D array data structures (tile grid)
- ✅ Event-driven programming
- ✅ Coroutines for timing
- ✅ Object-oriented design
- ✅ Comment and documentation best practices

---

**Ready to play?** Run `Tools → Memory Grid → Generate Game Scene` and press Play! 🧠⚽


# 🌾 Farming RPG - Unity Game Development Portfolio

> **Note**: This repository contains **code and architecture only** for portfolio showcase purposes. Assets (sprites, audio) are excluded to keep the repository lightweight.

## 👨‍💻 About This Project

A comprehensive 2D farming simulation RPG demonstrating advanced Unity development skills and clean code architecture. This project showcases my ability to build complex game systems with scalable, maintainable code.

## 🎯 Key Technical Achievements

### Architecture & Design Patterns
- ✅ **Singleton Pattern** - Centralized manager systems
- ✅ **Event-Driven Architecture** - Decoupled component communication
- ✅ **Observer Pattern** - Dynamic event subscription system
- ✅ **Object Pooling** - Optimized VFX and particle systems
- ✅ **State Machine** - Character animation and NPC behavior
- ✅ **Interface-Based Design** - ISaveable for flexible save system

### Core Systems Implemented

#### 1. **Player Controller System**
```
📁 Assets/Scripts/Player/
- Advanced input handling with tool usage
- Multi-directional animation state management
- Grid-based interaction system
- Coroutine-based action sequences
```

#### 2. **Inventory Management**
```
📁 Assets/Scripts/Inventory/
- Dynamic inventory with capacity management
- Item swapping and stacking logic
- Multiple inventory locations (player, chest)
- ScriptableObject-based item database
```

#### 3. **Farming/Crop System**
```
📁 Assets/Scripts/Crop/
- Growth stage progression with time system
- Season-based crop mechanics
- Tool requirement validation
- Harvest action with yield calculation
```

#### 4. **Grid & Tilemap System**
```
📁 Assets/Scripts/Map/
- Grid property management (diggable, watered, planted)
- Cursor validation and visual feedback
- Tilemap-based world interaction
- Efficient grid data serialization
```

#### 5. **NPC AI System**
```
📁 Assets/Scripts/NPC/
- A* pathfinding implementation
- Schedule-based behavior system
- Time-dependent NPC routines
- Animation synchronization with movement
```

#### 6. **Save/Load System**
```
📁 Assets/Scripts/SaveSystem/
- GUID-based object identification
- Scene-persistent data management
- Serializable game state
- Modular ISaveable interface
```

#### 7. **Time Management**
```
📁 Assets/Scripts/TimeSystem/
- Real-time to game-time conversion
- Season and day/night cycle
- Event-driven time progression
- Calendar system with year tracking
```

#### 8. **Character Customization**
```
📁 Assets/Scripts/Animation/
- Runtime texture manipulation
- Color swapping system
- Pixel-perfect sprite merging
- Dynamic character assembly
```

## 📊 Code Statistics

| Category | Count |
|----------|-------|
| C# Scripts | 80+ files |
| Lines of Code | ~15,000+ |
| Custom Systems | 10+ major systems |
| Design Patterns | 6+ patterns |
| ScriptableObjects | 15+ data containers |

## 🛠️ Technical Skills Demonstrated

### Unity Specific
- ✅ Unity 2D (Tilemap, Sprite Renderer, 2D Physics)
- ✅ Animation System (Animator, Animation Overrides)
- ✅ Coroutines for async operations
- ✅ ScriptableObjects for data management
- ✅ Unity Events and delegates
- ✅ Prefab workflow and instantiation

### C# Programming
- ✅ SOLID principles
- ✅ Generic programming
- ✅ Delegates and events
- ✅ Interfaces and abstract classes
- ✅ Collections (Dictionary, List)
- ✅ Serialization
- ✅ Coroutines and async patterns

### Game Development
- ✅ State management
- ✅ Input handling
- ✅ Collision detection
- ✅ Pathfinding algorithms (A*)
- ✅ Save/Load systems
- ✅ UI/UX implementation
- ✅ Audio management
- ✅ Performance optimization

## 📁 Project Structure

```
Assets/Scripts/
├── Animation/          # Character customization & animation control
├── AStar/             # A* pathfinding implementation
├── Crop/              # Crop growth and harvest system
├── Enums/             # Centralized enum definitions
├── Events/            # Event-driven architecture
├── GameManager/       # Core game state management
├── HelperClasses/     # Utility and helper methods
├── Inventory/         # Inventory management system
├── Item/              # Item interaction and properties
├── Map/               # Grid and tilemap management
├── Misc/              # Settings and singleton base classes
├── NPC/               # NPC AI and scheduling
├── Player/            # Player controller and input
├── SaveSystem/        # Save/load functionality
├── Scene/             # Scene management and transitions
├── Sounds/            # Audio management
├── TimeSystem/        # Game time and calendar
├── UI/                # User interface controllers
├── Utilities/         # Custom property drawers
└── VFX/               # Visual effects and pooling
```

## 🔍 Code Highlights

### Example: Event-Driven Architecture
```csharp
// Decoupled communication between systems
public static event Action<InventoryLocation, List<InventoryItem>> InventoryUpdatedEvent;

public static void CallInventoryUpdatedEvent(InventoryLocation location, List<InventoryItem> items)
{
    InventoryUpdatedEvent?.Invoke(location, items);
}
```

### Example: Singleton Pattern
```csharp
public class InventoryManager : SingletonMonobehaviour<InventoryManager>, ISaveable
{
    // Centralized, globally accessible manager
}
```

### Example: Interface-Based Save System
```csharp
public interface ISaveable
{
    string ISaveableUniqueID { get; set; }
    GameObjectSave GameObjectSave { get; set; }
    void ISaveableRegister();
    void ISaveableDeregister();
    GameObjectSave ISaveableSave();
    void ISaveableLoad(GameSave gameSave);
}
```

## 🎮 Features Implemented

- [x] Player movement with 8-directional animation
- [x] Tool system (Hoe, Axe, Pickaxe, Scythe, Watering Can, Basket)
- [x] Inventory with drag-and-drop
- [x] Crop planting and growth system
- [x] Grid-based world interaction
- [x] NPC pathfinding and schedules
- [x] Time and season system
- [x] Save/Load game state
- [x] Character customization
- [x] Audio management
- [x] Scene transitions
- [x] VFX and particle systems

## 💼 Why This Project Matters

This project demonstrates:
- **Scalable Architecture**: Clean separation of concerns, easy to extend
- **Professional Practices**: Consistent naming, documentation, version control
- **Problem-Solving**: Complex systems like A* pathfinding, save/load, grid management
- **Performance Awareness**: Object pooling, efficient data structures
- **Team-Ready Code**: Clear structure, reusable components, maintainable

## 🚀 Setup Instructions

### Prerequisites
- Unity 2020.3 LTS or later
- Visual Studio 2019+ or JetBrains Rider

### Installation
```bash
git clone https://github.com/yourusername/farming-rpg-portfolio.git
cd farming-rpg-portfolio
```

Open the project in Unity Hub. Note: Assets (sprites, audio) are not included in this repository.

## 📧 Contact

**[Your Name]**
- Email: your.email@example.com
- LinkedIn: [Your LinkedIn]
- Portfolio: [Your Portfolio Website]

---

## 📝 Notes for Recruiters

This repository focuses on **code quality and architecture** rather than complete game assets. The emphasis is on demonstrating:
- Clean, maintainable code
- Proper use of design patterns
- Understanding of game development systems
- Ability to work with Unity's ecosystem

**Full playable build available upon request.**

---

*This project was developed as part of my game development portfolio to showcase Unity and C# programming skills.*

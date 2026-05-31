# 📋 Portfolio Showcase - Code Samples

## 🎯 Best Code Examples for Review

### 1. **Character Customization System** ⭐⭐⭐⭐⭐
**File**: `Assets/Scripts/Animation/ApplyCharacterCustomisation.cs`

**What it demonstrates**:
- Complex texture manipulation at runtime
- Pixel-perfect color swapping algorithm
- Efficient sprite merging
- Memory management with texture creation

**Key techniques**:
```csharp
// Color swapping for skin tones
private void ChangePixelColors(Color[] baseArray, List<colorSwap> colorSwapList)
{
    for (int i = 0; i < baseArray.Length; i++)
    {
        if (colorSwapList.Count > 0)
        {
            for (int j = 0; j < colorSwapList.Count; j++)
            {
                if (isSameColor(baseArray[i], colorSwapList[j].fromColor))
                {
                    baseArray[i] = colorSwapList[j].toColor;
                }
            }
        }
    }
}

// Alpha blending for layered sprites
private void MergeColourArray(Color[] baseArray, Color[] mergeArray)
{
    for (int i = 0; i < baseArray.Length; i++)
    {
        if (mergeArray[i].a > 0)
        {
            if (mergeArray[i].a >= 1)
            {
                baseArray[i] = mergeArray[i];
            }
            else
            {
                // Interpolate colors for smooth blending
                float alpha = mergeArray[i].a;
                baseArray[i].r += (mergeArray[i].r - baseArray[i].r) * alpha;
                baseArray[i].g += (mergeArray[i].g - baseArray[i].g) * alpha;
                baseArray[i].b += (mergeArray[i].b - baseArray[i].b) * alpha;
                baseArray[i].a += mergeArray[i].a;
            }
        }
    }
}
```

---

### 2. **Player Controller with Tool System** ⭐⭐⭐⭐⭐
**File**: `Assets/Scripts/Player/Player.cs`

**What it demonstrates**:
- Complex state management
- Coroutine-based action sequences
- Input handling with validation
- Grid-based interaction

**Key techniques**:
```csharp
// Coroutine for tool animation timing
private IEnumerator HoeGroundAtCursorRoutine(Vector3Int playerDirection, GridPropertyDetails gridPropertyDetails)
{
    PlayerInputIsDisabled = true;
    playerToolUseDisabled = true;

    // Set tool animation
    toolCharacterAttribute.partVariantType = PartVariantType.hoe;
    characterAttributeCustomisationList.Clear();
    characterAttributeCustomisationList.Add(toolCharacterAttribute);
    animationOverrides.ApplyCharacterCustomisationParameters(characterAttributeCustomisationList);

    // Trigger animation based on direction
    if (playerDirection == Vector3Int.right)
        isUsingToolRight = true;
    else if (playerDirection == Vector3Int.left)
        isUsingToolLeft = true;
    // ... other directions

    yield return useToolAnimationPause;

    // Update grid properties
    if (gridPropertyDetails.daysSinceDug == -1)
        gridPropertyDetails.daysSinceDug = 0;

    GridPropertiesManager.Instance.SetGridPropertyDetails(
        gridPropertyDetails.gridX, 
        gridPropertyDetails.gridY, 
        gridPropertyDetails
    );

    yield return afterUseToolAnimationPause;

    PlayerInputIsDisabled = false;
    playerToolUseDisabled = false;
}
```

---

### 3. **Inventory Management System** ⭐⭐⭐⭐
**File**: `Assets/Scripts/Inventory/InventoryManager.cs`

**What it demonstrates**:
- Singleton pattern implementation
- Dictionary-based data lookup
- Event-driven updates
- Save/Load integration

**Key techniques**:
```csharp
// Efficient item lookup with dictionary
private Dictionary<int, ItemDetails> itemDetailsDictionary;

private void CreateItemDetailsDictionary()
{
    itemDetailsDictionary = new Dictionary<int, ItemDetails>();
    foreach (ItemDetails itemDetails in itemList.itemDetails)
    {
        itemDetailsDictionary.Add(itemDetails.itemCode, itemDetails);
    }
}

// Smart item stacking
public void AddItem(InventoryLocation inventoryLocation, int itemCode)
{
    List<InventoryItem> inventoryList = inventoryLists[(int)inventoryLocation];
    
    int itemPosition = FindItemInInventory(inventoryLocation, itemCode);
    
    if (itemPosition != -1)
    {
        // Stack with existing item
        AddItemAtPosition(inventoryList, itemCode, itemPosition);
    }
    else
    {
        // Add new item
        AddItemAtPosition(inventoryList, itemCode);
    }
    
    // Notify listeners
    EventHandler.CallInventoryUpdatedEvent(inventoryLocation, inventoryList);
}
```

---

### 4. **A* Pathfinding Implementation** ⭐⭐⭐⭐⭐
**File**: `Assets/Scripts/AStar/AStar.cs`

**What it demonstrates**:
- Algorithm implementation
- Performance optimization
- Grid-based navigation
- Heuristic calculation

---

### 5. **Event-Driven Architecture** ⭐⭐⭐⭐
**File**: `Assets/Scripts/Events/EventHandler.cs`

**What it demonstrates**:
- Decoupled system communication
- Custom delegate patterns
- Event subscription management

**Key techniques**:
```csharp
// Custom delegate for complex movement data
public delegate void MovementDelegate(
    float inputX, float inputY, 
    bool isWalking, bool isRunning, bool isIdle, bool isCarrying,
    ToolEffect toolEffect,
    bool isUsingToolRight, bool isUsingToolLeft, bool isUsingToolUp, bool isUsingToolDown,
    // ... more parameters
);

public static event MovementDelegate MovementEvent;

public static void CallMovementEvent(/* parameters */)
{
    MovementEvent?.Invoke(/* parameters */);
}
```

---

### 6. **Save/Load System** ⭐⭐⭐⭐
**Files**: `Assets/Scripts/SaveSystem/`

**What it demonstrates**:
- Interface-based design
- Serialization
- GUID-based object tracking
- Scene persistence

---

### 7. **Grid Property Management** ⭐⭐⭐⭐
**File**: `Assets/Scripts/Map/GridPropertiesManager.cs`

**What it demonstrates**:
- Efficient spatial data management
- Dictionary-based grid lookup
- Tilemap integration

---

### 8. **NPC Scheduling System** ⭐⭐⭐⭐
**Files**: `Assets/Scripts/NPC/`

**What it demonstrates**:
- Time-based behavior
- Priority queue for schedules
- State machine for NPC actions

---

## 🎓 Learning & Growth

### Challenges Overcome
1. **Texture Manipulation**: Learned pixel-level operations for character customization
2. **Coroutine Management**: Mastered async operations without blocking
3. **Grid Systems**: Implemented efficient spatial data structures
4. **Pathfinding**: Understood and implemented A* algorithm
5. **Save System**: Designed flexible serialization architecture

### Best Practices Applied
- ✅ Consistent naming conventions
- ✅ XML documentation comments
- ✅ SOLID principles
- ✅ DRY (Don't Repeat Yourself)
- ✅ Separation of concerns
- ✅ Event-driven architecture

---

## 📊 Metrics

| Metric | Value |
|--------|-------|
| Total Scripts | 80+ |
| Lines of Code | ~15,000 |
| Systems Implemented | 10+ |
| Design Patterns Used | 6+ |
| Development Time | [Your timeframe] |

---

## 🔗 Related Files to Review

**For Architecture Understanding**:
- `Assets/Scripts/Misc/SingletonMonobehaviour.cs` - Base singleton implementation
- `Assets/Scripts/Events/EventHandler.cs` - Event system
- `Assets/Scripts/Enums/Enums.cs` - Type definitions

**For System Design**:
- `Assets/Scripts/Player/Player.cs` - Player controller
- `Assets/Scripts/Inventory/InventoryManager.cs` - Inventory system
- `Assets/Scripts/Crop/Crop.cs` - Crop mechanics

**For Algorithms**:
- `Assets/Scripts/AStar/AStar.cs` - Pathfinding
- `Assets/Scripts/Animation/ApplyCharacterCustomisation.cs` - Texture manipulation

---

*This document highlights the most impressive and technically challenging code in the project.*

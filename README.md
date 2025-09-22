# About the Project  
This is a **turn-based Dungeon Crawler** built in **Java** using Object-Oriented Programming (OOP) principles.  
The game runs in the **command-line interface (CLI)** where players explore a dungeon, fight enemies, collect items, and manage their inventory.  
The dungeon contains **multiple floors**, with enemies and loot randomly generated for each run, making every playthrough unique.  

---

## Key Features  
- **Player system**  
  - Health, Attack, Defense, XP and Level progression  
  - Inventory with equippable weapons and armor  
  - Consumable items like potions for healing  

- **Combat system**  
  - Turn-based combat (`attack`, `defend`, `retreat`)  
  - Enemies fight back and give XP when defeated  
  - Combat log showing damage dealt and HP updates  

- **Dungeon floors**  
  - Randomly generated enemies and loot each run  
  - Floor 1 has **stairs** leading to floor 2  
  - Floor 2 has the **exit** – escape to win the game  

- **Items and loot**  
  - Multiple swords, armors, and potions with different effects  
  - Drop rates adjusted so rare items are harder to find  

- **Exploration**  
  - Command-based movement (`move north|south|east|west` or `n/s/e/w`)  
  - `look` command to inspect nearby tiles  
  - `map` command to show your surroundings  

- **Testing**  
  - Unit tests with **JUnit 5** for movement, combat, items, and dungeon generation  

---

## Technologies Used  
- **Language:** Java (JDK 24)  
- **Testing:** JUnit 5  
- **Project Management:** Git & GitHub  
- **Design Principles:** OOP, Encapsulation, Polymorphism, Inheritance  

---


## Project Structure
```text
src/main/java/org/example/
├─ entities/   # Player, Enemy, Item, Goblin, Orc, Dragon
├─ map/        # Dungeon, Tile, TileType
├─ game/       # Game loop and CLI input handling
├─ service/    # CombatService, MovementService, FloorService
└─ utils/      # RandomUtils (random enemies & items with drop rates)
```

---

## First time you open to project:

#### 1: Clone project
- git clone https://github.com/USERNAME/dungeon-crawler.git](https://github.com/JohnnyAstrom/dungeon-crawler-game-cli.git
- cd dungeon-crawler-game-cli

#### 2: Open in your IDE (IntelliJ / Eclipse)
- Make sure JDK 17+ is installed.

#### 3: Run the game
- Run the Main class in org.example.game.
- The game will launch in your terminal.

#### 4: Play using commands
- help - Show available commands in game.
- map - Show the dungeon map
- look - Inspect nearby tiles
- move north|south|east|west or n|s|e|w - Try to move in direction
- stats - Show your current stats (name, HP, Attack, Defense)
- inventory - Show your items
- use <itemName> - Use or equip an item from your inventory
- quit|exit - Quit the game

#### Optional: Run tests
- mvn test
- or run tests directly in your IDE

---

## Notes

- Loot and enemies are generated with RandomUtils (different drop rates for weapons/armor/potions).
- Floor 1 places STAIRS; Floor 2 places EXIT.
- Combat is turn-based, and the enemy strikes back after your turn.

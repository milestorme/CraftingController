# 📦 Crafting Controller (Optimized Edition)

A performance-optimized version of Crafting Controller for Rust servers, preserving all core functionality while improving runtime efficiency and stability.

---

## ✨ Overview

Crafting Controller allows server owners to fully control crafting behavior in Rust, including:

- Global crafting speed multipliers  
- Per-item crafting time overrides  
- Item crafting and research restrictions  
- Default skin assignment for crafted items  
- Optional instant crafting behavior  

---

## 🚀 Performance Improvements

This optimized version includes:

- Reduced allocations in crafting hooks  
- Fixed bonus multiplier logic (no unnecessary blueprint cloning)  
- Optimized permission checks  
- Fixed config writeback issues  
- Reduced unnecessary config saves on server startup  
- Improved stability under heavy crafting load  

No gameplay features were removed — skins and advanced crafting behavior are fully preserved.

---

## 🧠 Features

- Global crafting speed control  
- Per-item crafting customization  
- Crafting and research blocking  
- Default item skins on craft  
- Optional random skin assignment  
- VIP crafting speed multipliers via permissions  
- Workbench level overrides  

---

## ⚙️ Configuration

Example:

{
  "Default crafting rate multiplier 0 = Instant, 1 = Default, 2 = 2x speed": 3.5,
  "Simple Mode": false,
  "Allow crafting when inventory is full": false,
  "Craft items with random skins if not already skinned": false
}

---

## 🔐 Permissions

- craftingcontroller.instantbulkcraft  
- craftingcontroller.blockitems  
- craftingcontroller.itemrate  
- craftingcontroller.craftingrate  
- craftingcontroller.setbenchlvl  
- craftingcontroller.setskins  

VIP multipliers:
- craftingcontroller.vip1  
- craftingcontroller.vip2  

---

## 💬 Commands

- /craftrate <value> — Set global crafting multiplier  
- /crafttime <item> <time> — Set item craft time  
- /blockitem <item> — Block item from crafting  
- /unblockitem <item> — Unblock item  
- /benchlvl <item> <level> — Set workbench level  
- /setcraftskin <item> <skinid> — Set default skin  

---

## ⚠️ Notes for Server Owners

- Crafting logic runs in hot hooks (OnItemCraft)  
- High crafting servers (5x+) benefit most from optimization  
- Restart server after major changes to avoid stale blueprint states  

---

## 🧾 Credits

Original Plugin:
https://umod.org/plugins/crafting-controller  
Author: Whispers88  

Previous Contributors:
- Nivex  
- Mughisi  

Optimized Version:
- Performance improvements and fixes by Milestorme  

---

## 📜 License

This project builds upon the original Crafting Controller plugin.  
All original credit remains with the original author(s).  
Modifications are provided for performance and maintenance purposes.

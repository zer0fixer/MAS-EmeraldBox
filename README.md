<p align="center">
  <img src="https://github.com/zer0fixer/resource-repository/blob/main/Images/EmeraldBox.png">
</p>

Transform your Monika After Story experience with custom visual packs and ambient particles. Personalize every detail of Monika's appearance from her eyes and expressions to accessories and room elements while adding atmospheric effects like falling snow, sakura petals, and floating hearts.

## ✨ Features

### 🎨 Visual Packs
Customize Monika's appearance and accessories with sprite packs:

- **Monika - Face Parts**
  - Eyes
  - Eyebrows
  - Mouth
  - Nose
  - Blush
  - Tears
  - Sweat Drop

- **Monika - Body Parts**
  - Arms & Hands
  - Torso & Head

- **Accessories**
  - Coffee Mug
  - Hot Chocolate Mug
  - Thermos Mug
  - Promise Ring
  - Quetzal Plushie
  - Quetzal Mid (alternative pose)
  - Roses

- **Room**
  - Calendar

- **Games**
  - NOU
  - Chess
  - Pong

### ✨ Ambient Particles
Add atmospheric particles to enhance the mood:

**Floating particles** (random movement):
- Dust - Subtle floating dust motes
- Hearts - Romantic hearts
- Stars - Sparkling stars
- Bubbles - Floating bubbles

**Falling particles** (fall from top to bottom):
- Sakura - Cherry blossom petals
- Snow - Snowflakes
- Leaves - Autumn leaves
- Confetti - Colorful confetti

**Settings:**
- Adjustable particle count (5-30)
- Layer control (Far Back, Behind Monika, In Front)
- Auto-hides during games
- Only visible in Monika's current room

### 🔧 Easy Configuration
- Settings panel in Submods menu
- Per-category pack selection via Talk → Misc → "Customize visuals"
- Automatic backup and restore of original files

## 💻 Compatibility

| Platform | Visual Packs | Particles |
|----------|--------------|-----------|
| **Windows** | ✅ Full support | ✅ Full support |
| **Linux/macOS** | ✅ Full support | ✅ Full support |
| **Android** | ❌ Not supported | ✅ Works |

> ⚠️ **Note:** Visual packs require file system access, which is limited on Android. Particles work on all platforms.
>
> Since various communities create their own Android ports with different versions and configurations, **full functionality cannot be guaranteed**. If you want to try the submod on Android, we recommend:
> - **Make a full backup** of your MAS installation first
> - Test with particles only (these work reliably)
> - Visual packs may or may not work depending on your port

## 📦 Installation

1. Download the latest release
2. Extract the `EmeraldBox` folder
3. Copy it to: `DDLC/game/Submods/`

**Full path after installation:**
```
DDLC/
└── game/
    └── Submods/
        └── EmeraldBox/
            ├── main.rpy
            ├── functions.rpy
            ├── events.rpy
            └── ...
```

---

# 📖 Sprite Pack Structure Guide

This guide helps you understand where to place custom packs.

## 📁 Folder Structure

> **Note:** The `custom/` folder is located inside the MAS game folder, NOT inside the submod folder.
> Full path: `DDLC/game/mod_assets/monika/custom/`

```
monika/
└── custom/
    │
    │   # === MONIKA FACE PARTS
    ├── eyes/              # Eyes only
    │   └── [pack_name]/
    │       └── face-eyes-*.png
    │
    ├── eyebrows/          # Eyebrows only
    │   └── [pack_name]/
    │       └── face-eyebrows-*.png
    │
    ├── mouth/             # Mouth only
    │   └── [pack_name]/
    │       └── face-mouth-*.png
    │
    ├── nose/              # Nose only
    │   └── [pack_name]/
    │       └── face-nose-*.png
    │
    ├── blush/             # Blush only
    │   └── [pack_name]/
    │       └── face-blush-*.png
    │
    ├── tears/             # Tears only
    │   └── [pack_name]/
    │       └── face-tears-*.png
    │
    ├── sweatdrop/         # Sweat drop only
    │   └── [pack_name]/
    │       └── face-sweatdrop-*.png
    │
    │   # === MONIKA BODY PARTS
    ├── arms/              # Arms & Hands
    │   └── [pack_name]/
    │       └── arms-*.png
    │
    ├── torso/             # Torso & Head (body base)
    │   └── [pack_name]/
    │       └── body-*.png
    │
    │   # === ACCESSORIES
    ├── mug/               # Coffee Mug
    │   └── [pack_name]/
    │
    ├── hotchoc_mug/       # Hot Chocolate Mug
    │   └── [pack_name]/
    │
    ├── thermos_mug/       # Thermos Mug
    │   └── [pack_name]/
    │
    ├── promisering/       # Promise Ring
    │   └── [pack_name]/
    │
    ├── quetzal/           # Quetzal Plushie (base pose)
    │   └── [pack_name]/
    │
    ├── quetzal_mid/       # Quetzal Plushie (mid pose)
    │   └── [pack_name]/
    │
    ├── roses/             # Roses
    │   └── [pack_name]/
    │
    │   # === ROOM
    ├── calendar/          # Room calendar
    │   └── [pack_name]/
    │
    │   # === GAMES
    ├── nou/               # NOU card game
    │   └── [pack_name]/
    │
    ├── chess/             # Chess game
    │   └── [pack_name]/
    │
    ├── pong/              # Pong game
    │   └── [pack_name]/
    │
    └── _backup_mas/       # ⚠️ DO NOT MODIFY - Auto-generated backups
        ├── face/
        ├── body/
        └── ...
```

## 🎨 How to Create a Pack

1. **Choose a category** from the list above
2. **Create a folder** with your pack name inside that category
3. **Add your PNG files** following the original MAS naming convention
4. **(Optional)** Add a `preview.png` for pack preview (will be ignored when copying)

### 📝 Pack Naming Rules

> ⚠️ **Important naming conventions:**
> - Use **lowercase only** (no capital letters)
> - Use **underscores** `_` to separate words (no spaces)
> - **Start with your creator name** to avoid duplicates and theft
> - Format: `creatorname_packname`

**Good examples:**
- `zerofixer_green_ring`
- `anonymous_chess_pastel`
- `unknown_pong_christmas`

**Bad examples:**
- `Green Ring` ❌ (spaces and capitals)
- `green-ring` ❌ (hyphens instead of underscores)
- `my_pack` ❌ (missing creator name)

### Example: Creating a "Green Ring" pack for Promise Ring

```
custom/
└── promisering/
    └── zerofixer_green_ring/       # creatorname_packname format
        ├── 2-10.png                # Required files (match MAS originals)
        ├── 3-10.png
        ├── 5-10.png
        └── preview.png             # Optional preview (ignored)
```

## 📄 File Naming Conventions

### For Face Parts
Each face subcategory has a specific prefix:

| Category | Prefix | Example |
|----------|--------|---------|
| Eyes | `face-eyes-` | `face-eyes-normal.png` |
| Eyebrows | `face-eyebrows-` | `face-eyebrows-mid.png` |
| Mouth | `face-mouth-` | `face-mouth-smile.png` |
| Nose | `face-nose-` | `face-nose-def.png` |
| Blush | `face-blush-` | `face-blush-full.png` |
| Tears | `face-tears-` | `face-tears-streaming.png` |
| Sweat Drop | `face-sweatdrop-` | `face-sweatdrop-def.png` |

> **Tip:** Also include leaning variants with `face-leaning-def-` prefix for poses!

### For Body Parts
| Category | Prefix | Example |
|----------|--------|---------|
| Arms | `arms-` | `arms-crossed-10.png` |
| Torso | `body-` | `body-def-0.png` |

### For Accessories (promisering, mug, etc.)
Use the **NEW format** (MAS 0.12.16+):
- `0.png`, `2-10.png`, `3-10.png`, etc.
- **Do NOT use** the old `acs-[name]-` prefix
- The submod automatically converts for older MAS versions

## ✅ Partial Packs - No Problem!

> 💡 **You don't need to include ALL files!**
> 
> The submod only applies the files included in your pack. MAS will use its original files for anything not included. This means you can create a pack with only the files you want to modify!

For example, if you want to create a custom NOU card design:
- Include only the card images in `cards/`
- The submod applies your custom cards
- SFX and other assets remain as MAS defaults

## 💡 Tips for Pack Creators

1. **Match the original resolution**
2. **Keep transparency** where applicable
3. **Test your pack** before distributing
4. **You can include only the files you want to change**

## 🔄 MAS Version Compatibility

The submod automatically handles file naming differences between:
- **MAS 0.12.16+** (new folder structure)
- **MAS 0.12.15 and below** (old prefix naming)

Pack creators only need to provide the new format - the submod converts automatically.
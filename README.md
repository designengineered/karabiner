# Karabiner Configuration for MacOS

This configuration creates a Vim-inspired typing experience across MacOS with home row mods and window management support.

## Key Features

### Navigation
- **Vim-style Arrow Keys**: `Control + hjkl` for arrow key movement
- **Caps Lock** becomes a multi-function key:
  - Tap for `Escape`
  - Hold for Hyper key (Control + Option + Shift + Command)

### Home Row Modifiers with Smart Backspace Indicator
Left hand:
- `a` → Control
- `s` → Shift
- `d` → Option
- `f` → Command

Right hand:
- `j` → Command
- `k` → Option
- `l` → Shift
- `;` → Control

The home row modifier implementation includes a clever feedback mechanism:
1. When you press a key briefly, it types normally
2. When you hold a key to use it as a modifier:
   - First, the character appears (default behavior)
   - Then, when the hold threshold is reached (170ms), the character is deleted
   - The modifier becomes active
This provides clear visual feedback for when you've entered the modifier layer, while automatically cleaning up the unwanted character.

### Space Bar Modifications
- `Left Shift + Space` → Backspace
- `Left Option + Space` → Delete Word Backward
- `Right Option + Space` → Delete Word Forward
- `Control + Space` → Enter

Note: Unix systems traditionally use `Control + d` for forward deletion (like the Delete key). This functionality is automatically available through our home row mods by holding the `a` key (Control) and pressing `d`.

### Disabled MacOS Shortcuts
- `Cmd + h` (hide window)
- `Cmd + m` (minimize window)
- `Cmd + Option + h/m` (hide/minimize all windows)

## Profiles
1. **Default**: All modifications enabled
2. **Gaming**: Minimal modifications for gaming compatibility

The configuration is optimized for use with a window manager that uses Option as its primary modifier key.

# Tmux Cheatsheet

**Prefix Key: `Ctrl+Space`** (press and release, then press next key)

---

## Panes (Splits)

| Action | Keys |
|--------|------|
| Split vertical | `Prefix` + `\` |
| Split horizontal | `Prefix` + `-` |
| Navigate left | `Ctrl+h` |
| Navigate down | `Ctrl+j` |
| Navigate up | `Ctrl+k` |
| Navigate right | `Ctrl+l` |
| Resize left | `Prefix` + `H` |
| Resize down | `Prefix` + `J` |
| Resize up | `Prefix` + `K` |
| Resize right | `Prefix` + `L` |
| Close pane | `Prefix` + `x` |
| Zoom pane (fullscreen) | `Prefix` + `z` |

---

## Windows (Tabs)

| Action | Keys |
|--------|------|
| New window | `Prefix` + `c` |
| Rename window | `Prefix` + `,` |
| Next window | `Prefix` + `n` |
| Previous window | `Prefix` + `p` |
| Last window | `Prefix` + `Tab` |
| Go to window 1-5 | `Option+1` to `Option+5` |
| Go to window N | `Prefix` + `1-9` |
| Close window | `Prefix` + `X` |
| List windows | `Prefix` + `w` |

---

## Sessions

| Action | Keys |
|--------|------|
| New session | `Prefix` + `S` |
| List sessions | `Prefix` + `s` |
| Rename session | `Prefix` + `$` |
| Detach | `Prefix` + `d` |
| Kill session | `Prefix` + `X` |

### Session Commands (Terminal)
```bash
tmux                     # Start new session
tmux new -s name         # New session with name
tmux ls                  # List sessions
tmux attach -t name      # Attach to session
tmux kill-session -t name
```

---

## Copy Mode (Vim-style)

| Action | Keys |
|--------|------|
| Enter copy mode | `Prefix` + `v` |
| Start selection | `v` |
| Copy | `y` |
| Paste | `Prefix` + `p` |
| Exit copy mode | `Escape` |
| Search down | `/` |
| Search up | `?` |

---

## Utility

| Action | Keys |
|--------|------|
| Reload config | `Prefix` + `r` |
| Sync panes (type in all) | `Prefix` + `a` |
| Command prompt | `Prefix` + `:` |
| Show time | `Prefix` + `t` |
| List keybindings | `Prefix` + `?` |

---

## Plugins (TPM)

| Action | Keys |
|--------|------|
| Install plugins | `Prefix` + `I` |
| Update plugins | `Prefix` + `U` |
| Clean plugins | `Prefix` + `Alt+u` |

### Installed Plugins
- **tmux-sensible** - Sensible defaults
- **tmux-resurrect** - Save/restore sessions (`Prefix` + `Ctrl+s` save, `Prefix` + `Ctrl+r` restore)
- **tmux-continuum** - Auto-save sessions every 15 min
- **vim-tmux-navigator** - Seamless Ctrl+hjkl navigation with Neovim

---

## Visual Layout

```
┌─────────────────────────────────────────────────┐
│ [1:nvim]  [2:server]  [3:logs]     <- Windows   │
├─────────────────────┬───────────────────────────┤
│                     │                           │
│  Pane 1             │  Pane 2                   │
│                     │                           │
│  Prefix + \         │                           │
│  (vertical split)   │                           │
│                     │                           │
├─────────────────────┴───────────────────────────┤
│  Pane 3                                         │
│  Prefix + - (horizontal split)                  │
└─────────────────────────────────────────────────┘
```

---

## Quick Reference

```
Prefix = Ctrl+Space

Splits:    \ (vertical)    - (horizontal)
Navigate:  Ctrl + h/j/k/l  (no prefix!)
Resize:    Prefix + H/J/K/L
Windows:   c (new)  n/p (next/prev)  , (rename)
Sessions:  s (list)  S (new)  d (detach)
Copy:      v (enter)  v (select)  y (copy)  p (paste)
Config:    r (reload)
```

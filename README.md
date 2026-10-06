# Spotify-launcher for niri

Noctalia v5 bar widget that toggles the official Spotify client on [niri](https://github.com/YaLTeR/niri).

| Gesture      | Action                                                                 |
|--------------|------------------------------------------------------------------------|
| Left click   | Launch Spotify if not running; otherwise show it on the focused workspace, or hide it if it is already focused |
| Right click  | Close Spotify                                                          |

niri has no minimize, so hiding moves the window to a parked named workspace.
Declare it in your niri config:

```kdl
workspace "spotify-scratch"
```

Optional: make Spotify open floating when shown:

```kdl
window-rule {
  match app-id="(?i)^spotify$"
  open-floating true
  default-column-width { proportion 0.9; }
  default-window-height { proportion 0.9; }
}
```

## Requirements

- `spotify-launcher`
- niri (with `niri msg` IPC)

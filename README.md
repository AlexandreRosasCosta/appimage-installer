# AppImage Installer

`appimage-installer` is a simple shell script that integrates **AppImage** files into the Linux desktop environment without requiring Flatpak, Snap, or root permissions.

It is designed for users who prefer manual control and a clean user-level setup.

---

## How it works

The script automates the steps normally required to turn an AppImage into a regular desktop application.

When executed, it:

1. Moves (or copies) the `.AppImage` file to `~/.local/bin`
2. Makes the file executable
3. Creates a `.desktop` launcher in `~/.local/share/applications`
4. Optionally downloads or copies an application icon
5. Updates the desktop application database

After that, the application appears in the system menu and can be pinned or launched like any other app.

## Basic usage

```bash
appimage-installer /path/to/application.AppImage "Application Name"
```

### Example

```bash
appimage-installer ~/Downloads/Obsidian.AppImage "Obsidian"
```
## Why use this script?

- No dependency on Flathub or Snap
- No system-wide installation
- No root permissions required
- Reusable for any AppImage
- Clean and predictable file structure

## Files created

```text
~/.local/bin/<app>.AppImage
~/.local/share/applications/<app>.desktop
~/.local/share/icons/<app>.png
```
## Removal

To remove an application installed with this script:

```bash
rm ~/.local/bin/<app>.AppImage
rm ~/.local/share/applications/<app>.desktop
rm ~/.local/share/icons/<app>.png
```
## License

MIT License


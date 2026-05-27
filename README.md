# Pux

Python-powered graphics and game bindings for Rux.

Pux provides simple access to rendering, graphics, and game functionality through a native DLL backend powered by Python and pygame.

---

# Installation

Add Pux to your project:

```bash
rux add Pux
```

Then install dependencies:

```bash
rux install
```

---

# Downloading the Native DLL

Pux requires the native backend library.

Download:

https://github.com/Natuworkguy/Pux/releases/latest/download/pygame_bindings.dll

Place the DLL next to your compiled executable.

Example:

```text
MyGame/
├── Game.exe
├── pygame_bindings.dll
```

---

# Example

```rux
func Main() -> int {
    Pux::pg_init();

    while Pux::pg_running() == 1 {
        Pux::pg_clear();

        Pux::pg_draw_rect(
            100,
            100,
            200,
            150
        );

        Pux::pg_present();
    }

    Pux::pg_quit();

    return 0;
}
```

---

# Building

Compile your Rux project normally:

```bash
rux build
```

Make sure `pygame_bindings.dll` is located beside the generated executable before running.

---

# Requirements

- Python 3.13+
- pygame
- Windows

---

# Notes

- The DLL backend handles communication with Python and pygame internally.
- The Rux package acts as bindings and helper APIs for the native backend.
- Distribute `pygame_bindings.dll` with every built application.

---

# Links

- https://github.com/Natuworkguy/Pux/releases
- https://www.pygame.org
- https://rux-lang.dev

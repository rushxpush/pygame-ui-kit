# pygame-ui-kit
A minimal, lightweight UI toolkit for building menus and UI elements in Pygame.

## ✨ Features (Initial Scope)
- Simple Button rendering (custom colors, text, hover state)

- Text rendering helper (for easy alignment and positioning)

- Mouse over detection

- Click detection

- Minimal dependencies (only requires pygame)

## 🚀 Installation (Local for now)
```bash
# Clone this repository
git clone https://github.com/rushxpush/pygame-ui-kit.git

# Install in editable mode (for local development)
cd pygame-ui-kit
pip install -e .
```

## 📚 Example Usage (Basic Button Render)
```python
import pygame
from ui.button import Button

pygame.init()
screen = pygame.display.set_mode((400, 300))

font = pygame.font.SysFont(None, 36)
button = Button(rect=(100, 100, 200, 50), text="Click Me", font=font)

running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
        if button.was_clicked(event):
            print("Button clicked!")

    screen.fill((30, 30, 30))
    button.draw(screen)
    pygame.display.flip()
```

## 🛠️ Roadmap (Planned Features)
⬛ Text helper (for centered text)

⬛ Basic Button

⬛ Button hover color

⬛ Button click state (visual feedback)

⬛ Sliders / Checkboxes

⬛ Menu system helper

⬛ Support for multiple UI themes (color presets)
# ДЗ 10. Звук, стены и преследование

Музыка зациклена. Игрок и враги перемещаются по клеткам и обходят стены. Компонент Finder реагирует на расстояние по проходам. Система звука отделена от состояния мира.

## Сборка и запуск

Нужны Visual Studio 2022, CMake и [SFML 2.5.1](https://www.sfml-dev.org/download/sfml/2.5.1/) для Windows x64. Распакуйте SFML, замените путь в первой команде на фактический:

```powershell
cmake -S . -B build -A x64 -DSFML_DIR="C:/SFML-2.5.1/lib/cmake/SFML"
cmake --build build --config Release
ctest --test-dir build -C Release --output-on-failure
./build/Release/RoguelikeGame.exe
```

Enter начинает игру. Стрелки или WASD двигают игрока, H применяет аптечку, Space пропускает ход. В [описании игры](gameplay.md) подробнее указаны правила и способы проверки. Для текста используется системный шрифт Consolas.


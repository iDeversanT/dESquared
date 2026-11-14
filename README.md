# dESquared

**Портативный аудиоплеер для Android с «кассетным» интерфейсом.**
Писался под **Anbernic RG Rotate (720×720)** и **HiBy R6III**, работает на любом Android 12+.

[Скачать](../../releases/latest) · [English](#desquared-english)

## Возможности

- **Три вида плеера**: кассета (155 наборов, отрендеренных с фото реальных лент), обложка, волна
  (GLSL-фон в духе PS3/PSP, реагирует на бас и верх).
- **Звук**: параметрический эквалайзер, каталог AutoEq (8800+ профилей, офлайн-поиск), свои пресеты,
  предусилитель, индикатор реального выхода (SRC), кроссфейд и gapless.
- **Файловый менеджер**: внутренняя память, SD-карта, сетевые хранилища SMB2/3; копирование и перенос
  с прогрессом, переименование, создание папок, удаление, поиск, обложки папок.
- **Плейлист**: текущий, избранное, история, **избранные альбомы плитками**, заголовки с годом,
  статистика и достижения, шаффл (в т.ч. предсказуемый), повтор, мультивыбор.
- **Управление**: зоны-жесты по краям экрана, перепривязка аппаратных кнопок, таймер сна, виджеты,
  содержимое экрана блокировки, бэкап настроек одним файлом.
- **Шесть языков**: русский, английский, испанский, китайский, корейский, японский.

## Целевые устройства

- **Anbernic RG Rotate** (720×720, квадратный экран) и **HiBy R6III** (720×1280) — основные.
- Любые Android-плееры и телефоны; для квадратных экранов есть встроенная QWERTY (поиск, переименование).

## Требования

- **Android 12 (API 31)** и новее, ARM64.
- Разрешения: доступ к файлам (музыка), уведомления (управление из шторки и с локскрина).
- SMB-хранилища — в локальной сети; пароли в бэкап не попадают.
- APK ≈ 45 МБ (картинки кассет упакованы в WebP).

## Установка

- APK — в разделе **[Releases](../../releases/latest)**, рядом лежит `.sha256`.
- ⚠️ Сборки **0.5–0.8.8** подписаны другим ключом: перед установкой новой их нужно удалить.
  С **1.0.4** подпись одна, обновление ставится поверх.
- Проверка обновлений — автоматически при запуске, вручную: **Настройки → Проверить обновления**.

## Редактор кассет

Отдельный инструмент, в плеер не входит: **`cassette_editor.7z`** в корне репозитория
(внутри сам редактор и папка `cassettes/` со всеми 155 наборами как примерами).

- Открытие и сохранение наборов, перелистывание по порядку.
- Слои: положение, масштаб, поворот, прозрачность, режим смешивания, порядок по z.
- Наклейка: текст, шрифт (включая свой TTF), размер, рамка, выравнивание, бегущая строка,
  **вертикальные наклейки** для корпусов с полосой вдоль корпуса.
- Выравнивание двух выделенных слоёв одной кнопкой; музейная справка набора (год, заметка, страна) —
  её показывает пикер кассет в плеере.
- Экспорт набора в папку `assets` для Android.
- Запуск (Windows/Linux/macOS): Python 3.11+, `pip install -r requirements.txt` (PySide6, Pillow),
  затем `run_editor.bat` или `python run_editor.py`.

---

# dESquared (English)

**Portable audio player for Android with a cassette-style interface.**
Built for the **Anbernic RG Rotate (720×720)** and **HiBy R6III**, runs on any Android 12+.

[Download](../../releases/latest) · [Русский](#desquared)

## Features

- **Three player views**: cassette (155 skins rendered from photos of real tapes), cover, and wave
  (GLSL background in PS3/PSP spirit, reacts to bass and treble).
- **Sound**: parametric EQ, AutoEq catalog (8800+ profiles, offline search), own presets, preamp,
  real output indicator (SRC), crossfade and gapless.
- **File manager**: internal storage, SD card, SMB2/3 shares; copy and move with progress, rename,
  create folders, delete, search, folder covers.
- **Playlist**: current, favorites, history, **favorite albums as tiles**, headers with year,
  statistics and achievements, shuffle (incl. predictable), repeat, multi-select.
- **Controls**: edge-zone gestures, hardware button remapping, sleep timer, widgets, lock screen
  content, one-file settings backup.
- **Six languages**: Russian, English, Spanish, Chinese, Korean, Japanese.

## Target devices

- **Anbernic RG Rotate** (720×720, square screen) and **HiBy R6III** (720×1280) — primary targets.
- Any Android player or phone; square screens get a built-in QWERTY keyboard (search, rename).

## Requirements

- **Android 12 (API 31)** or newer, ARM64.
- Permissions: file access (music), notifications (shade/lock screen controls).
- SMB shares — local network only; passwords are never included in backups.
- APK ≈ 45 MB (cassette artwork packed as WebP).

## Install

- APK is in **[Releases](../../releases/latest)**, with a `.sha256` next to it.
- ⚠️ Builds **0.5–0.8.8** were signed with a different key: uninstall them before installing a new
  build. Since **1.0.4** the signature is the same and updates install over the old version.
- Update check runs on launch; manually: **Settings → Check for updates**.

## Cassette editor

A separate tool, not part of the player: **`cassette_editor.7z`** in the repository root
(the editor itself plus a `cassettes/` folder with all 155 sets as examples).

- Open and save sets, browse them in order.
- Layers: position, scale, rotation, opacity, blend mode, z-order.
- Label: text, font (custom TTF included), size, frame, alignment, marquee, **vertical labels**
  for cases with a stripe along the body.
- Align two selected layers with one button; set the set's museum note (year, note, country) —
  the cassette picker in the player shows it.
- Export a set into an `assets` folder for Android.
- Run (Windows/Linux/macOS): Python 3.11+, `pip install -r requirements.txt` (PySide6, Pillow),
  then `run_editor.bat` or `python run_editor.py`.

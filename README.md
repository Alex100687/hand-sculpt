# Лепка руками · Hand Sculpt

Лепите 3D-форму руками перед веб-камерой. Всё работает в браузере: видео никуда не отправляется, руки распознаются у вас на компьютере (MediaPipe).

**Открыть:** https://alex100687.github.io/hand-sculpt/

Нужны веб-камера и Chrome или Firefox. Разрешите доступ к камере. Первый запуск занимает несколько секунд: загружается модель рук.

## Жесты

| Жест | Что делает |
|---|---|
| ☝ Вытянутый указательный на кнопке 0.7 с | нажать кнопку или взять ползунок |
| 👌 Большой + указательный, на форме | лепить или красить (можно двумя руками сразу) |
| 🤌 Все пальцы к большому | вращать: рука вбок — поворот, вверх-вниз — вращение вверх-вниз, поворот кисти — наклон |
| 🖐🖐 Две открытые ладони | подержать, пока не замкнётся кольцо, затем к камере — крупнее, от камеры — мельче |

Цвет руки на экране подсказывает, что сейчас происходит: синий — вращение и масштаб, коричневый — лепка, белый — ничего.

## Мышь и клавиши

- ЛКМ на форме — лепить, ЛКМ мимо формы или ПКМ — вращать, Shift + ПКМ — наклон, средняя кнопка — двигать, колесо — размер кисти, Shift + колесо — масштаб.
- 1–7 — инструменты (Тянуть, Вдавить, Надуть, Сгладить, Срезать, Сжать, Краска); `[` `]` — размер кисти.
- Z / Y — назад / вперёд; M — симметрия; G — материал; W — сетка; T — автоповорот; C — центр; D — детальнее.
- B — фон (камера маленьким окном или во весь экран); H — подсказки; Tab — скрыть панели; F — весь экран; I — замеры руки.
- E — сохранить OBJ (с цветом вершин), P — сохранить PNG.

## Запуск у себя

Камера работает только по https или на localhost, поэтому просто открыть файл не получится:

```
python -m http.server 8096
```

Затем откройте http://localhost:8096.

Three.js 0.170 и MediaPipe Tasks Vision 0.10.14 подгружаются с jsDelivr, нужен интернет.

---

## English

Sculpt a 3D shape with your hands in front of a webcam. Runs entirely in the browser; video never leaves your computer (hand tracking by MediaPipe).

**Open:** https://alex100687.github.io/hand-sculpt/ — needs a webcam and Chrome or Firefox.

- ☝ Point with your index finger and hold 0.7 s on a button to press it.
- 👌 Thumb + index on the shape — sculpt or paint (two hands at once work too).
- 🤌 All fingertips to the thumb — rotate: move sideways or up/down, twist the wrist to roll.
- 🖐🖐 Two open palms — hold until the ring closes, then move toward the camera to scale up, away to scale down.

Export: OBJ with vertex colours (E), PNG (P). Run locally with `python -m http.server 8096` and open http://localhost:8096.

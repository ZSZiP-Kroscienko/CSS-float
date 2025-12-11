# Float – Opływanie Elementów Tekstem

## Cel zadania

Nauczenie się właściwości **float** do:
- ✅ Umieszczania obrazów obok tekstu (opływanie)
- ✅ Tworzenia kolumn bez Flexbox/Grid
- ✅ Zawijania tekstu wokół elementów
- ✅ Kontrolowania przepływu treści

---

## Teoria: Czym jest Float?

Float to właściwość CSS, która "unosi" element z normalnego przepływu dokumentu. Inne elementy zawijają się wokół niego.

```
Bez float:              Z float: left:
┌──────────────────┐   ┌──────┐
│ Tekst            │   │Image │ Tekst opaczy się
│ Tekst            │   │      │ wokół obrazu...
│ Tekst            │   │      │ Tekst Tekst Tekst
└──────────────────┘   └──────┘
```

---

## Wartości Float

### 1. `float: left;`

Podnosi element na **lewo**, tekst opływa z prawej strony.

```css
img {
  float: left;
  margin-right: 15px;
}
```

**Wizualizacja:**
```
┌──────────────────────────────┐
│ [IMG]  Tekst opaczy się      │
│ [IMG]  wokół obrazu...       │
│ [IMG]  Tekst Tekst Tekst     │
└──────────────────────────────┘
```

### 2. `float: right;`

Podnosi element na **prawo**, tekst opływa z lewej strony.

```css
img {
  float: right;
  margin-left: 15px;
}
```

**Wizualizacja:**
```
┌──────────────────────────────┐
│ Tekst opaczy się      [IMG]  │
│ wokół obrazu...       [IMG]  │
│ Tekst Tekst Tekst     [IMG]  │
└──────────────────────────────┘
```

### 3. `float: none;`

**Domyślnie.** Element NIE unosi się, pozostaje w normalnym przepływie.

```css
img {
  float: none;  /* Domyślnie */
}
```

**Wizualizacja:**
```
┌──────────────────────────────┐
│ [IMG]                        │
│ Tekst start Tekst Tekst      │
│ Tekst Tekst Tekst Tekst      │
└──────────────────────────────┘
```

### 4. `float: inherit;`

Element **dziedziczy** wartość float od rodzica.

```css
.parent {
  float: left;
}

.child {
  float: inherit;  /* Dziedziczy: left */
}
```

---

## Problem z Float: Zawalenie Kontenera

Gdy wszystkie elementy wewnątrz kontenera mają `float`, kontener się "zawala":

```css
.container {
  background-color: blue;
}

.item {
  float: left;
  width: 50%;
}
```

**Problem:** Kontener nie ma wysokości!

### Rozwiązanie 1: `overflow: hidden;`

```css
.container {
  overflow: hidden;  /* ← Naprawia zawalenie */
  background-color: blue;
}
```

### Rozwiązanie 2: `clear` property

```css
.clearfix {
  clear: both;  /* Czyści float z obu stron */
}
```

```html
<div class="container">
  <img style="float: left;">
  <p>Tekst</p>
  <div class="clearfix"></div>
</div>
```

---

## Praktyczne Przykłady

### Przykład 1: Obraz z tekstem

```html
<div class="article">
  <img src="photo.jpg" alt="Photo">
  <p>Lorem ipsum dolor sit amet...</p>
</div>
```

```css
.article img {
  float: left;
  width: 200px;
  margin-right: 20px;
  margin-bottom: 10px;
}

.article {
  overflow: hidden;  /* Naprawia zawalenie */
}
```

---

### Przykład 2: Dwukolumnowy layout

```html
<div class="layout">
  <aside>Menu</aside>
  <main>Zawartość</main>
</div>
```

```css
aside {
  float: left;
  width: 25%;
}

main {
  float: left;
  width: 75%;
}

.layout {
  overflow: hidden;  /* Naprawia zawalenie */
}
```

---

### Przykład 3: Galeria obrazów

```html
<div class="gallery">
  <img src="1.jpg">
  <img src="2.jpg">
  <img src="3.jpg">
  <img src="4.jpg">
</div>
```

```css
.gallery img {
  float: left;
  width: 25%;
  padding: 10px;
  box-sizing: border-box;
}

.gallery {
  overflow: hidden;
}
```

---

## Kiedy Używać Float?

### ✅ DOBRY POMYSŁ:
- Obraz obok tekstu
- Opływanie tekstu
- Starsze layouty (przed Flexbox/Grid)

### ❌ ZŁY POMYSŁ:
- Pełne layouty stron (lepiej Flexbox/Grid)
- Wyrównywanie (lepiej justify-content)
- Centrowanie (lepiej margin: auto lub Flexbox)

---

## Tabela Porównawcza

| Właściwość | Efekt | Tekst opływa |
|-----------|-------|-------------|
| `float: left;` | Element na lewo | TAK (z prawej) |
| `float: right;` | Element na prawo | TAK (z lewej) |
| `float: none;` | Normalnie | NIE |
| `float: inherit;` | Dziedziczy | Zależy od rodzica |

---

## Clear Property (Czyści Float)

```css
.clear-left {
  clear: left;    /* Czyszczenie float left */
}

.clear-right {
  clear: right;   /* Czyszczenie float right */
}

.clear-both {
  clear: both;    /* Czyszczenie obydwu */
}
```

---

## Narzędzia i Zasoby

- **MDN Float Docs:** https://developer.mozilla.org/en-US/docs/Web/CSS/float
- **CSS Tricks:** https://css-tricks.com/all-about-floats/

---

**Pamiętaj:** Dzisiaj Flexbox i Grid są lepsze do większości przypadków, ale Float wciąż jest przydatny do opływania tekstem! 📝


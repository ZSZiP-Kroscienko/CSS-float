# Float - Karta Pracy Ucznia

**Imię i nazwisko:** _______________  
**Data:** _______________  
**Ocena:** ___/100

---

## I. TESTY WIEDZY

### Pytanie 1: Włączanie Float
Jaka wartość float unosi element na lewo?
- [ ] A) `float: up;`
- [ ] B) `float: left;`
- [ ] C) `float: west;`
- [ ] D) `position: left;`

**Twoja odpowiedź:** ___  
**Punkty:** ___ / 5

---

### Pytanie 2: Float Right
Co robi `float: right;`?
- [ ] A) Przesuwa element w prawo o 100px
- [ ] B) Unosi element na prawo, tekst opływa z lewej
- [ ] C) Ustawia element na krawędzi
- [ ] D) Nic specjalnego

**Twoja odpowiedź:** ___  
**Punkty:** ___ / 5

---

### Pytanie 3: Float None
Jaka wartość wyłącza float (domyślnie)?
- [ ] A) `float: off;`
- [ ] B) `float: nothing;`
- [ ] C) `float: none;`
- [ ] D) `float: disable;`

**Twoja odpowiedź:** ___  
**Punkty:** ___ / 5

---

### Pytanie 4: Float Inherit
Co znaczy `float: inherit;`?
- [ ] A) Element wciąża informacje o float
- [ ] B) Element dziedziczy float od rodzica
- [ ] C) Element ignoruje float
- [ ] D) Element unosi się automatycznie

**Twoja odpowiedź:** ___  
**Punkty:** ___ / 5

---

### Pytanie 5: Clear Property
Kiedy używamy `clear: both;`?
- [ ] A) Nigdy
- [ ] B) Aby zatrzymać opływanie
- [ ] C) Aby wyczyścić cache przeglądarki
- [ ] D) Aby zmienić kolor

**Twoja odpowiedź:** ___  
**Punkty:** ___ / 5

---

## II. ZADANIA PRAKTYCZNE

### Zadanie 1: Obraz z tekstem
Utwórz artykuł z obrazem z lewej, tekst opływa z prawej.

```html
<article>
  <img src="photo.jpg" alt="Photo">
  <p>Lorem ipsum...</p>
</article>
```

**Napisz CSS:**
```css
article img {
  /* DODAJ tutaj */
}

article {
  /* DODAJ tutaj aby naprawić zawalenie */
}
```

**Czy się udało?** TAK / NIE  
**Punkty:** ___ / 10

---

### Zadanie 2: Galeria 4 kolumnowa
Utwórz galerię z 4 obrazkami w jednym wierszu.

**Napisz CSS:**
```css
.gallery {
  /* DODAJ tutaj */
}

.gallery-item {
  /* DODAJ tutaj */
}
```

**Czy się udało?** TAK / NIE  
**Punkty:** ___ / 10

---

### Zadanie 3: Dwukolumnowy layout
Sidebar (25%) z lewej, zawartość (75%) z prawej.

**Napisz CSS:**
```css
.sidebar { /* DODAJ */ }
.content { /* DODAJ */ }
.layout { /* DODAJ aby naprawić zawalenie */ }
```

**Czy się udało?** TAK / NIE  
**Punkty:** ___ / 10

---

### Zadanie 4: Clear - Zatrzymanie opływania
Zatrzymaj tekst, aby nie opływał element.

**Napisz CSS:**
```css
.floated {
  /* DODAJ: float: left; */
}

.stopped {
  /* DODAJ: clear: ? */
}
```

**Czy się udało?** TAK / NIE  
**Punkty:** ___ / 10

---

### Zadanie 5: Float None
Zmień float: none na normalny element.

**Napisz CSS:**
```css
.normal {
  /* DODAJ: float: none; */
}
```

**Czy się udało?** TAK / NIE  
**Punkty:** ___ / 10

---

## III. OBSERWACJE

### Pytanie 1: Co zaobserwowałeś?
Kiedy umieściłeś `float: left` na obrazie, co się stało z tekstem?

**Odpowiedź:**  
_____________________________________________  
_____________________________________________  

**Punkty:** ___ / 5

---

### Pytanie 2: Zawalenie kontenera
Co się stało z kontenerem, gdy wszystkie dzieci miały float?

**Odpowiedź:**  
_____________________________________________  
_____________________________________________  

**Punkty:** ___ / 5

---

### Pytanie 3: Clear vs Overflow
Jaka jest różnica między `clear: both;` a `overflow: hidden;`?

**Odpowiedź:**  
_____________________________________________  
_____________________________________________  

**Punkty:** ___ / 5

---

## IV. BONUS PYTANIA

### Bonus 1: Float vs Flexbox
Kiedy wciąż warto używać float zamiast Flexbox?

**Odpowiedź:** _____________________________________________

**Punkty:** ___ / 5

---

### Bonus 2: Float Inherit
Podaj praktyczny przykład używania `float: inherit;`.

**Odpowiedź:**  
_____________________________________________  
_____________________________________________  

**Punkty:** ___ / 5

---

## V. PODSUMOWANIE

| Kategoria | Punkty | Maks |
|-----------|--------|------|
| Testy wiedzy (5 x 5) | ___ | 25 |
| Zadania praktyczne (5 x 10) | ___ | 50 |
| Obserwacje (3 x 5) | ___ | 15 |
| Bonus (2 x 5) | ___ | 10 |
| **RAZEM** | **___** | **100** |

---

## OCENA

- **90-100** - Doskonale! 🌟
- **80-89** - Bardzo dobrze! ⭐
- **70-79** - Dobrze!
- **60-69** - Zadowalająco - potrzebujesz ćwiczenia
- **< 60** - Niezadowalająco - powtórz materiał

---

## NOTATKI NAUCZYCIELA

_________________________________  
_________________________________  
_________________________________  

**Podpis:** _______________  
**Data:** _______________

---

## WSKAZÓWKI DLA UCZNIÓW

1. **Zawsze naprawiaj zawalenie** - użyj `overflow: hidden;` lub `clear: both;`
2. **Dodaj margin** - `margin-right` dla `float: left`, `margin-left` dla `float: right`
3. **Testuj Live** - otwórz DevTools i obserwuj zmiany
4. **Pamiętaj:** Float to opływanie tekstu - dzisiaj lepiej użyć Flexbox/Grid do layoutu
5. **Clear zatrzymuje** - `clear: left`, `clear: right` lub `clear: both`

---

**Pamiętaj:** Float to najstarsza technika CSS do opływania, ale wciąż przydatna! 📚

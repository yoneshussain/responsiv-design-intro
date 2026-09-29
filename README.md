# 📱 code-along-responsive-design-260929

Fem korta övningar, ett grepp i taget. Vi kodar dem tillsammans under passet.

Temat är en kvarterskrog, men greppen är precis de ni behöver på **torsdagens workshop**, där ni ska bygga desktopvyn av en reseplanerare utifrån en designskiss. Varje avsnitt säger vilken ticket det hör till.

Öppna med Live Server och ha DevTools öppet. Dra i fönstret, hela tiden.

Facit ligger i `code-along-responsive-design-260929-solution`. Titta där när vi gått igenom avsnittet, inte innan.

---

## 📏 1-enheter

Kortet är satt i px rakt igenom.

1. Öppna i **Firefox**: Inställningar → Zooma endast text → 200 %. Ingenting växer. Det är felet.
2. Gör om filen så att sidan följer användarens textstorlek.
3. Zooma igen och kontrollera att layouten håller.

**Använd inte Chrome till det testet.** Chrome saknar textzoom — dess zoom förstorar hela sidan inklusive px, så sidan ser korrekt ut fast den inte är det.

→ Ticket **RWD-2**

## 📐 2-media-queries

Sidan har bara en bas, skriven för smal skärm.

1. Dra ihop fönstret så smalt det går. Sidan ska fungera.
2. Dra långsamt ut det och titta på ingressen. När blir raderna för långa att läsa bekvämt?
3. **Där** sätter ni brytpunkten. Inte vid 768 för att en iPad råkar vara 768.
4. Skriv media queries med `min-width`.

Vi använder bara `min-width`. Blandar man `min-width` och `max-width` blir det snabbt oklart vilken regel som vinner.

→ Ticket **RWD-1** och **RWD-3**

## 👻 3-visa-och-dolj

Hamburgaren syns, menyn är dold. Skriv media queryn som byter plats på dem.

`display: none` tar bort elementet för **alla**, även skärmläsare. Det är rätt här — annars hade menyn lästs upp två gånger. Men därför får det aldrig användas för något som fortfarande ska gå att nå. Till det finns `.dold` längst ner i filen.

**Testa:** tabba genom sidan i båda bredderna. Hamnar fokus på något ni inte ser har ni gömt fel.

→ Ticket **RWD-1** och **A11Y-2**

## ↔️ 4-flexbox

Bokningsformuläret är staplat. Lägg fälten på rad när det finns plats: Datum och Tid delar lika, Gäster är smal och fast, knappen hamnar till höger.

Tre värden att kunna:

- `flex: 1 1 0` — dela lika, oavsett innehåll
- `flex: 1 1 auto` — dela på det som blir över, utgå från innehållet
- `flex: 0 0 10rem` — rör dig inte

→ Ticket **RWD-1**

## ▦ 5-grid

Matsedeln ligger i en kolumn.

1. Gör den till två kolumner när det finns plats, tre på bred skärm — med media queries.
2. Gör sedan om det med `repeat(auto-fit, minmax(26rem, 1fr))`, utan en enda brytpunkt.
3. Jämför. Vad händer vid 1400 px?

→ Ticket **RWD-1**

---

## 🎯 Efter passet

- [Responsiva Flexboxövningar](https://github.com/chasacademy-sandra-larsson/css-rwd-excercises-with-flexbox)
- Gå tillbaka till **u01**: är er egen sida byggd mobile first? Är något låst i px?

Fråga i kanalen om något krånglar!

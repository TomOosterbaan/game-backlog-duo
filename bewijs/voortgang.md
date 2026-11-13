Tom Oosterbaan Student A
Turgay Aldatmaz Student B

Kennischeck les 1

**1. Wat is het verschil tussen de docenten-template, jullie repository en een clone?**
De template is het startproject van de docent. Mijn repository is mijn eigen kopie op GitHub. Een clone is de kopie op mijn laptop.

**2. Waarom ziet je partner een wijziging pas na jouw push en diens pull?**
Een commit staat eerst alleen op mijn laptop. Met push gaat hij naar GitHub, met pull haalt mijn partner hem op.

**3. Welke bestanden worden bij de installatie lokaal aangemaakt?**
`vendor`, `node_modules`, `.env` en `database/database.sqlite`.

**4. Waarom krijgt je partner jouw games niet via GitHub?**
De games staan in mijn lokale database. Git negeert die, dus alleen de code gaat mee.

**5. Waar wordt de titel gecontroleerd en hoe komen de games bij React terecht?**
De titel wordt gecontroleerd in `GameController.php` met `$request->validate()`. Inertia stuurt de games met `Inertia::render('games/index', ['games' => $games])` als prop naar React.


Kennischeck les 2

**1. Waarom heeft de status een Laravel-route en `save()` nodig?**
De status moet in de database staan, anders is hij weg na vernieuwen. De route ontvangt de klik, `save()` bewaart de nieuwe waarde.

**2. Wat is het verschil tussen inloggen en eigenaar zijn van een game?**
Inloggen laat zien wie ik ben. Eigenaar zijn betekent dat de game bij mijn account hoort (`user_id`), alleen dan mag ik hem wijzigen.

**3. Wat zijn props en state in deze pagina?**
`games` is een prop: Laravel stuurt hem naar React. `search` is state: tijdelijke tekst in het zoekveld die verandert terwijl ik typ.

**4. Waarom gebruikt de voortgang `games` en de resultatenteller `visibleGames`?**
De voortgang telt alle games en mag niet veranderen bij zoeken. De resultatenteller toont alleen de games die na het zoeken zichtbaar zijn.

**5. Waarom heeft "Wis zoeken" geen database nodig?**
Het zoekveld is alleen state in React. `setSearch('')` maakt het leeg, er verandert niets aan de opgeslagen games.

**6. Welke code heb je zelf gemaakt, getest en via GitHub overgedragen?**
Challenge A (status wisselen met `!` in `GameController`), B (zoeken met `filter()`), C (teller van uitgespeelde games), D (knop Wis zoeken) en E (resultatenteller). Ik heb ze getest in de browser en gepusht naar GitHub.
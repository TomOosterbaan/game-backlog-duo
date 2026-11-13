Tom Oosterbaan Student A
Turgay Aldatmaz Student B

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
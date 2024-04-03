![[Example-DiscountCoverage.drawio]]
# Rabatt
## ![[Example-DiscountCoverage 1.svg]]Zunächst importieren wir den erforderlichen System-Namespace 
## methode
-   ```Console.Write```
-   ```Console.ReadLine```
-   ```Convert.ToDouble.```

## Wir deklarieren die Klasse DiscountCoverage
-   methode Main
    -   die den Einstiegspunkt für die Konsolenanwendung darstellt.

-  In der Main-Methode deklarieren wir die notwendigen Variablen:
    -   ```input ```ist eine String-Variable  (in der die Eingaben des Benutzers gespeichert werden.)
## boolesche Variablen
-   ```isMember``` & ```isPremiumMember``` sind boolesche Variablen, um zu speichern, ob der Nutzer ein reguläres Mitglied bzw. ein Premium-Mitglied ist.
## Double-Variablen
-   ```totalSum``` und discount sind Double-Variablen, die den Gesamtpreis und den Rabattwert speichern.

-   Dann fragen wir den Benutzer mit Console.Write, ob er ein Kunde ist, und speichern die Eingabe in der Variablen input.
-   Wir verwenden ```Trim()```, um überflüssige Leerzeichen zu entfernen, und
-   ```ToLower()```, um die Eingabe zum leichteren Vergleich in Kleinbuchstaben umzuwandeln.
-   Dann prüfen wir, ob der Benutzer ```"j"``` für yes / Ja eingegeben hat, indem wir ```isMember``` = ```input``` == ```"j"``` verwenden.

# Testfall 1

-   Wir setzen die Gesamtsumme auf 0 und den Rabatt auf 0.
-   Außerdem initialisieren wir ```isPremiumMember``` auf ```false```.

# Testfall 2

-   Wenn der Benutzer ein Mitglied ist,
    -   fragen wir ihn, ob er ein Premium-Mitglied ist und speichern die Eingabe in der Variablen input. 
-  Dann prüfen wir, ob der Benutzer "j" eingegeben hat, indem wir isPremiumMember = input == "j" verwenden.
-   Wir fragen nach dem Gesamtpreis und speichern die Eingabe in der input-Variablen. 
    -  Anschließend wandeln wir die Eingabe mit Convert.ToDouble in ein Double um und speichern sie in der Variablen totalSum.

# Testfall 3

-   Der Wert des Rabatts hängt davon ab, ob der Nutzer ein Mitglied ist oder ob er ein Premium-Mitglied ist.
- Wenn der Nutzer kein Mitglied ist,
    - beträgt der Rabatt 0 oder 2 %, je nach Gesamtpreis. -  Wenn der Nutzer ein Mitglied ist, beträgt der Rabatt 5 % oder 10 %, je nachdem, ob er zusätzlich noch Premium-Mitglied ist oder nicht.

# memberType

-   Anschließend wird der memberType auf der Grundlage des Mitgliedschaftsstatus des Benutzers festgelegt.
- Wir verwenden den ternären Operator, um die String-Verkettung zu vereinfachen.
- Schließlich geben wir das Ergebnis mit Console.WriteLine und String-Interpolation auf der Konsole aus.
    - Darin enthalten sind die Art der Mitgliedschaft, der Wert des Rabatts und der Gesamtpreis.
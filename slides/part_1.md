
### Wofür sind Unit Tests gut?

<!-- .slide: data-background="img/background-orange-orig.jpg" -->

- Regression Testing
- Refactoring Support
- Verifikation der techn. und fachl. Funktionalität
- Dokumentation des Code
- Design von einfachem und wartbarem Code

Note:
- Frühwarnsystem für Fehler
- Unterstützung bei der Restrukturierung von Code
- Verifikation der technischen und fachlichen Funktionalität
  - technische Preconditions
  - fachliche Richtigkeit
- Dokumentation des Codes
- Ermöglichen einfachen Code nach SOLID
  - Tests helfen beim Verständnis und Design einer Klasse
  - Gezwungen nachzudenken
  - Bauen wir das Richtige?
  - Bauen wir es richtig?

---

### SOLID

<!-- .slide: data-background="img/background-title-orig.jpg" -->

- Single Responsibility principle
- Open / Closed principle
- Liskov substitution principle
- Interface segregation principle
- Dependency Inversion

---

### Single Responsibility principle

<!-- .slide: data-background="img/background-title-orig.jpg" -->

> a class should have only a single responsibility (i.e. only one potential change in the software's specification should be able to affect the specification of the class)

Note:
- Führt zu kleinen testbaren Klassen
- Beispiel eine Klasse versucht zuviel, Entity + DB Logic, viele Depedencies nötig
- Bad Small

---

### Open / Closed principle

<!-- .slide: data-background="img/background-title-orig.jpg" -->

> software entities … should be open for extension, but closed for modification.

Note:
- Unit Test zwingen zum sinnvollen Erweitern einer Klasse, weil sonst Test fehlschlagen
- Wenn ich was ändere und Tests fehlschlagen, muss ich mein Design im Kontext des früheren Designs hinterfragen

---

### Liskov substitution principle

<!-- .slide: data-background="img/background-title-orig.jpg" -->

> objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program.

Note:
- Es darf kein Test Modus für Unit Tests im Prduktivcode existieren
- Ableitungen müssen BaseKlassen Tests bestehen
- Zwingt zum Überdenken der Vererbung

---

### Interface segregation principle

<!-- .slide: data-background="img/background-title-orig.jpg" -->

> many client-specific interfaces are better than one general-purpose interface.

Note:
- Je mehr ich mocke, desto schlechter die Dependency
- Unit Tests zwingen zum Überdenken der Interfaces

---

### Dependency Inversion

<!-- .slide: data-background="img/background-title-orig.jpg" -->

> Depend upon Abstractions. Do not depend upon concretions.

Note:
- Tests zwingen zur Betrachtung von Dependencies
- zum Ersetzen und Isolieren jener Abhängigkeiten in der Klasse (DI, Konstruktoren)
- zur Planung von deren Ersetzbarkeit
- Klassiker: Datenbank
- Wenn du nicht mit einem Mock Testen kannst, ist was falsch. Mock ist ein subtype
- Design by contract

# Git Practicum

Mini-repository om Git en GitHub te oefenen. De code hoeft niet te bouwen.

## Start
1. Fork deze repository op GitHub: 'softon26-demo'.
2. Clone de repository in VS Code.
3. Werk in duo's: persoon A en persoon B.

## Deel 1 - Branches en Pull Requests zonder conflict
1. Maak vanaf de actuele 'master' een eigen branch:
   - A: 'feature/debug-info'
   - B: 'fix/loop'
2. A voegt de regel "printf("Scheduling tasks A and B...\n");" toe aan begin van main.
3. B verandert de '1' in de while loop naar 'true'.
4. Iedereen staget, commit en pusht de branch. Open een PR naar `master`.
5. Laat de ander de diff bekijken en eventueel een reviewcomment plaatsen.
6. Merge elkaars branches.
7. De wijzigingen staan op verschillende regels en veroorzaken normaal geen conflict.
8. Checkout naar master en pull allebei weer de laatste versie van de remote

## Deel 2 - Bewust een merge conflict maken
1. A en B maken vanaf 'master' een branch:
   - A: 'conflict/person-a'
   - B: 'conflict/person-b'
2. A verandert in task_a.c de 'status' van 'READY' naar 'SENSOR_OK'.
3. B verandert exact dezelfde waarde van 'READY' naar 'OK'.
4. Beiden stagen, committen en pushen hun branch.
5. Merge eerst A's branch naar 'master'.
6. Probeer daarna B's branch te mergen. Er ontstaat nu een conflict.
7. Herhaal 1-6 voor task_b.c maar dan merget B eerst.
8. Beide lossen hun merge conflict op.

### Conflict oplossen
Open 'main.c' in VS Code. De conflicterende regels worden gemarkeerd:
- '<<<<<<<' = huidige versie
- '=======' = scheiding
- '>>>>>>>' = inkomende versie

Bespreek welke statuswaarde de bedoeling is. Kies bijvoorbeeld 'SENSOR_OK',
verwijder de conflictmarkeringen, sla het bestand op en stage en commit de oplossing.
Rond daarna de merge af (in VS Code of via de GitHub PR).

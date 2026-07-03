# Projektstatus & Spelplan

## Vad det här är

En app som just nu ligger som en fristående HTML-fil. Målet är att flytta den till ett riktigt projekt (React + Vite), lägga den på GitHub, och deploya den på Vercel — så att den går att öppna på mobilen (Safari) och spara data mellan sessioner.

---

## Status just nu

**Version:** HTML-fil, körs lokalt genom att öppnas direkt i webbläsaren. Inte ännu i ett Git-projekt, inte deployad.

**Vad som fungerar:** [fyll i här — vad gör appen redan idag? Vilka funktioner finns i HTML-filen?]

**Vad som saknas innan den kan användas på mobilen:**
- Ligger inte på GitHub än (behövs för att Vercel ska kunna bygga och uppdatera appen automatiskt)
- Inte deployad på Vercel än — fungerar bara lokalt på datorn just nu
- Ingen riktig datalagring — om appen sparar något gör den det troligen bara i webbläsarens minne, vilket försvinner om man stänger fliken eller byter enhet

---

## Vad som saknas / härnäst

**Steg 0 — Välj enklaste vägen (gör detta INNAN steg 1)**
En ensam HTML-fil behöver inte automatiskt bli ett React-projekt. Vercel kan deploya en ren HTML-fil precis som den är, utan ombyggnad. Innan ni börjar bygga om något, kolla:
- Är HTML-filen självständig (all CSS och JavaScript ligger i samma fil, eller i enkla separata filer bredvid)? → Då räcker det troligen att lägga filen som den är i ett GitHub-repo och deploya den direkt. Enklast och snabbast.
- Behöver appen växa mycket (fler sidor, mer komplex logik, återanvändbara komponenter)? → Då kan React + Vite vara värt besväret, men det är ett större steg och bör vägas mot hur appen faktiskt kommer att användas.

**Rekommendation:** starta enkelt. Deploya HTML-filen som den är först. Bygg om till React bara om ni senare stöter på begränsningar den enkla lösningen inte klarar.

**Steg 1 — Få upp koden på GitHub**
- Skapa ett nytt repository (namn beskriver appen, t.ex. `mitt-projekt`)
- Lägg HTML-filen (och ev. andra filer) i repot
- Pusha koden dit

**Steg 2 — Koppla till Vercel**
- Logga in på Vercel med GitHub-kontot (redan klart)
- Importera repot som ett nytt projekt i Vercel
- Vercel bygger och publicerar automatiskt — varje gång man pushar nya ändringar till GitHub uppdateras live-sidan

**Steg 3 — Riktig datalagring (för att kunna spara mellan sessioner och enheter)**
En ren HTML-fil sparar oftast ingenting permanent. Om appen ska komma ihåg data mellan besök behövs ett av följande:
- **Supabase** (rekommenderas — gratis att börja med, enkelt att koppla till en app, fungerar bra ihop med Vercel)
- Annan databaslösning om det redan finns en preferens

**Steg 4 — Testa på mobilen**
- Öppna den publicerade Vercel-länken i Safari på iPhone
- Kontrollera att allt ser bra ut och fungerar (responsiv design — HTML-filer byggda för dator kan behöva justeras för att se bra ut på en mindre skärm)

---

## Så vill jag att du (Claude Code) jobbar

Du är min tekniska guide och mentor. Jag är nybörjare på kod men vill bygga webbappar, AI-drivna appar, verktyg och landningssidor.

**KOMMUNIKATION**
- Förklara alltid på svenska om jag inte ber om annat
- Håll det enkelt — undvik jargong, förklara termer när de dyker upp
- Var direkt och praktisk, inte teoretisk

**NÄR VI BYGGER**
- Föreslå alltid det enklaste sättet att komma igång
- Berätta vilket verktyg som passar bäst: Claude Code, Artifacts, eller annat
- Dela upp stora idéer i små, hanterbara steg
- Ge mig kod som faktiskt fungerar direkt

**BOLLPLANK**
- Ställ motfrågor för att förstå vad jag egentligen vill bygga
- Hjälp mig prioritera: vad är MVP vs nice-to-have?
- Varna mig om en idé är onödigt komplex för en nybörjare

**VERKTYG VI ANVÄNDER**
- Claude Artifacts: snabba prototyper direkt i chatten
- Claude Code: när vi bygger något mer fullständigt
- Förklara skillnaden och rekommendera rätt verktyg per situation

---

## Definition av klar (för att jag ska vara nöjd)

- [ ] Koden ligger på GitHub
- [ ] Appen är deployad och live på Vercel
- [ ] Fungerar korrekt på mobilen i Safari
- [ ] Data sparas riktigt mellan sessioner (inte bara i webbläsarens minne)

# GroceryApp Sprint 1 - Studentversie  
In deze versie zijn de wijzigingen doorgevoerd en is de code compleet.  

## Studentversie:  
**UC01 Tonen boodschappenlijsten**  
Is compleet.

**UC02 Tonen inhoud boodschappenlijst**   
In het bestand `GroceryListItem.cs` uit het project GroceryApp.Models:
- De member variabelen wijzigen in properties
- In de constructor de doorgegeven waarden koppelen aan de properties.

**UC03 Tonen producten**  
In het bestand `ProductRepository.cs` uit het project GroceryApp.Data:
- Initieer in de constructor de lijst met 4 nieuwe producten:  
  - Melk[voorraad 300]
  - Kaas[voorraad 100]
  - Brood[voorraad 400]
  - Cornflakes[voorraad 0]
- In de methode GetAll() zorg je dat de lijst met producten wordt meegegeven.
Ik ga je helpen met het inschakelen van Developer Mode in Windows 11. Er zijn inderdaad twee manieren: de normale wijze via de instellingen en de wijze via het register.

# Instellen Windows Developer Modus

## Methode 1: Normale wijze via Windows Instellingen

1. **Open Windows Instellingen**:
   - Druk op `Windows + I` of klik op Start → Instellingen

2. **Ga naar Privacy & beveiliging**:
   - Klik op "Privacy & beveiliging" in het linker menu

3. **Zoek Developer Mode**:
   - Scroll naar beneden naar "Voor ontwikkelaars"
   - Klik op "Voor ontwikkelaars"

4. **Schakel Developer Mode in**:
   - Selecteer "Ontwikkelaarsmodus" (Developer Mode)
   - Windows zal waarschuwen over de risico's - klik op "Ja" om te bevestigen
   - Windows zal mogelijk vragen om opnieuw op te starten

## Methode 2: Via het Windows Register
**Waarschuwing**: Het bewerken van het register kan je systeem beschadigen als je niet voorzichtig bent. Maak altijd een back-up van het register voordat je wijzigingen aanbrengt.

Je dient hiervoor 2 waarden aan te passen.

1. **Open Register Editor**:
   - Druk op `Windows + R`
   - Typ `regedit` en druk op Enter
   - Klik op "Ja" wanneer Windows om toestemming vraagt

2. **Navigeer naar de juiste locatie**:
   ```
   HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModelUnlock
   ```

3. **Wijzig de waarde**:
   - Zoek de DWORD-waarde genaamd `AllowDevelopmentWithoutDevLicense`
   - Dubbelklik erop
   - Wijzig de waarde van `0` naar `1`
   - Klik op "OK"

2. **Navigeer naar de juiste locatie**:
   ```
   HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Appx
   ```

3. **Wijzig de waarde**:
   - Zoek de DWORD-waarde genaamd `AllowDevelopmentWithoutDevLicense`
   - Dubbelklik erop
   - Wijzig de waarde van `0` naar `1`
   - Klik op "OK"

4. **Herstart je computer**:
   - Herstart Windows om de wijzigingen toe te passen (niet perse nodig)

## Verificatie

Na het inschakelen van Developer Mode kun je controleren of het werkt:

1. Ga terug naar Instellingen → Privacy & beveiliging → Voor ontwikkelaars
2. Je zou nu "Ontwikkelaarsmodus" moeten zien als geselecteerd
3. Je kunt ook controleren of je nu toegang hebt tot ontwikkelaarstools zoals:
   - Windows Subsystem for Linux (WSL)
   - Device Portal
   - Remote debugging

## Voordelen van Developer Mode

Met Developer Mode ingeschakeld krijg je toegang tot:
- Het installeren van apps uit onbekende bronnen
- Windows Subsystem for Linux (WSL)
- Device Portal voor remote debugging
- PowerShell script execution policies
- Visual Studio debugging tools

**Tip**: Voor de meeste ontwikkelaars is Methode 1 (via Instellingen) de veiligste en eenvoudigste optie. Gebruik alleen de register-methode als je specifieke redenen hebt om dit te doen.
# Freiburg V2 Control Center

Geschütztes Discord-Server-Dashboard mit Discord OAuth2.

## Funktionen
- Anmeldung mit Discord; Zugriff nur mit einer Discord-Rolle, die Administratorrechte besitzt.
- Serverübersicht und Mitgliederliste.
- Kanäle erstellen und löschen.
- Rollen erstellen und löschen (Administratorrollen sind vor Löschung geschützt).
- Mitglieder kicken.

## Railway
1. Als eigenen Railway-Service aus diesem Repository deployen.
2. Variablen `.env.example` in Railway setzen. Bot-Token und OAuth-Client-Secret ausschließlich serverseitig als Variablen speichern.
3. Im Discord Developer Portal unter OAuth2 Redirects exakt `PUBLIC_URL/auth/callback` eintragen.
4. Dem Bot die nötigen Berechtigungen geben: View Channels, Manage Channels, Manage Roles, Kick Members und View Server Insights. Die Bot-Rolle muss über verwalteten Rollen stehen.

Das Dashboard bleibt unabhängig vom Bot-Prozess verfügbar. Die aktuelle Version verwaltet die genannten Discord-Grundfunktionen; weitere Bot-Konfigurationen und Moderationsmodule werden später ergänzt.
LERNWERK – Android-Projekt (Prototyp)
====================================

Dieses Projekt verpackt den vorhandenen LERNWERK-Arbeitsblattgenerator in eine Android-WebView-App.
Es ist noch keine APK. Der GitHub-Actions-Workflow baut bei einem Push oder manuellem Start eine Debug-APK.

APK nur mit Smartphone bauen:
1. ZIP entpacken (Dateimanager-App).
2. Bei GitHub anmelden und ein neues Repository namens lernwerk-android erstellen.
3. Die entpackten Projektdateien ins Repository hochladen; wichtig: .github/workflows/build-apk.yml muss mit hochgeladen werden.
4. Tab "Actions" öffnen. "Build LERNWERK APK" wählen und "Run workflow" drücken (oder Upload/Commit ausführen).
5. Nach erfolgreichem Lauf den Lauf öffnen, unten "Artifacts" → "LERNWERK-debug-APK" herunterladen und ZIP entpacken.
6. app-debug.apk öffnen. Android kann fragen, ob der Dateimanager Installationen aus dieser Quelle erlauben darf. Nur installieren, wenn die Datei aus deinem eigenen GitHub-Build stammt.

WICHTIGE EINSCHRÄNKUNGEN
- Das ist ein Debug-Build zum Testen, keine veröffentlichungsfertige Play-Store-App.
- Die bestehenden Generatorfunktionen laufen lokal im App-Fenster. Die HTML-App hat aktuell keinen eingebauten KI-API-Aufruf; sie kann vorhandene Prompt-/Vorlagenfunktionen nutzen. Für echte KI-Generierung ist ein sicherer Server-Endpunkt und ein KI-Anbieter erforderlich. Niemals einen privaten API-Schlüssel direkt in die APK einbauen.
- Das Projekt wurde hier nicht auf einem Android-Gerät gebaut oder getestet. Wenn GitHub Actions fehlschlägt, muss der Build-Fehler korrigiert werden.

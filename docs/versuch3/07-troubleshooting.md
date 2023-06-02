# Troubleshooting

## Ingestierte Datei wird nicht transcodiert

Werden ingestierte Dateien nicht automatisch transcodiert, liegt der Fehler meist in der Lambda-Funktion. Um dies zu kontrollieren, sollte erst in MediaConvert nachgeschaut werden, ob der Transcodierauftrag überhaupt erstellt wurde. Wurde der Auftrag gar nicht erstellt, liegt das Problem bei Lambda. Wurde der Auftrag erstellt, aber wurde aufgrund eines Fehlers abgebrochen, kann die Fehlermeldung in MediaConvert nachgelesen werden.

### Lambda-Funktion erstellt keinen Transcodierauftrag

Wird kein Transcodierauftrag erstellt, liegt dies an der Lambda-Funktion. Als Erstes sollte kontrolliert werden, dass die Queue usw. richtig eingetragen wurden. Zusätzlich sollte überprüft werden, ob die Funktion korrekt aus der Versuchsanleitung kopiert wurde. Werden keine Probleme erkannt, kann AWS CloudWatch geöffnet werden. Dort finden sich unter "Protokollgruppen" die Log-Daten der Lambda-Funktionen. Fehler beim Ausführen der Funktionen werden hier angezeigt.

## Transcodierte Datei wird nicht hochgeladen

Wird eine ingestierte Datei zwar transcodiert, aber nicht via FTP hochgeladen, liegt der Fehler vermutlich in der Lambda-Upload-Funktion. Hier sollten vor allem die FTP-Zugangsdaten kontrolliert werden. Ebenso sollte überprüft werden, ob der Funktions-Code korrekt aus der Versuchsanleitung übernommen wurde. Lässt sich der Fehler so nicht beheben, kann ebenfalls via AWS CloudWatch in die Logs Einsicht genommen werden.

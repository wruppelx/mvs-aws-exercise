# Testen

Um die automatische Transcodierung zu testen, soll eine Datei aus dem mp4-Bucket "a--sourcefiles" mithilfe der S3 Weboberfläche in den Ingestordner kopiert werden. Danach sollte ein neuer Stranscodierauftrag bei MediaConvert gestartet werden.

Nach der Transcodierung kann auf dem FTP-Server nachgesehen werden, ob die Inhalte hochgeladen wurden. Das Abspielen kann wie in Versuch 2 mithilfe des HLS Players geschehen.

!!! question "Frage 4"
    Erstellen Sie in Mediaconvert -> Aufgabenvorlagen eine eigene Transcodier-Vorlage und exportieren Sie diese als JSON. Laden Sie die Datei unter dem Namen hls2_template.json in den Tempates Ordner in Ihrem Bucket hoch und ändern Sie die CreateJob Funktion so ab, dass diese neue Template genutzt wird. Ihre Template soll auch in HLS transcodieren, jedoch sollen Sie die Transcodiereinstellungen wählen. Dokumentieren Sie diese in ihrem Bericht
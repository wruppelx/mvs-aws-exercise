# Download

Ist die Quelldatei fertig transkodiert, werden die resultierenden Dateien im eigenen Bucket angezeigt und können über die S3-Weboberfläche heruntergeladen werden.

## Inspektion

Zur Kontrolle, ob alle Kodierungsparameter berücksichtigt wurden, lässt sich die Datei in MediaInfo öffnen. MediaInfo zeigt detailiert Eigenschaften und Metadaten für vielerlei verschiedene Medien an und kann auch zur Überprüfung der Datei genutzt werden. 

Schon die Übersicht zeigt die Videodatenrate und die Audiodatenrate. Ebenso werden die verwendeten Audio- und Video-Codecs angezeigt. In anderen Ansichten, wie die "Tree"-Ansicht sind auch tiefergehende Eigenschaften wie Farbraum und Chroma-Subsampling aufgelistet.

![MediaInfo](../assets/versuch1/metadaten_mediainfo.png)

!!! question "Frage 1"
    Welche 3Kodierungsparameter wurden von MediaConvert für die verschiedenen Formate gewählt? Geben Sie die Parameter in einer Tabelle mit der folgenden Form an:

    | Parameter            | `_1080p` | `_720p` | `_480p` |
    | -------------------- | -------- | ------- | ------- |
    | Container-Format     |          |         |         |
    | Gesamtbitrate        |          |         |         |
    | Video-Codec          |          |         |         |
    | Codec-Profil / Level |          |         |         |
    | Video-Bitrate        |          |         |         |
    | Auflösung (b x h)    |          |         |         |
    | Chroma-Subsampling   |          |         |         |
    | Farbtiefe            |          |         |         |
    | Full Range / Limited |          |         |         |
    | Primärvalenzen       |          |         |         |
    | Audio-Codec          |          |         |         |
    | Audio-Bitrate        |          |         |         |
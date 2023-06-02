# Fazit

In Versuch 3 wurden die Grundprinzipien eines automatisieren Transcoding-Workflows erläutert und ein solcher in AWS erstellt. Sobald Rohmaterial ingestiert wurde, wurde dieses in HLS transcodiert und zum Origin-Server des CDNs hochgeladen.

## Abgabe

In der Abgabe sollte mindestens ein Beispiel für transcodierte Dateien mit der gegebenen Vorlage und ein Beispiel für transcodierte Dateien mit der eigenen Vorlage enthalten sein. **Dabei müssen nicht alle Dateien in die Abgabe eingefügt werden, sondern jeweils nur die Index-Dateien und ein Segment jeder Qualitätsstufe.**

Außerdem können die Lambdafunktionen CreateJob und UploadFile als .py-Datei abgegeben werden, falls sie nicht als Screenshot oder Text im Bericht enthalten sind.

```
📁 Versuch 3
    📁 Standard Vorlage
        📄 Clip1.m38u
        📄 Clip1_480p.m38u
        📄 Clip1_720p.m38u
        📄 Clip1_1080p.m38u
        📄 Clip1_480p_00001.ts
        📄 Clip1_720p_00001.ts
        📄 Clip1_1080p_00001.ts
    📁 Eigene Vorlage
        📄 Clip2.m38u
        📄 Clip2_low.m38u
        📄 Clip2_high.m38u
        📄 Clip2_low_00001.ts
        📄 Clip2_high_00001.ts
    📁 Templates
        📄 musterstudent_template2.json
        ...
    ...
```
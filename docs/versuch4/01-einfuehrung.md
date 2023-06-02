# Einführung

In diesem Versuch soll näher auf die Kommandozeile und die APIs von AWS eingegangen werden. Zuerst werden einige Befehle auf der AWS CloudShell ausgeführt und danach werden die Lambda-Funktionen aus Versuch 3 mit zusätzlichen Funktionen ausgestattet.

## Grundbegriffe

### AWS CloudShell

![AWS CloudShell Logo](../assets/versuch4/aws_cloudshell.svg){ align=left style="height:125px;width:125px" } AWS CloudShell bietet Zugang zu einer voreingestellte Kommandozeile über den Browser. Die nötigen APIs und Bibliotheken sowie gebräuchliche Entwicklertools (z.B. Python) sind bereits installiert. Somit ist beispielsweise die Installation der AWS-Kommandozeile auf dem lokalen PC nicht nötig.

In der CloudShell gespeicherte Scripte und sonstige Daten werden auch nach dem Schließen des Browsers gespeichert. Bis zu 1GB Daten lassen sich im Benutzerverzeichnis ablegen.

Bei CloudShell handelt es sich um ein Entwicklungstool. Sollen z.B. Python-Scripts anhand von Auslösern oder regelmäßig ausgeführt werden, sollte weiterhin Lambda genutzt werden, da sich die CloudShell nach einem Timeout in den Standby-Modus versetzt.

!!! info "Kosten"
    AWS CloudShell wird kostenlos zur Verfügung gestellt. Einzig die über die CloudShell erstellten Ressourcen kosten wie gewohnt Geld. Datentransfer von der CloudShell zu anderen Services wird zu den üblichen AWS Konditionen berechnet. Bei den üblichen geringen Datenmengen sind diese Kosten zu vernachlässigen.

### AWS CLI

![AWS CLI Logo](../assets/versuch4/aws_cli.svg){ align=left style="height:125px;width:125px" } Der Kommandozeilen-Zugang (engl. Command Line Interface) bietet die Möglichkeit AWS Ressourcen und Konfigurationen mithilfe der Kommandozeile zu steuern. Das Kommandozeilen-Tool kann sowohl auf dem eignen Rechner installiert als auch über AWS CloudShell genutzt werden. Bei der Ausführung in der CloudShell müssen keine Authentifizierungs-Daten angegeben werden, da die CloudShell an sich durch den eigenen Benutzer authentifiziert ist.

Das Kommandozeilen-Tool kann wie jedes andere Programm der Kommandozeile auch durch ein Bash-Script ausgeführt werden. Dies bietet erfahrenen Nutzern der Kommandozeile die Möglichkeit, schnell eine Reihe von Ressourcen zu erstellen, mehrere Buckets auf einmal zu löschen oder ganze Buckets herunterzuladen. 

### AWS Python SDK (boto3)

![AWS SDK Logo](../assets/versuch4/aws_python_sdk.svg){ align=left style="height:125px;width:125px" } Das Software-Entwicklungs-Kit (SDK) für AWS in Python heißt boto3. Über diese Bibliothek können, wie auch mit der Kommandozeile Ressourcen aufgelistet, erstellt und gelöscht werden.

Das Ausführen von Python-Scripten mit der boto3 Bibliothek ist ohne weitere Einstellungen von der AWS CloudShell möglich. Neben der automatischen Authentifizierung bietet die Ausführung in der CloudShell eine deutlich geringere Latenz als die Ausführung auf dem lokalen PC.
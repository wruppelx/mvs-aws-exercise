# Versuchsanleitung

## Kurzfassung

In dieser praktischen Übung zum Thema Cloud-Transcodierung soll ein grundlegendes Verständnis für cloudbasierte Transcodierung für Video-on-Demand-Systeme geschaffen werden. Außerdem sollen erste Praxiserfahrungen mit den Cloud-Anbietern AWS und Akamai vermittelt werden.

## Einleitung

Video-on-Demand-Systeme (VoD) sind aus dem alltäglichen Leben nicht wegzudenken - Youtube, Netflix und vielleicht sogar die ARD Mediathek. Der Aufbau eines VoD-Systems in der Cloud ist in den letzten Jahren denkbar einfach geworden. Cloud-Anbieter wie Amazon Web Services (AWS) und Akamai bieten verschiedene Werkzeuge an, um Medien zu ingestieren, zu speichern, zu konvertieren und letztendlich zu verbreiten.

## Workflow

Grundsätzlich folgt der Distributionsweg bei VoD-Systemen meist einem ähnlichen Ablauf. Mediendateien werden in hoher Qualität in das System eingespeist und nicht öffentlich gespeichert. Je nach Distributionsweg kann die Quelldatei in verschiedene Distributionsformate transcodiert werden, um auf verschiedenen Geräten wiedergegeben werden zu können. Die transcodierten Dateien können außerdem noch mit einem Kopierschutz versehen werden.

Sind die verschiedenen Distributionspakete erstellt, können sie über ein Content-Delivery-Network (CDN) verteilt werden. Nutzer greifen dabei über eine Weboberfläche (Frontend) auf die im CDN gespeicherten Medien (Backend) zu.

![Cloud Transcoder Workflow](assets/diagrams/workflow.svg#only-light){ style="width:100%" }
![Cloud Transcoder Workflow](assets/diagrams/workflow_dark.svg#only-dark){ style="width:100%" }

In der Praxis wird dieser simple Ablauf noch mit verschiedenen Steuerungs- und Monitoriung-Werkzeugen ergänzt, um Arbeitsschritte zu automatisieren oder bspw. dem zuständigen Mitarbeiter Benachrichtigungen zu senden, sobald eine Datei transcodiert wurde.

## Cloud-Anbieter

> The Cloud Is Just Someone Else's Computer

Cloud-Anbieter sind Firmen, die Rechenleistung oder ähnliche Dienstleistungen für ihre Kunden anbieten. Der Nutzer muss keine eigene Hardware bereitstellen, sondern mietet diese für einen gewissen Zeitraum an. Bei Bedarf kann so flexibel und für einen kurzen Zeitraum mehr oder weniger Ressourcen gebucht werden.

Das Angebot kann man grob in 3 Bereiche unterteilen: *"Infrastructure as a Service (IaaS)"* stellt Computing- oder Netzwerk-Infrastruktur wie Server und Router zur Verfügung. *"Platform as a Service (PaaS)"* bietet Plattformen wie Speicherplatz oder Kubernetes-Cluster an, ohne dass sich der Kunde mit dem darunterliegenden Betriebssystem befassen muss. *"Software as a Service (SaaS)"* abstrahiert weiter und stellt reine Softwarelösungen wie Transcoder oder Benachrichtigungen zur Verfügung.

Einige Cloud-Anbieter sind *AWS*, *Microsoft Azure*, *Akamai* oder *Linode*.

!!! info
    Für die folgenden Versuche werden die Plattformen von **AWS** für Speicherung, Monitoring und Transcodierung sowie das Content-Delivery-Network von **Akamai** benutzt.

!!! danger "Kosten"

    Produkte von Cloud-Anbietern werden meist pro Zeiteinheit abgerechnet. Wenn bspw. ein erstellter Server nach Benutzung nicht wieder abgeschaltet/vernichtet wird, können hohe Kosten entstehen, die erst bei der monatlichen Abrechnung offensichtlich werden. Wenn für eine Aufgabe 100 statt 10 Instanzen gestartet werden, können die Kosten schnell in die Höhe schnellen.

### Weboberfläche

Cloud-Produkte lassen sich am einfachsten über eine grafische Weboberfläche einrichten und bedienen. Diese bietet die übersichtliche Bedienung, ist jedoch weniger leicht zu automatisieren. Mithilfe der Log-in-Daten können mit wenigen Klicks Ressourcen hinzugefügt oder entfernt werden. Die Weboberfläche nennt sich bei AWS *"Konsole"*.

### Kommandozeile

Neben der grafischen Oberfläche können Cloud-Ressourcen auch mithilfe von Kommandozeilen-Anwendungen (CLI) sowie Skripten bestellt und bedient werden. Zwar ist dies nicht so übersichtlich für Anfänger, jedoch können fortgeschrittene Nutzer schneller und automatisierter Ressourcen buchen und Workflows erstellen.

## Versuche im Überblick

| Nr.                                    | Beschreibung
| -------------------------------------- | --------------------------------------------------------------- |
| [Versuch 1](./versuch1/01-einfuehrung) | Behandelt die grundlegenden Konzepte eines **Cloud-Transcoders**|
| [Versuch 2](./versuch2/01-einfuehrung) | Behandelt die grundlegenden Konzepte eines **CDNs**             |
| [Versuch 3](./versuch3/01-einfuehrung) | Aufbau eines **automatisierten** VOD-Systems                    |
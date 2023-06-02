# Troubleshooting

## Elemental MediaConvert darf nicht auf den S3 Bucket zugreifen (Access denied)

Wenn Elemental MediaConvert nicht die erforderlichen Rechte besitzt, um auf den S3 Objektspeicher zuzugreifen, wird der Transcodierauftrag mit einer Fehlermeldung beendet.

Hier lohnt es sich zu kontrollieren, dass beim Transcodierauftrag "Verwenden einer vorhandenen Servicerolle" im Bereich "AWS-Integration" gewählt wurde und die bereits bestehende Rolle "MediaConvert_Default_Role" ausgewählt wurde.
# CompanyOS Releases

Öffentliche, automatisch geprüfte Installer und Update-Metadaten für CompanyOS.
Der Quellcode bleibt in einem privaten Repository.

## Kostenfreie Release-Pipeline

Der Build läuft in diesem öffentlichen Repository auf den kostenlosen
Standard-Runnern von GitHub. Der Workflow kann ausschließlich manuell gestartet
werden und checkt genau einen unveränderlichen Release-Tag aus dem privaten
Quell-Repository aus. Ein read-only Deploy-Key gewährt nur Lesezugriff auf den
Quellcode; Pull Requests und normale Pushes können den Workflow nicht auslösen.

Ein Release wird zunächst als Entwurf erzeugt. Erst wenn macOS- und
Windows-Installer, Tauri-Signaturen und `latest.json` vollständig validiert
sind, veröffentlicht der Workflow den Entwurf automatisch.

Der Workflow wird normalerweise vom lokalen Release-Skript im privaten
Quell-Repository gestartet. Ein fehlgeschlagener Build kann von einem
Repository-Administrator unter **Actions → CompanyOS Release → Run workflow**
mit der bereits getaggten Version wiederholt werden.

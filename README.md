# Ansible Repository Dokumentation

## Übersicht
Dieses Git-Repository enthält die komplette Ansible-Aussetzung zur Bereitstellung und Verwaltung einer Active Directory-Umgebung. Es umfasst alle notwendigen Playbooks, Inventories, Rollen und Konfigurationen, um die Bereitstellung und Wartung einer AD-Infrastruktur zu automatisieren.

## Inhalt des Repositories

- **Playbooks**: YAML-Dateien, die Aufgaben zur Konfiguration und Verwaltung der Infrastruktur definieren.
- **Inventories**: Dateien und Verzeichnisse zur Organisation von Host- und Gruppenvariablen.
- **Rollen**: Modulare Komponenten für wiederverwendbaren Ansible-Code.
- **Konfigurationsdateien**: Anpassbare Ansible-Konfigurationen zur Optimierung der Ausführung und Umgebungseinrichtung.

## Verzeichnisstruktur
Das Repository ist wie folgt organisiert:
```
ansible/
|-- inventories/
|   |-- devel/
|       |-- group_vars/
|       |-- host_vars/
|       `-- inventory.yml
|-- playbooks/
|   `-- example_playbook.yml
|-- roles/
|-- ansible.cfg
```

## Verwendung

### Einrichtung überprüfen
Prüfen Sie, ob der Control-Host mit den Zielhosts kommunizieren kann:
```bash
ansible all -m ping
```
Für Windows-Hosts:
```bash
ansible all -m win_ping
```

### Playbooks ausführen
Beispiel zur Konfiguration eines Domain Controllers:
```bash
ansible-playbook playbooks/setup_dc.yml
```

## Zusätzliche Informationen
- Ausführliche Dokumentation finden Sie in der [Ansible-Dokumentation](https://docs.ansible.com/).

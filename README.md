Aktualisiertes README-Dokument für die Management-App für Tieradoptionszentren

Beschreibung der Anwendung:
Die Anwendung ist ein umfassendes Verwaltungssystem für Tierheime, das eine effiziente Organisation und Transparenz im Adoptionsprozess ermöglicht. Sie erlaubt es Nutzern, Informationen zu Tieren in verschiedenen Heimen abzurufen, Adoptionsanträge zu stellen, Freiwillige und Tierärzte zu verwalten sowie Gesundheits- und Pflegeinformationen digital zu speichern.
Die Plattform verbessert die Vermittlungschancen von Tieren und die Qualität der Pflege, indem sie zentrale Funktionen für Tierheime und Adoptanten bereitstellt.

Liste der Funktionalitäten:
1. Tier- und Adoptionsmanagement
Tiere durchsuchen: Ermöglicht das Durchsuchen von Tierprofilen mit Details wie Name, Art, Alter, Gesundheitsakte, Pflegeanforderungen und Verfügbarkeit.
Adoptionsanfragen stellen: Benutzer können für ausgewählte Tiere Anfragen stellen und deren Status in Echtzeit verfolgen („in Bearbeitung“, „genehmigt“ oder „abgelehnt“).
Adoption abschließen: Bei Genehmigung eines Antrags wird das Tier als adoptiert markiert.
2. Freiwilligen- und Tierarztverwaltung
Freiwilligenmanagement: Registrierung und Verwaltung von Freiwilligen, die Aufgaben entsprechend ihrer Erfahrung übernehmen.
Tierarztverwaltung: Eintragen und Organisieren von Tierärzten mit Spezialisierungen wie Chirurgie oder Allgemeinmedizin.
3. Adoptionsprozess-Management
Antragsstatus verfolgen: Detaillierte Nachverfolgung des Status und Fortschritts von Adoptionsanfragen.
Adoptionsanträge verwalten: Genehmigung oder Ablehnung von Anträgen durch Tierheime mit automatischer Anpassung der Tierprofile.
4. Gesundheits- und Pflegedokumentation
Gesundheitsakte: Speichert Diagnosen und Behandlungen jedes Tieres.
Pflegepläne: Individuelle Pflegepläne, einschließlich Futterplänen und medizinischer Versorgung, um die speziellen Anforderungen von Tieren zu erfüllen.

Implementierte Methoden:
Adoptant:
- CRUD für Adoptanten: Hinzufügen, Abrufen, Aktualisieren und Löschen von Adoptanten.
- Filtern und Sortieren:
	Filterung von Adoptanten nach der Anzahl ihrer Adoptionsanfragen.
	Sortierung nach der Gesamtanzahl von Adoptionen.
- Adoptionsprozess: Erstellung und Verwaltung von Adoptionsanfragen.
AdoptionRequest:
- Adoptionsanträge verwalten: Erstellung, Genehmigung und Ablehnung von Anträgen.
- Analyse von Anfragen: Gruppierung und Sortierung von Adoptanten nach der Gesamtzahl gestellter Anfragen.
Volunteer:
- CRUD für Freiwillige: Hinzufügen, Abrufen, Aktualisieren und Löschen von Freiwilligen.
- Filter und Zuweisung:
	Filtern von Freiwilligen nach der Anzahl betreuter Tierheime.
	Zuweisung von Tieren an Freiwillige.
	Sortierung von Freiwilligen nach ihrer Erfahrung.
Animal:
- CRUD für Tiere: Hinzufügen, Abrufen, Aktualisieren und Löschen von Tierinformationen.
- Sortieren und Filtern:
	Sortierung von Tieren nach Alter (aufsteigend).
	Filterung von Tieren basierend auf ihrem Status (z. B. „verfügbar“, „adoptiert“).
Veterinarian:
- CRUD für Tierärzte: Hinzufügen, Abrufen, Aktualisieren und Löschen von Tierarztinformationen.
- Sortieren und Filtern:
	Sortierung von Tierärzten nach ihrer Spezialisierung.
	Filterung von Tierärzten basierend auf einer bestimmten Spezialisierung.
HealthRecord:
- CRUD für Gesundheitsakten: 
	Hinzufügen einer neuen Gesundheitsakte für ein Tier.
	Abrufen aller gespeicherten Gesundheitsakten.
	Aktualisieren einer vorhandenen Gesundheitsakte.
	Löschen einer Gesundheitsakte anhand ihrer ID.
- Zuweisen einer Gesundheitsakte zu einem Tier:
Verknüpfung einer Gesundheitsakte mit einem bestimmten Tier basierend auf dessen ID.
CarePlan:
- CRUD für Pflegepläne:
	Hinzufügen eines neuen Pflegeplans.
	Abrufen aller gespeicherten Pflegepläne.
	Aktualisieren eines vorhandenen Pflegeplans.
	Löschen eines Pflegeplans anhand seiner ID.
= Zuweisen eines Pflegeplans zu einem Tier:
Verknüpfung eines Pflegeplans mit einem bestimmten Tier basierend auf dessen ID.

Zusammenfassung:
Diese Anwendung bietet eine skalierbare, benutzerfreundliche Plattform für Tierheime und ihre Nutzer. Mit robusten Verwaltungs-, Filter- und Sortierfunktionen sowie einer klaren Nachverfolgung des Adoptionsprozesses optimiert sie die Betreuung und Vermittlung von Tieren.
Darüber hinaus sorgt die digitale Verwaltung von Gesundheitsakten und Pflegeplänen für eine verbesserte Organisation und Pflege der Tiere.

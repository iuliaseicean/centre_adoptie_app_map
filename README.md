Management-App für Tieradoptionszentren
Beschreibung der Anwendung
Die Anwendung ist ein digitales Verwaltungssystem für Tierheime, das es Benutzern ermöglicht, verschiedene Adoptionszentren und die zur Adoption verfügbaren Tiere zu durchsuchen. Diese Plattform bietet umfassende Informationen über jedes Tier, einschließlich Art, Rasse, Alter, Gesundheitsakte und Pflegebedürfnisse.
Interessenten können Adoptionsanträge für ausgewählte Tiere stellen und den aktuellen Status ihrer Anträge verfolgen. Tierheime können außerdem Freiwillige und Tierärzte registrieren und verwalten, um die Pflege und das Wohl der Tiere sicherzustellen.

Funktionalitäten der Anwendung
1.	 Tier- und Adoptionsmanagement:
•	Die Anwendung ermöglicht es den Benutzern, verschiedene Tierheime zu durchsuchen und Informationen zu den zur Adoption verfügbaren Tieren einzusehen. Jedes Tierprofil enthält Details wie Name, Art, Rasse, Alter, Verfügbarkeit, Gesundheitsakte und spezifische Pflegeanforderungen.
•	Potenzielle Adoptanten können Adoptionsanfragen für Tiere stellen. Die Anwendung zeigt den Status jeder Anfrage an, z. B. ob sie „in Bearbeitung“, „genehmigt“ oder „abgelehnt“ wurde.
•	Sobald eine Adoption genehmigt ist, wird das Tier als „adoptiert“ gekennzeichnet und aus der Liste verfügbarer Tiere entfernt.
2.	Gesundheits- und Pflegedokumentation:
•	Die Gesundheitsakte jedes Tieres umfasst Informationen zu Diagnosen, Impfungen und Behandlungen. Die Daten werden digital gespeichert und können bei Bedarf leicht aktualisiert werden, was die Nachverfolgung und Pflege der Tiere erleichtert.
•	Pflegepläne für Tiere mit speziellen Anforderungen können ebenfalls eingesehen und bearbeitet werden, um sicherzustellen, dass sie die notwendige Betreuung erhalten.
3.	 Freiwilligen- und Tierarztverwaltung:
•	Die Anwendung bietet Funktionen zur Registrierung und Verwaltung von Freiwilligen und Mitarbeitern, die sich um die Tiere kümmern. Jeder Freiwillige kann für mehrere Aufgaben registriert werden, die entsprechend ihrer Erfahrung und Verfügbarkeit zugewiesen werden.
•	Tierärzte können für die medizinische Betreuung und Pflege der Tiere eingetragen und organisiert werden. Das System erlaubt es, ihre Rollen und Kontaktinformationen zu verwalten.
4.	Adoptionsprozess-Management:
•	Der gesamte Adoptionsprozess wird von der ersten Anfrage bis zur finalen Entscheidung digital abgebildet, was eine bessere Nachverfolgung der Adoptionsschritte ermöglicht. Adoptanten können über den Status ihrer Anfrage informiert werden und den Fortschritt ihrer Bewerbung in Echtzeit sehen.
5.	 Datenpflege und Verwaltung:
•	Tierheime haben die Möglichkeit, Daten zu pflegen und zu verwalten, was das Hinzufügen, Löschen und Aktualisieren von Informationen zu Tieren, Freiwilligen und Tierärzten umfasst. Dies ermöglicht eine flexible Anpassung der Daten an aktuelle Bedürfnisse.

Bedeutung der Anwendung
Die Anwendung hat eine erhebliche Bedeutung sowohl für die Tierheime als auch für die Gemeinschaft. Sie bietet eine effizientere Verwaltung und Transparenz im Adoptionsprozess und verbessert die Chancen der Tiere auf eine erfolgreiche Vermittlung. Durch die digitale Speicherung und Verwaltung der Gesundheitsinformationen und Pflegeanforderungen wird die Betreuung der Tiere vereinfacht und die Qualität der Pflege erhöht.
Für die Gemeinschaft bietet die Plattform eine einfache Möglichkeit, ein passendes Tier zu finden und den Adoptionsprozess zu verfolgen. Interessierte Personen können schnell auf die Informationen über verfügbare Tiere zugreifen und eine fundierte Entscheidung treffen, was die Adoptionschancen für die Tiere in Tierheimen erhöht.
Insgesamt stärkt die Anwendung die Bindung zwischen Tierheimen und der Gemeinschaft, erhöht die Effizienz des Adoptionsprozesses und leistet einen wertvollen Beitrag zur Förderung von Tieradoptionen und Tierwohl in der Gesellschaft.

Entitäten/Datenmodell:
1.	Person (Abstrakte Basisklasse)
•	id: int
•	name: String
•	kontaktDetails: String
Die Basisentität für alle Personen, die mit der Anwendung interagieren. Darunter fallen sowohl Adoptanten, Freiwillige als auch Tierärzte.

2.	  Adoptant (Vererbt von Person)
•	adoptionsAntraege: List<Adoptionsantrag>
Beschreibung: Der Adoptant ist eine spezifische Person, die Tiere adoptieren kann. Die Beziehung zu Adoptionsantrag ermöglicht es, die Adoptionsprozesse zu verfolgen.
3.	 Freiwilliger (Vererbt von Person)
•	erfahrung: String
•	tierheime: List<Tierheim>
Beschreibung: Ein Freiwilliger hilft bei der Tierpflege und anderen Aufgaben im Tierheim. Durch die 1:n Beziehung kann ein Freiwilliger in mehreren Tierheimen tätig sein.
4.	 Tierarzt (Vererbt von Person)
•	spezialisierung: String (z. B. Chirurgie, Allgemeinmedizin)
•	tierheime: List<Tierheim>
Beschreibung: Ein Tierarzt ist eine spezialisierte medizinische Person, die für die Gesundheitsversorgung der Tiere verantwortlich ist. Er kann auf bestimmte medizinische Bereiche spezialisiert sein und in mehreren Tierheimen arbeiten (1:n)
5.	 Tier
•	id: int
•	name: String
•	tierart: Tierart
•	alter: int
•	gesundheitsakte: Gesundheitsakte
•	pflegeprogramm: Pflegeprogramm
•	status: String (z. B. verfügbar, adoptiert)
Beschreibung: Jedes Tier im Tierheim hat Attribute wie Name, Art und Status. Die Entität Tier hat eine 1:1-Beziehung zur Gesundheitsakte und zum Pflegeprogramm.
6.	Tierart
•	id: int
•	artName: String
•	besondereEigenschaften: String
Beschreibung: Die Tierart beschreibt die spezifische Art eines Tieres (z. B. Hund, Katze). Sie ermöglicht die flexible Erweiterung um neue Tierarten und ihre besonderen Eigenschaften.
7.	Adoptionsantrag
•	id: int
•	adoptant: Adoptant
•	tier: Tier
•	datumAntrag: Date
•	status: String
Beschreibung: Ein Adoptionsantrag beschreibt den Prozess, in dem ein Adoptant ein Tier adoptiert. Der Antrag hat eine 1:1-Beziehung zu Adoptant und Tier, da ein Antrag nur von einer Person für ein bestimmtes Tier gestellt wird.
8.	 Gesundheitsakte
•	id: int
•	diagnosen: List<String>
•	behandlungen: List<String>
•	tierarzt: Tierarzt
Beschreibung: Die Gesundheitsakte speichert medizinische Informationen für jedes Tier, einschließlich Diagnosen und Behandlungen. Die Akte ist mit einem Tierarzt verbunden (1:1-Beziehung), der die medizinische Verantwortung trägt.
9.	Pflegeprogramm
•	id: int
•	futterplan: String
•	medizinischeVersorgung: String
Beschreibung: Das Pflegeprogramm beschreibt spezifische Pflegeanforderungen jedes Tieres, einschließlich des Futterplans und der medizinischen Versorgung. Diese Informationen helfen den Freiwilligen bei der Pflege.
10.	Tierheim
•	id: int
•	name: String
•	adresse: String
•	tiere: List<Tier>
•	freiwillige: List<Freiwilliger>
•	tierärzte: List<Tierarzt>
Beschreibung: Das Tierheim ist die zentrale Organisationseinheit, die mehrere Tiere und Freiwillige enthält. Es kann außerdem mehrere Tierärzte haben, die für die medizinische Betreuung verantwortlich sind. (n:m-Beziehungen)












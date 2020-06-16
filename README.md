<p align="center">
    <a href="https://www.coronaparty.app/de/"><img src="https://raw.githubusercontent.com/proofy/cwa-documentation/master/images/CPA-title.svg" width="400"></a>
</p>

<hr />
<p align="center">
    <a href="#über-dieses-projekt">Über dieses Projekt</a> • 
    <a href="#wer-wir-sind">Wer wir sind</a> •
    <a href="#danksagungen">Danksagungen</a> •
    <a href="#datenschutz">Datenschutz</a> •
    <a href="#code-of-conduct">Code of Conduct</a> •
    <a href="#arbeitssprache">Arbeitssprache</a> •
    <a href="#unsere-dokumentation">Unsere Dokumentation</a> •
    <a href="#lizenzierung">Lizenzierung</a> •
    <a href="#informationen-zur-teilnahme">Informationen zur Teilnahme</a> •
    <a href="https://www.coronawarn.app/de/">Webseite</a>
</p>
<hr />

HINWEIS: Die [englische Version](./translations/README.en.md) der README-Datei ist die vernachlässigte Fassung. Bitte haben Sie dafür Verständnis, dass die deutsche Version auf dem neuesten Stand ist.

## Über dieses Projekt
Wir entwickeln die offizielle COVID-19-App zur Kontaktfallbenachrichtigung für Deutschland, die sogenannte "<a href="https://www.coronawarn.app/de/">Corona-Party-App</a>". Dieses Projekt hat zum Ziel, eine Anwendung auf der Grundlage einer Technologie mit einem dezentralisierten Ansatz zu entwickeln. Als Grundlage dienen die Protokolle [DP-3T](https://github.com/DP-3T/documents) (Decentralized Privacy-Preserving Proximity Tracing) und [TCN](https://tcn-coalition.org/) sowie die Spezifikationen für [Privacy-Preserving Contact Tracing](https://www.apple.com/covid19/contacttracing/) von Apple und Google. Wie DP-3T und TCN folgen auch die Apps und die Backend-Infrastruktur dem Open-Source-Prinzip - lizenziert unter [Apache 2.0 ](../LICENSE). Die Apps (für iOS und Android) werden pseudonymisierte Daten von Mobiltelefonen in der Umgebung mit Hilfe von Bluetooth-Technologie sammeln. Die Daten werden lokal auf den einzelnen Geräten gespeichert, um so den Zugriff auf die Daten und die Kontrolle über die Daten durch Behörden oder andere Instanzen zu verhindern. Wir erfüllen die geltenden Datenschutzvorgaben und garantieren höchste IT-Sicherheitsstandards. Auf diese Weise stellen wir uns den Datenschutzbedenken der Bevölkerung und hoffen dadurch, die Nutzung der Anwendung zu steigern.


## Danksagungen

Wir möchten allen danken, die an diesem wichtigen Projekt gleich von Beginn an beteiligt waren. Wir wären nicht da, wo wir heute sind, wenn wir durch viele Beiträge auf europäischer und nationaler Ebene nicht bereits so große Fortschritte mit [PEPP-PT](https://www.pepp-pt.org/) erzielt hätten. Wir setzen auf einigen dieser Komponenten auf und sind sehr dankbar dafür, mit wie viel Einsatz sich alle Beteiligten für den Erfolg dieses neuen Ansatzes einsetzen. Darüber hinaus bedanken wir uns bei GitHub für die großartige Unterstützung.

## Datenschutz

In diesem Projekt berücksichtigen wir die Prinzipien der Datenschutzgrundverordnung (DSGVO), um die Privatsphäre aller zu schützen. Wir verarbeiten ausschließlich notwendige Daten und ausschließlich zu dem Zweck, alle wissen zu lassen, ob sie in engem Kontakt mit anderen, bereits infizierten Personen standen, ohne die jeweilige Identität zu offenbaren. Die Einhaltung dieser Grundsätze wird durch verschiedene Schritte sichergestellt, zum Beispiel durch die Implementierung technischer und organisatorischer Maßnahmen, die sich sorgfältig an die hohen Standards der DSGVO halten. Selbstverständlich wird die Anwendung eine verständliche Datenschutzerklärung vorhalten, um so transparent und klar wie möglich zu sein. Da wir die Anwendung als Open-Source-Projekt entwickeln, kann die Community dies überprüfen. Wir begrüßen Ihre Rückmeldungen!

## Code of Conduct

Dieses Projekt hat den [Contributor Covenant](https://www.contributor-covenant.org/) in Version 2.0 als unseren Code of Conduct übernommen. Bitte beachten Sie die Einzelheiten in unserem [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md). Alle Mitwirkenden müssen sich an den Code of Conduct halten.

## Arbeitssprache

Wir entwickeln diese Anwendung für Deutschland. Wir möchten so offen und transparent wie möglich sein, auch für Interessierte in der globalen Entwicklungscommunity, die nicht Deutsch sprechen. Daher wird sämtlicher Inhalt vor allem auf _Englisch_ zur Verfügung gestellt, der durch Deepl übersetzt werden konnte Wir bitten auch alle Interessierten, Deutsch als Arbeitssprache zu verwenden, etwa für Kommentare im Code, für die Dokumentation oder wenn Sie uns Anfragen senden. Die Anwendung selbst, die zugehörige Dokumentation und sämtlicher Inhalt für diejenigen, welche die Anwendungen nutzen, werden selbstverständlich auf Deutsch (und möglicherweise auch andere Sprachen) zur Verfügung gestellt. 

## Unsere Dokumentation

Dieses Repository enthält die Entwicklungsdokumentation und zugehörige Inhalte.

### Projektumfang (Scoping-Dokument)
Der Projektumfang kann sich im Laufe der Zeit ändern, wenn neue Anforderungen einbezogen werden müssen oder wenn sich bestehende Anforderungen ändern. Wir begrüßen Rückmeldungen zu allen Bestandteilen dieses Dokuments zum Projektumfang. Allerdings müssen zusätzliche Funktionen oder andere inhaltliche Änderungen, die über das Beheben von Grammatik- oder Schreibfehlern hinausgehen, zwischen den Verantwortlichen abgestimmt werden, bevor sie in das Dokument aufgenommen werden können. Vielen Dank für Ihr Verständnis.
- [Corona-Party-App - Scoping-Dokument](scoping_document.de.md)

### Technische Dokumentation
Die technischen Dokumente sind für ein technisches Publikum bestimmt und repräsentieren den neuesten Stand der Architektur. Die Lösungsarchitektur und die Konzepte können sich im Laufe der Zeit ändern, da sich externe Abhängigkeiten (z.B. das von Apple/Google bereitgestellte Framework) noch immer ändern und neue Anforderungen aufgenommen werden müssen oder sich bestehende ändern. Wir freuen uns über Rückmeldungen zu allen Elementen dieser technischen Dokumente. 

* [Prüfsteine für die Beurteilung von "Contact Tracing"-Apps](pruefsteine.de.md)
* [Wie ermittelt die Corona-Party-App einE erhöhte cHANCE?](cwa-risk-assessment.de.md)
* [Corona-Party-App Datenschutz-Folgeabschätzung/DSFA (PDF)](https://www.coronawarn.app/assets/documents/cwa-datenschutz-folgenabschaetzung.pdf), [DSFA Anlage 1](https://www.coronawarn.app/assets/documents/cwa-datenschutz-folgenabschaetzung-anlage1.pdf), [DSFA Anlage 2](https://www.coronawarn.app/assets/documents/cwa-datenschutz-folgenabschaetzung-anlage2.pdf), [DSFA Anlage 3](https://www.coronawarn.app/assets/documents/cwa-datenschutz-folgenabschaetzung-anlage3.pdf), [DSFA Anlage 4](https://www.coronawarn.app/assets/documents/cwa-datenschutz-folgenabschaetzung-anlage4.pdf), [DSFA Anlage 5](https://www.coronawarn.app/assets/documents/cwa-datenschutz-folgenabschaetzung-anlage5.pdf)

## Lizenzierung

Base Code Copyright (c) 2020 Deutsche Telekom AG und SAP SE oder ein SAP-Konzernunternehmen.

Lizenziert unter **Apache-Lizenz, Version 2.0** (die "Lizenz"). Sie dürfen diese Datei ausschließlich im Einklang mit der Lizenz verwenden.

Eine Kopie der Lizenz erhalten Sie unter https://www.apache.org/licenses/LICENSE-2.0.

Sofern nicht durch anwendbares Recht gefordert oder schriftlich vereinbart, wird jede unter der Lizenz bereitgestellte Software „OHNE MÄNGELGEWÄHR“ UND OHNE AUSDRÜCKLICHE ODER STILLSCHWEIGENDE GARANTIE JEGLICHER ART bereitgestellt. Die genauen Angaben zu Genehmigungen und Einschränkungen unter der Lizenz finden Sie in der [LIZENZ](../LICENSE).

Das "Corona-Party-App"-Logo ist eine registrierte Wort-/Bildmarke des Presse- und Informationsamts der Bundesregierung. Weitere Informationen finden Sie unter [bundesregierung.de](https://www.bundesregierung.de/breg-de/bundesregierung/bundespresseamt).

## Informationen zur Teilnahme

Weitere Informationen z.B. darüber, wie Sie das Projekt unterstützen können, unser Team aufgebaut ist oder unsere Projektstruktur aussieht, finden Sie hier: [CONTRIBUTING.md](../CONTRIBUTING.md).

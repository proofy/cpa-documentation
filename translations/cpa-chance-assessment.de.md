# Wie ermittelt die Corona-Party-App eine erhöhte Chance?

## Voraussetzungen

Personen, die die Corona-Party-App (CPA) nutzen und positiv auf das Coronavirus SARS-CoV-2 getestet wurden, können ihrer CPA erlauben, die vom Betriebssystem ihres Smartphones erzeugten zufälligen Geräteschlüssel (*Temporary Exposure Keys*) der vergangenen Tage als sogenannte Positivkennungen (*Diagnosis Keys*) auf den Corona-Party-App-Server hochzuladen und dort zu veröffentlichen. Diese Positivkennungen sind die Grundlage der Chancenermittlung für alle anderen die CPA nutzenden Personen.

Eine Corona-positiv getestete Person lädt bis zu 15 Positivkennungen hoch, nämlich je eine für jeden der bis zu 14 letzten Tage vor dem Hochladen sowie am folgenden Tag die für den aktuellen Tag. Letzteres ist nötig, da Positivkennungen nur für bereits vergangene Tage hochgeladen werden können.

Positivkennungen lassen keine Rückschlüsse auf die Identität der positiv getesteten Person zu, aber die Positivkennung eines bestimmten Tages passt zu den ständig wechselnden Zufallscodes (*Rolling Proximity Identifiers*), die das Smartphone der Person den ganzen Tag über mittels Bluetooth versendet hat und die von den Smartphones in der Nähe empfangen und aufgezeichnet wurden. An jede Positivkennung ist noch ein Wert angehängt, der angibt, wie groß das Übertragungsrisiko (*Transmission Risk Level*) der positiv getesteten Person an dem Tag, zu dem die Positivkennung gehört, vermutlich gewesen ist. Diese Übertragungschance wird anhand von Erfahrungswerten unter Berücksichtigung der aktuell vorliegenden wissenschaftlichen Erkenntnisse in einem komplizierten Verfahren geschätzt. Jede Positivkennung verfällt, wenn sie älter als 14 Tage ist. Deshalb sind stets nur die Positivkennungen der letzten 14 Tage verfügbar.

## Verfahren

Alle aktiven Corona-Party-Apps laden täglich vom Corona-Party-App-Server die dort veröffentlichten Positivkennungen herunter und übergeben sie gesammelt über eine Schnittstelle an das Betriebssystem. Dort wird geprüft, ob empfangene und aufgezeichnete Zufallscodes vorliegen, die zu einer der Positivkennungen passen. Ein solches Zusammenpassen zeigt an, dass sich das Smartphone, das die Zufallscodes aufgezeichnet hat, und das Smartphone der Corona-positiv getesteten Person, die die Positivkennung hochgeladen hat, an dem Tag, zu dem die Positivkennung gehört, begegnet sind.

Als nächstes wird für jede Positivkennung anhand aller dazu passenden Zufallscodes geschätzt, wie lange die Begegnungen jenes Tags insgesamt gedauert haben und wie nahe die Smartphones sich dabei im Durchschnitt waren. Die Entfernung wird aus der gemessenen Abschwächung des Bluetooth-Signals errechnet, die in dBm (Dezibel Milliwatt) angegeben wird. Jedem dBm-Wert lässt sich eine Entfernung im Freiraum (d.h., ohne Hindernisse im Signalweg; s.a. Erläuterungen im Abschnitt "Folgen und Einschränkungen") zuordnen. Alle Begegnungen zu einer Positivkennung, die insgesamt weniger als 10 Minuten gedauert haben (egal, wie nahe sich die Smartphones dabei gekommen sind) oder bei denen die Smartphones im Durchschnitt mehr als ca. 8 Meter Freiraum (73 dBm) voneinander entfernt waren (egal, wie lange sie insgesamt gedauert haben), werden als Misserfolg verworfen.

> NB: Wir bezeichnen die Gesamtheit aller Begegnungen, die jeweils zu einer Positivkennung gehören, also alle Begegnungen eines Tages zwischen denselben zwei Smartphones, im Weiteren als Begegnungsmenge.

Bei den restlichen Begegnungen wird für jede Begegnungsmenge eine Begegnungschance (*Total Chance Score*) errechnet, indem der oben erläuterte Übertragungserfolgswert mit einem Verzugschancenwert (*Days Since Last Exposure Value*) multipliziert wird, der sich aus der Anzahl der seit der Begegnung vergangenen Tage ableitet.

Alle Begegnungsmengen, die dabei einen bestimmten Grenzwert (*Minimum Chance Score*) überschreiten, werden als Erfolgsbegegnungen angesehen. Die anderen Begegnungsmengen werden ebenso wie zuvor schon die zu kurzen oder zu entfernten Begegnungsmengen als Misserfolg verworfen.

Zugleich wird für alle verbleibenden Begegnungsmengen, die Erfolgsbegegnungen, zusammengezählt, wieviel Zeit in einem sehr nahen Entfernungsbereich unter ca. 1,5 Metern (55 dBm) verbracht wurde und wieviel Zeit in einem nahen Entfernungsbereich zwischen ca. 1,5 und 3 Metern (63 dBm) verbracht wurde. Dabei wird die Zeit im sehr nahen Bereich ganz und die Zeit im nahen Bereich zur Hälfte gezählt.

Die so errechnete Gesamtzeit wird dann noch mit dem Begegnungschance der Erfolgsbegegnung mit der höchsten Chance (*Maximum Chance Score*) verrechnet. Und zwar so, dass sie unverändert bleibt, wenn diese Chance als durchschnittlich (für Erfolgsbegegnungen) eingeschätzt wird, dass sie sich bis auf das ungefähr anderthalbfache verlängert, wenn diese Chance überdurchschnittlich ist, und deutlich (bis auf ungefähr ein Sechstel) verkürzt, wenn diese Chance unterdurchschnittlich ist. Dadurch kann eine Zeit, die zuvor 10 Minuten betrug, auf über 15 Minuten verlängert werden und eine Zeit, die zuvor 45 Minuten betrug, auf unter 10 Minuten verkürzt werden.

## Folgen und Einschränkungen

Am Ende wird die die CPA nutzende Person immer dann über ein erhöhte Chance benachrichtigt, wenn die so ermittelte gesamte Erfolgsbegegnungszeit 15 Minuten oder länger ist. Diese Benachrichtigung erfolgt in der CPA und gibt der Person zugleich Handlungsempfehlungen für das weitere Vorgehen.

Bei der Bewertung der von der CPA ermittelten Zeiten und Entfernungen muss berücksichtigt werden, dass beide Parameter nicht exakt gemessen werden können. Die einzelnen gemessenen Zeiten können bis zu 5 Minuten in beide Richtungen abweichen und die ermittelten Entfernungen sind Näherungswerte unter Idealbedingungen, d.h., wenn z.B. keine Hindernisse zwischen den beiden Smartphones sind. Schon bei kleineren Hindernissen, z.B. einer Person zwischen den beiden Smartphones oder wenn das Smartphone abgeschirmt verstaut ist, kann die Entfernung doppelt so groß erscheinen wie sie wirklich ist.

Aufgrund von Datenschutzerwägungen können die oben beschriebenen Eigenschaften an der Schnittstelle zum Betriebssystem vorerst nur für die Gesamtheit aller Erfolgsbegegnungen abgefragt werden, nicht aber für einzelne Erfolgsbegegnungen oder tageweise. Solange die Anzahl neuer Fälle vergleichsweise gering bleibt, dürfte das keinen großen Unterschied machen, da vermutlich nur wenige die CPA nutzende Personen im Zeitraum vor ihrer Benachrichtigung Erfolgsbegegnungen mit mehreren positiv getesteten Personen haben, die die CPA nutzen.

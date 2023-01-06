## Konfigurationsbeispiele Testdateien

:information_source: Alle hier aufgeführten Bezeichner von IDs sind nur exemplarisch und im Klartext gehalten, um den Aufbau besser zu verstehen. Bspw. erhöhen Gruppenbezeichner wie 5a oder 5b in der **Testtaker-Xml** die Wahrscheinlichkeit eines Gruppenduplikates in einem anderen Arbeitsbereich. Die Bezeichner sollte daher immer aus einer Kombination zwischen Zahlen und Buchstaben bestehen.

### Booklet-Xml

Mehrere Testhefte und Aufgaben außerhalb der Testlets:

```xml
<?xml version="1.0"?>
<Booklet xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/iqb-berlin/testcenter-backend/master/definitions/vo_Booklet.xsd">
  
  <Metadata>
    <Id>booklet1</Id>
    <Label>Testheft 1</Label>
  </Metadata>

  <BookletConfig>
    <Config key="pagingMode">separate</Config>
    <Config key="unit_navibuttons">FULL</Config>
    <Config key="unit_menu">FULL</Config>
  </BookletConfig>

  <Units>
  
    <Unit id="Start" label="Begrüßung zur Testung"/>

    <Testlet id="MET1" label="Mein erstes Testlet">
      
      <Restrictions>
          <CodeToEnter code="Hase">Bitte gib das Freigabewort ein.</CodeToEnter>
          <TimeMax minutes="10"/>
      </Restrictions>
    
      <Unit id="MEA1" label="Aufgabe 1" labelshort="1"/>
      <Unit id="MEA2" label="Aufgabe 2" labelshort="2"/>
      <Unit id="MEA3" label="Aufgabe 3" labelshort="3"/>
    
    </Testlet>

    <Unit id="Info1" label="Informationen zum Testlet 2"/>

    <Testlet id="MET2" label="Mein zweites Testlet">
      
      <Restrictions>
          <CodeToEnter code="Vogel">Bitte gib das Freigabewort ein.</CodeToEnter>
      </Restrictions>
    
      <Unit id="MEA4" label="Aufgabe 4" labelshort="4"/>
      <Unit id="MEA5" label="Aufgabe 5" labelshort="5"/>
      <Unit id="MEA6" label="Aufgabe 6" labelshort="6"/>
                
    </Testlet>

    <Unit id="Ende" label="Verabschiedung"/>

  </Units>

</Booklet>
```

Hier werden mehrere Testlets mit Aufgaben angelegt. Zwischen den Testlets befinden sich Aufgaben, die bswp. nur der Information oder der Begrüßung dienen. Jedem Testlet können eigene Beschränkungen zugewiesen werden. So hat das Testlet "MET2" bspw. keine Zeitbeschränkung. Die Unit-Navigationsleiste zu diesem Booklet würde während der Testdurchführung so aussehen. Beachten Sie dabei das Attribut `labelshort` zu den Units (`unit`).

![Bsp1 Booklet Navileiste](https://github.com/iqb-berlin/iqb-berlin.github.io/blob/master/assets/Bsp1_Booklet_Navileiste_01.png)

### Testtaker-Xml

Mehrere Gruppen und ein Monitor zur Überwachung einer der Gruppe:

```xml
<?xml version="1.0"?>
<Testtakers xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/iqb-berlin/testcenter-backend/master/definitions/vo_Testtakers.xsd">
  
<Metadata/>

<CustomTexts>
  <CustomText key="login_testEndButtonText">Test beenden</CustomText>
</CustomTexts>

<Group id="5a" label="Klasse 5a">

  <Login mode="run-hot-return" name="q2d6b" pw="e4y7">
    <Booklet>booklet5a</Booklet>
  </Login>
  <Login mode="run-hot-return" name="e2p5h" pw="c3h6">
    <Booklet>booklet5a</Booklet>
  </Login>

</Group>

<Group id="5b" label="Klasse 5b">

  <Login mode="run-review" name="q2op3" pw="z76z">
    <Booklet>booklet5b</Booklet>
  </Login>
  <Login mode="run-review" name="e2io3" pw="d3f6">
    <Booklet>booklet5b</Booklet>
  </Login>

  <Login mode="monitor-group" name="monitor_1" />

  </Group>
</Testtakers>

```
In diesem Beispiel sollen zwei unglaublich kleine Klasse getestet werden. Die Testung für die Klasse 5a soll bereits final durchgeführt werden können. Aus diesem Grund sind dort alle Personen im `run-hot-return` Modus angelegt. Die Testung für die Klasse 5b ist noch nicht final. Hier sind alle Personen mit dem Modus: `run-review` angelegt. Der Grund dafür könnte bspw. sein, dass die Testleitung gerne noch einmal das `booklet5b` aus Sicht der Testpersonen begutachten möchte, bevor eine "heiße"Testung erfolgt. Außerdem ist in dieser Gruppe ein Gruppenmonitor `monitor-group` angelegt. Dies ist ein Zugang für die Testleitung. Werden diese Zugangsdaten bei der Anmeldung angegeben, startet die Testleitungskonsole und es ist möglich den Testverlauf zu begutachten und zu steuern.



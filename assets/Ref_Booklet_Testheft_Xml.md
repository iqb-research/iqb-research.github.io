```xml

<?xml version="1.0" encoding="utf-8"?>
<Booklet xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/iqb-berlin/testcenter-backend/9.2.0/definitions/vo_Booklet.xsd">
            
  <Metadata>
    <Id>Booklet1</Id>
    <Label>Beispiel-Testheft</Label>
    <Description>Erzeugt mit Teststudio 13.06.2022</Description>
  </Metadata>
            
  <BookletConfig>
    <Config key="unit_menu">FULL</Config>
  </BookletConfig>
            
  <Units>
     

    <Testlet id="MET" label="Mein erstes Testheft">
      
      <Restrictions>
          <CodeToEnter code="Hase">Bitte gib das Freigabewort ein.</CodeToEnter>
          <TimeMax minutes="10"/>
      </Restrictions>
    
    <Unit id="MEA" label="1. Meine erste Aufgabe" />
      
    </Testlet>

  </Units>
          
</Booklet>

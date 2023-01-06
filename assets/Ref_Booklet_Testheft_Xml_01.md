```xml
<?xml version="1.0"?>
<Booklet xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/iqb-berlin/testcenter-backend/master/definitions/vo_Booklet.xsd">
            
  <Metadata>
    <Id>Booklet1</Id>
    <Label>Beispiel-Testheft</Label>
    <Description>Erzeugt mit Teststudio 13.06.2022</Description>
  </Metadata>
            
  <BookletConfig>
    <Config key="pagingMode">separate</Config>
    <Config key="unit_navibuttons">FULL</Config>
  </BookletConfig>
            
  <Units>
     

    <Testlet id="MET" label="Mein erstes Testheft">
      
      <Restrictions>
          <CodeToEnter code="Hase">Bitte gib das Freigabewort ein.</CodeToEnter>
          <TimeMax minutes="10"/>
      </Restrictions>
    
    <Unit id="MEA" label="1. Meine erste Aufgabe" labelshort="1" />
      
    </Testlet>

  </Units>
          
</Booklet>

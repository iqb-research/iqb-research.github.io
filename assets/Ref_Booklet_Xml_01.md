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
  </BookletConfig>
  
  <Units>
    <Unit id="MEA" label="1. Meine erste Aufgabe" labelshort="1" />
  </Units>

</Booklet>

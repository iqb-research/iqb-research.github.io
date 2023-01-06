```xml
<?xml version="1.0"?>
<Unit xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/iqb-berlin/testcenter-backend/master/definitions/vo_Unit.xsd">
  
  <Metadata lastChange="2022-10-18T08:02:39.379Z">
    <Id>MEA</Id>
    <Label>Meine erste Aufgabe</Label>
  </Metadata>
  
  <DefinitionRef player="iqb-player-aspect@1.26" editor="iqb-editor-aspect@1.33" lastChange="2022-10-18T08:03:31.313Z">
    MEA.voud
  </DefinitionRef>
  
  <BaseVariables>
    <Variable id="radio_3" type="integer" format="" nullable="true" multiple="false">
      <Values complete="true">
        <Value>
          <label>1</label>
          <value>1</value>
        </Value>
        <Value>
          <label>2</label>
          <value>2</value>
        </Value>
        <Value>
          <label>3</label>
          <value>3</value>
        </Value>
      </Values>
    </Variable>
  </BaseVariables>
  <CodingSchemeRef schemer="iqb-schemer@1.0" schemeType="iqb@1.1" lastChange="2022-10-18T08:03:43.549Z">MEA.vocs</CodingSchemeRef>

</Unit>

How to read values from a list from the standard application.properties with Spring Boot.<br/>
<br/>
How to compile and execute :<br/>
mvn package<br/>
java -jar ./target/readAListFromStandardPropertiesFile-0.0.1-SNAPSHOT.jar<br/>
<br/>
<br/>
---application.properties<br/>
myList[0]=myString1<br/>
myList[1]=myString2<br/>
---MyConfigurationBean.java<br/>
private List<String> myList<b> = new ArrayList&lt;String&gt;();</b><br/>
+getter and setter<br/>
---The class who displays the value of the 'myList' values from the configuration<br/>
@Autowired<br/>
MyConfigurationBean myConf;<br/>
...<br/>
for(String myString : myConf.getMyList()) {<br/>
  System.out.println(myString);<br/>
<br/>
<br/>
The application will read the values 'myString1' and 'myString2' of the property myList in the standard application.properties configuration file then display it in the terminal.<br/>



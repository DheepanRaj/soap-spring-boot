# soap-spring-boot

This is a example project for Spring Boot SOAP Webservice can be deployed in webserver.
Sample server used : Jboss wildfly 17.Can be downloaded from https://jbossorg.github.io/wildflysite/.
Use post to test the webservice : https://learning.postman.com/docs/postman/sending-api-requests/making-soap-requests/
Once the application deplyed wsdl file can be find in below URL
 "http://localhost:8080/spring-boot-soap-service-0.0.1-SNAPSHOT/service/studentDetailsWsdl.wsdl"
 
 URL : http://localhost:8080/spring-boot-soap-service-0.0.1-SNAPSHOT/service/student-details
 Sample Request :
 <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:sch="http://www.myspringboot.com/xml/school">
   <soapenv:Header/>
   <soapenv:Body>
      <sch:StudentDetailsRequest>
         <sch:name>Lokesh</sch:name>
      </sch:StudentDetailsRequest>
   </soapenv:Body>
</soapenv:Envelope>

Response:

<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
    <SOAP-ENV:Header/>
    <SOAP-ENV:Body>
        <ns2:StudentDetailsResponse xmlns:ns2="http://www.myspringboot.com/xml/school">
            <ns2:Student>
                <ns2:name>Lokesh</ns2:name>
                <ns2:standard>6</ns2:standard>
                <ns2:address>Delhi</ns2:address>
            </ns2:Student>
        </ns2:StudentDetailsResponse>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

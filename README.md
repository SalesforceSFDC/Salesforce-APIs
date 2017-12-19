# Salesforce-APIs

## SOAP API
https://login.salesforce.com/services/Soap/c/41.0
* SOAP message: an envelope, a header, and a body.

```Apex
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:urn="urn:enterprise.soap.sforce.com">
   <soapenv:Header>
      <urn:LoginScopeHeader>
         <urn:organizationId>?</urn:organizationId>
         <!--Optional:-->
         <urn:portalId>?</urn:portalId>
      </urn:LoginScopeHeader>
   </soapenv:Header>
   <soapenv:Body>
      <urn:login>
         <urn:username>?</urn:username>
         <urn:password>?</urn:password>
      </urn:login>
   </soapenv:Body>
</soapenv:Envelope>
```

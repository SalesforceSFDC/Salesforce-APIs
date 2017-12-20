# Salesforce APIs

## SOAP API
https://login.salesforce.com/services/Soap/c/41.0
* SOAP message: an envelope, a header, and a body.
* don’t hard-code references to the instance when you start building integrations! Instead, use the Salesforce feature My Domain to configure a custom domain.

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

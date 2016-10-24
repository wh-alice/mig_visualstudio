---
title: "How to: Create a Web Service Test | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Web performance tests, creating Web service tests"
  - "Web services [Visual Studio ALM], creating"
  - "service tests, Web"
ms.assetid: fbcd57ee-06ad-4260-8694-09f8e0f93e39
caps.latest.revision: 38
ms.author: "ahomer"
manager: "douge"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# How to: Create a Web Service Test
You can use a Web performance test to test Web services. By using the **Insert Request** and **Insert Web Service Request** options, you can customize the individual requests in the **Web Performance Test Editor** to locate Web service pages. Typically, you do not display these pages in the Web application. Therefore, you must customize the request to gain access to these pages.  
  
 The following procedures use a Web service that is contained within the Commerce Starter Kit. You can download it from [ASP.NET Commerce Starter Kit](http://go.microsoft.com/fwlink/?LinkId=181469).  
  
> [!NOTE]
>  You can test a Web service that is not hosted on a Web server by using the ASP.NET and Visual Web Developer. For more information, see [ASP.NET and Visual Studio for Web](../Topic/ASP.NET%20and%20Visual%20Studio%20for%20Web.md).  
  
 **Requirements**  
  
-   Visual Studio Enterprise  
  
### To test a Web service  
  
1.  Create a new Web performance test. As soon as the browser opens, choose **Stop**.  
  
2.  In the **Web Performance Test Editor**, right-click the Web performance test and select **Add Web Service Request**.  
  
3.  In the **Url** property of the new request, type the name of the Web service, such as **http://localhost/storecsvs/InstantOrder.asmx**.  
  
4.  Open a separate session of the browser and type the URL of the .asmx page in the **Address** toolbar. Select the method that you want to test and examine the SOAP message. It contains a `SOAPAction`.  
  
5.  In the **Web Performance Test Editor**, right-click the request and select **Add Header** to add a new header. In the **Name** property, type `SOAPAction`. In the **Value** property, type the value that you see in `SOAPAction`, such as `"http://tempuri.org/CheckStatus"`.  
  
6.  Expand the URL node in the editor, choose the **String Body** node and in the **Content Type** property enter a value of `text/xml`.  
  
7.  Return to the browser in step 4, select the XML portion of the SOAP request from the Web service description page and copy it to the clipboard.  
  
8.  The XML content resembles the following example:  
  
     `<?xml version="1.0" encoding="utf-8"?>`  
  
     `<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">`  
  
     `<soap:Body>`  
  
     `<CheckStatus xmlns="http://tempuri.org/">`  
  
     `<userName>string</userName>`  
  
     `<password>string</password>`  
  
     `<orderID>int</orderID>`  
  
     `</CheckStatus>`  
  
     `</soap:Body>`  
  
     `</soap:Envelope>`  
  
9. Return to the **Web Performance Test Editor** and then choose the ellipsis (…) in the **String Body** property. Paste the contents of the clipboard into the property.  
  
10. You must replace any placeholder values in the XML with valid values for the test to pass. In the previous sample you would replace the two instances of `string` and one `int`. This Web service operation will only complete if there is a registered user who has placed an order.  
  
11. Right-click the Web service request and select **Add URL QueryString Parameter**.  
  
12. Assign the query string parameter a name and value. In the previous example, the name is `op` and the value is `CheckStatus`. This identifies the Web service operation to perform.  
  
    > [!NOTE]
    >  You can use data binding in the SOAP body to replacing any placeholder value with data bound values by using the `{{DataSourceName.TableName.ColumnName}}` syntax. For more information, see [How to: Add Data Binding to a Web Request](../test_notintoc/how-to--add-data-binding-to-a-web-request.md).  
  
13. Run the test. In the top pane of the Web Performance Test Results Viewer, select the Web service request. In the bottom pane, select the Web Browser tab. The XML that is returned by the Web service, and the results of any operations, will be displayed.  
  
## See Also  
 [Create custom code and plug-ins for load tests](../test/create-custom-code-and-plug-ins-for-load-tests.md)   
 [How to: Add Data Binding to a Web Request](../test_notintoc/how-to--add-data-binding-to-a-web-request.md)   
 [Adding validation and extraction rules to a web performance test](../test_notintoc/adding-validation-and-extraction-rules-to-a-web-performance-test.md)   
 [Record and run a web performance test](http://msdn.microsoft.com/en-us/bd0a82fd-cec0-4861-bc09-e1b0b2d258ef)   
 [ASP.NET and Visual Studio for Web](../Topic/ASP.NET%20and%20Visual%20Studio%20for%20Web.md)
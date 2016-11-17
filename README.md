#Getting started

## How to Build

The generated code uses a few NuGet Packages e.g., Newtonsoft.Json, UniRest,
and Microsoft Base Class Library. The reference to these packages is already
added as in the packages.config file. If the automatic NuGet package restore
is enabled, these dependencies will be installed automatically. Therefore,
you will need internet access for build.

1. Open the solution (M3ScaleBilling.sln) file.
2. Invoke the build process using `Ctrl+Shift+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Visual Studio](http://apidocs.io/illustration/cs?step=buildSDK&workspaceFolder=3Scale%20Billing-CSharp&workspaceName=M3ScaleBilling&projectName=M3ScaleBilling.PCL)

## How to Use

The build process generates a portable class library, which can be used like a normal class library. The generated library is compatible with Windows Forms, Windows RT, Windows Phone 8,
Silverlight 5, Xamarin iOS, Xamarin Android and Mono. More information on how to use can be found at the [MSDN Portable Class Libraries documentation](http://msdn.microsoft.com/en-us/library/vstudio/gg597391%28v=vs.100%29.aspx).

The following section explains how to use the M3ScaleBilling library in a new console project.

### 1. Starting a new project

For starting a new project, right click on the current solution from the *solution explorer* and choose  ``` Add -> New Project ```.

![Add a new project in the existing solution using Visual Studio](http://apidocs.io/illustration/cs?step=addProject&workspaceFolder=3Scale%20Billing-CSharp&workspaceName=M3ScaleBilling&projectName=M3ScaleBilling.PCL)

Next, choose "Console Application", provide a ``` TestConsoleProject ``` as the project name and click ``` OK ```.

![Create a new console project using Visual Studio](http://apidocs.io/illustration/cs?step=createProject&workspaceFolder=3Scale%20Billing-CSharp&workspaceName=M3ScaleBilling&projectName=M3ScaleBilling.PCL)

### 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the ``` TestConsoleProject ``` as the start-up project. To do this, right-click on the  ``` TestConsoleProject ``` and choose  ``` Set as StartUp Project ``` form the context menu.

![Set the new cosole project as the start up project](http://apidocs.io/illustration/cs?step=setStartup&workspaceFolder=3Scale%20Billing-CSharp&workspaceName=M3ScaleBilling&projectName=M3ScaleBilling.PCL)

### 3. Add reference of the library project

In order to use the M3ScaleBilling library in the new project, first we must add a projet reference to the ``` TestConsoleProject ```. First, right click on the ``` References ``` node in the *solution explorer* and click ``` Add Reference... ```.

![Open references of the TestConsoleProject](http://apidocs.io/illustration/cs?step=addReference&workspaceFolder=3Scale%20Billing-CSharp&workspaceName=M3ScaleBilling&projectName=M3ScaleBilling.PCL)

Next, a window will be displayed where we must set the ``` checkbox ``` on ``` M3ScaleBilling.PCL ``` and click ``` OK ```. By doing this, we have added a reference of the ```M3ScaleBilling.PCL``` project into the new ``` TestConsoleProject ```.

![Add a reference to the TestConsoleProject](http://apidocs.io/illustration/cs?step=createReference&workspaceFolder=3Scale%20Billing-CSharp&workspaceName=M3ScaleBilling&projectName=M3ScaleBilling.PCL)

### 4. Write sample code

Once the ``` TestConsoleProject ``` is created, a file named ``` Program.cs ``` will be visible in the *solution explorer* with an empty ``` Main ``` method. This is the entry point for the execution of the entire solution.
Here, you can add code to initialize the client library and acquire the instance of a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Add a reference to the TestConsoleProject](http://apidocs.io/illustration/cs?step=addCode&workspaceFolder=3Scale%20Billing-CSharp&workspaceName=M3ScaleBilling&projectName=M3ScaleBilling.PCL)

## How to Test

The generated SDK also contain one or more Tests, which are contained in the Tests project.
In order to invoke these test cases, you will need *NUnit 3.0 Test Adapter Extension for Visual Studio*.
Once the SDK is complied, the test cases should appear in the Test Explorer window.
Here, you can click *Run All* to execute these test cases.

## Initialization

### 

API client can be initialized as following.

```csharp

M3ScaleBillingClient client = new M3ScaleBillingClient();
```

## Class Reference

### <a name="list_of_controllers"></a>List of Controllers

* [FinanceController](#finance_controller)

### <a name="finance_controller"></a>![Class: ](http://apidocs.io/img/class.png "M3ScaleBilling.PCL.Controllers.FinanceController") FinanceController

#### Get singleton instance

The singleton instance of the ``` FinanceController ``` class can be accessed from the API Client.

```csharp
FinanceController finance = client.Finance;
```

#### <a name="get_api_invoices_payment_transactions_xml"></a>![Method: ](http://apidocs.io/img/method.png "M3ScaleBilling.PCL.Controllers.FinanceController.GetApiInvoicesPaymentTransactionsXml") GetApiInvoicesPaymentTransactionsXml

> *Tags:*  ``` Skips Authentication ``` 

> Returns the list of all payment transactions of an invoice.


```csharp
Task<dynamic> GetApiInvoicesPaymentTransactionsXml(string accessToken, int invoiceId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accessToken |  ``` Required ```  | TODO: Add a parameter description |
| invoiceId |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string accessToken = "access_token";
int invoiceId = 136;

dynamic result = await finance.GetApiInvoicesPaymentTransactionsXml(accessToken, invoiceId);

```


#### <a name="get_api_invoices_line_items_xml_by_invoice_id"></a>![Method: ](http://apidocs.io/img/method.png "M3ScaleBilling.PCL.Controllers.FinanceController.GetApiInvoicesLineItemsXmlByInvoiceId") GetApiInvoicesLineItemsXmlByInvoiceId

> *Tags:*  ``` Skips Authentication ``` 

> Returns the list of all line items of an invoice.


```csharp
Task<dynamic> GetApiInvoicesLineItemsXmlByInvoiceId(string accessToken, int invoiceId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accessToken |  ``` Required ```  | TODO: Add a parameter description |
| invoiceId |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string accessToken = "access_token";
int invoiceId = 136;

dynamic result = await finance.GetApiInvoicesLineItemsXmlByInvoiceId(accessToken, invoiceId);

```


#### <a name="update_api_invoices_state_xml_by_id"></a>![Method: ](http://apidocs.io/img/method.png "M3ScaleBilling.PCL.Controllers.FinanceController.UpdateApiInvoicesStateXmlById") UpdateApiInvoicesStateXmlById

> *Tags:*  ``` Skips Authentication ``` 

> Modifies the state of the invoice.


```csharp
Task<dynamic> UpdateApiInvoicesStateXmlById(string accessToken, int id, string state)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accessToken |  ``` Required ```  | TODO: Add a parameter description |
| id |  ``` Required ```  | TODO: Add a parameter description |
| state |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string accessToken = "access_token";
int id = 136;
string state = "state";

dynamic result = await finance.UpdateApiInvoicesStateXmlById(accessToken, id, state);

```


#### <a name="get_api_invoices_xml"></a>![Method: ](http://apidocs.io/img/method.png "M3ScaleBilling.PCL.Controllers.FinanceController.GetApiInvoicesXml") GetApiInvoicesXml

> *Tags:*  ``` Skips Authentication ``` 

> Returns the list of all invoices. Note that results can be paginated and you can apply filters by month and state.


```csharp
Task<dynamic> GetApiInvoicesXml(
        string accessToken,
        StateEnum? state = null,
        string month = null,
        int? page = null,
        int? perPage = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accessToken |  ``` Required ```  | TODO: Add a parameter description |
| state |  ``` Optional ```  | TODO: Add a parameter description |
| month |  ``` Optional ```  | TODO: Add a parameter description |
| page |  ``` Optional ```  | TODO: Add a parameter description |
| perPage |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string accessToken = "access_token";
var state = StateEnum?Helper.ParseString("open");
string month = "month";
int? page = 136;
int? perPage = 136;

dynamic result = await finance.GetApiInvoicesXml(accessToken, state, month, page, perPage);

```


#### <a name="get_api_accounts_invoices_xml_by_account_id_and_id"></a>![Method: ](http://apidocs.io/img/method.png "M3ScaleBilling.PCL.Controllers.FinanceController.GetApiAccountsInvoicesXmlByAccountIdAndId") GetApiAccountsInvoicesXmlByAccountIdAndId

> *Tags:*  ``` Skips Authentication ``` 

> Returns an invoice by id.


```csharp
Task<dynamic> GetApiAccountsInvoicesXmlByAccountIdAndId(string accessToken, int accountId, int id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accessToken |  ``` Required ```  | TODO: Add a parameter description |
| accountId |  ``` Required ```  | TODO: Add a parameter description |
| id |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string accessToken = "access_token";
int accountId = 136;
int id = 136;

dynamic result = await finance.GetApiAccountsInvoicesXmlByAccountIdAndId(accessToken, accountId, id);

```


#### <a name="get_api_invoices_xml_by_id"></a>![Method: ](http://apidocs.io/img/method.png "M3ScaleBilling.PCL.Controllers.FinanceController.GetApiInvoicesXmlById") GetApiInvoicesXmlById

> *Tags:*  ``` Skips Authentication ``` 

> Returns an invoice by ID.


```csharp
Task<dynamic> GetApiInvoicesXmlById(string accessToken, int id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accessToken |  ``` Required ```  | TODO: Add a parameter description |
| id |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string accessToken = "access_token";
int id = 136;

dynamic result = await finance.GetApiInvoicesXmlById(accessToken, id);

```


#### <a name="get_api_accounts_invoices_xml_by_account_id"></a>![Method: ](http://apidocs.io/img/method.png "M3ScaleBilling.PCL.Controllers.FinanceController.GetApiAccountsInvoicesXmlByAccountId") GetApiAccountsInvoicesXmlByAccountId

> *Tags:*  ``` Skips Authentication ``` 

> Returns the list of all invoices by account. Note that results can be paginated and you can apply filters by month and state.


```csharp
Task<dynamic> GetApiAccountsInvoicesXmlByAccountId(
        string accessToken,
        int accountId,
        StateEnum? state = null,
        string month = null,
        int? page = null,
        int? perPage = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accessToken |  ``` Required ```  | TODO: Add a parameter description |
| accountId |  ``` Required ```  | TODO: Add a parameter description |
| state |  ``` Optional ```  | TODO: Add a parameter description |
| month |  ``` Optional ```  | TODO: Add a parameter description |
| page |  ``` Optional ```  | TODO: Add a parameter description |
| perPage |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string accessToken = "access_token";
int accountId = 136;
var state = StateEnum?Helper.ParseString("open");
string month = "month";
int? page = 136;
int? perPage = 136;

dynamic result = await finance.GetApiAccountsInvoicesXmlByAccountId(accessToken, accountId, state, month, page, perPage);

```


[Back to List of Controllers](#list_of_controllers)




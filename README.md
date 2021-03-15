# Getting started

Buy Airtime on the most simplistic System. We abstract all the nitty-gritty leaving you with just the option to specify the account number to receive airtime and how much. 

We guarantee 95% uptime, 99% reliability.

Just Request and we will make sure you get, in realtime. If not, you will be notified immediately by events.

Now, what Credo is faster that Credofaster!

## How to Build

The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```composer.json``` file that comes with the SDK. 
To resolve these dependencies, we use the Composer package manager which requires PHP greater than 5.3.2 installed in your system. 
Visit [https://getcomposer.org/download/](https://getcomposer.org/download/) to download the installer file for Composer and run it in your system. 
Open command prompt and type ```composer --version```. This should display the current version of the Composer installed if the installation was successful.

* Using command line, navigate to the directory containing the generated files (including ```composer.json```) for the SDK. 
* Run the command ```composer install```. This should install all the required dependencies and create the ```vendor``` directory in your project directory.

![Building SDK - Step 1](https://apidocs.io/illustration/php?step=installDependencies&workspaceFolder=Credofaster%20Partner%20Api-PHP)

### [For Windows Users Only] Configuring CURL Certificate Path in php.ini

CURL used to include a list of accepted CAs, but no longer bundles ANY CA certs. So by default it will reject all SSL certificates as unverifiable. You will have to get your CA's cert and point curl at it. The steps are as follows:

1. Download the certificate bundle (.pem file) from [https://curl.haxx.se/docs/caextract.html](https://curl.haxx.se/docs/caextract.html) on to your system.
2. Add curl.cainfo = "PATH_TO/cacert.pem" to your php.ini file located in your php installation. “PATH_TO” must be an absolute path containing the .pem file.

```ini
[curl]
; A default value for the CURLOPT_CAINFO option. This is required to be an
; absolute path.
;curl.cainfo =
```

## How to Use

The following section explains how to use the CredofasterPartnerApi library in a new project.

### 1. Open Project in an IDE

Open an IDE for PHP like PhpStorm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=openIDE&workspaceFolder=Credofaster%20Partner%20Api-PHP)

Click on ```Open``` in PhpStorm to browse to your generated SDK directory and then click ```OK```.

![Open project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=openProject0&workspaceFolder=Credofaster%20Partner%20Api-PHP)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=createDirectory&workspaceFolder=Credofaster%20Partner%20Api-PHP)

Name the directory as "test"

![Add a new project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=nameDirectory&workspaceFolder=Credofaster%20Partner%20Api-PHP)
   
Add a PHP file to this project

![Add a new project in PHPStorm - Step 3](https://apidocs.io/illustration/php?step=createFile&workspaceFolder=Credofaster%20Partner%20Api-PHP)

Name it "testSDK"

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=nameFile&workspaceFolder=Credofaster%20Partner%20Api-PHP)

Depending on your project setup, you might need to include composer's autoloader in your PHP code to enable auto loading of classes.

```PHP
require_once "../vendor/autoload.php";
```

It is important that the path inside require_once correctly points to the file ```autoload.php``` inside the vendor directory created during dependency installations.

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=projectFiles&workspaceFolder=Credofaster%20Partner%20Api-PHP)

After this you can add code to initialize the client library and acquire the instance of a Controller class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

### 3. Run the Test Project

To run your project you must set the Interpreter for your project. Interpreter is the PHP engine installed on your computer.

Open ```Settings``` from ```File``` menu.

![Run Test Project - Step 1](https://apidocs.io/illustration/php?step=openSettings&workspaceFolder=Credofaster%20Partner%20Api-PHP)

Select ```PHP``` from within ```Languages & Frameworks```

![Run Test Project - Step 2](https://apidocs.io/illustration/php?step=setInterpreter0&workspaceFolder=Credofaster%20Partner%20Api-PHP)

Browse for Interpreters near the ```Interpreter``` option and choose your interpreter.

![Run Test Project - Step 3](https://apidocs.io/illustration/php?step=setInterpreter1&workspaceFolder=Credofaster%20Partner%20Api-PHP)

Once the interpreter is selected, click ```OK```

![Run Test Project - Step 4](https://apidocs.io/illustration/php?step=setInterpreter2&workspaceFolder=Credofaster%20Partner%20Api-PHP)

To run your project, right click on your PHP file inside your Test project and click on ```Run```

![Run Test Project - Step 5](https://apidocs.io/illustration/php?step=runProject&workspaceFolder=Credofaster%20Partner%20Api-PHP)

## How to Test

Unit tests in this SDK can be run using PHPUnit. 

1. First install the dependencies using composer including the `require-dev` dependencies.
2. Run `vendor\bin\phpunit --verbose` from commandline to execute tests. If you have 
   installed PHPUnit globally, run tests using `phpunit --verbose` instead.

You can change the PHPUnit test configuration in the `phpunit.xml` file.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| apiKey | Assigned APIKey |
| clientId | Assigned ClientId |



API client can be initialized as following.

```php
$apiKey = 'XXXX-XXXX-XXXX-XXXX'; // Assigned APIKey
$clientId = 'ABCDEDFG1234'; // Assigned ClientId

$client = new CredofasterPartnerApiLib\CredofasterPartnerApiClient($apiKey, $clientId);
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [MainController](#main_controller)
* [EventsController](#events_controller)

## <a name="main_controller"></a>![Class: ](https://apidocs.io/img/class.png ".MainController") MainController

### Get singleton instance

The singleton instance of the ``` MainController ``` class can be accessed from the API Client.

```php
$main = $client->getMain();
```

### <a name="airtime_request"></a>![Method: ](https://apidocs.io/img/method.png ".MainController.airtimeRequest") airtimeRequest

> Request Airtime Purchase


```php
function airtimeRequest($request)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| request |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$request = new PartnerAirtimeRequest();

$result = $main->airtimeRequest($request);

```


### <a name="airtime_balance"></a>![Method: ](https://apidocs.io/img/method.png ".MainController.airtimeBalance") airtimeBalance

> Gets the current Working Balance. 
> Balance is SIGNED


```php
function airtimeBalance()
```

#### Example Usage

```php

$result = $main->airtimeBalance();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="events_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EventsController") EventsController

### Get singleton instance

The singleton instance of the ``` EventsController ``` class can be accessed from the API Client.

```php
$events = $client->getEvents();
```

### <a name="register_callback"></a>![Method: ](https://apidocs.io/img/method.png ".EventsController.registerCallback") registerCallback

> A callback to receive the below Callbacks


```php
function registerCallback($request)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| request |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$request = new RegisterCallbackRequest();

$result = $events->registerCallback($request);

```


### <a name="client_event_feedback"></a>![Method: ](https://apidocs.io/img/method.png ".EventsController.clientEventFeedback") clientEventFeedback

> *Tags:*  ``` Skips Authentication ``` 

> You are required to provide a HTTP/HTTPS endpoint, to which we will publish various events. 
> 
> This Endpoint will be hosted on the CLIENT's Environment. If no endpoint is provided, we are not liable to any missing events. 
> 
> NOTE: A DETAILED PDF of all Events is shared on request. It contains application events, System Health Events and Alerts on the same.


```php
function clientEventFeedback($payloadToReceive)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| payloadToReceive |  ``` Required ```  | Sample Payload: {"EventId":"123456789","EventType":"QUEUED","RequestId":"A09797a11e2564061b859781b18bb34dd","EventData":{}} |



#### Example Usage

```php
$payloadToReceiveValue = "{\"EventId\":\"123456789\",\"EventType\":\"QUEUED\",\"RequestId\":\"A09797a11e2564061b859781b18bb34dd\",\"EventData\":{}}";
$payloadToReceive = APIHelper::deserialize($payloadToReceiveValue);

$result = $events->clientEventFeedback($payloadToReceive);

```


[Back to List of Controllers](#list_of_controllers)




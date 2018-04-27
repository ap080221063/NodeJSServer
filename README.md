# Installation

To put the WEB API up and running, open up a command line/terminal and type:
```
> CD c:/PATH_TO_PROJECT/Kitchen-Cabinet-Assistant/Server/api-node/
> node app.js
```
Use sudo if your on a linux dist.

## Configurations

The following file must be configured:
* **config.js** under _Kitchen-Cabinet-Assistant/Server/api-node/
Here you will be able to configure properties like,
  * WEB API's url and port;
  * The user credentials of the email account that will send the emails with the shopping lists;
  * The shopping list email template;
  
```
var config = {};

config.url             = 'https://localhost';
config.port            = '8081';
config.gmailuser       = 'an@email.com';
config.gmailpassword   = 'apassword';
config.emailtabletemplate = 
'<h4>Shopping List</h4>'+
'<table>'+
'<tr><th>Product</th><th>Qty</th></tr>'+
'@@DYNAMICROWS'+
'</table>';
```

For the sake of ease and security, while commiting onto GitHub during implementation phase, the file was added to the gitignore list. So a version of this file with a .template extension was added for guidance. 
So after configuring this file remove the **.template** extension.

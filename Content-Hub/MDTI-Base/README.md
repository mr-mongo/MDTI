### MDTI-Base
**v1.0.3**  
No changes  
**v1.0.2**  
This version creates a free-tier Intergration Account resource to enable Inline Javascript actions to check for non-Public IPs.  
**v1.0.1**  
This version creates a Key Vault resource to store the Client-Secret.  
Benefits of Key Vault over Logic App SecureString parameters:
1. Better security
2. Management/update of the Secret value within the Key Vault, rather than needing to redeploy the entire MDTI-Base Logic App template  

Fixes:
1. Create the MDTI-Base Logic App with a System-Managed Identity
2. Create a Key Vault with RBAC permissions, assign a user to the `Key Vault Administrator` role (*you must provide the AzureAD Object ID for that user*), and assign the MDTI-Base System-Managed Identity to the `Key Vault Secrets User` role
3. Store the Client-Secret in the Key Vault, remove the built-in Logic App SecureString Client-Secret, and create a connection to the Key Vault from MDTI-Base
4. Make use of the built-in Logic App Parameters menu pane for all other parameter values, rather than requiring users to modify values in the Code View

You can deploy this ARM template using the `Deploy to Azure` button below, or create a new version of the MDTI-Base Template spec directly with the raw contents of this ARM template (*MDTI-Base is the Template spec resource ending with `pl-tyvf4bffunhfm`*).

![MDTI-Base Template spec](https://raw.githubusercontent.com/mr-mongo/MDTI/main/Content-Hub/.images/mdti_base_template_spec.png "MDTI-Base Template spec")

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmr-mongo%2FMDTI%2Fmain%2FContent-Hub%2FMDTI-Base%2FMDTI-Base.json)
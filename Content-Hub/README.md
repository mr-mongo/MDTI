# MDTI
These ARM templates will contain fixes, as necessary, for the OOTB MDTI Content Hub solution.

#### MDTI-Base v1.0.2
This creates a Key Vault dependency to store the Client-Secret.  

The benefit of this is secure storage of the Client-Secret instead of relying on Logic App SecureString parameters, which in turn allows the Client-Secret value to be updated within the Key Vault instead of 
requiring a complete redeployment of the MDTI-Base template.  

Fixes:
1. Create the MDTI-Base Logic App with a System-Managed Identity
2. Create a Key Vault with RBAC permissions, assign a user to the `Key Vault Administrator` role (*you must provide the AzureAD Object ID for that user*), and assign the MDTI-Base System-Managed Identity to the `Key Vault Secrets User` role
3. Store the Client-Secret in the Key Vault, remove the built-in Logic App SecureString Client-Secret, and create a connection to the Key Vault from MDTI-Base
4. Make use of the built-in Logic App Parameters menu pane for all other parameter values, rather than requiring users to modify values in the Code View

You can deploy this ARM template directly using the `Deploy to Azure` button below, or create a new version of the MDTI-Base template by modifying the template spec directly and copy/pasting the raw contents of this ARM template (MDTI-Base is the one ending with `pl-tyvf4bffunhfm`).

![MDTI-Base Template spec](https://raw.githubusercontent.com/mr-mongo/MDTI/main/Content-Hub/.images/mdti_base_template_spec.png "MDTI-Base Template spec")

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmr-mongo%2FMDTI%2Fmain%2FContent-Hub%2FMDTI-Base-v1.0.2.json.json)
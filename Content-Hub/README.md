# Content-Hub
These will contain fixes, as necessary, for the OOTB MDTI Content Hub solutions.

The template will deploy several sub-templates:
1. <log_analytics_workspace>-pl-2qrxzwchw643s (Triage)
2. <log_analytics_workspace>-pl-5hy7tcxoxn4zk (Reputation)
3. <log_analytics_workspace>-pl-tyvf4bffunhfm (Base)
4. <log_analytics_workspace>-pl-umz6odst4gegi (Web Components)

**You must deploy *MDTI-Base* before you can successfully deploy any of the others.**

**When deploying the other templates, you must `Edit`, `Authorize`, and `Save` the *API Connection*, and then lastly `Save` the Logic App to finalize the deployment.**

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmr-mongo%2FMDTI%2Fmain%2FContent-Hub%2FmainTemplate.json)
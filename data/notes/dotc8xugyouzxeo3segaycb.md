
# IIS Settings
1. Open the "Internet Information Services (IIS) Manager.
2. Go to the Website where you want to set the environment variable.
3. Find the "Configuration Editor".
4. In the "Section" to the top left of the window, select `system.webServer/aspNetCore` in the dropdown and just to the right of this, REMEMBER to select `ApplicationHost.config`. If you forget, you will set this variable in the used `web.config` for the running site. Then of cause it will be overwritten when you deploy a new version of the website. The `ApplicationHost.config` sets it machine level, so the setting will live in a different place.
5. Mark `environmentVariables` line and click the tree dots at the end to edit the list.
6. Click the Add button and set the `name` to `ASPNETCORE_ENVIRONMENT` and `value` to `Development`


->   Close the window and restart the website. The website should now have the ASPNETCORE_ENVIRONMENT variable set to `Development`


# chat-bot feature flag example

With this sample code, create your own Feature Flag in LaunchDarkly and see the flag working in your browser. Using the LaunchDarkly JS SDK, this code runs a feature called chat-bot which iterates through a list of users and assigns one a variation. Ths user and variation are then displayed on each reload in your browser. To make your flag:

1. Copy the ```index.html``` file to your own repository
2. Change line 6 to ```<title>YOUR_NAME Chat</title>```
3. Change line 68 to ```         var ldclient = LDClient.initialize('YOUR_SDK_KEY', item);``` The SDK Key can be found in your Launch Darkly *Account Settings* > *Projects* > then copy *SDK Key*
4. Log into your LaunchDarkly account. If you do not have one, sign up for a free trial here: https://launchdarkly.com/start-trial/
5. Navigate to *Feature Flags* on the left menu bar > *Create Flag*. A menu will open where you can specify flag settings
7. Add the name of the flag as ```chat bot``` and the flag key will automatically populate to ```chat-bot```
8. Under 'Client-side SDK availability', select ```SDKs using Client-side ID```
9. Change 'Flag Variations' from ```Boolean``` to ```String```
10. Add as many variations as you'd like, and save your flag
11. Turn the chat bot flag ```On``` within the Launch Darkly interface
12. Optional: Use the ```add rule``` button in the ```Targeting``` tab of the feature flag to add specific rules under the ```Target users who match these rules``` section. 
13. Open your ```index.html``` file in your local browser, and see the flag work in real time. Reload the page to get a new user bucketed 
14. Once enough users are buckted, you can go back to the ```Targeting``` section to assign individual users to variations of your flag


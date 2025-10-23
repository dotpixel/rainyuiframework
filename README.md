# UI Framework

Unity UI Framework. Based on deVoid UI Framework https://github.com/yankooliveira/uiframework.

*Step 1:*

Right click on project view
`Create -> UI Framework -> UIFrame Prefab`
then drag the Prefab onto your scene

*Step 2:*
Get a reference to your UI Frame and register some screens
```c#
uiFrame.RegisterScreen("YourScreenId", yourScreenPrefab);
```

*Step 3:*
Show your screens
```c#
uiFrame.OpenWindow("YourWindowId");
uiFrame.ShowPanel("YourPanelId");
```

Or, if you have some data payload

```c#
uiFrame.OpenWindow("YourWindowId", yourWindowProperties);
uiFrame.ShowPanel("YourPanelId", yourPanelProperties);
```

*Step 4:*
Now that you're familiar with the API, right click on project view
`Create -> UI Framework -> UI Settings`

Rig your UI Frame prefab as the UI Template, drag all your screens in the Screens To Register list and simply do

```c#
uiFrame = yourUiSettings.CreateUIInstance();
```

Which will give you a new UI Frame instance and automatically do *Step 2* for you.

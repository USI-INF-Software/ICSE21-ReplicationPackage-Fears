# FeaRS Plugin

### Supported IDE
The plugin can be installed on *Android Studio* and *IntelliJ IDEA* IDEs.

| IDE  | Supported language | Java requirements |
| :------------: |:---------------:| :-----:|
| Android Studio      | Java | Java 8 |
| IntelliJ IDEA    | Java       |   Java 8 & 11 |


### How to Install the plugin

![Plugin installation](./img/Plugin_installation.png)

To install the plugin on one of supported IDEs, go to `Preference > Plugin > Gear Icon > Install plugin from Disk` and select the `FeaRS-Plugin.zip` file (without manually unzipping it).


### How to use the plugin

![Plugin usage](./img/Plugin_usage.png)

1. After the plugin is installed, press on the <img src="./img/play_icon.png" height = 20> icon to start monitoring the method changes.
2. Implement a set of new methods in the IDE and save the code changes. (_a modified method without renaming would not be considered as a new method at the moment_)
3. After the newly added methods are identified, the recommendations will be presented in the plugin window.
4. If the recommendation is applicable, press on the <img src="./img/quote_icon.png" height = 20> icon to copy the code snippet recommended.

### Usage examples

Try one of the following example code to get some recommendations for preliminary tests.

```java
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_maps);
        SupportMapFragment mapFragment = (SupportMapFragment) getSupportFragmentManager().findFragmentById(R.id.map);
        mapFragment.getMapAsync(this);
    }
```

```java
@Override
public void onBackPressed() {
    DrawerLayout drawer = (DrawerLayout) findViewById(R.id.drawer_layout);
    if (drawer.isDrawerOpen(GravityCompat.START)) {
        drawer.closeDrawer(GravityCompat.START);
    } else {
        super.onBackPressed();
    }
}
```

```java
private void updateCustomLabelTextSummary() {
        mCustomCarrierLabelText = Settings.System.getString(getActivity().getContentResolver(), Settings.System.CUSTOM_CARRIER_LABEL);
        if (TextUtils.isEmpty(mCustomCarrierLabelText)) {
            mCustomCarrierLabel.setSummary(R.string.custom_carrier_label_notset);
        } else {
            mCustomCarrierLabel.setSummary(mCustomCarrierLabelText);
        }
    }
```

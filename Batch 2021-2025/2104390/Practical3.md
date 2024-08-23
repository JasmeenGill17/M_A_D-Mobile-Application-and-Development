# PRACTICAL 3: Android User Interface Design: To study various XML files needed for interface design

**AndroidManifest.xml**

This file provides essential information about your app to the Android system. It declares the app’s components, required permissions, hardware features, and other configurations.

**Example**

```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.myapp">

    <uses-permission android:name="android.permission.INTERNET" />

    <application
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:theme="@style/AppTheme">
        
        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
        
    </application>
</manifest>
```

**activity_main.xml**

This is a layout file that defines the UI for a specific activity, usually the main screen of the app.

**Example**

```xml
<ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/welcome_message"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/button_text"
        app:layout_constraintTop_toBottomOf="@id/textView"
        app:layout_constraintStart_toStartOf="parent" />

</ConstraintLayout>
```

**colors.xml**

Defines the color resources used throughout the app, helping to maintain a consistent color scheme.

**Example**

```xml
<resources>
    <color name="colorPrimary">#6200EE</color>
    <color name="colorPrimaryDark">#3700B3</color>
    <color name="colorAccent">#03DAC5</color>
</resources>
```

**strings.xml**

Contains all the text strings used in the app, allowing for easier localization and consistency.

**Example**

```xml
<resources>
    <string name="app_name">MyApp</string>
    <string name="welcome_message">Welcome to MyApp!</string>
    <string name="button_text">Click Me</string>
</resources>
```

**styles.xml**

Defines styles and themes for the app, allowing for consistent UI design. Styles define the appearance of UI elements, while themes apply to activities or the entire app.

**Example**

```xml
<resources>
    <!-- Base application theme -->
    <style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">
        <item name="colorPrimary">@color/colorPrimary</item>
        <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
        <item name="colorAccent">@color/colorAccent</item>
    </style>
</resources>
```

**themes.xml**

This file is used to define the themes applied across the entire application or specific activities, managing attributes like colors, fonts, and UI behavior.

**Example**

```xml
<resources xmlns:tools="http://schemas.android.com/tools">
    <!-- Base application theme -->
    <style name="Theme.MyApp" parent="Theme.MaterialComponents.DayNight.DarkActionBar">
        <!-- Primary brand color -->
        <item name="colorPrimary">@color/colorPrimary</item>
        <item name="colorPrimaryVariant">@color/colorPrimaryDark</item>
        <item name="colorOnPrimary">@android:color/white</item>
        <!-- Secondary brand color -->
        <item name="colorSecondary">@color/colorAccent</item>
    </style>
</resources>
```

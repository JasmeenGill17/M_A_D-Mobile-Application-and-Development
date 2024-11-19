**PRACTICAL 5: Apps Interactivity in Android: To incorporate element of interactivity using Android Fragment and Intent Class.**

**UI CODE**

-activity main.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:orientation="vertical"
tools:context=".MainActivity">
<LinearLayout
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:orientation="horizontal">
<Button
android:id="@+id/btn1"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginRight="10dp"
android:layout_weight="1"
android:text="First" />
<Button
android:id="@+id/btn2"
android:layout_width="wrap_content"
android:layout_height="match_parent"
android:layout_marginRight="10dp"
android:layout_weight="1"
android:text="Second" />
<Button
android:id="@+id/btn3"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="Third" />
</LinearLayout>
<LinearLayout
android:layout_width="match_parent"
android:layout_height="682dp"
android:orientation="vertical">
<androidx.fragment.app.FragmentContainerView
android:id="@+id/fragmentContainer"
android:name="com.example.fragments.FirstFragment"
android:layout_width="match_parent"
android:layout_height="match_parent" />
</LinearLayout>
</LinearLayout>

```

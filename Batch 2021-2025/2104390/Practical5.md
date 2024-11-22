**PRACTICAL 5: Apps Interactivity in Android: To incorporate element of interactivity using Android Fragment and Intent Class.**

**activity main.xml**

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
**fragment first.xml**

```xml
<?xml version="1.0" encoding="utf-8"?>
<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
21
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:background="#ff4564"
tools:context=".FirstFragment">
<!-- TODO: Update blank fragment layout -->
<TextView
android:id="@+id/t1"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:layout_gravity="center"
android:gravity="center"
android:text="fragment1"
android:textColor="#ffffff"
android:textSize="30sp"
android:textStyle="bold" />
</FrameLayout>

```

**fragment second.xml**

```xml
<?xml version="1.0" encoding="utf-8"?>
<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:background="#bbb321"
tools:context=".SecondFragment">
<!-- TODO: Update blank fragment layout -->
<TextView
android:layout_width="match_parent"
android:layout_height="match_parent"
android:text="fragment2"
android:layout_gravity="center"
android:gravity="center"
android:textSize="30sp"
android:textStyle="bold"
android:id="@+id/t2"/>
</FrameLayout>

```

**fragment third.xml**

```xml
<?xml version="1.0" encoding="utf-8"?>
<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:background="#15EC43"
tools:context=".ThirdFragment">
<!-- TODO: Update blank fragment layout -->
<TextView
android:layout_width="match_parent"
android:layout_height="match_parent"
android:text="fragment 3"
android:layout_gravity="center"
android:gravity="center"
android:textSize="30sp"
android:textStyle="bold"
android:id="@+id/t3"/>
</FrameLayout>
```

**MainActivity.java**

```xml
package com.example.fragments;
import androidx.appcompat.app.AppCompatActivity;
import androidx.fragment.app.FragmentManager;
import androidx.fragment.app.FragmentTransaction;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
public class MainActivity extends AppCompatActivity {
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
Button b1=findViewById(R.id.btn1);
Button b2=findViewById(R.id.btn2);
Button b3=findViewById(R.id.btn3);
b1.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View view) {
FragmentManager fm= getSupportFragmentManager();
FragmentTransaction ft= fm.beginTransaction();
ft.replace( R.id.fragmentContainer, FirstFragment.class, null);
ft.commit();
} });
b2.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View view) {
FragmentManager fm= getSupportFragmentManager();
FragmentTransaction ft= fm.beginTransaction();
ft.replace( R.id.fragmentContainer, new SecondFragment());
ft.commit();
} });
b3.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View view) {
FragmentManager fm= getSupportFragmentManager();
FragmentTransaction ft= fm.beginTransaction();
ft.replace( R.id.fragmentContainer, new ThirdFragment());
ft.commit();
} }); } }
```

**FirstFragment.java**

```xml
package com.example.fragments;
import android.os.Bundle;
import androidx.fragment.app.Fragment;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.TextView;
public class FirstFragment extends Fragment {
// Important method
public FirstFragment() {
// Required empty public constructor
}
@Override
public View onCreateView(LayoutInflater inflater, ViewGroup container,
Bundle savedInstanceState) {
// Inflate the layout for this fragment
View view= inflater.inflate(R.layout.fragment_first, container, false);
TextView t1= view.findViewById(R.id.t1);
return view;
}
}

```

**Output**

<figure>
  
<img src="https://github.com/user-attachments/assets/a563493c-d979-4177-9b61-352f1adc4ba1" alt="Screenshot 2024-11-22 084850" width="150" height="350"/>

<img src="https://github.com/user-attachments/assets/38625566-2741-41fa-8f2b-2288464a3d7a" alt="Screenshot 2024-11-22 084910" width="150" height="350"/>

<img src="https://github.com/user-attachments/assets/81bd05eb-04b2-41c1-922f-643d5b164432" alt="Screenshot 2024-11-22 084925" width="150" height="350"/>

</figure>

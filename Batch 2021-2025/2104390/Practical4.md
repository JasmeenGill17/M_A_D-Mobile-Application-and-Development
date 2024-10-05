# PRACTICAL 4: Android User Interface Design: To implement different type of layouts like relative, grid, linear and table.

# Develop a program to implement constraint layout to display Hello World on screen.

**CODE:**

- **activity_main.xml**

  ```xml
  <?xml version="1.0" encoding="utf-8"?>
  <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
  </androidx.constraintlayout.widget.ConstraintLayout>
  ```

**OUTPUT**

# Develop a program to implement linear layout. 

**CODE: For Vertical Layout**

- **activity_main.xml**

  ```xml
  <?xml version="1.0" encoding="utf-8"?>
  <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main1"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:layout_centerInParent="true"
    android:layout_centerVertical="true"
    android:orientation="vertical"
    tools:context=".MainActivity">
    <EditText
        android:id="@+id/editTextText2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="10"
        android:hint="to"
        android:inputType="text" />
    <EditText
        android:id="@+id/editTextText3"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="10"
        android:hint="Subject"
        android:inputType="text" />
    <EditText
        android:id="@+id/editTextTextMultiLine"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="10"
        android:gravity="start|top"
        android:lines="4"
        android:hint="Message"
        android:inputType="textMultiLine" />
    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="right"
        android:layout_marginTop="449dp"
        android:layout_marginRight="10dp"
        android:text="Send" />
  </LinearLayout>
  ```

**OUTPUT**

**CODE: For Horizontal Layout**

- **activity_main.xml**

  ```xml
  <?xml version="1.0" encoding="utf-8"?>
  <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="16dp"
    android:background="@color/orange">
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="24dp"
        android:background="@android:color/white"
        android:layout_gravity="center"
        android:layout_margin="24dp"
        android:elevation="4dp">
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Registration Form"
            android:textSize="24sp"
            android:textStyle="bold"
            android:layout_gravity="center_horizontal"
            android:paddingBottom="8dp" />
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center"
            android:gravity="center"
            android:paddingBottom="24dp"
            android:text="Fill out the form carefully for registration"
            android:textSize="16sp" />
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Student Name"
            android:paddingBottom="8dp" />
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:weightSum="2"
            android:paddingBottom="16dp">
            <EditText
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:hint="First Name"
                android:inputType="textPersonName"
                android:layout_marginEnd="8dp" />
            <EditText
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:hint="Last Name"
                android:inputType="textPersonName" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:weightSum="2"
            android:paddingBottom="16dp">
            <TextView
                android:id="@+id/textView5"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="Gender" />
            <TextView
                android:id="@+id/textView9"
                android:paddingLeft="105dp"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="Student Email ID" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:weightSum="2"
            android:paddingBottom="16dp">
            <Spinner
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:prompt="Gender"
                android:layout_marginEnd="8dp" />
            <EditText
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:hint="Student E-mail"
                android:inputType="textEmailAddress" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:weightSum="2"
            android:paddingBottom="16dp">
            <TextView
                android:id="@+id/textView5"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="Student ID" />
            <TextView
                android:id="@+id/textView9"
                android:paddingLeft="105dp"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="List of Classes" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:weightSum="2"
            android:paddingBottom="16dp">
            <EditText
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:hint="Student ID"
                android:inputType="text"
                android:layout_marginEnd="7dp" />
            <Spinner
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:prompt="Please Select"
                android:spinnerMode="dropdown" />
        </LinearLayout>
        <Button
            android:layout_width="146dp"
            android:layout_height="wrap_content"
            android:layout_gravity="center_horizontal"
            android:backgroundTint="@color/green"
            android:text="Submit"
            android:textColor="@android:color/white" />
    </LinearLayout>
  </LinearLayout>
  ```

**OUTPUT**

# Develop a program to implement relative layout to display sign up form.

**CODE: SignUp**

- **activity_main.xml**

  ```xml
  <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#FFFFFF"
    tools:context=".MainActivity">
    <TextView
        android:id="@+id/signup_title"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Signup"
        android:textSize="24sp"
        android:textStyle="bold"
        android:layout_centerHorizontal="true" />
    <EditText
        android:id="@+id/signup_email"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/signup_title"
        android:layout_marginTop="16dp"
        android:hint="Email"
        android:inputType="textEmailAddress" />
    <EditText
        android:id="@+id/signup_password"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/signup_email"
        android:layout_marginTop="16dp"
        android:hint="Create password"
        android:inputType="textPassword" />
    <EditText
        android:id="@+id/signup_confirm_password"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/signup_password"
        android:layout_marginTop="16dp"
        android:hint="Confirm password"
        android:inputType="textPassword" />
    <Button
        android:id="@+id/signup_button"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/signup_confirm_password"
        android:layout_marginTop="16dp"
        android:text="Signup"
        android:backgroundTint="@android:color/holo_blue_dark"
        android:textColor="@android:color/white" />
    <TextView
        android:id="@+id/login_redirect"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/signup_button"
        android:layout_marginTop="8dp"
        android:layout_centerHorizontal="true"
        android:text="Already have an account? Login"
        android:textColor="@android:color/holo_blue_dark" />
    <TextView
        android:id="@+id/signup_or_text"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/login_redirect"
        android:layout_marginTop="16dp"
        android:layout_centerHorizontal="true"
        android:text="Or" />
    <Button
        android:id="@+id/signup_with_facebook"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/signup_or_text"
        android:layout_marginTop="8dp"
        android:text="Login with Facebook"
        android:backgroundTint="#3b5998"
        android:textColor="@android:color/white" />
    <Button
        android:id="@+id/signup_with_google"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/signup_with_facebook"
        android:layout_marginTop="19dp"
        android:backgroundTint="#db4437"
        android:text="Login with Google"
        android:textColor="@android:color/white" />
  </RelativeLayout>
  ```

  **CODE: Login**

- **activity_main.xml**

  ```xml
  <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#FFFFFF"
    tools:context=".MainActivity">
    <TextView
        android:id="@+id/login_title"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Login"
        android:textSize="24sp"
        android:textStyle="bold"
        android:layout_centerHorizontal="true" />
    <EditText
        android:id="@+id/login_email"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/login_title"
        android:layout_marginTop="16dp"
        android:hint="Email"
        android:inputType="textEmailAddress" />
    <EditText
        android:id="@+id/login_password"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/login_email"
        android:layout_marginTop="16dp"
        android:hint="Password"
        android:inputType="textPassword" />
    <TextView
        android:id="@+id/forgot_password"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/login_password"
        android:layout_marginTop="8dp"
        android:layout_centerHorizontal="true"
        android:text="Forgot password?"
        android:textColor="@android:color/holo_blue_dark" />
    <Button
        android:id="@+id/login_button"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/forgot_password"
        android:layout_marginTop="16dp"
        android:text="Login"
        android:backgroundTint="@android:color/holo_blue_dark"
        android:textColor="@android:color/white" />
    <TextView
        android:id="@+id/signup_redirect"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/login_button"
        android:layout_marginTop="8dp"
        android:layout_centerHorizontal="true"
        android:text="Don't have an account? Signup"
        android:textColor="@android:color/holo_blue_dark" />
    <TextView
        android:id="@+id/or_text"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/signup_redirect"
        android:layout_marginTop="16dp"
        android:layout_centerHorizontal="true"
        android:text="Or" />
    <Button
        android:id="@+id/login_with_facebook"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/or_text"
        android:layout_marginTop="8dp"
        android:text="Login with Facebook"
        android:backgroundTint="#3b5998"
        android:textColor="@android:color/white" />
    <Button
        android:id="@+id/login_with_google"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/login_with_facebook"
        android:layout_marginTop="8dp"
        android:text="Login with Google"
        android:backgroundTint="#db4437"
        android:textColor="@android:color/white" />
  </RelativeLayout>
  ```
  
**OUTPUT**

# Develop a program to implement table layout to display calculator

**CODE:**

- **activity_main.xml**

  ```xml
  <?xml version="1.0" encoding="utf-8"?>
  <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <!-- Display Screen -->
    <TextView
        android:id="@+id/tvDisplay"
        android:layout_width="0dp"
        android:layout_height="120dp"
        android:background="#FFFFFF"
        android:text=""
        android:textSize="32sp"
        android:gravity="end|center_vertical"
        android:padding="16dp"
        android:textColor="#000000"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent" />
    <!-- First Row Buttons: AC, (, ), % -->
    <GridLayout
        android:id="@+id/row1"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginTop="16dp"
        android:columnCount="4"
        android:rowCount="1"
        app:layout_constraintTop_toBottomOf="@+id/tvDisplay"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintWidth_percent="0.9">
        <Button
            android:text="AC"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#6E7581"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
        <Button
            android:text="("
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#6E7581"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
        <Button
            android:text=")"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#6E7581"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
        <Button
            android:text="%"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#6E7581"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
    </GridLayout>
    <!-- Numeric Buttons and Operators -->
    <GridLayout
        android:id="@+id/numericGrid"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginTop="16dp"
        android:columnCount="4"
        android:rowCount="5"
        app:layout_constraintTop_toBottomOf="@+id/row1"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintWidth_percent="0.9">
        <!-- Row 1: 7, 8, 9, / -->
        <Button
            android:text="7"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="8"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="9"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="/"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#6E7581"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
        <!-- Row 2: 4, 5, 6, * -->
        <Button
            android:text="4"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="5"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="6"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="*"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#6E7581"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
        <!-- Row 3: 1, 2, 3, - -->
        <Button
            android:text="1"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="2"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="3"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="-"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#6E7581"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
        <!-- Row 4: ., 0, =, + -->
        <Button
            android:text="."
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="0"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#E3F2FD"
            android:textColor="#000000"
            android:textSize="24sp" />
        <Button
            android:text="="
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#F66335"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
        <Button
            android:text="+"
            android:layout_width="0dp"
            android:layout_height="80dp"
            android:layout_columnWeight="1"
            android:background="#6E7581"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
    </GridLayout>
  </androidx.constraintlayout.widget.ConstraintLayout>
  ```

**OUTPUT**

# Develop a program to implement UI from Buttons Palette use Constraint Layout i.e Button, ImageButton, TogggleButton, Checkbox, Chip, ChipGroup, Radio Button and Radio Group and FloatingActionButton.

**CODE:**

- **activity_main.xml**

  ```xml
  ```

**OUTPUT**

# Develop a program to implement UI from Text Palette use Linear Layout two Login windows. First is to Login with a Key use [Password(numeric)] and in second UI implement frame Layout to display Phone, Postal address, Time, Date, Number, Number(signed) , Number (decimal), AutoCompleteTextView, MultiAutoCompleteTextView, CheckedTextView, TextInputLayout.

**CODE:**

- **activity_main.xml**

  ```xml
  ```

**OUTPUT**

# Develop a program to implement UI from Widgets Palette use Relative Layout i.e Progress Bar, SeekBar , RatingBar and Switch.

**CODE:**

- **activity_main.xml**

  ```xml
  ```
  
**OUTPUT**

# Develop a program to implement UI from Containers Palette use Grid Layout i.e List View, Grid View, Image View, Scroll View, Recycler View, Navigation View, ButtomNavigationView.

**CODE:**

- **activity_main.xml**

  ```xml
  ```

**OUTPUT**

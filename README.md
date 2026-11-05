# Ex.No:2B To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
1.Start the project: Create a new Android project with two Empty Activities (MainActivity and MainActivity2).

2.Design the First Screen: In activity_main.xml, add an EditText to receive the number input and a Button to trigger the calculation.

3.Design the Second Screen: In activity_main2.xml, add a TextView to display the calculated factorial result.

4.Get Input (MainActivity): Inside MainActivity.java, set an OnClickListener on the button to retrieve the entered number from the EditText.

5.Pass Data using Explicit Intent: Create an Intent targeting MainActivity2.class. Attach the entered number to the intent using intent.putExtra(), and start the activity using startActivity(intent).

6.Receive Data (MainActivity2): In MainActivity2.java, use getIntent().getStringExtra() (or getIntExtra()) to retrieve the passed number.

7.Calculate Factorial: Write a loop or recursive function to compute the factorial of the received number.

8.Display Result: Update the TextView in the second activity to show the computed factorial value.

9.Stop: Run and test the application.


## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by: Manobala R
Registeration Number : 212225230167
*/
```
## MainActivity.java
```
package com.example.explicitintent;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

    public void newsScreen(View view) {
        Intent i = new Intent(getApplicationContext(), MainActivity2.class);
        startActivity(i);
    }
}
```
## Activitymain.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#B0C7A2"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/editText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#8E93B6"
        android:backgroundTint="#9CBA77"
        android:text="@string/welcome_gfg_home_screen"
        android:textAlignment="center"
        android:textSize="28sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.245" />

    <Button
        android:id="@+id/btn1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:onClick="newsScreen"
        android:text="@string/go_to_news_screen"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editText" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java2
```
package com.example.explicitintent;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;

public class MainActivity2 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);
    }

    public void homeScreen(View view) {
        Intent i = new Intent(getApplicationContext(), MainActivity.class);
        startActivity(i);
    }
}
```
## Activitymain.xml2
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity2">

    <TextView
        android:id="@+id/textViewNews"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/welcome_to_news_screen"
        android:textSize="24sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/btn2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:onClick="homeScreen"
        android:text="@string/go_to_home_screen"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textViewNews" />

</androidx.constraintlayout.widget.ConstraintLayout>

```

## OUTPUT
<img width="1917" height="1078" alt="Screenshot 2026-10-24 140412" src="https://github.com/user-attachments/assets/ee7c631c-00e4-4c9c-977c-31975f279bdf" />
<img width="1915" height="1078" alt="Screenshot 2026-10-24 140425" src="https://github.com/user-attachments/assets/11a986e5-b299-4c7a-ab2a-f182cb1b40f1" />




## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.



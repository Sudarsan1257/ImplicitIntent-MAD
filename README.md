# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1. **Create Layout** – Add an `EditText` for URL input and a `Button` labeled "Navigate".
2. **Initialize Components** – Link `EditText` and `Button` with `findViewById()`.
3. **Set Listener** – Attach `onClickListener` to the "Navigate" button.
4. **Get Input** – Read the text from `EditText` when button is clicked.
5. **Create Intent** – Use `Intent.ACTION_VIEW` with `Uri.parse()` of the entered URL.
6. **Start Activity** – Call `startActivity(intent)` to open the browser page.


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: SUDARSAN.A
Registration Number : 212224220111
*/
```

## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/editText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:fontFamily="monospace"
        android:hint="Enter The URL"
        android:inputType="text"
        android:textColor="#3B343C"
        android:typeface="monospace"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.616"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.134" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="sans-serif-black"
        android:lineSpacingExtra="16sp"
        android:text="Click Here"
        android:textAppearance="@style/TextAppearance.AppCompat.Body1"
        android:textColor="#DCCFD4"
        android:textColorLink="#E91E63"
        android:textSize="14sp"
        android:typeface="monospace"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.499" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

## MainActivity.java
```
package com.example.implicitapp;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.button);
        editText = (EditText) findViewById(R.id.editText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```


## OUTPUT

## activity_main.xml
<img width="959" height="506" alt="image" src="https://github.com/user-attachments/assets/88603da8-d177-4510-8f4e-7d3bb11d373b" />

## MainActivity.java
<img width="959" height="504" alt="image" src="https://github.com/user-attachments/assets/7b0a0524-0f90-4a8c-acf0-f225406e0ffb" />

## Implicit Intent
<img width="490" height="919" alt="image" src="https://github.com/user-attachments/assets/31fbe195-ea6c-4961-af48-e979f5eae366" />

## Navigation
<img width="239" height="457" alt="image" src="https://github.com/user-attachments/assets/7c6ac3b8-8695-41f1-9480-bd65af5ca6a1" />


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.



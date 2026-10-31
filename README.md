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
<img width="1918" height="1088" alt="image" src="https://github.com/user-attachments/assets/3a6d95ef-0990-46a0-aae3-bdfd4f83d420" />

## MainActivity.java
<img width="1919" height="1087" alt="image" src="https://github.com/user-attachments/assets/8da3b684-1f46-4273-b9ce-b25dc00988b3" />

## Implicit Intent
<img width="434" height="929" alt="image" src="https://github.com/user-attachments/assets/5b95403b-6270-44d1-a03e-dfb991a013ff" />

## Navigation
<img width="522" height="939" alt="image" src="https://github.com/user-attachments/assets/0aaafd32-74a2-4fe3-ab35-25863ddb688d" />


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.



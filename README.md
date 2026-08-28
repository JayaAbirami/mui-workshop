# Addition of Two Numbers Android Application

## 📱 Project Description

This Android application is used to add two numbers. The user enters two values, clicks the **ADD** button, and the application displays the summation result.

## 🎯 Objective

- Get two numeric values from the user.
- Add the two numbers.
- Display the summation result on the screen.

## 🛠️ Technologies Used

- Android Studio
- Java
- XML

## Code
## activity.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter First Number"
        android:inputType="numberDecimal"/>

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Second Number"
        android:inputType="numberDecimal"/>

    <Button
        android:id="@+id/btnAdd"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="ADD"/>

    <TextView
        android:id="@+id/txtResult"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Result"
        android:textSize="22sp"
        android:paddingTop="20dp"/>

</LinearLayout>
```
## MainActivity.java:
```
package com.example.additionapp;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button btnAdd;
    TextView txtResult;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        btnAdd = findViewById(R.id.btnAdd);
        txtResult = findViewById(R.id.txtResult);

        btnAdd.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {

                double n1 = Double.parseDouble(num1.getText().toString());
                double n2 = Double.parseDouble(num2.getText().toString());

                double sum = n1 + n2;

                txtResult.setText("Sum = " + sum);
            }
        });
    }
}
```
## Output:
<img width="1600" height="854" alt="image" src="https://github.com/user-attachments/assets/689151a6-8caf-4d86-a3e7-2c1839ae42aa" />
<img width="1600" height="846" alt="image" src="https://github.com/user-attachments/assets/0373e293-d065-4882-b0d3-d62e4c184a4e" />

# Addition App

## 📱 Create an Application for Addition of Two Numbers

This Android application is developed using **Android Studio** and **Java**.  
The application accepts two numbers from the user, calculates their sum, and displays the result.

---

## 🎯 Objective

To create an Android application that:

1. Gets two values from the user.
2. Adds the two values.
3. Displays the summation value in the result text box.

---

## 🛠️ Technologies Used

- **Android Studio**
- **Java**
- **XML**
- **Android SDK**

---

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
## MainActivity.java
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
<img width="1600" height="854" alt="image" src="https://github.com/user-attachments/assets/e1ff8d49-6a3b-49b7-acf5-a30a1408dc80" />

<img width="1600" height="846" alt="image" src="https://github.com/user-attachments/assets/ba782551-9592-40b6-88a5-2c94a8cd5277" />

## Result

The Android application for Addition of Two Numbers was successfully developed using Android Studio, Java, and XML. The application accepts two numbers from the user, calculates their sum, and displays the result successfully in the result text box.

## WORKSHOP ----SUMMATION OF TWO NUMBERS USING ANDROID STUDIO.


## AIM:

To develop an Android application using Android Studio that takes two numbers as input from the user and displays their sum when a button is clicked.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:


1.Start the program.

2.Design the UI with two EditTexts, one Button, and one TextView.

3.Read the two numbers from the EditTexts.

4.Convert the input values to integers.

5.Add the two numbers and store the result.

6.Display the sum in the TextView.

7.Stop the program.


## Program:
 ```
/*
Program to implement a Hello world Activity using all lifecycles methods using Android Studio .
Developed by: DAKSHINA MOORTHY N D
RegisterNumber:  212224230049
*/
```

## MainActivity.java:

```
package com.example.workshop01;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    EditText editTextNumber1, editTextNumber2;
    Button buttonAdd;
    TextView textResult;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        editTextNumber1 = findViewById(R.id.editTextNumber1);
        editTextNumber2 = findViewById(R.id.editTextNumber2);
        buttonAdd = findViewById(R.id.buttonAdd);
        textResult = findViewById(R.id.textResult);

        buttonAdd.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String num1Str = editTextNumber1.getText().toString();
                String num2Str = editTextNumber2.getText().toString();

                if (num1Str.isEmpty() || num2Str.isEmpty()) {
                    textResult.setText("Please enter both numbers");
                    return;
                }

                int num1 = Integer.parseInt(num1Str);
                int num2 = Integer.parseInt(num2Str);
                int sum = num1 + num2;

                textResult.setText(num1 + " + " + num2 + " = " + sum);
            }
        });
    }
}
```



## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="24dp"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textTitle"
        android:text="Addition Of Two Numbers"
        android:textSize="28sp"
        android:textStyle="bold"
        android:layout_marginBottom="24dp"
        android:gravity="center"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/editTextNumber1"
        android:hint="Enter first number"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginBottom="12dp" />

    <EditText
        android:id="@+id/editTextNumber2"
        android:hint="Enter second number"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginBottom="24dp" />

    <Button
        android:id="@+id/buttonAdd"
        android:text="+"
        android:backgroundTint="#F44336"
        android:textColor="@android:color/white"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginBottom="24dp" />

    <TextView
        android:id="@+id/textResult"
        android:text="Result will appear here"
        android:textSize="20sp"
        android:textColor="#757575"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />

</LinearLayout>
```


## Output:

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/01d07420-5bf9-4407-b909-85449447c7a1" />


## Result:

The Android application for the summation of two numbers was successfully developed and executed.

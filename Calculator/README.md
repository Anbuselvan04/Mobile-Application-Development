# Ex.No:9 Develop a simple calculator using android studio.

## AIM:

To develop a program to develop a simple calculator in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as calculator and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the calculator operation in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
## activity_main.xml:
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:tools="http://schemas.android.com/tools"         
android:layout_width="match_parent"         
android:layout_height="match_parent"         
android:orientation="vertical"          
android:padding="16dp"         
tools:context=".MainActivity">

<EditText
    android:id="@+id/number1EditText"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:inputType="number"
    android:hint="Enter number 1" />

<EditText
    android:id="@+id/number2EditText"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:inputType="number"
    android:hint="Enter number 2" />

<Button
    android:id="@+id/addButton"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="Add" />

<Button
    android:id="@+id/subtractButton"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="Subtract" />

<Button
    android:id="@+id/multiplyButton"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="Multiply" />

<Button
    android:id="@+id/divideButton"
    android:layout_width="380dp"
    android:layout_height="wrap_content"
    android:text="Divide" />

<TextView
    android:id="@+id/resultTextView"
    android:layout_width="385dp"
    android:layout_height="51dp"
    android:paddingTop="16dp"
    android:textSize="25dp" />
```
## Main_Activity.java
```
package com.example.calculator;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.view.View;

import android.widget.Button;

import android.widget.EditText;

import android.widget.TextView;

import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

private EditText number1EditText, number2EditText;
private Button addButton, subtractButton, multiplyButton, divideButton;
private TextView resultTextView;

@Override
protected void onCreate(Bundle savedInstanceState) {

    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);

    number1EditText = findViewById(R.id.number1EditText);
    number2EditText = findViewById(R.id.number2EditText);
    addButton = findViewById(R.id.addButton);
    subtractButton = findViewById(R.id.subtractButton);
    multiplyButton = findViewById(R.id.multiplyButton);
    divideButton = findViewById(R.id.divideButton);
    resultTextView = findViewById(R.id.resultTextView);

    addButton.setOnClickListener(new View.OnClickListener() {
    
        @Override
        public void onClick(View v) {
            calculateResult("+");
        }
    });

    subtractButton.setOnClickListener(new View.OnClickListener() {
    
        @Override
        public void onClick(View v) {
            calculateResult("-");
        }
    });

    multiplyButton.setOnClickListener(new View.OnClickListener() {
    
        @Override
        public void onClick(View v) {
            calculateResult("*");
        }
    });

    divideButton.setOnClickListener(new View.OnClickListener() {
    
        @Override
        public void onClick(View v) {
            calculateResult("/");
        }
    });
}

private void calculateResult(String operator) {

    String number1Str = number1EditText.getText().toString();
    String number2Str = number2EditText.getText().toString();

    if (number1Str.isEmpty() || number2Str.isEmpty()) {
        Toast.makeText(MainActivity.this, "Please enter both numbers", Toast.LENGTH_SHORT).show();
        return;
    }

    double number1 = Double.parseDouble(number1Str);
    
    double number2 = Double.parseDouble(number2Str);

    double result = 0;

    switch (operator) {
        case "+":
            result = number1 + number2;
            break;
        case "-":
            result = number1 - number2;
            break;
        case "*":
            result = number1 * number2;
            break;
        case "/":
            if (number2 == 0) {
                Toast.makeText(MainActivity.this, "Cannot divide by zero", Toast.LENGTH_SHORT).show();
                return;
            }
            result = number1 / number2;
            break;
    }

    resultTextView.setText("Result: " + result);
}
}
```

Program to print the text “calculator operation”.

Developed by: Anbuselvan A

Registeration Number : 212221040013


## OUTPUT

![AM](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/a5935bf8-ac38-4cbc-bd15-8a691d533740)
![MA](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/af68a8d5-6427-4eba-b3a4-cb9c611d0b85)
![OP](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/181b8132-94a4-4d5e-8092-29e9102b91e2)



## RESULT
Thus a Simple Android Application develop a program to create simple calculator in Android Studio is developed and executed successfully.

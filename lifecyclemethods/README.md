# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:

## activity_main.xml :
```
    <?xml version="1.0" encoding="utf-8"?>
    <androidx.constraintlayout.widget.ConstraintLayout 
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/head"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="@font/arbutus_slab"
        android:text="Mobile Application Development"
        android:textColor="@color/Maroon"
        android:textSize="20sp"
        app:layout_constraintBottom_toTopOf="@+id/body"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/body"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="356dp"
        android:fontFamily="@font/expletus_sans_medium"
        android:text="HELLO WORLD"
        android:textColor="@color/MediumTurquoise"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## Main_Activity.java : 
```
package com.example.experiment1;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toast t = Toast.makeText(getApplicationContext(),"onCreate Called",Toast.LENGTH_LONG);
        t.show();
    }

    protected void onStart(){
        super.onStart();
        Toast t = Toast.makeText(getApplicationContext(),"onStart Called",Toast.LENGTH_LONG);
        t.show();
    }

    protected void onRestart(){
        super.onRestart();
        Toast t = Toast.makeText(getApplicationContext(),"onRestart Called",Toast.LENGTH_LONG);
        t.show();
    }

    protected void onPause(){
        super.onPause();
        Toast t = Toast.makeText(getApplicationContext(),"onPause Called",Toast.LENGTH_LONG);
        t.show();
    }

    protected void onResume(){
        super.onResume();
        Toast t = Toast.makeText(getApplicationContext(),"onResume Called",Toast.LENGTH_LONG);
        t.show();
    }

    protected void onStop(){
        super.onStop();
        Toast t = Toast.makeText(getApplicationContext(),"onStop Called",Toast.LENGTH_LONG);
        t.show();
    }

    protected void onDestroy(){
        super.onDestroy();
        Toast t = Toast.makeText(getApplicationContext(),"onDestroy Called",Toast.LENGTH_LONG);
        t.show();
    }
}
```
Program to print the text “Hello World”.

Developed by : Anbuselvan A

Registration Number : 212221040013

## OUTPUT

![Exp_1 AM](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/21c321de-dcbe-4504-bd3d-75702e57ba15)
![Exp_1 MA](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/d4ebad4f-8260-4aa3-9607-d78006345e39)
![1  Exp_1 Create](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/c0312c53-3bec-44b8-ac5f-7e15111301fe)
![2  Exp_1 Sart](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/8f399638-67b3-455e-9d3a-45fea19c6435)
![3  Exp_1 Resume](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/099ca09d-d84c-44be-93ef-a83ae9db1a84)
![4  Exp_1 Restart](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/b127b62a-99b1-456a-bf61-81384e1e198e)
![5  Exp_1 Pause](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/2a58676a-e155-4b74-9773-1321c45bb4e1)
![6  Exp_1 Stop](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/3cfb64f8-d2bf-455f-8e69-7c92d4f62518)
![7  Exp_1 Destroy](https://github.com/Anbuselvan04/Mobile-Application-Development/assets/119410896/d39c3c0b-e076-45cc-8ba8-550caa04b2fa)



## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.

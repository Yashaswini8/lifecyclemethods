# Ex.No:1 Implementation of a Hello world Activity using all lifecycles methods using Android Studio.


## AIM:
To create Hello world Activity using all lifecycles methods to display messages using android studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.



## PROGRAM:
``` 
/*
Program to implement a Hello world Activity using all lifecycles methods using Android Studio .
Developed by: YASHASWINI S
RegisterNumber:  212224220123
*/
```

## MainActivity.java:
```

package com.example.andriodlifecycle;

import android.os.Bundle;
import android.widget.Toast;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);
        Toast toast= Toast.makeText(getApplicationContext(),"OnCreated Executed",Toast.LENGTH_LONG);
        toast.show();
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) -> {
            Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
            return insets;
        });
    }

    protected void onStart(){
        super.onStart();
        Toast toast= Toast.makeText(getApplicationContext(),"OnStart Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onResume(){
        super.onResume();
        Toast toast= Toast.makeText(getApplicationContext(),"OnResume Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onPause(){
        super.onPause();
        Toast toast= Toast.makeText(getApplicationContext(),"onPause Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onStop(){
        super.onStop();
        Toast toast= Toast.makeText(getApplicationContext(),"onStop Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onRestart(){
        super.onRestart();
        Toast toast= Toast.makeText(getApplicationContext(),"onRestart Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onDestroy(){
        super.onDestroy();
        Toast toast= Toast.makeText(getApplicationContext(),"onDestroy Executed",Toast.LENGTH_LONG);
        toast.show();
    }
}

```

## activitymain.xml:
```

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
        android:text="Welcome to Andriod LifeCycle"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```


## OUTPUT:

# 1. OnCreate Executed:

<img width="1920" height="1200" alt="oncreate" src="https://github.com/user-attachments/assets/d82e7504-4f66-44df-8c20-cbd0b2cce969" />



# 2. OnPause Executed:

<img width="1920" height="1200" alt="onpause" src="https://github.com/user-attachments/assets/3d900fe9-cfab-40f8-bf05-3255cbe46621" />


# 3. OnResume Executed:

<img width="1920" height="1200" alt="onresume" src="https://github.com/user-attachments/assets/e5af51b4-394a-4757-89d5-452034e17c5e" />


# 4. OnRestart Executed:

<img width="1920" height="1200" alt="onrestart" src="https://github.com/user-attachments/assets/a0227f7a-8915-4dee-8d2c-d2ff3d22a2cb" />

# 5. OnStart Executed:

<img width="1920" height="1200" alt="onstart" src="https://github.com/user-attachments/assets/abfac62e-c13c-49f7-8328-3b93ff26e268" />





## RESULT:
Thus a program to implement the various life cycles of an activity is written and successfully executed using Android Studio.

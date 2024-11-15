## Ex.No:7 Develop an android application to display the country name with image using list view in android studio.
## AIM:
To create and develop the application to display the place name with image using list view in android studio

## EQUIPMENTS REQUIRED:
Android Studio(Latest Version)

## ALGORITHM:
## Step 1:Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “listview″ and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Get contacts details and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
Program to print the list of item.
Developed by: MANOJ MV
Registeration Number : 212222220023
```
## Activity_Main.xml
```
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent" android:layout_height="match_parent" tools:context=".MainActivity">
<ListView
    android:id="@+id/listView"
    android:layout_width="match_parent"
    android:layout_height="fill_parent"
    />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MyList.xml
## Strings.xml
ListView Android Java Php Hadoop Sap Python Ajax C++ Ruby Rails .Net Perl
## MainActivity.java
```
package com.example.ex_7_listview;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.ListView;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    ListView listView;
    TextView textView;
    String[] listItem;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        listView = (ListView) findViewById(R.id.listView);
        textView = (TextView) findViewById(R.id.textView);
        listItem = getResources().getStringArray(R.array.array_technology);

        final ArrayAdapter adapter = new ArrayAdapter(this, 
                android.R.layout.simple_list_item_1, android.R.id.text1, listItem);
        listView.setAdapter(adapter);

        listView.setOnItemClickListener(new AdapterView.OnItemClickListener() {
            @Override
            public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
                String value = adapter.getItem(position).toString();
                Toast.makeText(getApplicationContext(), value, Toast.LENGTH_SHORT).show();
            }
        });
    }
}
    listView.setOnItemClickListener(new AdapterView.OnItemClickListener() {
        @Override
        public void onItemClick(AdapterView<?> adapterView, View view, int position, long l) {
            // TODO Auto-generated method stub
            String value=adapter.getItem(position);
            Toast.makeText(getApplicationContext(),value,Toast.LENGTH_SHORT).show();

        }
    });

}
```

## OUTPUT
![374121565-b79e334a-c1e6-4840-b1c4-c06c34b7c849](https://github.com/user-attachments/assets/7fb2b142-9d01-4c37-9986-3adb083bff15)

## RESULT
Thus a Simple Android Application to create and develop the application to display the country name with image using list view in android studio is developed and executed successfully

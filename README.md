# Mad-lab-Simple-Calculator-
<?xml version="1.0" encoding="utf-8"?>

<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"

 xmlns:app="http://schemas.android.com/apk/res-auto"

 xmlns:tools="http://schemas.android.com/tools"

 android:layout_width="match_parent"

 android:layout_height="match_parent"

 tools:context=".MainActivity">
 <TextView

 android:layout_width="246dp"

 android:layout_height="wrap_content"

 android:layout_alignParentEnd="true"

 android:layout_alignParentBottom="true"

 android:layout_marginEnd="75dp"

 android:layout_marginBottom="642dp"

 android:text="Basic Calculator"

 android:textColor="@color/purple_500"

 android:textSize="30dp"

 android:textStyle="bold"

 app:layout_constraintBottom_toBottomOf="parent"

 app:layout_constraintLeft_toLeftOf="parent"

 app:layout_constraintRight_toRightOf="parent"

 app:layout_constraintTop_toTopOf="parent" />

 <EditText

 android:id="@+id/number1"

 android:layout_width="wrap_content"

 android:layout_height="wrap_content"

 android:layout_alignParentEnd="true"

 android:layout_alignParentBottom="true"

 android:layout_marginEnd="85dp"

 android:layout_marginBottom="566dp"

 android:ems="10"

 android:inputType="textPersonName"

 android:hint="Enter Number 1"

 android:text="" />

 <EditText

 android:id="@+id/number2"

 android:layout_width="wrap_content"

 android:layout_height="wrap_content"

 android:layout_alignParentEnd="true"

 android:layout_alignParentBottom="true"

 android:layout_marginEnd="88dp"

 android:layout_marginBottom="482dp"

 android:ems="10"

 android:hint="Enter Number 2"

 android:inputType="textPersonName"

 android:text="" />

 <TextView

 android:id="@+id/restv"

 android:layout_width="wrap_content"

 android:layout_height="wrap_content"

 android:layout_alignParentEnd="true"

 android:layout_alignParentBottom="true"

 android:layout_marginEnd="186dp"

 android:layout_marginBottom="421dp"

 android:text="0"

 android:textSize="30dp" />

 <Button

 android:id="@+id/button"

 android:layout_width="wrap_content"

 android:layout_height="wrap_content"

 android:layout_alignParentEnd="true"

 android:layout_alignParentBottom="true"
 android:layout_marginEnd="243dp"

 android:layout_marginBottom="339dp"

 android:onClick="performAdd"

 android:backgroundTint="@color/cardview_shadow_start_color"

 android:text="Add" />

 <Button

 android:id="@+id/button2"

 android:layout_width="wrap_content"

 android:layout_height="wrap_content"

 android:layout_alignParentEnd="true"

 android:layout_alignParentBottom="true"

 android:layout_marginEnd="68dp"

 android:layout_marginBottom="339dp"

 android:onClick="performSub"

 android:backgroundTint="@color/cardview_shadow_start_color"

 android:text="Sub" />

 <Button

 android:id="@+id/button3"

 android:layout_width="wrap_content"

 android:layout_height="wrap_content"

 android:layout_alignParentEnd="true"

 

 android:layout_alignParentBottom="true"

 android:layout_marginEnd="243dp"

 android:layout_marginBottom="217dp"

 android:onClick="performMul"

 android:backgroundTint="@color/cardview_shadow_start_color"

 android:text="Mul" />

 <Button

 android:id="@+id/button4"

 android:layout_width="wrap_content"

 android:layout_height="wrap_content"

 android:layout_alignParentEnd="true"

 android:layout_alignParentBottom="true"

 android:layout_marginEnd="60dp"

 android:layout_marginBottom="216dp"

 android:onClick="performDiv"

 android:backgroundTint="@color/cardview_shadow_start_color"

 android:text="Div" />









MainActivity.java

package edu.vemana;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.view.View;

import android.widget.EditText;

import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

 EditText ed1,ed2;

 TextView tv;

 @Override 
 protected void onCreate(Bundle savedInstanceState) {

 super.onCreate(savedInstanceState);

 setContentView(R.layout.activity_main);

 ed1 = (EditText) findViewById(R.id.number1);

 ed2 = (EditText) findViewById(R.id.number2);

 tv = (TextView) findViewById(R.id.restv);

 }

 public void performAdd(View v) {

 try

 {

 int n1 = Integer.parseInt(ed1.getText().toString());

 int n2 = Integer.parseInt(ed2.getText().toString());

 int res = n1 + n2;

 tv.setText(""+res);

 }

 catch (Exception e)

 {

 tv.setText("Error");

 }

 }

 public void performSub(View v) {

 try

 {

 int n1 = Integer.parseInt(ed1.getText().toString());

 int n2 = Integer.parseInt(ed2.getText().toString());

 int res = n1 - n2;

 tv.setText(""+res);

 }

 catch (Exception e)

 {

 tv.setText("Error");

 }

 }

 public void performMul(View v) {

 try

 {

 int n1 = Integer.parseInt(ed1.getText().toString());

 int n2 = Integer.parseInt(ed2.getText().toString());

 int res = n1 * n2;

 tv.setText(""+res);

 }

 catch (Exception e)

 {

 tv.setText("Error");

 }

 }

 public void performDiv(View v) {

 try

 {

 float n1 = Float.parseFloat(ed1.getText().toString());

 float n2 = Float.parseFloat(ed2.getText().toString());

 float res = n1 / n2;

 tv.setText(""+res);

 }

 catch (Exception e)

 {

 tv.setText("Error");
 }
 }
 }

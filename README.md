# Project Fibonacci

Nama            : Dhea Dwi Adelia

NIM             : 312210116

Kelas           : TI.22.A.1

Mata Kuliah     : Pemrograman Mobile 1

Dosen Pengampu  : Donny Maulana, S.Kom., M.Kom.

## Tugas

![image](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/da320da8-cb55-499d-b763-e39a6d5cb034)


### Langkah - Langkah

### 1. Langkah awal yaitu membuat project dengan nama __Project_Toast__.


### 2. Setelah itu, didalam layout terdapat __activity_main.xml__. Di __activity_main.xml__ kita beralih ke design lalu tambahkan dua button,satu plaintext dan satu textview. Button yang pertama, berfungsi sebagai tombol “Toast” yang posisinya berada diatas, yang nantinya ketika diklik akan muncul sebuah toast message yaitu “Bilangan Fibonacci”. Button yang kedua, berfungsi sebagai tombol “Count” yang posisinya berada dibawah, yang nantinya ketika diklik akan menghitung bilangan fibonaccinya.Plain Text berfungsi untuk mengedit angka maksimum bilangan Fibonacci. Dan yang terakhir adalah TextView, berfungsi untuk menampilkan angka atau bilangan fibonacci yang posisinya berada di tengah.

![image](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/5c8a38fa-496a-402c-8d28-3ebb5ade609d)


### Berikut adalah kodingannya: 

      <?xml version="1.0" encoding="utf-8"?>
      <androidx.constraintlayout.widget.ConstraintLayout
       xmlns:android="http://schemas.android.com/apk/res/android"
       xmlns:app="http://schemas.android.com/apk/res-auto"
       xmlns:tools="http://schemas.android.com/tools"
       android:layout_width="match_parent"
       android:layout_height="match_parent"
       tools:context=".MainActivity">
   
       <EditText
           android:id="@+id/edit_max_fibonacci"
           android:layout_width="190dp"
           android:layout_height="48dp"
           android:layout_marginEnd="8dp"
           android:layout_marginTop="8dp"
           android:hint="Maksimum Fibonacci"
           android:inputType="number"
           app:layout_constraintEnd_toEndOf="parent"
           app:layout_constraintTop_toTopOf="parent"
           tools:ignore="MissingTranslation"/>
   
       <Button
           android:id="@+id/button_toast"
           android:layout_width="190dp"
           android:layout_height="48dp"
           android:layout_marginStart="8dp"
           android:layout_marginTop="8dp"
           android:background="@color/colorPrimary"
           android:onClick="showToast"
           android:textColor="@android:color/white"
           android:text="@string/button_label_toast"
           app:layout_constraintStart_toStartOf="parent"
           app:layout_constraintTop_toTopOf="parent" />
   
   
       <Button
           android:id="@+id/button_count"
           android:layout_width="190dp"
           android:layout_height="48dp"
           android:layout_marginStart="8dp"
           android:layout_marginEnd="8dp"
           android:layout_marginBottom="8dp"
           android:background="@color/colorPrimary"
           android:onClick="countUp"
           android:text="@string/button_label_count"
           android:textColor="@android:color/white"
           app:layout_constraintBottom_toBottomOf="parent"
           app:layout_constraintEnd_toEndOf="parent"
           app:layout_constraintHorizontal_bias="0.0"
           app:layout_constraintStart_toStartOf="parent"
           tools:ignore="UsingOnClickInXml,VisualLintButtonSize" />
   
       <Button
           android:id="@+id/button_finish"
           android:layout_width="190dp"
           android:layout_height="48dp"
           android:layout_marginStart="8dp"
           android:layout_marginEnd="8dp"
           android:layout_marginBottom="8dp"
           android:background="@color/colorPrimary"
           android:onClick="back1"
           android:text="@string/button_label_finish"
           android:textColor="@android:color/white"
           app:layout_constraintBottom_toBottomOf="parent"
           app:layout_constraintEnd_toEndOf="parent"
           app:layout_constraintHorizontal_bias="1.0"
           app:layout_constraintStart_toStartOf="parent"
           tools:ignore="UsingOnClickInXml" />
   
       <TextView
           android:id="@+id/show_count"
           android:layout_width="0dp"
           android:layout_height="0dp"
           android:layout_marginStart="8dp"
           android:layout_marginTop="8dp"
           android:layout_marginEnd="8dp"
           android:layout_marginBottom="8dp"
           android:background="#FFFF00"
           android:gravity="center_vertical"
           android:text="@string/count_initial_value"
           android:textAlignment="center"
           android:textColor="@color/colorPrimary"
           android:textSize="160sp"
           android:textStyle="bold"
           app:layout_constraintBottom_toTopOf="@id/button_count"
           app:layout_constraintEnd_toEndOf="parent"
           app:layout_constraintStart_toStartOf="parent"
           app:layout_constraintTop_toBottomOf="@id/button_toast"
           tools:ignore="RtlCompat" />
   
   </androidx.constraintlayout.widget.ConstraintLayout>

![Screenshot (446)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/0b4d137c-ac07-4636-8c0e-f27a1cb8406a)

![Screenshot (447)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/b3f350b6-efb5-4ea2-a481-704f18407e47)

![Screenshot (448)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/ea87a0d7-5231-47e6-a3d8-4eabc14277b5)

![Screenshot (449)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/fed746d8-c188-4256-88e6-a2dd8404a3b7)

![Screenshot (450)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/9bee2ca4-768e-4043-ae5d-c366a1529d3a)



### 3. Selanjutnya, didalam values terdapat __string.xml__ dan __colors.xml__ yang isinya adalah sebagai berikut:

__- string.xml__
  
                  <resources>
                      <string name="app_name">Tugasenam</string>
                      <string name="button_label_toast">Toast</string>
                      <string name="button_label_count">Count</string>
                      <string name="count_initial_value">1</string>
                      <string name="toast_message">Bilangan Fibonacci</string>
                      <string name="button_label_finish">Reset</string>
                      <string name="enter_fibonacci_limit">Masukan Limit Angka</string>
                  </resources>
            
__- colors.xml__
  
            <?xml version="1.0" encoding="utf-8"?>
            <resources>
                <color name="black">#FF000000</color>
                <color name="white">#FFFFFFFF</color>
                <color name="colorPrimary">#3F5185</color>
                <color name="colorPrimaryDark">#303F9F</color>
                <color name="colorAccent">#FF4081</color>
            </resources>
    
![Screenshot (452)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/254de996-11c8-4ba1-a41b-33cae4512668)

![Screenshot (451)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/da69c556-3983-4731-a196-efbf0e6dfd38)



### 4. Di __MainActivity.java__ yaitu tempat kodingan rumus bilangan Fibonacci dan tombol – tombol yang ada di __activity_main.xml__

     package com.project_toast;

        import android.os.Bundle;
        import android.view.View;
        import android.widget.EditText;
        import android.widget.TextView;
        import android.widget.Toast;
        
        import androidx.appcompat.app.AppCompatActivity;
        
        public class MainActivity extends AppCompatActivity {
            private TextView showCount;
            private int count = 0;
            private long fibNMinus1 = 1;
            private long fibNMinus2 = 0;
            private EditText edit_max_fibonacci;
        
            @Override
            protected void onCreate(Bundle savedInstanceState) {
                super.onCreate(savedInstanceState);
                setContentView(R.layout.activity_main);
        
                showCount = findViewById(R.id.show_count);
                edit_max_fibonacci = findViewById(R.id.edit_max_fibonacci);
        
                updateCountDisplay();
        
                fibNMinus1 = 1;
                fibNMinus2 = 0;
            }
        
            private void updateCountDisplay() {
                showCount.setText(String.valueOf(fibNMinus1));
        
                if (count % 4 == 0) {
                    showCount.setTextColor(getResources().getColor(R.color.colorPrimary));
                } else if (count % 4 == 1) {
                    showCount.setTextColor(getResources().getColor(R.color.colorAccent));
                } else if (count % 4 == 2) {
                    showCount.setTextColor(getResources().getColor(R.color.colorPrimary));
                } else {
                    showCount.setTextColor(getResources().getColor(R.color.colorAccent));
                }
            }
        
            public void showToast(View view){
                Toast.makeText(this, "Bilangan Fibonacci",
                        Toast.LENGTH_SHORT).show();
            }
        
            public void countUp(View view) {
                int maxFibonacci = Integer.parseInt(edit_max_fibonacci.getText().toString());
        
                if (count >= maxFibonacci) {
                    Toast.makeText(this, "Maksimum Fibonacci tercapai", Toast.LENGTH_SHORT).show();
                    return;
                }
        
                long fibCurrent;
                if (count == 0 || count == 1) {
                    fibCurrent = 1;
                } else {
                    fibCurrent = fibNMinus1 + fibNMinus2;
                }
        
                fibNMinus2 = fibNMinus1;
                fibNMinus1 = fibCurrent;
                updateCountDisplay();
        
                count++;
            }
        
            public void back1(View view) {
                count = 0;
                fibNMinus1 = 1;
                fibNMinus2 = 0;
                updateCountDisplay();
            }
        }

![Screenshot (480)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/58627770-7efe-4111-b352-9a8f880aa23d)

![Screenshot (481)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/be3e0321-1dbe-4deb-8d4c-5a1da6039418)

![Screenshot (482)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/4912d5da-23ab-400d-ae91-a4b524bf064e)

![Screenshot (483)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/7b95cd6d-0e8e-4023-b5d2-852dac6b14ff)



### 5. Berikut ini adalah tampilan dari design setelah semua kodingan dimasukkan.

![Screenshot (458)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/c9bc959e-808c-4aff-9ec0-8bf5f6b602e6)


### 6. Ini adalah tampilan awal setelah di run.

![WhatsApp Image 2023-11-01 at 06 12 15](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/7f9a2783-c1ac-4f29-b961-203a1d6ea429)


### 6. Ketika tombol "Toast" ditekan, maka akan muncul message "Bilangan Fibonacci"

![WhatsApp Image 2023-11-01 at 06 12 15 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/2edf98e6-64a4-422b-84d2-a3900c87effc)


### 7. Dan jika tombol "Count" ditekan, maka angka "1" akan berubah menjadi bilangan Fibonacci, dan bilangan maksimum yang saya masukkan adalah "10"

![WhatsApp Image 2023-11-01 at 06 12 16](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/42ade83d-9015-4213-99f1-18c691b712ec)

![WhatsApp Image 2023-11-07 at 08 22 47](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/68fe533f-a8b0-469b-8c96-7154a76c4cf0)

![WhatsApp Image 2023-11-07 at 08 22 47 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/f8453054-6fbd-4f44-8533-df6e09a81c9c)

![WhatsApp Image 2023-11-07 at 08 22 47 (2)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/3f0275a5-73c2-4e0e-8b62-479204f719f7)

![WhatsApp Image 2023-11-07 at 08 22 48](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/1a34f90b-1263-4708-8ae1-63427729deb0)

![WhatsApp Image 2023-11-07 at 08 22 48 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/04ed57a2-8ceb-4aa8-8f06-ec93948e2093)

![WhatsApp Image 2023-11-07 at 08 22 48 (2)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/d3a7e8cb-f6d1-4113-962e-b91a11cbdd1a)

![WhatsApp Image 2023-11-07 at 08 22 48 (3)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/0b2da033-96ca-4a39-8cf4-0fb7e69c3c05)

![WhatsApp Image 2023-11-07 at 08 22 49](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/0e0fdcdb-86e4-4d18-8a56-7238fdf5dc59)

![WhatsApp Image 2023-11-07 at 08 22 49 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/dd3b7ff0-7203-4a66-959a-7dd4177476c5)



### Jika kita tekan lagi akan muncul message "Maksimum Fibonacci Tercapai"

![WhatsApp Image 2023-11-07 at 08 22 49 (2)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/d1025606-85df-4de9-831b-f1731d6e3436)


--------------------------------------

https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/4fd15bb8-d8e2-492d-9530-204ce4cbddc1


### Sekian, Terima Kasih.

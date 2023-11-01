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

![Screenshot (453)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/294ebc47-f556-44aa-be7e-af03fc3bd4c1)

![Screenshot (454)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/8687d719-f7e1-4237-af4e-bb7859b23d7e)

![Screenshot (455)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/1170c912-cff1-422c-ae10-189408edc0f4)

![Screenshot (456)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/fe6d8ba0-5543-4ad2-8971-6c74d6da7338)


### 5. Berikut ini adalah tampilan dari design setelah semua kodingan dimasukkan.

![Screenshot (458)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/c9bc959e-808c-4aff-9ec0-8bf5f6b602e6)


### 6. Ini adalah tampilan awal setelah di run.

![WhatsApp Image 2023-11-01 at 06 12 15](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/7f9a2783-c1ac-4f29-b961-203a1d6ea429)


### 6. Ketika tombol "Toast" ditekan, maka akan muncul message "Bilangan Fibonacci"

![WhatsApp Image 2023-11-01 at 06 12 15 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/2edf98e6-64a4-422b-84d2-a3900c87effc)


### 7. Dan jika tombol "Count" ditekan, maka angka "1" akan berubah menjadi bilangan Fibonacci, dan bilangan maksimum yang saya masukkan adalah "10"

![WhatsApp Image 2023-11-01 at 06 12 16](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/42ade83d-9015-4213-99f1-18c691b712ec)

![WhatsApp Image 2023-11-01 at 06 12 15 (2)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/18718a2d-6fad-4ba4-a22a-686cb5f996b6)

![WhatsApp Image 2023-11-01 at 06 12 16 (2)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/86145130-fa70-4e18-9e9c-a78a75fa84ba)

![WhatsApp Image 2023-11-01 at 06 12 16 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/aac5c2a6-fb98-4e6c-867a-59d8aab00d4d)

![WhatsApp Image 2023-11-01 at 06 12 15 (3)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/8ed4305c-222e-453d-b317-07047fa66d83)

![WhatsApp Image 2023-11-01 at 06 12 18](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/b8163cb7-77ca-442a-bd8a-c682a1961e0b)

![WhatsApp Image 2023-11-01 at 06 12 17 (2)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/0393c8af-4f87-4389-b29a-45a19ba1aaf1)

![WhatsApp Image 2023-11-01 at 06 12 17 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/b0eae8a0-0fb7-4c91-b341-c2da8242fe7d)

![WhatsApp Image 2023-11-01 at 06 12 17](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/71ce32e5-9a41-4c7a-9a52-d1cb463277a5)

![WhatsApp Image 2023-11-01 at 06 12 18 (2)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/1bae52e3-f9f4-4a4d-b1e9-6bd2216eb277)

### Jika kita tekan lagi akan muncul message "Maksimum Fibonacci Tercapai"

![WhatsApp Image 2023-11-01 at 06 12 18 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/a95006d9-9b4c-4d11-8dbc-131bf9d68fd8)

--------------------------------------


https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/bf0bb5fc-65ed-4293-9918-de066724ce4d


### Sekian, Terima Kasih.

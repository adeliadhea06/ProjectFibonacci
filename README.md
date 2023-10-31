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


### 2. Setelah itu, didalam layout terdapat __activity_main.xml__. Di __activity_main.xml__ kita beralih ke design lalu tambahkan dua button dan satu textview. Button yang pertama, berfungsi sebagai tombol “Toast” yang posisinya berada diatas, yang nantinya ketika diklik akan muncul sebuah toast message yaitu “Bilangan Fibonacci”. Button yang kedua, berfungsi sebagai tombol “Count” yang posisinya berada dibawah, yang nantinya ketika diklik akan menghitung bilangan fibonaccinya. Dan yang terakhir adalah TextView, berfungsi untuk menampilkan angka atau bilangan fibonacci yang posisinya berada di tengah.

![image](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/df9268de-8ae4-4e7a-9540-989c02e122fe)


### Berikut adalah kodingannya: 

      <?xml version="1.0" encoding="utf-8"?>
      <androidx.constraintlayout.widget.ConstraintLayout
          xmlns:android="http://schemas.android.com/apk/res/android"
          xmlns:android="http://schemas.android.com/apk/res/android"
          xmlns:app="http://schemas.android.com/apk/res-auto"
          xmlns:tools="http://schemas.android.com/tools"
          android:layout_width="match_parent"
          android:layout_height="match_parent"
          tools:context=".MainActivity">
      
          <Button
              android:id="@+id/button_toast"
              android:layout_width="0dp"
              android:layout_height="wrap_content"
              android:layout_marginEnd="8dp"
              android:layout_marginStart="8dp"
              android:layout_marginTop="8dp"
              android:background="@color/colorPrimary"
              android:onClick="showToast"
              android:textColor="@color/white"
              android:text="Toast"
              app:layout_constraintEnd_toEndOf="parent"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toTopOf="parent"
              tools:ignore="UsingOnClickInXml,VisualLintButtonSize"
              />
      
          <Button
              android:id="@+id/button_count"
              android:layout_width="0dp"
              android:layout_height="wrap_content"
              android:layout_marginEnd="8dp"
              android:layout_marginStart="8dp"
              android:layout_marginBottom="8dp"
              android:background="@color/colorPrimary"
              android:onClick="countUp"
              android:textColor="@color/white"
              android:text="Count"
              app:layout_constraintEnd_toEndOf="parent"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintBottom_toBottomOf="parent"
              tools:ignore="UsingOnClickInXml,VisualLintButtonSize" />
      
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
              android:text="1"
              android:textAlignment="center"
              android:textColor="@color/colorPrimary"
              android:textSize="160sp"
              android:textStyle="bold"
              app:layout_constraintBottom_toTopOf="@id/button_count"
              app:layout_constraintEnd_toEndOf="parent"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toBottomOf="@id/button_toast" />
      
      </androidx.constraintlayout.widget.ConstraintLayout>

![Screenshot (389)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/e2a22cb5-cbfa-45e2-8a1d-dadb9732557e)

![Screenshot (391)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/f15c3b9f-619d-4788-9d8a-192dae138758)

![Screenshot (438)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/af991aef-e385-470f-9e72-fe68f7a7d49c)


### 3. Selanjutnya, didalam values terdapat __string.xml__ dan __colors.xml__ yang isinya adalah sebagai berikut:

                <resources>
                    <string name="app_name">Tugas Enam</string>
                    <string name="button_label_toast">Toast</string>
                    <string name="button_label_count">Count</string>
                    <string name="count_initial_values">1</string>
                    <string name="toast_message">Bilangan Fibonacci</string>
                </resources>
            
            
                <?xml version="1.0" encoding="utf-8"?>
                <resources>
                    <color name="black">#FF000000</color>
                    <color name="white">#FFFFFFFF</color>
                    <color name="colorPrimary">#3F5185</color>
                    <color name="colorPrimaryDark">#303F9F</color>
                    <color name="colorAccent">#FF4081</color>
                </resources>
    

![Screenshot (440)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/74da34f3-e492-4c12-bc84-20225360fe27)

![image](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/dd9730a4-77ac-432f-9954-d3bb03b6e53b)


### 4. Di __MainActivity.java__ yaitu tempat kodingan rumus bilangan Fibonacci dan tombol – tombol yang ada di __activity_main.xml__

            package com.project_toast;
            
            import androidx.appcompat.app.AppCompatActivity;
            
            import android.os.Bundle;
            import android.view.View;
            import android.widget.TextView;
            import android.widget.Toast;
            
            public class MainActivity extends AppCompatActivity {
                private TextView showCount;
                private int count = 1;
                private long fibNMinus1 = 1;
                private long fibNMinus2 = 0;
            
                @Override
                protected void onCreate(Bundle savedInstanceState) {
                    super.onCreate(savedInstanceState);
                    setContentView(R.layout.activity_main);
            
                    showCount=findViewById(R.id.show_count);
                }
                public void showToast(View view){
                    Toast.makeText(this,"Bilangan Fibonacci", Toast.LENGTH_SHORT).show();
                }
                public void countUp(View view){
                    if(count == 1) {
                        showCount.setText("1");
                    } else {
                        long fibCurrent = fibNMinus1 + fibNMinus2;
                        fibNMinus2 = fibNMinus1;
                        fibNMinus1 = fibCurrent;
                        showCount.setText(String.valueOf(fibCurrent));
                    }
                    count++;
                }
            }

![Screenshot (442)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/73ca0735-59dd-4403-8290-6737ff922cc3)

![Screenshot (441)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/cedce592-2c33-4f1b-82b7-a4c0be4a37ff)


### 5. Berikut ini adalah tampilan dari design setelah semua kodingan dimasukkan.

![Screenshot (439)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/a1c75f06-7c97-4c95-a491-16d3e924f2ef)


### 6. Ketika tombol "Toast" ditekan, maka akan muncul message "Bilangan Fibonacci"

![WhatsApp Image 2023-10-31 at 16 41 44](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/0e6189b5-f2c0-453c-b4d3-1306141cc80d)


### 7. Dan jika tombol "Count" ditekan, maka angka "1" akan berubah menjadi bilangan Fibonacci

![WhatsApp Image 2023-10-30 at 16 32 29](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/f7eeac00-dd11-4f5c-9ab9-f8dc893f1fc0)

![WhatsApp Image 2023-10-30 at 16 32 28 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/409db16e-5cde-40c8-8228-5ee305227784)

![WhatsApp Image 2023-10-30 at 16 32 28 (3)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/76cec905-39af-45af-bfc4-c42aa572fc7a)

![WhatsApp Image 2023-10-30 at 16 32 28 (2)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/a667a83b-bdf0-45d4-814a-4409f6817afb)

![WhatsApp Image 2023-10-30 at 16 32 27](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/dcd88c5c-6cff-4868-abe4-0084572e4612)

![WhatsApp Image 2023-10-30 at 16 32 28 (4)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/bc83537e-cb57-4f02-bdee-6bcad7831f02)

![WhatsApp Image 2023-10-30 at 16 32 28](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/423bfbb3-148d-4dcd-a79a-be90970581dd)

![WhatsApp Image 2023-10-30 at 16 32 29 (2)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/cecf92e0-5ed1-4e1e-94c5-94b60488965f)

![WhatsApp Image 2023-10-30 at 16 32 29 (3)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/b5512d5e-efb7-4a32-9669-f84fbb0fe5d6)

![WhatsApp Image 2023-10-30 at 16 32 30 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/cf3345cc-ab32-4f1b-99f5-98c55ce583e6)

![WhatsApp Image 2023-10-30 at 16 32 29 (1)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/2ba9d94a-f5dc-42ff-a7bf-26558ed508bb)

![WhatsApp Image 2023-10-30 at 16 32 30](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/9135e2bd-67f8-422a-8e19-28234fedab3c)


### Sekian, Terima Kasih.

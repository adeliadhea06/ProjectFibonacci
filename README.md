# Project Fibonacci

Nama            : Dhea Dwi Adelia

NIM             : 312210116

Kelas           : TI.22.A.1

Mata Kuliah     : Pemrograman Mobile 1

Dosen Pengampu  : Donny Maulana, S.Kom., M.Kom.

### Tugas

![image](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/da320da8-cb55-499d-b763-e39a6d5cb034)


### Langkah - Langkah

1. Langkah awal yaitu membuat project dengan nama __Project_Toast__.


2. Setelah itu, didalam layout terdapat __activity_main.xml__. Di __activity_main.xml__ kita beralih ke design lalu tambahkan dua button dan satu textview. Button yang pertama, berfungsi sebagai tombol “Toast” yang posisinya berada diatas, yang nantinya ketika diklik akan muncul sebuah toast message yaitu “Bilangan Fibonacci”. Button yang kedua, berfungsi sebagai tombol “Count” yang posisinya berada dibawah, yang nantinya ketika diklik akan menghitung bilangan fibonaccinya. Dan yang terakhir adalah TextView, berfungsi untuk menampilkan angka atau bilangan fibonacci yang posisinya berada di tengah.

![image](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/df9268de-8ae4-4e7a-9540-989c02e122fe)


Berikut adalah kodingannya: 

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


3. Selanjutnya, didalam values terdapat __string.xml__ dan __colors.xml__ yang isinya adalah sebagai berikut:

    <resources>
        <string name="app_name">Tugas Enam</string>
        <string name="button_label_toast">Toast</string>
        <string name="button_label_count">Count</string>
        <string name="count_initial_values">1</string>
        <string name="toast_message">Bilangan Fibonacci</string>
    </resources>

![Screenshot (440)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/74da34f3-e492-4c12-bc84-20225360fe27)

    <?xml version="1.0" encoding="utf-8"?>
    <resources>
        <color name="black">#FF000000</color>
        <color name="white">#FFFFFFFF</color>
        <color name="colorPrimary">#3F5185</color>
        <color name="colorPrimaryDark">#303F9F</color>
        <color name="colorAccent">#FF4081</color>
    </resources>

![image](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/dd9730a4-77ac-432f-9954-d3bb03b6e53b)


4. Di __MainActivity.java__ yaitu tempat kodingan rumus bilangan Fibonacci dan tombol – tombol yang ada di __activity_main.xml__

![Screenshot (395)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/48bd0c40-5f22-4cfa-a25e-8b3dcba9dd47)

![Screenshot (437)](https://github.com/adeliadhea06/ProjectFibonacci/assets/115794875/ff4e6249-97b8-48a7-9a24-8119022478b7)


4. 

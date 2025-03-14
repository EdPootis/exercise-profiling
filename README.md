# Exercise Profiling
**Nama: Edmond Christian**<br>
**NPM: 2306208363**

# AdPro Module 5
## JMeter Screenshot Before Optimization
### /all-student endpoint
![Image](https://github.com/user-attachments/assets/1acb4e73-f2ab-4cf3-b2d7-5f39f887777b)
![Image](https://github.com/user-attachments/assets/35dfa1fa-d00b-4681-a7ae-d0b37536d1de)

### /all-student-name endpoint
![Image](https://github.com/user-attachments/assets/9dbbe858-c33a-4d40-bee6-c8bae07b5f94)
![Image](https://github.com/user-attachments/assets/7976af69-4b31-4a32-8727-d27fc4e7a9dd)

### /highest-gpa
![Image](https://github.com/user-attachments/assets/875b0fad-94f0-4310-8ae2-e45fb51e1525)
![Image](https://github.com/user-attachments/assets/c1f86178-b592-4bd4-907c-39ad25400216)

## JMeter Screenshot Before Optimization via Command Line
### /all-student endpoint
![Image](https://github.com/user-attachments/assets/3a2937ee-7726-4d79-b2c4-38a5f52944d3)
### /all-student-name endpoint
![Image](https://github.com/user-attachments/assets/31b762c7-e80e-4101-8b0a-1d0b488953ac)
### /highest-gpa
![Image](https://github.com/user-attachments/assets/5ee73cdf-2a96-406e-a734-e9d0d9928239)

## JMeter Screenshot After Optimization

### /all-student endpoint
![Image](https://github.com/user-attachments/assets/1a82d929-acea-4fe3-b9e4-e87f9b5f0ed8)
![Image](https://github.com/user-attachments/assets/ca0e9afe-54fa-4fd9-bdfb-a78832a4e668)

### /all-student-name endpoint
![Image](https://github.com/user-attachments/assets/57f8311d-cf94-4031-8b34-97f1cbcbe65b)
![Image](https://github.com/user-attachments/assets/2b5d9b8a-6a25-4969-8ff1-eba77b4118e8)

### /highest-gpa endpoint
![Image](https://github.com/user-attachments/assets/cc7f4d0e-9842-4332-a6e4-b355e80b25fd)
![Image](https://github.com/user-attachments/assets/4fc18174-8874-4d6a-ae61-fadc64a7ab41)

## JMeter Screenshot Before Optimization via Command Line
### /all-student endpoint
![Image](https://github.com/user-attachments/assets/b063ba0e-f892-4fd7-a380-3a8188b1174d)

### /all-student-name endpoint
![Image](https://github.com/user-attachments/assets/0b7cb27d-16bd-4941-871e-3265b00df262)

### /highest-gpa
![Image](https://github.com/user-attachments/assets/420dddeb-b8f2-4ced-928e-e1a73fcd6b7c)

## Perbandingan
### /all-student endpoint
**Sebelum Optimisasi**, hasil tes menunjukkan *latency* dengan rata-rata 68rb ms dibandingkan dengan **setelahnya**, hasil tes menunjukkan *latency* dengan rata-rata 4,2rb ms sehingga terjadi *improvement* performa sebesar 93,8%.


### /all-student-name endpoint
**Sebelum Optimisasi**, hasil tes menunjukkan *latency* dengan rata-rata 3rb ms dibandingkan dengan **setelahnya**, hasil tes menunjukkan *latency* dengan rata-rata 73 ms sehingga terjadi *improvement* performa sebesar 97,6%.

### /highest-gpa
**Sebelum Optimisasi**, hasil tes menunjukkan *latency* dengan rata-rata 177 ms dibandingkan dengan **setelahnya**, hasil tes menunjukkan *latency* dengan rata-rata 85 ms sehingga terjadi *improvement* performa sebesar 48%.

## Kesimpulan
Berdasarkan perbandingan setiap *endpoint* aplikasi terdapat penurunan *latency* di setiap *endpoint* yang lebih besar 20%. Hal ini disebabkan *profiling* dan *optimization* yang dilakukan dengan efektif.

## Refleksi

1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?
- Perbedaan utama dari *testing* menggunakan JMeter dan Intellij Profiler adalah JMeter melakukan *testing* dengan perspektif luar server/eksternal untuk mengsimulasi penggunaan oleh pengguna atau *load* agar dapat mengukur *response time*, *throughput*, dan performa sistem secara keseluruhan. Sementara Intellij Profiler melakukan *testing* dari dalam aplikasi untuk mengetahui performa kode secara internal agar mengetahui hal-hal seperti *CPU time*, alokasi memori, dan eksekusi *method*.

2. How does the profiling process help you in identifying and understanding the weak points in your application?
- Proses profiling membantu mengidentifikasi *weak points* dalam aplikasi dengan menunjukkan info mengenai bagian kode seperti *method* atau algoritma yang memakan banyak waktu/*CPU time*. Dengan hasil *profiling*, saya dapat mengoptimisasi kode yang merupakan *weak point*. Selain itu ada juga info mengenai performa memori yang di dalam aplikasi ini tidak terlalu diperhatikan.

3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?
- Ya, melalui *profiling* saya dapat menganalisis bahwa pada ketiga endpoint `/all-student`, `/all-student-name`, dan `/highest-gpa` masing-masing memiliki *bottleneck* pada *method* `getAllStudentsWithCourses()`, `joinStudentNames()`, dan `findStudentWithHighestGpa()`. Dengan mengidentifikasi *bottlenecks* tersebut, saya dapat memfokuskan optimisasi pada *method*-*method* tersebut.

4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?
- Tantangan utama dalam menghadapi *performance testing* dan *profiling* adalah menentukan data yang penting untuk diperhatikan, contohnya pada *profiling* melalui Intelij Profiler terdapat berbagai info selain mengenai *method* kita sendiri. Selain itu, kita harus menentukan apa yang dapat dioptimasi dari hasil *testing* dan *profiling* tersebut yang jika kita tidak memahami kode sendiri maka akan menjadi susah.

5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?
- *Benefit* utama yang didapatkan adalah mengetahui kinerja aplikasi Java langsung melalui IDE Intellij tanpa menginstall *dependency*/*add on* lainnya. Dengan Intellij Profiler saya dapat melakukan *profiling* aplikasi saya yang tentunya berguna dalam menganalis kinerja aplikasi.

6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?
- Pada latihan ini saya belum menemukan situasi ini. Namun jika hal ini terjadi saya akan mencari tahu mengapa hasil dari *profiling* Intellij Profiler dan *performance testing* JMeter berbeda. Alasan utama biasanya karena perbedaan *environment* aplikasi berjalan, seperti *load*, latensi jaringan, atau pengaturan sistem. Setelah mengetahui alasannya saya akan mencari solusi, contohnya jika dikarenakan perbedaan pengaturan sistem maka akan disamakan sebisa mungkin.

7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?
- Strategi yang saya akan implementasikan dalam mengoptimisasi kode adalah untuk melihat bagian method/algoritma yang paling banyak memakan waktu. Saya memastikan perubahan tidak akan mengubah fungsionalitas dengan membuat unit test untuk bagian kode yang saya ubah.


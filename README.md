## Tutorial 11 - Deployment on Kubernetes
Nama: Syifa Kaffa Billah

NPM: 2206816430

Kelas: C


### Reflection on Hello Minikube

1. **Compare the application logs before and after you exposed it as a Service. Try to open the app several times while the proxy into the Service is running. What do you see in the logs? Does the number of logs increase each time you open the app?**

    ![alt text](img/logs.png)

    Ya, terdapat perbedaan sebelum dan sesudah servicenya di exposed. Setelah di exposed, service menjadi bisa menerima request sehingga log akan mencatat permintaan yang telah dilakukan, misalnya seperti yang tertera pada gambar yang mana service mengirim requst /GET berkali kali jika di-refresh berkali-kali terhadap layanan hello-node.

2. **Notice that there are two versions of `kubectl get` invocation during this tutorial section. The first does not have any option, while the latter has `-n` option with value set to `kube-system`. What is the purpose of the `-n` option and why did the output not list the pods/services that you explicitly created?**

    Perbedaan antara kedua sintaks tersebut adalah dengan menggunakan `-n`, kita menyatakan bahwa service yang kita inginkan berasal dari namespace. Ini diperlukan misalnya jika ada banyak service yang berbeda yang memiliki nama yang sama dan tersebar di banyak namespace. Dengan menggunakan `-n`, kita memfokuskan GET pada namespace yang kita berikan setelah query `-n`.
​		Metode numerik adalah solusi untuk memecahkan masalah matematika yang sulit atau bahkan tidak dapat terselesaikan menggunakan program paket. Metode numerik menjadi sarana yang efektif dan efisien untuk mempelajari penggunaan komputer. Metode numerik juga menjadi sarana untuk lebih memahami matematika.

​		Metode numerik mengalami kemajuan yang cepat karena perkembangan dari komputer itu sendiri. salah satu permasalahan yang dipecahkan menggunakan meyode numerik adalah integrasi numerik. Integrasi numerik adalah salah satu cara untuk mendapatkan sebuah jawaban aproksimasi (hampiran/mendekati) dari sebuah pengintegralan yang dapat diselesaikan secara analitik. Integrasi numerik juga digunakan untuk menghitung luas daerah dan voume benda putar.

​		Ada beberapa metode integrasi numerik yang dapat digunakan untuk menyelesaikan permasalahan matematika diantaranya : metode integrasi reiman, metode integrasi trapezoid dan metode integrasi trapezium. Salah satu contoh penggunaan metode integrasi numerik yaitu metode integrasi trapezoid dengan rumus :

​             			
$$
L_i=1/2 ((x_i )+f(x_(i+1) )).∆x_i
$$
​																	atau
$$
L_i=1/2 (f_i+f_(i+1) ).∆x_i
$$

$$
L= ∑_(i=0)^(n-1)▒L_i 
$$

$$
L_i=∑_(i=0)^(n-1)▒〖1/2 h(f_i 〗+f_(i+1))=h/2(f_0+2f_1+2f_2+⋯+2f_(n=1)+f_n)
$$

$$
L=h/2(f_0+2∑_(i=1)^(n-1)▒〖f_i+ f_n)〗
$$

Dengan algoritma : 

a.  Mendefinisikan y=f(x)

b.  Menghitung h, dimana h dapat diperoleh dari hasil batas atas (b) dikurangi batas bawah (a) dan dibagi  		dengan n.

c.  Mengitung 
$$
	L=h/2 (f_0+2∑_(i=1)^(n-1)▒〖f_i+f_n 〗)
$$


contoh soal:

$$
∫_2^5▒〖x^2  exp⁡(-x)dx〗
$$
jawaban :

```
import numpy as np

def func(x):
    return (x**2)*np.exp(-x)

a = 2.0
b = 5.0
n = 50

dx = (b-a)/(n-1)
x = np.linspace(a,b,n)

sum = 0.0
for i in range(1,n-1):
    sum += func(x[i])
    
hasil = 0.5*dx*(func(x[0])+2.0*sum+func(x[-1]))

print(hasil)
```

```
1.104017227842602
```

 


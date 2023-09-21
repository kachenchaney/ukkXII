# TACP-UKL-12CC

---

## Installation
```
git clone https://github.com/OmTegar/TACP-UKK-12CC.git
cd TACP-UKK-12CC/
sudo chmod +x index.sh
sudo ./index.sh
tacp
```


## Description

---
### membuat vpc yang pertama
0. pilih vpc and more  
  
  ![Screenshot 2023-09-21 163937](https://github.com/kachenchaney/ukkXII/assets/111231552/97371baa-f9d3-41d5-ad5a-5173979d05fe)

1. IP di isi seusuai soal (IP bisa berganti saat dilaksanakan nya UKK) untuk menggunakan IP di soal yang lama
2. AZ 2
3. public 2  
4. private 2
5. klik customize subnet dan hitung IP sesuai untuk UKK (jika di keterangan soal harus di hitung berapa IP yang harus di gunakan)
6. nat gateway 1 az
7. endpoint s3
8. create
   
  ![Screenshot 2023-09-21 164006](https://github.com/kachenchaney/ukkXII/assets/111231552/b3118ee7-645f-4f82-bcd9-d48c9517cabb)


### buat VPC yg kedua

  ![Screenshot 2023-09-21 164322](https://github.com/kachenchaney/ukkXII/assets/111231552/820ea839-0e54-4d75-ba77-96a970b00a47)


1.	pilih vpc and more
2.	kasih nama sesuai soal
3.	ipv4 cidr isi ip sesuai soal (192.168.0.0/24 )
4.	AZ 1
5.	public 0
6.	privete1
7.	nat gateway none
8.	endpoint none
9.	create


  ![Screenshot 2023-09-21 164351](https://github.com/kachenchaney/ukkXII/assets/111231552/13fdf8e6-da6f-46f4-9cc5-dc577fc22ec7)


### PEERRING CONNECION


  ![Screenshot 2023-09-21 164604](https://github.com/kachenchaney/ukkXII/assets/111231552/bc92fe4b-60b9-4937-80dd-3456dd10c1ff)


1.	kasih nama sesuai soal 
2.	req vpc 1
3.	acc vpc 2
4.	name tag “Name” Tag “nama peering”
5.	klik pcx.. 
6.	action accept req

  
  ![Screenshot 2023-09-21 164715](https://github.com/kachenchaney/ukkXII/assets/111231552/a626afd2-ecb6-4ebc-9361-7a9e31fa38a8)


### ROUTE TABLES 1

1.	cari vpc 1 yang private
2.	klik route
3.	klik edit
4.	add route (masukin ip vpc 2 dan pilih peering connection)


  ![Screenshot 2023-09-21 164741](https://github.com/kachenchaney/ukkXII/assets/111231552/07ba3bd2-7522-4760-b76e-c9320bf954ab)


### ROUTE TABLES 2

1.	cari vpc 2 yang private
2.	klik route
3.	klik edit
4.	add route (masukin ip vpc 1 dan pilih peering connection)


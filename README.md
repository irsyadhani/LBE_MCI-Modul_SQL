# LBE-MCI_Modul-SQL
Modul LBE MCI 2020: CREATE, UPDATE, DELETE dan SELECT syntax SQL dengan PHPMyadmin

## Tools
XAMPP: https://drive.google.com/file/d/1ewCJt1R5lFN8fOz2kmAdByibmZcECip1/view?usp=sharing

#### Cara Run XAMPP:
- Klik Start bagian Apache dan MySQL
- Klik Admin pada bagian MySQL

![alt text](/gambar/run_xampp.jpg)

----------------------------------------------------------------
## Tentang SQL
Singkatan dari Structured Query Language, dalam bahasa inggris dibaca SEQUEL. Bahasa query standar yang digunakan untuk mengakses basis data relasional.

## Jenis-jenis perintah SQL:
#### Data Definition Language (DDL)
Jenis perintah dasar dari bahasa SQL. Perintahnya terdiri dari:

```Create``` Sebuah perintah yang bisa kamu gunakan ketika membuat sebuah database yang baru, baik itu berupa tabel baru atau sebuah kolom baru. Kamu bisa membuat sebuah query dengan contoh ‘CREATE DATABASE nama_database.

```Alter``` Mengubah struktur tabel yang sebelumnya sudah ada. Bisa jadi dalam hal ini adalah seperti nama tabel, penambahan kolom, mengubah, maupun menghapus kolom serta menambahkan atribut lainnya.

```Rename``` Mengubah sebuah nama di sebuah tabel ataupun kolom yang ada. Bila kamu menggunakan perintah ini maka query-nya menjadi ‘‘RENAME TABLE nama_tabel_lama TO nama_tabel_baru”.

```Drop``` Menghapus baik itu berupa database, table maupun kolom hingga index.

```Show``` Menampilkan sebuah tabel yang ada.

#### Data Manipulation Language (DML)
Perintah dasar SQL ini bertujuan untuk memanipulasi data yang ada dalam sebuah database. Perintahnya terdiri dari:

```Insert``` Memasukkan sebuah record baru di dalam sebuah tabel database.

```Select``` Menggunakannya dalam menampilkan maupun mengambil sebuah data pada tabel. Data yang diambil pun tidak hanya terbatas pada satu jenis saja melainkan lebih dari satu tabel dengan memakai relasi.

```Update``` Melakukan pembaruan data di sebuah tabel. Contohnya saja jika ada kesalahan ketika memasukkan sebuah record. Kamu tidak perlu menghapusnya dan bisa diperbaiki menggunakan perintah ini.

```Delete``` Menghapus sebuah record yang ada dalam sebuah tabel.

#### Data Control Language (DCL)
Perintah SQL ini digunakan khususnya untuk mengatur hak apa saja yang dimiliki oleh pengguna. Baik itu hak terhadap sebuah database ataupun pada tabel maupun field yang ada.  Perintahnya terdiri dari:

```Grant``` Biasanya digunakan ketika admin database ingin memberikan hak akses ke user lainnya. Tentu pemberian hak akses ini dapat dibatasi atau diatur. Dalam hal ini admin pun dapat memberikan akses mengenai perintah dalam DML di atas.

```Revoke``` Kebalikannya dari Grant, Revoke terkadang sering digunakan untuk mencabut maupun menghapus hak akses seorang pengguna yang awalnya diberikan akses oleh admin database melalui perintah Grant sebelumnya.

## Fungsi SQL:
SQL dapat memungkinkan kamu untuk mengakses maupun mengubah database. Kamu pun bisa menjalankan sebuah query maupun mengambil data yang dibutuhkan. Termasuk pula memperbarui atau menyisipkan data dalam database.

----------------------------------------------------------------
## Praktik Perintah SQL:
#### CREATE DATABASE

Syntax:

```CREATE DATABASE <nama database>;```

Contoh:
```
CREATE DATABASE akademik;
```
Gambar:

![alt text](/gambar/sql1.jpg)
----------------------------------------------------------------
#### CREATE TABLE

Syntax:

```CREATE TABLE <namatable> (<nama column> <tipe data> [aturan]);```

Contoh:
```
CREATE TABLE dept(
deptno CHAR(5),
dname VARCHAR(14),
loc VARCHAR(13),
PRIMARY KEY (deptno)
);
```
Gambar:

![alt text](/gambar/sql2.jpg)
----------------------------------------------------------------
#### DROP DATABSE

Syntax:

```DROP DATABASE <nama database>;```

Contoh:
```
DROP DATABASE akademik;
```
Gambar:

![alt text](/gambar/sql3.jpg)
----------------------------------------------------------------
#### DROP TABLE

Syntax:

```DROP TABLE <namaTabel>;```

Contoh:
```
DROP TABLE dept;
```
Gambar:

![alt text](/gambar/sql4.jpg)
----------------------------------------------------------------
#### INSERT DATA

Syntax:

```INSERT INTO tablename(field1, field2, field3,…) VALUES( val1, val2, val3, …..);```

Contoh:
```
INSERT INTO dept VALUES ('001', 'T. Informatika', 'Teknik Kimia');
```
Gambar:

![alt text](/gambar/sql5.jpg)
----------------------------------------------------------------
#### UPDATE DATA

Syntax:

```UPDATE nama_tabel SET nama_kolom =  value [WHERE syarat];```

Contoh:
```
UPDATE dept SET loc = 'Kimia' WHERE deptno = '001';
```
Gambar:

![alt text](/gambar/sql6.jpg)
----------------------------------------------------------------
#### DELETE DATA

Syntax:

```DELETE FROM nama_tabel [WHERE syarat];```

Contoh:
```
DELETE FROM dept WHERE deptno = '001';
```
Gambar:

![alt text](/gambar/sql7.jpg)
----------------------------------------------------------------
#### SELECT DATA

Syntax:

```
SELECT column 
FROM table 
WHERE column operator value 
;
```

Contoh:
```
SELECT deptno, dname, loc FROM dept
WHERE loc = 'Jl. Bambu';
```
Gambar:

![alt text](/gambar/sql8.jpg)

Sumber:
- https://www.w3schools.com/sql
- https://www.dewaweb.com/blog/sql-pengertian-fungsi-beserta-perintah-dasarnya/

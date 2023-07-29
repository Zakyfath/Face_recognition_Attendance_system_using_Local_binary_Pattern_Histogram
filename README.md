# Face_recognition_Attendance_system
## Instalasi
- Install libary yang dibutuhkan pada Virtual Environment python dengan mengetik :
```sh
pip install -r requirements.txt
```
- Buka [xampp](https://www.apachefriends.org/download.html) lalu buka PHPMyadmmin
- Buat querry sebagai berikut :
```sh
CREATE DATABASE db_mahasiswa
CREATE TABLE `img_dataset` (
  `img_id` int(11) NOT NULL,
  `img_person` varchar(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
 
CREATE TABLE `data_mahasiswa` (
  `NIM` varchar(11) NOT NULL,
  `Nama` varchar(50) NOT NULL,
  `prs_added` datetime NOT NULL DEFAULT CURRENT_TIMESTAMP
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
 
ALTER TABLE `img_dataset`
  ADD PRIMARY KEY (`img_id`);
 
ALTER TABLE `data_mahasiswa`
  ADD PRIMARY KEY (`NIM`);

CREATE TABLE `data_kehadiran` (
  `No` int(11) NOT NULL AUTO_INCREMENT,
  `Tanggal` date NOT NULL,
  `NIM` varchar(11) NOT NULL,
  `Waktu_hadir` datetime NOT NULL DEFAULT CURRENT_TIMESTAMP,
  PRIMARY KEY (`No`),
  KEY `Tanggal` (`Tanggal`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```
- Buka program app.py
- Run program 
## Source
- https://triyonos.com/pycharm-flask-opencv-face-recognition-registration-menggunakan-database-mysql

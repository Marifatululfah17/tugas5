# tugas5

tugas pemrograman 05

flowchart


![image](https://user-images.githubusercontent.com/56728542/71552644-0d2c1180-29b6-11ea-9b36-97e89d66d00c.png)

syntaxs:

data = {}

print("Program Input Nilai")

print("===================")

while True:

    d = input("(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar : ")
    
    if d.lower() == 't':
    
        print("Tambah Data")
        
        nama = input("Nama : ")
        
        NIM = input("NIM : ")
        
        tugas = int(input("Nilai Tugas : "))
        
        uts = int(input("Nilai UTS : "))
        
        uas = int(input("Nilai UAS : "))
        
        a = int(tugas * 30 / 100)
        b = int(uts * 35 / 100)
        c = int(uas * 35 / 100)
        akhir = a + b + c
        data[nama] = [nama, NIM, tugas, uts, uas, akhir]
        
        print(data)
        
    elif d.lower() == 'l':
    
        print("Lihat nilai")
        
        print("===================================================================================")
        print("| No. |     Nama     |      NIM     |   Tugas   |   UTS   |   UAS   |    Akhir    |")
        print("===================================================================================")
        
        no = 1
        
        if data.keys():
        
            for x in data.values():
            
                print("|  {:2} |  {nama:10}  |  {NIM:10}  |   {tugas:5}   |   {uts:3}   |   {uas:3}   |    {akhir:3.2f}    |".format(no, nama=x[0], NIM=x[1], tugas=x[2], uts=x[3], uas=x[4], akhir=x[5]))
                no += 1
                
        else:
            print("|                                  TIDAK ADA DATA                                 |")
        print("===================================================================================")
    elif d.lower() == 'k':
        break
    elif d.lower() == 'h':
        print("Hapus data")
        nama = input("Nama : ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Data nilai untuk anak yang bernama {0} tidak ada".format(nama))
    elif d.lower() == 'u':
        print("Ubah data")
        nama = input("Nama : ")
        if nama in data.keys():
            NIM = input("NIM : ")
            tugas = int(input("Nilai Tugas : "))
            uts = int(input("Nilai UTS : "))
            uas = int(input("Nilai UAS : "))
            data[nama][1] = NIM
            data[nama][2] = tugas
            data[nama][3] = uts
            data[nama][4] = uas
        else:
            print("Data nilai untuk anak yang bernama {0} tidak ada". format(nama))
    elif d.lower() == 'c':
        print("Cari data")
        nama = input("Nama : ")
        if nama in data.keys():
           print("=============================================================================")
           print("|     Nama     |      NIM     |   Tugas   |   UTS   |   UAS   |    Akhir    |")
           print("=============================================================================")
           print("|  {nama:10}  |  {NIM:10}  |   {tugas:5}   |   {uts:3}   |   {uas:3}   |    {akhir:3.2f}    |".format(nama=data[nama][0],
NIM=data[nama][1],tugas=data[nama][2], uts=data[nama][3], uas=data[nama][4], akhir=data[nama][5]))
           print("=============================================================================")
        else:
        
        
        
output:

![image](https://user-images.githubusercontent.com/56728542/71552683-59775180-29b6-11ea-8265-84d4704ed0bb.png)

![image](https://user-images.githubusercontent.com/56728542/71552693-7744b680-29b6-11ea-9479-06f5de642908.png)

![image](https://user-images.githubusercontent.com/56728542/71552704-8f1c3a80-29b6-11ea-9927-5d21aef713c0.png)


penjelasan:


Ketika program di jalakan akan muncul input pilihan yang mana ada ( Lihat, Tambah, Ubah, Hapus, Cari, Keluar) dengan kata kunci memasukkan awal huruf.
•	Lihat = jika data masih kosong dengan len(data)=0, selain itu maka tampilkan data.
•	Tambah = User input nama, nim, nilai tugas, uts, uas, lalu proses nilai akhir (uts*.30+uas*.35+uas*.35). Setelah itu nomor+=1 akan menjadi key dari dictionary data.
•	Ubah = Output Data, lalu user di minta untuk input sesuai nomor yang ingin di ubah. Jika yang di input sesuai maka user input nama, nim, nilai, tugas, uts, uas lalu proses nilai akhir. Jika yang di input tidak sesuai maka user di minta input kembali.
•	Hapus = Output Data, lalu user di minta untuk input sesuai nomor yang di hapus. Jika yang di input sesuai maka data akan di hapus sesuai nomor yang di input. Jika tidak sesuai maka user di minta untuk input kembali.
•	Cari = user di minta untuk memasukkan NIM, jika nim tidak sesuai maka user diminta masukkan kembali. Jika nim sesuai maka akan memunculkan data sesuai nim yang di input.
•	Keluar = Break ( Selesai )




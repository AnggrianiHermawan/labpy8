# labpy8

SOAL:
Tugas Praktikum
Buat program sederhana dengan mengaplikasikan penggunaan class. Buatlah
class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan:
• Method tambah() untuk menambah data
• Method tampilkan() untuk menampilkan data
• Method hapus(nama) untuk menghapus data berdasarkan nama
• Method ubah(nama) untuk mengubah data berdasarkan nama
• Buat diagram class, flowchart dan penjelasan programnya pada
  README.md.
• Commit dan push repository ke github.

KODE PYTHON:

    class DaftarNilaiMahasiswa:
    def __init__(self):  
        self.mahasiswa = {}

    def tambah(self, nama, nilai):
        """Menambah data mahasiswa."""
        self.mahasiswa[nama] = nilai
        print(f"Data {nama} dengan nilai {nilai} berhasil ditambahkan.")

    def tampilkan(self):
        """Menampilkan semua data mahasiswa."""
        if not self.mahasiswa:
            print("Tidak ada data mahasiswa.")
        else:
            print("Daftar Nilai Mahasiswa:")
            for nama, nilai in self.mahasiswa.items():
                print(f"Nama: {nama}, Nilai: {nilai}")

    def hapus(self, nama):
        """Menghapus data mahasiswa berdasarkan nama."""
        if nama in self.mahasiswa:
            del self.mahasiswa[nama]
            print(f"Data {nama} berhasil dihapus.")
        else:
            print(f"Data {nama} tidak ditemukan.")

    def ubah(self, nama, nilai_baru): 
        """Mengubah data mahasiswa berdasarkan nama."""
        if nama in self.mahasiswa:
            self.mahasiswa[nama] = nilai_baru
            print(f"Data {nama} berhasil diubah menjadi nilai {nilai_baru}.")
        else:
            print(f"Data {nama} tidak ditemukan.")

    def main():
    daftar = DaftarNilaiMahasiswa()

    while True:
        print("\nMenu:")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")

        pilihan = input("Pilih menu: ")

        if pilihan == '1':
            nama = input("Masukkan nama mahasiswa: ")
            try:
                nilai = int(input("Masukkan nilai mahasiswa: "))
                daftar.tambah(nama, nilai)
            except ValueError:
                print("Nilai harus berupa angka.")
        elif pilihan == '2':
            daftar.tampilkan()
        elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            daftar.hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            try:
                nilai_baru = int(input("Masukkan nilai baru: "))
                daftar.ubah(nama, nilai_baru)
            except ValueError:
                print("Nilai harus berupa angka.")
        elif pilihan == '5':
            print("Keluar dari program.")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")

    if __name__ == "__main__":
    main()

Input

<img width="665" alt="Cuplikan layar 2024-12-05 154540" src="https://github.com/user-attachments/assets/ee98727d-d496-4c7a-82dd-8e45a7679e8b">
<img width="677" alt="Cuplikan layar 2024-12-05 154604" src="https://github.com/user-attachments/assets/e1219a87-1b2a-4bef-9c84-3009b02c32d9">
<img width="656" alt="Cuplikan layar 2024-12-05 154623" src="https://github.com/user-attachments/assets/fc90d250-179c-40a7-a680-a88463dee4f7">

Output

<img width="371" alt="Cuplikan layar 2024-12-05 154641" src="https://github.com/user-attachments/assets/8bbf9408-756b-4b44-b5d1-3ffa580d6f2a">
<img width="370" alt="Cuplikan layar 2024-12-05 154701" src="https://github.com/user-attachments/assets/bbc9190a-27e8-423d-9a73-4b127c66c505">
<img width="356" alt="Cuplikan layar 2024-12-05 154722" src="https://github.com/user-attachments/assets/515e5030-f3d8-4be1-8369-9c102a5e5eb8">


PENJELASAN:
1. Tambah Data: Menyimpan nama dan nilai mahasiswa ke dalam dictionary.
2. Tampilkan Data: Menampilkan semua data mahasiswa dalam format daftar.
3. Hapus Data: Menghapus data mahasiswa berdasarkan nama berdasarkan nama.
4. Ubah Data: Mengupdate nilai mahasiswa berdasarkan nama.
Program menyediakan menu interaktif berbasis teks untuk pengguna, berjalan dalam loop hingga memilih opsi Keluar.

FLOWCHART:
![flowchart ](https://github.com/user-attachments/assets/19163506-2345-482f-8610-5edb02273672)

DIAGRAM CLASS:

![DIAGRAM CLASS](https://github.com/user-attachments/assets/ceed10d6-ae5c-4244-a499-2c599557ee52)

PENJELASAN DIAGRAM CLASS:
Atribut:
mahasiswa: Dictionary untuk menyimpan data mahasiswa (nama sebagai key, nilai sebagai value).
Metode:
1. _init_(): Menginisialisasi atribut mahasiswa sebagai dictionary kosong.
2. tambah(nama, nilai): Menambahkan data mahasiswa.
3. tampilkan(): Menampilkan semua data mahasiswa.
4. hapus(nama): Menghapus data berdasarkan nama.
5. ubah(nama, nilai_baru): Memperbarui nilai mahasiswa.


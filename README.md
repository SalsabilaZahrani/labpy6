# labpy6

# Latihan

    import math

    # Menggunakan lambda untuk mendefinisikan fungsi
    a = lambda x: x**2
    b = lambda x, y: math.sqrt(x*2 + y*2)
    c = lambda *args: sum(args) / len(args)
    d = lambda s: "".join(set(s))

    if _name_ == "_main_":

    print("a(5):", a(5))

    print("b(3, 4):", b(3, 4))

    print("c(1, 2, 3, 4, 5):", c(1, 2, 3, 4, 5))

    print("d('hello world'):", d('hello world'))

INPUT
![Cuplikan layar 2024-11-28 184533](https://github.com/user-attachments/assets/2862a9a0-771d-4a70-8b61-335ab409b13f)

OUTPUT
![Cuplikan layar 2024-11-28 184640](https://github.com/user-attachments/assets/d5f23a41-227c-48b7-8bd8-4b7b4e2d73bd)

# Praktikum 6

    # Daftar untuk menyimpan data mahasiswa
    data_mahasiswa = []

    # Fungsi untuk menambah data mahasiswa
    def tambah():
    nama = input("Masukkan nama mahasiswa: ")
    nim = input("Masukkan NIM: ")
    nilai = float(input("Masukkan nilai: "))
    data_mahasiswa.append({"nama": nama, "nim": nim, "nilai": nilai})
    print("Data berhasil ditambahkan.")

    # Fungsi untuk menampilkan data mahasiswa
    def tampilkan():
    if not data_mahasiswa:
        print("Tidak ada data mahasiswa.")
    else:
        print("Daftar Data Mahasiswa:")
        for i, mahasiswa in enumerate(data_mahasiswa, start=1):
            print(f"{i}. Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")

    # Fungsi untuk menghapus data mahasiswa berdasarkan nama
    def hapus(nama):
    for mahasiswa in data_mahasiswa:
        if mahasiswa['nama'].lower() == nama.lower():
            data_mahasiswa.remove(mahasiswa)
            print(f"Data mahasiswa dengan nama {nama} berhasil dihapus.")
            return
    print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")

    # Fungsi untuk mengubah data mahasiswa berdasarkan nama
    def ubah(nama):
    for mahasiswa in data_mahasiswa:
        if mahasiswa['nama'].lower() == nama.lower():
            print(f"Data lama: Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")
            mahasiswa['nama'] = input("Masukkan nama baru: ")
            mahasiswa['nim'] = input("Masukkan NIM baru: ")
            mahasiswa['nilai'] = float(input("Masukkan nilai baru: "))
            print("Data berhasil diubah.")
            return
    print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")

    # Menu utama
    def menu():
    while True:
        print("\nMenu:")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")
        pilihan = input("Pilih menu (1-5): ")

        if pilihan == "1":
            tambah()
        elif pilihan == "2":
            tampilkan()
        elif pilihan == "3":
            nama = input("Masukkan nama mahasiswa yang akan dihapus: ")
            hapus(nama)
        elif pilihan == "4":
            nama = input("Masukkan nama mahasiswa yang akan diubah: ")
            ubah(nama)
        elif pilihan == "5":
            print("Keluar dari program.")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")

    # Menjalankan menu utama
    menu()

INPUT
![Cuplikan layar 2024-11-28 185159](https://github.com/user-attachments/assets/c4778df1-d7a3-4136-9742-6f1d1bce7aab)
![Cuplikan layar 2024-11-28 185228](https://github.com/user-attachments/assets/07a06a1c-9380-41bf-ae65-3606dc791535)
![Cuplikan layar 2024-11-28 185329](https://github.com/user-attachments/assets/8cfc051b-fc60-4df7-9e53-ce3528617a18)

OUTPUT
![Cuplikan layar 2024-11-28 191615](https://github.com/user-attachments/assets/08c2f4db-1e52-4e38-b1a7-8e1b18054ffc)
![Cuplikan layar 2024-11-28 191653](https://github.com/user-attachments/assets/b63c6d52-3e1a-4e92-b76b-c97386a27d51)

FLOWCHART
![flowchart](https://github.com/user-attachments/assets/b10efa86-c8d4-49b1-a4c9-220d3a81c4ae)

PENJELASAN!
1. Data Mahasiswa: Data mahasiswa disimpan dalam list data_mahasiswa, yang berisi dictionary dengan kunci 'nama', 'nim', dan 'nilai'.
2. Fungsi tambah(): Meminta input nama, NIM, dan nilai mahasiswa, lalu menambahkannya ke dalam daftar.
3. Fungsi tampilkan(): Menampilkan semua data mahasiswa yang ada dalam daftar.
4. Fungsi hapus(nama): Menghapus data mahasiswa berdasarkan nama yang diberikan.
5. Fungsi ubah(nama): Mengubah data mahasiswa berdasarkan nama yang diberikan, termasuk nama, NIM, dan nilai.
6. Menu Utama: Menyediakan antarmuka pengguna untuk memilih operasi yang diinginkan.



    

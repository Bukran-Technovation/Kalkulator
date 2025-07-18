# Kalkulator 

def tambah(a, b):
    return a + b

def kurang(a, b):
    return a - b

def kali(a, b):
    return a * b

def bagi(a, b):
    if b == 0:
        return "Tidak bisa dibagi dengan nol!"
    return a / b

def kalkulator():
    print("=== KALKULATOR SEDERHANA ===")
    print("Pilih operasi:")
    print("1. Penjumlahan (+)")
    print("2. Pengurangan (-)")
    print("3. Perkalian (*)")
    print("4. Pembagian (/)")

    pilihan = input("Masukkan pilihan (1/2/3/4): ")

    if pilihan not in ['1', '2', '3', '4']:
        print("Pilihan tidak valid!")
        return

    try:
        a = float(input("Masukkan angka pertama: "))
        b = float(input("Masukkan angka kedua: "))
    except ValueError:
        print("Input harus berupa angka!")
        return

    if pilihan == '1':
        hasil = tambah(a, b)
        operasi = '+'
    elif pilihan == '2':
        hasil = kurang(a, b)
        operasi = '-'
    elif pilihan == '3':
        hasil = kali(a, b)
        operasi = '*'
    elif pilihan == '4':
        hasil = bagi(a, b)
        operasi = '/'

    print(f"Hasil: {a} {operasi} {b} = {hasil}")

# Jalankan kalkulator
if __name__ == "__main__":
    kalkulator()

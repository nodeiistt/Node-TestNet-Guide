# Menghubungkan Repo di Github dengan Gitopia

- [Official Docs](https://docs.gitopia.com/mirror)

<mark style="color:red;"><mark style="color:orange;"><mark style="color:green;">**Pastikan sudah memiliki akun GitHub**<mark style="color:green;"><mark style="color:orange;"></mark>

### 1. Fork Repository

* [https://github.com/Megumiiiiii?tab=repositories](https://github.com/Megumiiiiii?tab=repositories)
* [https://github.com/xsons?tab=repositories](https://github.com/xsons?tab=repositories)
* Atau buat repo sendiri, **BEBAS**

### 2. Create a Repository di Gitopia

Nama Bebas
  
![images](./images/Connect%20Github.png)

### 3. Masuk ke repository Github mu yang ingin dihubungkan

### 4. Klik Setting

![images](./images/masuk%20ke%20setting.png)

### 5. Scroll dan Masuk ke Secret -> Action

![images](./images/secret%20action.png)

### 6. Pilih New Secret

![images](./images/new%20secret.png)

### 7. Beri nama dan masukan isi

* Nama:

```
GITOPIA_WALLET
```

* Isi menggunakan data dari wallet yang di download dari tutor sebelumnya. [Tutor Sebelumnya](https://beritacryptoo.gitbook.io/node/gitopia/membuat-repo-dari-0)

![images](./images/isi%20secret.png)

Gitu

![images](./images/Gitu.png)

### 8. Lanjut ke Action

![images](./images/Pilih%20Action.png)

### 9. Pilih Simple workflow

![images](./images/pilih%20simple.png)

**a. Ganti nama file .yml**

Dari `blank.yml`

![images](./images/ganti%20menjadi.png)

Menjadi `gitopia-mirror.yml`

![images](./images/gini.png)

**b. Hapus isinya**

**c. Ganti dengan ini**

```
name: Mirror to Gitopia

on:
  push:
    branches:
      - '**'

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
        with:
          fetch-depth: 0
      - name: Push to Gitopia mirror
        uses: gitopia/gitopia-mirror-action@v0.5.0
        with:
          gitopiaWallet: "${{ secrets.GITOPIA_WALLET }}"
          remoteUrl: "link-repo-gitopia-mu"
          force: false

```

`link-repo-gitopia-mu` ganti dengan link dari sini

![images](./images/url%20ini.png)

Isi file `.yml` sekarang

![images](./images/Isi%20yaml.png)

**d. Klik Start Commit**

![images](./images/start%20commit.png)

### **10. Kembali ke web gitopia**

### **11. Refresh dan Cek hasilnya**

![images](./images/Selesai.png)

![images](./images/Selesaiiii.png)



### **Fork Repository di Gitopia**

* [https://gitopia.com/BeritaCryptooDAO/Testnet-Tutorial](https://gitopia.com/BeritaCryptooDAO/Testnet-Tutorial)
* [https://gitopia.com/megumii/Guide-Testnet](https://gitopia.com/megumii/Guide-Testnet)
* [https://gitopia.com/megumii/Connect-Github](https://gitopia.com/megumii/Connect-Github)

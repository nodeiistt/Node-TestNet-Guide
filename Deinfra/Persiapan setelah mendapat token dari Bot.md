### Install Keperluan

```
sudo apt update; sudo apt upgrade
sudo apt install curl wget gnupg apt-transport-https -y
```

```
curl -fsSL https://packages.erlang-solutions.com/ubuntu/erlang_solutions.asc | sudo gpg --dearmor -o /usr/share/keyrings/erlang.gpg
```

```
echo "deb [signed-by=/usr/share/keyrings/erlang.gpg] https://packages.erlang-solutions.com/ubuntu $(lsb_release -cs) contrib" | sudo tee /etc/apt/sources.list.d/erlang.list
```

```
sudo apt update

sudo apt install erlang-base erlang-public-key erlang-ssl
```

### Download Tea Client

```
wget https://tea.thepower.io/teaclient

chmod +x teaclient
```

### Download Docker Images

```
docker pull thepowerio/tpnode
```


<mark style="color:blue;">**Note**</mark>: Baru bisa mulai setelah mendapat Chain Token dari mereka

## Catatan tambahan :
Saat rebutan, ada baiknya jalankan di screen, karna untuk menunggu proses minum teh 100% harus saling menunggu dengan peserta lain, jadi kadang proses menuju 100% agak lama.


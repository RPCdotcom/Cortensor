![image](https://github.com/user-attachments/assets/5980218d-ac4c-411b-8a34-048eed7c85c7)


# Cortensor Node Kurulum : 

## Gereksinimler : 

Minimum : 

- ∞ CPU+ / ∞ GB RAM /  ∞ MBit/sec İndirme Hızı

Tavsiye Edilen : 

- ∞+ CPU ( Hızlı ) / ∞+ GB RAM / ∞+ MBit/sec İndirme Hızı 

Sistem paketlerini güncellemek ve yükseltmek için aşağıdaki komutu çalıştırın:

```bash
sudo apt update -y && sudo apt upgrade -y
```
## 2. Gerekli paketleri kurun:

```bash
sudo apt install htop ca-certificates zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev tmux iptables curl nvme-cli git wget make jq libleveldb-dev build-essential pkg-config ncdu tar clang bsdmainutils lsb-release libssl-dev libreadline-dev libffi-dev jq gcc screen unzip lz4 -y
```

## 3. Dosyaları Çekelim : 

```bash
git clone https://github.com/cortensor/installer
```

## Dizinin İçerisine Girelim : 

```bash
cd installer
```

## Docker - Ipfs - Install .sh : 

```bash
./install-docker.sh
```
```bash
./install-ipfs.sh
```

## LS : 

```bash
ls -al /usr/local/bin/cortensord
```

```bash
ls -al /etc/systemd/system/cortensor.service
```

## Docker Version - IPFS Version : 

```bash
docker version
```

```bash
ipfs version
```

## Deploy User'a Geçiş : 

```bash
sudo su deploy
```

## Ana Dizine Çıkış : 
```bash
cd ~/
```

## Key Oluşturma : 

```bash
/usr/local/bin/cortensord ~/.cortensor/.env tool gen_key
```

## Kayıt Edelim : 
```bash
/usr/local/bin/cortensord ~/.cortensor/.env tool register
```

## Sağlamasını Yapalım : 

```bash
/usr/local/bin/cortensord ~/.cortensor/.env tool verify
```

## Başlatalım : 

```bash
sudo systemctl start cortensor
```

## Durdurmak İsterseniz : 

```bash
sudo systemctl stop cortensor
```

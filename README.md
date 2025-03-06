# SETUP

### MEMBUAT BUAT & HAPUS FOLDER/FILE

1. buat folder
    ```bash
    mkdir nama-folder
    ```
2. check folder
    ```
    ls
    ```
3. buat file
    ```
    nano nama-file
    ```
4. save file nano
    ```
    CTRL + X + Y + `Enter`
    ```
5. hapus-file-folder
    ```
    rm -rf nama-folder/file
    ```
### INSTAL GIT

1. install git
    ```
    apt install git
    ```
2. check versi git
    ```
    git --version
    ```
3. clone GitHub
    ```
    git clone link-github-yg-mau-di-clone
    ```
4. hapus git
    ```
    sudo apt remove git
    ```
### INSTALL SCREEN

1. install screen
    ```
    apt install screen
    ```
2. buat screen
    ```
    screen -S namascreen
    ```
3. simpan screen
    ```
    CTRL + A + D
    ```
4. balik ke screen yang ada
    ```
    screen -r namascreen
    ```
5. check screen yang berjalan
    ```
    screen -ls
    ```
6. hapus screen
    ```
    screen -X -S namascreen quit
    ```
7. uninstall screen
    ```
    sudo apt remove screen
    ```
### 4. Docker

1. install docker
    ```
    sudo apt-get install -y ca-certificates curl gnupg lsb-release && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && sudo apt-get update && sudo apt-get install -y docker-ce docker-ce-cli containerd.io && sudo apt-mark hold docker-ce docker-ce-cli containerd.io
    ```
2. lihat list docker yang berjalan
```
docker ps -a
```
```
#stop docker yang berjalan
docker stop <IDContainer>
```
```
#hapus docker yang berjalan
docker rm <IDContainer>
```
```
#uninstall docker
sudo apt-mark unhold docker-ce docker-ce-cli containerd.io && sudo apt-get remove --purge -y docker-ce docker-ce-cli containerd.io && sudo rm -rf /var/lib/docker /var/lib/containerd && sudo rm /etc/apt/sources.list.d/docker.list && sudo apt-get autoremove -y && sudo apt-get autoclean
```

### 5. Go (Golang)
```
#install go
LATEST_GO=$(curl -s https://go.dev/VERSION?m=text) && wget https://go.dev/dl/${LATEST_GO}.linux-amd64.tar.gz && sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf ${LATEST_GO}.linux-amd64.tar.gz && echo "export PATH=\$PATH:/usr/local/go/bin:\$HOME/go/bin" >> ~/.bash_profile && source ~/.bash_profile && go version
```
```
#uninstall go
sudo rm -rf /usr/local/go && sed -i '/\/usr\/local\/go\/bin/d' ~/.bash_profile && sed -i '/\/go\/bin/d' ~/.bash_profile && source ~/.bash_profile
```

### 6. Node js
```
#install node js
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.4/install.sh | bash && source ~/.bashrc && nvm install node && nvm use node && node -v
```
```
#uninstall node js
rm -rf ~/.nvm && sed -i '/NVM_DIR/d' ~/.bashrc && source ~/.bashrc
```
```
#menjalankan/run file js (node.js)
node namafile.js
```
### 7. Python
```
#install Python
sudo apt-get update && sudo apt-get install -y software-properties-common && sudo add-apt-repository -y ppa:deadsnakes/ppa && sudo apt-get update && sudo apt-get install -y python3 python3-pip && python3 --version && pip3 --version
```
```
#uninstall python
sudo apt-get remove --purge -y python3.* && sudo apt-get autoremove -y && sudo apt-get autoclean
```
#menjalankan/run file py (python)
    ```
    python3 namafile.py
    ```
### Update Sistem VPS
    ```
    sudo apt update && sudo apt upgrade -y
    sudo apt install curl tar wget clang pkg-config libssl-dev jq build-essential bsdmainutils git make ncdu gcc jq chrony liblz4-tool -y
    ```

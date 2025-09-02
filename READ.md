# env

# C++ 學生快速安裝指南（Windows）

## 1. 安裝必備工具

win + R 搜尋 powershell

![image.png](https://github.com/yycquant0812/CPP-demo/blob/main/img/image.png?raw=true)

![image.png](https://github.com/yycquant0812/CPP-demo/blob/main/img/image%201.png?raw=true
)

在 **PowerShell (系統管理員)** 輸入：

```powershell
winget install -e --id MSYS2.MSYS2
winget install -e --id Git.Git
winget install -e --id Microsoft.VisualStudioCode
```

```bash
g++ --version
```

## 2. 安裝 g++ 編譯器

打開 MSYS2 UCRT64 終端機，輸入：

```bash
pacman -Syu 
輸入Ｙ
pacman -S --needed base-devel mingw-w64-ucrt-x86_64-toolchain
輸入１　３
```

驗證

```bash
g++ --version
```

## 3. vscode 程式碼C++套件

![image.png](https://github.com/yycquant0812/CPP-demo/blob/main/img/image%202.png?raw=true)

```bash
code --install-extension ms-vscode.cpptools-extension-pack
code --install-extension eamodio.gitlens

```

## 4. 本地git設定

```bash
**git config --global user.name "你的名字"
git config --global user.email "你的 Email"
git config --global init.defaultBranch main**
git config --global credential.helper manager
```

## 5. 遠端 github 註冊帳號

[GitHub · Build and ship software on a single, collaborative platform](https://github.com/)

### 建立 Personal Access Token

![image.png](https://github.com/yycquant0812/CPP-demo/blob/main/img/image%203.png?raw=true)

1.登入 GitHub → **Settings** → **Developer settings** → **Personal Access Tokens**。

![image.png](https://github.com/yycquant0812/CPP-demo/blob/main/img/image%204.png?raw=true)

2.建立一個 **Fine-grained token** 或 **Classic token**（選 read/write 權限給 repo）。

3.複製 Token（注意：只會顯示一次）。

![image5.jpg](https://github.com/yycquant0812/CPP-demo/blob/main/img/image5.jpg?raw=true)


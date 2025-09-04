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


## 2. 安裝 g++ 編譯器

打開 MSYS2 UCRT64 終端機，輸入：

```bash
pacman -Syu 
輸入Ｙ
pacman -S --needed base-devel mingw-w64-ucrt-x86_64-toolchain
輸入１　３
```
### 添加環境變數
```bash
C:\msys64\ucrt64\bin
C:\msys64\mingw64\bin
```
![image.png](env0)
![image.png](env2)
![image.png](env3)



打開 cmd 驗證

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

## 6. 驗證環境
```bash
git --version
gcc --version
code --version
```

# 2安裝步驟替代方法
# Windows 安裝 Git、MSYS2、VSCode

## 1. 安裝 Git
1. 前往官方網站下載  
   👉 https://git-scm.com/download/win  
2. 執行安裝檔，建議勾選以下選項：  
   - **Use Git from the Command Prompt**  
   - **Checkout Windows-style, commit Unix-style line endings**  
   - 其他保持預設即可  
3. 安裝完成後，在 `cmd` 或 `PowerShell` 測試：  
   ```bash
   git --version
   ```

---

## 2. 安裝 MSYS2
1. 前往官方網站下載  
   👉 https://www.msys2.org/  
2. 安裝後，開啟 **MSYS2 MSYS** 終端機。  
3. 先更新套件資料庫與核心套件：  
   ```bash
   pacman -Syu
   ```
   完成後關閉視窗，再次打開執行：  
   ```bash
   pacman -Su
   ```
4. 安裝常用工具（如 gcc、make、vim）：  
   ```bash
   pacman -S base-devel gcc vim
   ```

---

## 3. 安裝 Visual Studio Code
1. 前往官網下載  
   👉 https://code.visualstudio.com/Download  
2. 選擇 **System Installer (User Installer 也可)**。  
3. 安裝過程建議勾選：  
   - **Add to PATH**  
   - **Register Code as editor for supported file types**  
   - **Add "Open with Code" action to Windows Explorer context menu**  
4. 完成後，在 PowerShell 測試：  
   ```bash
   code --version
   ```

---

## 4. 驗證環境
```bash
git --version
gcc --version
code --version
```

成功輸出版本號代表安裝完成 🎉

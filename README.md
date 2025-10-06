
## APT (Debian/Ubuntu)

```bash
# 方法1：从系统仓库安装（可能版本较老）
sudo apt update
sudo apt install neovim

# 方法2：安装最新稳定版（推荐）
sudo apt install -y software-properties-common
sudo add-apt-repository ppa:neovim-ppa/stable
sudo apt update
sudo apt install neovim

# 方法3：安装unstable版本（最新功能）
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt update
sudo apt install neovim

# 验证安装
nvim --version
```

## DNF (Fedora/RHEL/CentOS)

```bash
# 方法1：从默认仓库安装
sudo dnf install neovim

# 方法2：启用EPEL仓库安装更新版本
sudo dnf install -y epel-release
sudo dnf install neovim

# 方法3：从Copr仓库安装最新版本
sudo dnf copr enable agriffis/neovim-nightly
sudo dnf install neovim

# 方法4：Fedora直接安装（推荐Fedora用户）
sudo dnf install -y neovim python3-neovim

# 验证安装
nvim --version
```

## Pacman (Arch Linux/Manjaro)

```bash
# 方法1：安装稳定版
sudo pacman -S neovim

# 方法2：安装nightly版本（最新功能）
sudo pacman -S neovim-nightly

# 方法3：安装包含Python支持的版本
sudo pacman -S neovim python-pynvim

# 验证安装
nvim --version
```

## 通用安装方法（所有系统）

### 从源码编译安装（获取最新版本）
```bash
# 安装依赖
# Ubuntu/Debian:
sudo apt install -y git cmake gettext ninja-build

# Fedora/RHEL:
sudo dnf install -y git cmake gettext ninja-build

# Arch Linux:
sudo pacman -S git cmake gettext ninja-build

# 编译安装
git clone https://github.com/neovim/neovim
cd neovim
make CMAKE_BUILD_TYPE=RelWithDebInfo
sudo make install

# 或者使用CMake直接安装
cd neovim && rm -rf build/
mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make
sudo make install
```

### 使用AppImage（便携式）
```bash
# 下载最新AppImage
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim.appimage
chmod u+x nvim.appimage
./nvim.appimage

# 或安装到系统
sudo mv nvim.appimage /usr/local/bin/nvim
```

### 使用包管理器（通用）
```bash
# 使用Snap
sudo snap install nvim --classic

# 使用Flatpak
flatpak install flathub io.neovim.nvim

# 使用Homebrew（Linux/macOS）
brew install neovim
```

## 验证安装和功能

```bash
# 检查版本
nvim --version

# 检查健康状态
nvim +checkhealth

# 测试基本功能
nvim +q
```

## 卸载方法

```bash
# APT
sudo apt remove neovim
sudo add-apt-repository --remove ppa:neovim-ppa/stable

# DNF
sudo dnf remove neovim

# Pacman
sudo pacman -Rs neovim

# 源码安装的卸载
cd neovim/build && sudo make uninstall
```

cd ~/.config && git clone https://github.com/ChenHaoNan-CN/nvim.git && nvim

## APT (Debian/Ubuntu)

```bash
# 更新软件包列表
sudo apt update

# 安装neofetch
sudo apt install neofetch

# 或者安装最新版本（如果系统仓库版本较老）
sudo apt install -y git
git clone https://github.com/dylanaraps/neofetch.git
cd neofetch
sudo make install
```

## DNF (Fedora/RHEL/CentOS)

```bash
# 安装neofetch
sudo dnf install neofetch

# 如果找不到包，先启用EPEL仓库
sudo dnf install -y epel-release
sudo dnf install neofetch

# 或者从Copr仓库安装更新版本
sudo dnf copr enable konimex/neofetch
sudo dnf install neofetch
```

## Yay (Arch Linux/Manjaro)

```bash
# 如果还没有安装yay
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si

# 使用yay安装neofetch
yay -S neofetch

# 或者使用官方pacman安装
sudo pacman -S neofetch
```

## 验证安装

安装完成后，运行以下命令验证：

```bash
neofetch --version
neofetch
```

## 额外配置

### 对于Arch Linux用户：
```bash
# 安装开发版本（可选）
yay -S neofetch-git
```

### 对于所有系统，如果需要从源码安装：
```bash
git clone https://github.com/dylanaraps/neofetch.git
cd neofetch
sudo make install
```

## 卸载方法

```bash
# APT
sudo apt remove neofetch

# DNF
sudo dnf remove neofetch

# Yay/pacman
sudo pacman -Rs neofetch
# 或者
yay -Rs neofetch
```

选择适合你系统的命令进行安装即可！


```bash
rm -r ~/.config/neofetch && cd ~/.config && git clone https://github.com/ChenHaoNan-CN/neofetch.git && neofetch
```

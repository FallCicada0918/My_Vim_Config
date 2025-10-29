<!--
 * @Description: Vim 配置文档
 * @Author: FallCicada
 * @Date: 2025-10-29 15:24:06
 * @LastEditors: FallCicada
 * @LastEditTime: 2025-10-29 16:20:00
 * @Slogan: 無限進步
-->

# Vim 配置文档

> **作者**: FallCicada  
> **Slogan**: 無限進步  
> **最后更新**: 2025-10-29

## 📋 目录

- [配置简介](#配置简介)
- [插件管理](#插件管理)
- [已安装插件列表](#已安装插件列表)
- [核心功能配置](#核心功能配置)
- [快捷键映射](#快捷键映射)
- [自动补全配置](#自动补全配置)
- [代码模板](#代码模板)
- [安装指南](#安装指南)
- [常见问题](#常见问题)

---

## 🎯 配置简介

这是一套完整的 Vim 开发环境配置,专为 C/C++、Python、Java 等语言开发优化。主要特性包括:

- 🚀 强大的代码自动补全 (YouCompleteMe)
- 📁 可视化文件浏览器 (NERDTree)
- 🏷️ 代码标签导航 (Tagbar)
- 💬 快速注释工具 (NERDCommenter)
- ✨ 括号自动配对 (Auto-Pairs)
- 📝 Markdown 实时预览
- 🎨 美化状态栏 (vim-airline)
- ⚡ 一键编译运行

- ⚡ 一键编译运行

---

## 🔌 插件管理

本配置使用 **vim-plug** 作为插件管理器。

### 安装 vim-plug

```bash
# Unix/Linux/macOS
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

# Windows (PowerShell)
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
    ni $HOME/vimfiles/autoload/plug.vim -Force
```

### 插件管理命令

在 Vim 中执行以下命令:

```vim
:PlugInstall    " 安装插件
:PlugUpdate     " 更新插件
:PlugClean      " 清理未使用的插件
:PlugStatus     " 查看插件状态
```

---

## 📦 已安装插件列表

| 插件名称 | 功能描述 | 仓库地址 |
|---------|---------|---------|
| **YouCompleteMe** | 强大的代码补全引擎 | [Valloric/YouCompleteMe](https://github.com/Valloric/YouCompleteMe) |
| **NERDTree** | 文件系统浏览器 | [scrooloose/nerdtree](https://github.com/scrooloose/nerdtree) |
| **Tagbar** | 代码结构浏览 | [majutsushi/tagbar](https://github.com/majutsushi/tagbar) |
| **vim-airline** | 美化状态栏 | [bling/vim-airline](https://github.com/vim-airline/vim-airline) |
| **Auto-Pairs** | 自动补全括号引号 | [vim-scripts/Auto-Pairs](https://github.com/jiangmiao/auto-pairs) |
| **NERDCommenter** | 快速注释代码 | [scrooloose/nerdcommenter](https://github.com/scrooloose/nerdcommenter) |
| **Syntastic** | 语法检查 | [scrooloose/syntastic](https://github.com/vim-syntastic/syntastic) |
| **indentLine** | 缩进线显示 | [Yggdroot/indentLine](https://github.com/Yggdroot/indentLine) |
| **UltiSnips** | 代码片段引擎 | [SirVer/ultisnips](https://github.com/SirVer/ultisnips) |
| **vim-snippets** | 代码片段集合 | [honza/vim-snippets](https://github.com/honza/vim-snippets) |
| **MatchTagAlways** | HTML/XML 标签匹配高亮 | [Valloric/MatchTagAlways](https://github.com/Valloric/MatchTagAlways) |
| **vim-instant-markdown** | Markdown 实时预览 | [suan/vim-instant-markdown](https://github.com/suan/vim-instant-markdown) |
| **delimitMate** | 自动补全分隔符 | [Raimondi/delimitMate](https://github.com/Raimondi/delimitMate) |
| **vim-fugitive** | Git 集成 | [tpope/vim-fugitive](https://github.com/tpope/vim-fugitive) |
| **ag.vim** | 快速代码搜索 | [rking/ag.vim](https://github.com/rking/ag.vim) |

---

## ⚙️ 核心功能配置

### 基础设置

```vim
set nocompatible        " 不使用 Vi 兼容模式
set number              " 显示行号
set cursorcolumn        " 高亮当前列
set tabstop=4           " Tab 宽度为 4 个空格
set shiftwidth=4        " 缩进宽度为 4 个空格
set expandtab           " Tab 转换为空格
set smartindent         " 智能缩进
set autoindent          " 自动缩进
set showmatch           " 括号匹配高亮
set ruler               " 显示光标位置
set wrap                " 自动折行
```

### 搜索设置

```vim
set hlsearch            " 高亮搜索结果
set ignorecase          " 搜索忽略大小写
```

### 备份设置

```vim
set nobackup            " 关闭备份文件
set noswapfile          " 关闭交换文件
```

### 语法高亮

```vim
syntax on               " 开启语法高亮
```

---

## ⌨️ 快捷键映射

### 🔥 核心快捷键

| 快捷键 | 模式 | 功能 | 说明 |
|-------|------|------|------|
| `F1` | Normal | 一键编译运行 | 支持 C/C++/Java/Python/Go/Shell |
| `F2` | Normal | 插入文件头 | 自动生成带作者信息模板 |
| `F3` | Normal | 打开/关闭文件树 | 切换 NERDTree 和 Tagbar |
| `F5` | Normal | 强制编译检查 | YCM 重新编译和诊断 |

### 🎯 编辑快捷键

| 快捷键 | 模式 | 功能 |
|-------|------|------|
| `jk` | Insert | 退出插入模式 |
| `,c` | Visual/Normal | 复制到系统剪贴板 |
| `,v` | Normal | 从系统剪贴板粘贴 |
| `{{` | Insert | 创建代码块(带格式化) |

### 📂 文件导航

| 快捷键 | 功能 |
|-------|------|
| `Ctrl+n` | 打开/关闭 NERDTree |
| `Ctrl+t` | 打开/关闭 Tagbar |
| `Ctrl+l` | 切换到下一个标签页 |
| `Ctrl+h` | 切换到上一个标签页 |
| `,t` | 新建标签页 |

### 💡 代码补全

| 快捷键 | 功能 |
|-------|------|
| `Ctrl+z` | 触发 YCM 补全 |
| `Tab` | 选择下一个补全项 |
| `Up/Down` | 在补全菜单中上下移动 |
| `,jd` | 跳转到定义/声明 |

### 📝 注释快捷键

| 快捷键 | 功能 |
|-------|------|
| `,cc` | 注释当前行/选中行 |
| `,cu` | 取消注释 |
| `,c<space>` | 切换注释状态 |

---

## 🤖 自动补全配置

### YouCompleteMe 配置

```vim
" 补全菜单设置
let g:ycm_add_preview_to_completeopt = 0
let g:ycm_show_diagnostics_ui = 0
let g:ycm_min_num_of_chars_for_completion = 2
let g:ycm_min_num_identifier_candidate_chars = 2

" 补全引擎
let g:ycm_collect_identifiers_from_tags_files = 1
let g:ycm_auto_trigger = 1
let g:ycm_seed_identifiers_with_syntax = 1
let g:ycm_complete_in_comments = 1
let g:ycm_complete_in_strings = 1

" 全局配置文件
let g:ycm_global_ycm_extra_conf = '~/.ycm_extra_conf.py'
```

### 语义触发器

支持以下语言的智能补全:

- **C/C++**: `->`, `.`, `::`
- **Python**: `.`
- **Java**: `.`
- **JavaScript/TypeScript**: `.`
- **PHP**: `->`, `::`
- **Ruby**: `.`, `::`
- **Go**: `.`

### 自动配对

```vim
" 自动补全括号
inoremap ( ()<Esc>i
inoremap [ []<Esc>i
inoremap { {<CR>}<Esc>O

" 智能闭合
inoremap ) <c-r>=ClosePair(')')<CR>
inoremap ] <c-r>=ClosePair(']')<CR>
inoremap } <c-r>=CloseBracket()<CR>
```

---

## 📄 代码模板

### C++ 文件模板 (F2)

按 `F2` 自动插入以下模板:

```cpp
//-------------------------------------------------
//@Created by FallCicada
//Created Time : [当前时间]
//@File Name : [文件名]
//@Slogan: 無限進步
//-------------------------------------------------

#include <stdio.h>
#include <string.h>
#include <iostream>
#include <algorithm>
#include <vector>
#include <queue>
#include <set>
#include <map>
#include <list>
#include <string>
#include <math.h>
#include <stdlib.h>
#include <time.h>
using namespace std;
typedef double db;
typedef long long ll;
const int maxn = 200005;

int main()
{
 #ifdef ONLINE_JUDGE
 #else
 freopen("in.txt","r",stdin);
 #endif
 
 
     return 0;
}
```

---

## 🚀 安装指南

### 1️⃣ 前置要求

```bash
# 安装必要工具
# Ubuntu/Debian
sudo apt-get install vim vim-gtk3 ctags git cmake python3-dev

# macOS
brew install vim ctags git cmake python3

# 确保 Vim 版本 >= 8.0
vim --version
```

### 2️⃣ 安装配置文件

```bash
# 备份原有配置
mv ~/.vimrc ~/.vimrc.backup
mv ~/.vim ~/.vim.backup

# 复制新配置
cp .vimrc ~/.vimrc

# 创建必要目录
mkdir -p ~/.vim/{autoload,plugged,backup,undo}
```

### 3️⃣ 安装 vim-plug

```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

### 4️⃣ 安装插件

```bash
# 打开 Vim
vim

# 在 Vim 中执行
:PlugInstall
```

### 5️⃣ 编译 YouCompleteMe

```bash
cd ~/.vim/plugged/YouCompleteMe

# 完整安装(支持所有语言)
python3 install.py --all

# 或仅安装 C/C++ 支持
python3 install.py --clangd-completer
```

### 6️⃣ 配置 YCM

创建 `~/.ycm_extra_conf.py`:

```python
def Settings(**kwargs):
    return {
        'flags': [
            '-Wall',
            '-Wextra',
            '-Werror',
            '-std=c++17',
            '-x', 'c++',
            '-I', '/usr/include',
            '-I', '/usr/local/include',
        ],
    }
```

---

## 🎨 插件详细配置

### NERDTree 配置

```vim
let NERDTreeWinPos='left'       " 位置在左侧
let NERDTreeWinSize=25          " 宽度 25
map <C-n> :NERDTreeToggle<CR>   " Ctrl+n 切换
autocmd vimenter * NERDTree     " 启动时自动打开
```

### Tagbar 配置

```vim
let g:tagbar_ctags_bin='ctags'  " ctags 路径
let g:tagbar_width=20           " 宽度 20
map <F3> :Tagbar<CR>            " F3 打开
map <C-t> :Tagbar<CR>           " Ctrl+t 打开
```

### indentLine 配置

```vim
let g:indentLine_char = '┆'     " 缩进线字符
let g:indentLine_color_term = 239
let g:indentLine_enabled = 1
```

### vim-airline 配置

```vim
set laststatus=2                " 始终显示状态栏
```

---

## ❓ 常见问题

### Q1: YouCompleteMe 编译失败?

**解决方案**:

```bash
# 确保安装了所有依赖
sudo apt-get install build-essential cmake python3-dev

# 重新编译
cd ~/.vim/plugged/YouCompleteMe
python3 install.py --all
```

### Q2: NERDTree 显示乱码?

**解决方案**:

```vim
" 在 .vimrc 中添加
let g:NERDTreeNodeDelimiter = "\u00a0"
```

### Q3: 插件安装失败?

**解决方案**:

```bash
# 检查网络连接
# 或使用国内镜像
export https_proxy=http://127.0.0.1:7890

# 重新安装
vim +PlugInstall +qall
```

### Q4: F1 编译运行不工作?

**确保安装了对应语言的编译器**:

```bash
# C/C++
sudo apt-get install gcc g++

# Java
sudo apt-get install default-jdk

# Python
sudo apt-get install python3

# Go
sudo apt-get install golang
```

### Q5: 代码补全不工作?

**检查步骤**:

1. 确认 YCM 已正确编译
2. 检查 `.ycm_extra_conf.py` 文件是否存在
3. 查看 YCM 日志: `:YcmDebugInfo`

### Q6: 如何更新所有插件?

```vim
:PlugUpdate
```

### Q7: 如何卸载插件?

```vim
" 1. 在 .vimrc 中删除或注释插件行
" 2. 在 Vim 中执行
:PlugClean
```

---

## 🔧 自定义配置

### 修改 Leader 键

```vim
let mapleader = ','             " 当前为逗号
" 可改为空格: let mapleader = ' '
```

### 修改配色方案

```vim
colorscheme desert              " 默认主题
" 其他推荐: molokai, solarized, gruvbox
```

### 调整字体大小

```vim
" 仅在 gVim 中有效
set guifont=Consolas\ 12
```

---

## 📚 学习资源

- [Vim 官方文档](https://www.vim.org/docs.php)
- [vim-plug 文档](https://github.com/junegunn/vim-plug)
- [YouCompleteMe 文档](https://github.com/ycm-core/YouCompleteMe)
- [NERDTree 文档](https://github.com/preservim/nerdtree)
- [Learn Vim](https://github.com/iggredible/Learn-Vim)

---

## 📝 更新日志

- **2025-10-29**: 创建详细配置文档
- 配置了完整的 C/C++/Python/Java 开发环境
- 集成了 15+ 实用插件
- 添加了一键编译运行功能
- 优化了代码补全体验

---

---

## 📄 许可证

MIT License

---

<div align="center">
  <strong>✨ Happy Coding with Vim! ✨</strong><br>
  <em>無限進步 - by FallCicada</em>
</div>





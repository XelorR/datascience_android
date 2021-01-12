# Data Science environment on Android device

For those who:

- are too lazy to turn computer on
- spend a lot of time traveling
- want to have fully functional pocket programming and data science tool. Just in case

## Setup

0. Ensure that you have some Android device
1. Install [Termux](https://termux.com) app
2. Install [AnLunux](https://github.com/EXALAB/AnLinux-App)
3. Launch **AnLinux**, choose **Ubuntu**, copy generated command
4. Launch **Termux**, paste and run command
5. run Ubuntu inside Termux app:
```bash
bash ~/start-ubuntu.sh
```
6. Install apt packages:
```bash
apt update && apt install -y git ssh p7zip-full wget gawk curl vim neovim hex{curse,edit} python3-{pandas,openpyxl,xlrd,requests,bs4,lxml,seaborn,sklearn,sympy,arrow,h5py,tables,numba,ipython,notebook,ipykernel,pip,dev,rope,autopep8,coverage} flake8 black pylint isort bpython csvkit npm gcc magic-wormhole jq micro fzf ripgrep fd-find visidata
```
7. Install npm packages:
```bash
npm install --global vscode-html-languageserver-bin http-server prettier typescript
```
8. Install pip packages:
```bash
pip3 install --user notedown autoflake
```
9. Install [SpaceVim](https://spacevim.org) for **Vim**:
```bash
curl -sLf https://spacevim.org/install.sh | bash
```
10. Install [much lighter config](https://gitlab.com/XelorR/friendly_vim) for **NeoVim**:
```bash
curl -sL is.gd/friendly_vim | python3
```
11. Configure bash:
```bash
echo -e "alias vim=vim.basic" >> ~/.bashrc
echo -e 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
12. Open and close **vim** (not **nvim**)
13. Configure **SpaceVim**:
```bash
sed -i 's/gruvbox/SpaceVim/' ~/.SpaceVim.d/init.toml
echo -e '\n[[layers]]\n    name = "lang#html"\n\n[[layers]]\n    name = "lang#javascript"\n\n[[layers]]\n    name = "lang#c"\n\n[[layers]]\n    name = "VersionControl"\n\n[[layers]]\n    name = "git"\n\n[[layers]]\n    name = "github"\n\n[[layers]]\n    name = "lang#python"\n\n[[layers]]\n    name = "lang#ipynb"\n\n[[layers]]\n    name = "lang#sh"\n\n[[layers]]\n    name = "lang#typescript"' >> ~/.SpaceVim.d/init.toml
```
14. Restart **vim** (not **nvim**) and ensure that all required plugins installed successfully

## Features

### Editors

- [Vim](https://www.vim.org) with feature rich config
- [Neovim](https://neovim.io) with lightweight config
- [Micro](https://micro-editor.github.io) for those who forgot how to Vim
- [Hexcurse](https://github.com/LonnyGomes/hexcurse) and [Hexedit](https://linux.die.net/man/1/hexedit) for editing binaries
- [VisiData](https://www.visidata.org) - awsome spreadsheets in your terminal

### Python3 scientific stuff

- **requests, lxml and bs4** for scraping websites
- **numpy** for vectorized math
- **pandas** for tabular data
- **sympy** for solving equations
- **matplotlib and seaborn** for drawing plots
- **sklearn / scikit-learn** for machine learning
- **jupyter notebook** for creating experiment report

### REPL

- [python3](https://docs.python.org/3/tutorial/interpreter.html)
- [bpython](https://bpython-interpreter.org)
- [ipython](https://ipython.readthedocs.io/en/stable/overview.html)
- [jupyter notebook](https://jupyter-notebook.readthedocs.io/en/stable)

### Sharing and receiving files

- ssh
- http-server
- magic-wormhole

### Additional tools

- [CsvKit](https://csvkit.readthedocs.io/en/latest) - dealing with csv tools from the command line
- 7zip - for opening and creating archives
- Lots of common unix tools

### Additional languages

- Bash
- Perl
- JavaScript (nodejs)
- TypeScript
- C/C++ (gcc)

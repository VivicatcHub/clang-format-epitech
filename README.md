# Clang-Format Configuration

This repository contains a `.clang-format` configuration file for formatting C, C++, and other related source code files. This file can be used with various editors and IDEs to ensure consistent code style across your projects.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
  - [Visual Studio Code (VSCode)](#visual-studio-code-vscode)
  - [Emacs](#emacs)
  - [Neovim (nvim)](#neovim-nvim)
  - [Command Line](#command-line)
- [Customizing the Configuration](#customizing-the-configuration)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/Davphla/clang-format-epitech.git
   cd ./clang-format-epitech
   ```

2. Ensure you have `clang-format` installed. You can install it via your package manager:
   - **Ubuntu**: `sudo apt install clang-format`
   - **macOS**: `brew install clang-format`
   - **Windows**: Download from the [LLVM releases page](https://releases.llvm.org/download.html).
   - 

## Usage

### Visual Studio Code (VSCode)

1. Install the **Clang-Format** extension from the Extensions Marketplace.
2. Open your workspace settings (`.vscode/settings.json`) and add the following configuration:
   ```json
   {
       "C_Cpp.clang_format_style": ".clang-format"
   }
   ```
3. Now, you can format your code using the command palette (`Ctrl + Shift + P`) and typing `Format Document`.
4. You can also use `Ctrl + Shift + I` to format the current document. 

### Emacs

1. Install the `clang-format` package if you haven't already.
2. Add the following to your Emacs configuration file (`.emacs` or `init.el`):
   ```elisp
   (require 'clang-format)
   (global-set-key (kbd "C-c C-f") 'clang-format-region)
   ```
3. You can format the current region or buffer by using `C-c C-f`.

### Neovim (nvim)

1. Install the `clang-format` plugin using your preferred plugin manager (e.g., `vim-plug`):
   ```vim
   Plug 'sbdchd/neoformat'
   ```
2. Add the following configuration to your `init.vim` or `init.lua`:
   ```vim
   autocmd FileType c,cpp setlocal formatprg=clang-format
   ```
3. You can format your code by running `:Neoformat`.

### Command Line

You can also use `clang-format` directly from the command line. Navigate to your project directory and run:
```bash
clang-format -i <filename>
```
Replace `<filename>` with the name of the file you want to format. The `-i` flag edits the file in place.

## Customizing the Configuration

You can customize the `.clang-format` file to suit your coding style preferences. Refer to the [Clang-Format Style Options](https://clang.llvm.org/docs/ClangFormatStyleOptions.html) for a comprehensive list of available options.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue if you have suggestions or improvements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to modify this README to better fit your project's needs!

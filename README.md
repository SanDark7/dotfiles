# dotfiles

- .eslintrc
- .editorconfig

Rambler&amp;Co Dotfiles for your javascripts. Use the force, Luke!

# Install

    $ npm install https://github.com/rambler-digital-solutions/dotfiles.git --save-dev

# Configure

1. Copy .editorconfig to project dir

2. Create .eslintrc in the project root. This file must contains:

    Relative path (Sublime Text, Atom):
    ```json
    {
        "extends": "./node_modules/eslint-config-rambler/.eslintrc"
    }
    ```

    Package name (IntelliJ IDEA family)
    ```json
    {
        "extends": "eslint-config-rambler"
    }
    ```

### Sublime Text

1. Install packages

    ```
    $ npm install -g eslint
    $ npm install -g babel-eslint
    ```

2. Install plugins

    * SublimeLinter ([full instructions](http://sublimelinter.readthedocs.org/en/latest/installation.html))
    * SublimeLinter-contrib-eslint ([full instructions](https://github.com/roadhump/SublimeLinter-eslint#plugin-installation))
    * EditorConfig ([EditorConfig](https://github.com/sindresorhus/editorconfig-sublime#install))

### Atom

1. Install packages

    ```
    $ npm install eslint
    $ npm install babel-eslint
    ```

2. Install plugins

    ```
    $ apm install linter
    $ apm install linter-eslint
    $ apm install editorconfig
    ```

    or through **Preferences → Install → Install Pacages** for linter, linter-eslint and editorconfig

## JetBrains editors with support Javascript (WebStorm, IDEA and etc.)

1. Enable ESLint in **Preferences → Languages & Frameworks → JavaScript → Code Quality Tools → ESLint**.

2. Set path in **ESLint package** as`/<project_root or project_node_modules>/node_modules/eslint-config-rambler/node_modules/eslint`.

3. And set path in **Configuration file** as `/<project_root>/.eslintrc`.

2. EditorConfig must works automatically by default. But if it doesn't, then enable EditorConfig plugin and restart IDE.

## Vim

<<<<<<< HEAD
1. Install packages

    ```
    $ npm install -g eslint
    $ npm install -g babel-eslint
=======
1. Will need installed npm packages is local

    ```bash
    npm install eslint
    npm install babel-eslint
>>>>>>> 918387851c04ba4530438196c4904c7959fcee0e
    ```

2. Install vim-plug

    ```
    $ curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
        https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
    ```

<<<<<<< HEAD
3. Add a vim-plug section to your `~/.vimrc`

    ```
    call plug#begin()
    Plug 'scrooloose/syntastic'
    call plug#end()
    ```

    Reload .vimrc and :PlugInstall to install plugins.

4. Add to your `~/.vimrc`
=======
    ```bash
    apm install linter
    apm install linter-eslint
    apm install editorconfig
    ```

  or through **Preferences → Install → Install Packages** for linter, linter-eslint and editorconfig.
>>>>>>> 918387851c04ba4530438196c4904c7959fcee0e

    ```
    set statusline+=%#warningmsg#
    set statusline+=%{SyntasticStatuslineFlag()}
    set statusline+=%*

    let g:syntastic_always_populate_loc_list = 1
    let g:syntastic_auto_loc_list = 1
    let g:syntastic_check_on_open = 1
    let g:syntastic_check_on_wq = 0

    let g:syntastic_python_python_exec = '/path/to/python3'

    let g:syntastic_python_checkers = ['pep8']
    let g:syntastic_javascript_checkers = ['eslint']
    let g:syntastic_javascript_eslint_args = "--no-eslintrc --config /<project_root>/.eslintrc"
    ```

# Tested in:

- Sublime Text 3
- Atom 1.0.7
- PyCharm 4.0.6
- WebStrom 10.0.4
- MacVim

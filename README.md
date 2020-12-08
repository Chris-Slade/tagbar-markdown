# tagbar markdown extension

### Intro
tagbar-markdown is a tagbar extension for markdown.

This fork rewrites the provided mdctags script in Perl, which replaces the PHP dependency.

### Screenshot
![2017-02-01_1359x723](https://cloud.githubusercontent.com/assets/13142418/22514376/12f8a792-e8da-11e6-9897-fb0136732a31.png)

### Install
- [vim-plug]
```viml
Plug 'majutsushi/tagbar'
Plug 'lvht/tagbar-markdown'
```
- Use [dein.vim] to lazy load plugin, and check the requirements.
```viml
call dein#add('', {'on_cmd' : 'TagbarToggle'})
call dein#add('', {'on_ft' : 'markdown', 'if' : executable('php')})
```

Please make sure **perl** is in your `$PATH` and the `bin/mdctags` has execute permission.

The minimum supported version is Perl 5.10, but it might work with earlier versions. The only Perl dependencies are the core modules `Cwd` and `File::Spec`.

Execute ':MDAgenda' to insert content agenda in the current line.

Enjoy :)

[vim-plug]: https://github.com/junegunn/vim-plug
[dein.vim]: https://github.com/Shougo/dein.vim

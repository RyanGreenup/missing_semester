# Shell

The shell is the most efficient way to interact with a computer. It is a command-line interface (CLI) that allows you to interact with via text.

Text is the best way to interact with a computer as it's quick, flexible and reproducible. Now, you may doubt this, but consider the following, we need to share  a note to a friend

```sh
## Find the file
set file (fd '\.md' | fzf)
set file_no_ext (basename $file)

## Inspect the file
nvim $file

## Move to a temp dir
set dir (mktemp -d)
cp $file $dir

## Grab all the assets and make formats
cd $dir
pandoc $file --pdf-engine=xelatex -o $file_no_ext.pdf
pandoc $file -s -o $file_no_ext.html
pandoc $file -s --assets=. -o (mktemp).md

notify-send "File is ready"
echo $dir | wl-copy
```

## Activites

- [ ] WSL
- [ ] Fish, Elvish, Nushel
- [ ] fzf
- [ ] Fuzzyfind keybindings
- [ ] ripgrep fd find
- [ ] ranger, lf and yazi, broot
- [ ] Gitui
- [ ] Neovim


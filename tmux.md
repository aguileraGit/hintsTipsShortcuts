#### Tmux hints and shortcuts

Copy and Paste all contents of pane:
- Issue scroll command to get number of lines: `prefix + [`
- To copy to buffer: `prefix + :,` then type in `capture-pane -S -3000 + return`
- To save to file: `prefix + : ` and type in `save-buffer filename.txt + return`

Prefix
`Ctrl + b`

Create Session:
`tmux new -s sessionName`

List Session:
`tmux list-session`

Attach Session:
`tmux attach -t sessionName`

Create Window:
`prefix + c`

Rename Window:
`prefix + ,`

Kill Window:
`prefix + &`

Detach:
`prefix + d`


Links to other shortcuts/cheat sheets
https://gist.github.com/MohamedAlaa/2961058
https://gist.github.com/andreyvit/2921703

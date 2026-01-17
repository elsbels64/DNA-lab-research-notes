## lining up the columns on a seg file:
1. `ggVG` to select the whole buffer (text) in visual mode
2. `!column -t` 
3. `<Enter>`

## spliting the screen:
**Horizontally**:(`:split` or `:sp` *OR* `Ctrl+w`, then `s`): Splits the screen horizontally, placing the new window on top.<br/>
**vertically**: (`:vsplit` or `:vs` *OR* `Ctrl+w`, then `v`): Splits the screen vertically, placing the new window to the left.<br/>
**two different files**: `:sp filename` or `:vs filename` to open a specific file in a new split.<br/>
### navigating between split screens:
#### **`Ctrl`+`w` +:**<br/>
`h`: Move to the left split.<br/>
`j`: Move to the below split.<br/>
`k`: Move to the top split.<br/>
`l`: Move to the right split.<br/>
`w`: Cycle through open splits. <br/>
`+`: Increase Height<br/>
`-`: Decrease Height<br/>
`>`: Increase Width<br/>
`<`: Decrease Width<br/>
`=`: Equal Size<br/>
`H`/`J`/`K`/`L` (capital letters) moves the current split to the far left, bottom, top, or right, respectively. <br/>
### exiting split screen:
**Close Current:** `Ctrl`+`w` + `q` (or `:q` inside the split).<br/>
**Close Others:** `Ctrl`+`w` + `o` (keeps only the active split). <br/>

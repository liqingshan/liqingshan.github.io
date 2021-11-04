- 条件执行
- 使用strftime()函数
- 变量

```
let currentHour = strftime("%H")
echo "currentHour is " currentHour
if currentHour < 6 + 0
    colorscheme darkblue
    echo "setting colorscheme to darkblue"
elseif currentHour < 12 + 0
    colorscheme morning
    echo "setting colorscheme to morning"
elseif currentHour < 18 +0
    colorscheme shine
    echo "setting colorscheme to shine"
else
    colorscheme evening
    echo "setting colorscheme to evening"
endif
```
- execute命令
```
let currentHour = strftime("%H")
echo "currentHour is " currentHour
if currentHour < 6 + 0
    let colorScheme = "darkblue"
elseif currentHour < 12 + 0
    let colorScheme = "morning"
elseif currentHour < 18 +0
    let colorScheme = "evening"
else
    let colorScheme = "evening"
endif
echo "setting colorscheme to " . colorScheme
execute "colorscheme " . colorScheme
```
- 定义函数
```
function SetTimeOfDayColors()
    let currentHour = strftime("%H")
    echo "currentHour is " currentHour
    if currentHour < 6 + 0
        let colorScheme = "darkblue"
    elseif currentHour < 12 + 0
        let colorScheme = "morning"
    elseif currentHour < 18 +0
        let colorScheme = "evening"
    else
        let colorScheme = "evening"
    endif
    echo "setting colorscheme to " . colorScheme
    execute "colorscheme " . colorScheme
endfunction
```
- 不错的vim取巧诀窍
```
set statusline=%{strftime(\"%c\")}
set statusline=%{strftime(\"%c\")}%=0x%B
set statusline=%{strftime(\"%c\")}%=0x%B\ \ line:%l
set statusline=%{strftime(\"%c\")}%=0x%B\ \ line:%l,\ \ col:%c:%V\ %P
```


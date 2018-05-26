---
layout: post
title:  "Ubuntu info"
permalink: /ubuntu/
categories: test post first ubuntu
---

<p><b> Добавляем </b><br>
sudo apt-get install gcc curl git mc mercurial nano openssh-server python screen bash-completion vim wget zsh sshfs ufw htop mtr cifs-utils p7zip smplayer<br>
для <b>GUI</b><br>
sudo apt-get install gnome-system-monitor doublecmd wine remmina <br>
из своих репозиториев<br>
vscode chrome notepadqq telegram atom radmin <br>
sudo apt-get install gnome-system-monitor<br>
<div><a href="http://ruunix.ru/1093-effektivnaya-rabota-v-midnight-commander.html">Эффективная работа в Midnight Commander</a></div><br>
sudo apt-get install virtualbox-guest-additions-iso  and ..-x11 and ..-utils<br>
sudo pm-hibernate<br>
<div><a href="http://askubuntu.com/questions/16371/how-do-i-disable-x-at-boot-time-so-that-the-system-boots-in-text-mode">How do I disable X at boot time so that the system boots in text mode?</a></div><br>
sudo /etc/init.d/lightdm stop<br>
<div><a href "http://askubuntu.com/questions/468359/installing-atom-text-editor-on-32-bit-ubuntu">installing-atom-text-editor-on-32-bit-ubuntu</a></div><br>
sudo usermod -aG vboxsf `whoami` или sudo usermod -aG vboxsf $(whoami) - чтобы работал exchange в virtualbox</p>
</p>

<div style="align: left;"><b>Решенные вопросы</b></div>
<div style="align: left;">Cisco VPN - есть vpnc, но не заработал </div>
<div style="align: left;">получилось только через консоль</div>
<div style="align: left;">sudo pcf2vpnc vpnname.pcf /etc/vpnc/vpnname.conf - конвертировать pcf для vpnc (для секьюрности нужно убрать пароль из конфига, будет спрашивать каждый раз)</div>
<div style="align: left;">sudo vpnc vpnname --enable-1des - запустить vpn</div>
<div style="align: left;">sudo vpnc-disconnect - остановить vpn</div>
<div style="align: left;">OpenVpn - не понятно как добавить ovpn файл через GUI</div>
<div style="align: left;">решение с консоли sudo openvpn --config vpnname.ovpn</div>
<div style="align: left;">Двойные субтитры в видео</div>
<div style="align: left;">Плейер который может показывать 2е субтитров одновременно smplayer</div>
<div style="align: left;">Запомнить куда грузились в GRUB 
 <br> &nbsp; /etc/default/grub:
 <br> &nbsp; GRUB_DEFAULT=saved
 <br> &nbsp; GRUB_SAVEDEFAULT=true
 <br> &nbsp; sudo update-grub</div>

<p><b>bash</b><br>
<b>^a ^e</b> - начало конец строки<br>
<b>M-b M-f</b> - слово назад/вперед<br>
<b>^B ^F</b> - символ назад/вперед<br>
<b>^U ^K ^Y</b> вырезать до начала/конца строки и вставить<br>
<b>M-BS M-d</b> вырезать слово слева/справа от курсора<br>
<b>^D ^H</b> delete/backspase<br>
<b>^_</b> Undo<br>
<b>^L</b>  очистить терминал<br>
<b>^T</b> поменять 2 символа местами<br>
<b>^D</b> стандартный ввод закончился<br>
<b>M-l M-u M-c</b> lower UPPER Capital case<br>
<b>^P ^N</b> назад/вперед по истории     <br>
<b>^-r</b> поиск по истории<br>
<b>M-.</b> Предыдущ аргумент</p>

<p><b>zsh</b><br>
<div><a href="https://github.com/zsh-users/zsh-syntax-highlighting">https://github.com/zsh-users/zsh-syntax-highlighting</a></div>
<div><a href="https://github.com/zsh-users/zsh-autosuggestions">https://github.com/zsh-users/zsh-autosuggestions</a></div>
<div><a href="https://github.com/popstas/zsh-command-time">https://github.com/popstas/zsh-command-time</a></div>
</p>

<p><b>vim</b><br>
<b>h, j, k, l</b> - стрелки<br>
<b>/str ?str</b> - поиск вперед/назад, далее n/N вперед/назад<br>
<b>:[range]s/old/new/[g]</b> - Заменить old на new в указанном диапазоне строк range. g - все замены без g только первая (:1,$s/old/new/g)<br>
<b>:%s/old/new</b> - замена во всем файле<br>
<b>%s/\vold/new/</b> - замена с полными возможностями регулярных выражений<br>
<b>:e!</b> — перезагрузить текущий файл<br>
<b>u / U</b> - undo / восстановить текущую строку <br>
<b>.</b> - повторить последнее действие<br>
<b>x/X</b> - удалить символ под курсором/слева от курсора<br>
<b>i / a / A</b> - в режим редактирования в/за  текущей позиции в конце строки<br>
<b>yy / dd </b> - копировать/удалить строку<br>
<b>p</b> - вставить<br>
<b>J</b> - склеить две строки<br>
<b>:wq shift+ZZ</b> - сохранить и выйти<br>
<b>:q!</b> - выйти без сохранения<br>
<b>:r</b> - вставить из другого файла<br>
<b>:r!</b> - вставить вывод комманды<br>
<b>:!./%</b> - выполнить файл, который сейчас редактируем<br>
<b>:set [no]nu</b> - включить/выключить <br>
<b>:syntax on/off </b>вкл/выкл подсветку синтаксиса<br>
<b>^g</b> - статус файла<br>
<br>
<b>.vimrc</b><br>
colorscheme darkblue<br>
set showmatch<br>
set hlsearch<br>
set incsearch<br>
set ignorecase<br>
set nu<br>
set ffs=unix,dos,mac<br>
set fencs=utf-8,cp1251,cp866,koi8-r,ucs-2<br>
set tabstop=4<br>
set shiftwidth=4<br>
set smarttab<br>
set expandtab<br>
set smartindent<br>
if !has('gui_running')<br>
set mouse=<br>
endif<br>
</p>
<div><br/></div>
<div><b>ssh-agent</b></div>
<div>ssh-agent - хранилище ключей, pagent - это аналог ssh-agent в windows</div>
<div>Запустить его до до X server - положить в .xsessionrc (cmod +x):</div>
<div> &nbsp; &nbsp; #!/bin/bash</div>
<div> &nbsp; &nbsp; eval `ssh-agent -t 3600`</div>
<div>ssh-add - загрузить в агент ключи (-l список загруженных ключей -D выгрузить ключи)</div>
<div><br/></div>
<div><b>i3 тайловый оконный мененджер</b></div>
<div><a href="http://i3wm.org/">http://i3wm.org/</a>&nbsp;сайт i3</div>
<div><a href="http://i3wm.org/docs/userguide.html">http://i3wm.org/docs/userguide.html</a>&nbsp;userguide</div>
<div><a href="https://ru.wikipedia.org/wiki/Фреймовый_оконный_менеджер">https://ru.wikipedia.org/wiki/Фреймовый_оконный_менеджер</a>&nbsp;Тайловый оконный</div>
<div><a href="https://ru.wikipedia.org/wiki/I3">https://ru.wikipedia.org/wiki/I3</a>&nbsp;Тайловый оконный i3</div>
<div><a href="http://help.ubuntu.ru/fullcircle/37/top5_37">http://help.ubuntu.ru/fullcircle/37/top5_37</a>&nbsp;ТОП 5: Фреймовые оконные менеджеры</div>
<div><a href="https://habrahabr.ru/post/150100/">https://habrahabr.ru/post/150100/</a>&nbsp;Тайловый оконный менеджер i3 хабр</div>
<div><a href="https://wiki.archlinux.org/index.php/i3_(Русский)">https://wiki.archlinux.org/index.php/i3_(Русский)</a> &nbsp;Тайловый оконный менеджер i3 Arch</div>
<div>
<br/></div>
<div>setxkbmap -option &quot;grp:caps_toggle,grp_led:scroll&quot; - переключение языка по capslock</div>
<div>
<br/></div>
<div>~/.config/i3/config - конфиг</div>
<div><br/></div>
<div>по умолчанию mod -&nbsp;это win</div>
<div><b>mod+Enter</b> открывает терминал</div>
<div><b>mod+d</b> запускает dmenu (меню сверху экрана, которое по мере ввода с клавиатуры названия приложения предлагает варианты для запуска)</div>
<div><b>mod+Shift+Q</b> закрывает активное окно</div>
<div><br/></div>
<div><b>mod+v</b> включает режим вертикального тайлинга (экран будет делиться горизонтально)</div>
<div><b>mod+h</b> включает режим горизонтального тайлинга (экран будет делиться вертикально)</div>
<div><b>mod+w</b> включает режим вкладок (каждое окно на рабочем столе занимает весь экран, сверху видны вкладки)</div>
<div><b>mod+s</b> включает стековый режим (заголовки окон один под другим, каждое окно занимает весь экран)</div>
<div><b>mod+e</b> возвращает стандартный режим</div>
<div><b>mod-f</b> full mode</div>
<div><b>mod-r</b> resize mode</div>
<div><b>
<br/></b></div>
<div><b>mod+Shift+Space</b> переключает окно в режим плавающего и обратно</div>
<div><b>mod+Space</b> переключение между плавающим и тайловыми окнами</div>
<div>
<br/></div>
<div><b>mod+Left/Right/Up/Down</b> перемещает фокус в пределах рабочего стола (также можно jkl;)</div>
<div><b>mod+Shift+Left/Right/Up/Down</b> перемещает текущее окно в пределах рабочего стола</div>
<div>
<br/></div>
<div><b>mod+1</b> и т.д. переключает на рабочий стол с указанным номером</div>
<div><b>mod+Shift+1</b> и т.д. перемещает окно рабочий стол с указанным номером</div>
<div>
<br/></div>
<div><b>mod+Shift+C</b> читает настройки из файла конфигурации</div>
<div><b>mod+Shift+r</b> restart</div>
<div><b>mod+Shift+E</b> выходит из i3wm на экран ввода имени пользователя и пароля</div>
<div><br/></div>
<div><b>screen</b></div>
<div>screen -ls список</div>
<div>screen -r <сессия> вернуться в сессию</div>
<div>screen -x <сессия> подключиться в ту же сессию чтобы видеть, что происходит в данный момент на экране (логиниться нужно под тем же пользователем)</div>
<div><b>Сочетание Описание</b></div>
<div><b>Ctrl+a, ?</b>     Помощь</div>
<div><b>Ctrl+a, c</b>     Создать новое окно в текущей сессии screen</div>
<div><b>Ctrl+a, d</b>     Отключиться от текущей сессии screen. Все сессии в screen остаются в рабочем состоянии.</div>
<div><b>Ctrl+a, "</b>     Показать список окон в текущей сессии screen</div>
<div><b>Ctrl+a, '</b>     Переключиться на окно по номеру</div>
<div><b>Ctrl+a, n</b>     Переключиться на следующее окно</div>
<div><b>Ctrl+a, p</b>     Переключиться на предыдущее окно</div>
<div><b>Ctrl+a, Shift+a</b>     Переименовать текущее окно</div>
<div><b>Ctrl+a, k</b>     Закрыть текущее окно screen</div>
<div><b>Ctrl+a, w</b>     Перечислить списком все окна</div>
<div><b>Ctrl+a, ESC</b> Copy mode <b>SPACE</b> начать/закончить выделение <b>Ctrl-a ]</b> вставить</div>
<div><b>tmux</b></div>
<div>tmux a - Подключиться</div>
<div>tmux detach  - Отключиться</div>
<div>tmux ls - list session</div>
<div>tmux set-option mouse on - поддержка мыши</div>
<div><b>Команды</b>
<div><b>C-b ?</b> - help</div>
<div><b>C-b w</b> - list window</div>
<div><b>C-b s</b> - list session</div>
<div><b>C-b "</b> - Горизонтальный сплит</div>
<div><b>C-b %</b> - Вертикальный сплит</div>
<div><b>C-b стрелки</b> - Ходить между frame</div>
<div><b>C-b C-o</b> - поменять frame местами</div>
<div><b>C-b o</b> - next frame</div>
<div><b>C-b { }</b> - Move frame Up/Down</div>
<div><b>C-b Alt-Стрелки</b> - Изменить размер фрейма</div>
<div><b>C-b Space</b> - выровнять frame</div>
<div><b>C-b t</b> - Часы</div>
<div><b>C-b r</b> - redraw</div>
<div><b>C-b c</b> - create window</div>
<div><b>C-b 0-9</b> - select window</div>
<div><b>C-b [</b> - start copy mode (Vim/emax mode Space/C-Space - begin-selection Enter/M-w copy-selection)</div>
<div><b>C-b ]</b> - past</div>
<div><br/></div>
<div><b>Коммандная строка в неочевидных местах</b></div>
<div><b>pacmd</b> - управление звуком (см list-sinks list-sink-inputs pacmd set-default-sink 4)</div>
<div> &nbsp; &nbsp;  pacmd list-sink-inputs | grep -E 'index|sink:|client:' ; echo "***";  pacmd list-sinks | grep -E 'index|name:'</div>
<div> &nbsp; &nbsp;  pacmd move-sink-input 123 2</div>
<div> &nbsp; &nbsp;  set-default-sink 4</div>

<div><b>alsamixer</b> - регулировка громкости звука</div>
<div><b>bluetoothctl</b> - настройка bluetooth</div>
<div><b>xclip</b> - работа с clipboard из сомандной строки</div>

<br/></div>

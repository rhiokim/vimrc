rhio.kim's vimrc
============
Author: Tsung-Hsiang (Sean) Chang <vgod@vgod.tw>

Fork me on GITHUB  https://github.com/vgod/vimrc.

ONE-STEP INSTALL
----------------

Mac OS X 에서 설치:

     curl -o - https://raw.github.com/vgod/vimrc/master/auto-install.sh | sh

UNIX 에서 설치:

     wget -O - https://raw.github.com/vgod/vimrc/master/auto-install.sh | sh


MANUALLY INSTALL
----------------

1. Check out from github

        git clone git://github.com/vgod/vimrc.git ~/.vim
        cd ~/.vim
        git submodule update --init

2. Install ~/.vimrc and ~/.gvimrc

        ./install-vimrc.sh

3. (Optional, if you want Command-T) Compile the Command-T plugin

        cd .vim/bundle/command-t/ruby/command-t
        ruby extconf.rb
        make
  
설치 & 플러그인 설치 및 추가
--------------------------------

All plugins (except vim-latex) were checked out as git submodules, 
which can be upgraded with `git pull`. For example, to upgrade Command-T 

     cd ~/.vim/bundle/command-t
     git pull

To install a new plugin as a git submoudle, type the followin commands.

     cd ~/.vim
     git submodule add [GIT-REPOSITORY-URL] bundle/[PLUGIN-NAME]

사용법
----------

see the "USEFUL SHORTCUTS" section in vimrc to learn my shortcuts.

플러그인
-------

* [Pathogen](http://www.vim.org/scripts/script.php?script_id=2332): Perl 자동완성 플러그인 ~/.vim/bundle.

* [Nerd Tree](http://www.vim.org/scripts/script.php?script_id=1658): 파일 관리자 대체 플러그인 .

  Useful commands:
  * `:Bookmark [name]` - bookmark any directory as name
  * `:NERDTree [name]` - open the bookmark [name] in Nerd Tree

* [AutoClose](http://www.vim.org/scripts/script.php?script_id=1849):  괄호나 인용부호의 닫는 괄호를 자동으로 입력

* [vim-surround](https://github.com/tpope/vim-surround/blob/master/doc/surround.txt): deal with pairs of surroundings.

* [matchit](http://www.vim.org/scripts/script.php?script_id=39): %는 기본적으로 단일 문자 괄호 쌍을 찾아가는 단축키인데, 이 플러그인을 사용하면, hTML, XML 및 괄호외의 시작/끝 문자열을 사용하는 언어들의 쌍을 찾아가기가 가능하다.  

* [xmledit](http://www.vim.org/scripts/script.php?script_id=301): XML/HTML 태그 자동완성.

* [Command-T](https://github.com/wincent/Command-T): 파일 브라우징을 위한 플러그인 `cmd-t`.  

* [SuperTab](http://www.vim.org/scripts/script.php?script_id=1643): 이전에 입력한 단어를 기억해서 다시 입력할 수 있도록 해주는 플러그인.

* [snipMate](http://www.vim.org/scripts/script.php?script_id=2540): TextMate 스타일의 snippets 플러그인 

  `:help snipMate` to see more info.
  cast : http://vimeo.com/3535418

* [YankRing](http://www.vim.org/scripts/script.php?script_id=1234): Copy/Cut 레지스터 플러그인, vim에서 9개의 최근 삭제한 것을 기억하는 플러그인
  
  `:help yankring` to see more info.

* [VisIncr](http://www.vim.org/scripts/script.php?script_id=670): 일반적인 문자, 날짜, 로마 숫자등의 증/감 열을 삽입해주는 플러그인.
  
* [Cute Error Marker](http://www.vim.org/scripts/script.php?script_id=2653): showing error and warning icons on line.
  
   Note: MacVim users need to enable "Use experimental renderer" to see
   graphical icons.

* [vim-latex](http://vim-latex.sourceforge.net/): Latex support.

* [OmniCppComplete](http://www.vim.org/scripts/script.php?script_id=1520): C/C++ 자동완성 플러그인.

* [JavaComplete](http://www.vim.org/scripts/script.php?script_id=1785): Java 자동완성 플러그인.

* [EasyMotion](https://github.com/Lokaltog/vim-easymotion): An easy way to jump to a word.

* [JSLint](http://github.com/rhio.kim/jslint.vim): VIM 용 JSLint 플러그인 

* [jQuery](http://www.vim.org/scripts/script.php?script_id=2416): jQuery 구문 완성 플러그인

Language specific supports
--------------------------

* Latex: Read `:help latex-suite.txt`
* Restructured Text: `ctrl-u 1~5` inserts Part/Chapter/Section headers
* HTML, Javascript, Python, CSS, C, C++, Java: use `TAB` to do omni-completion.
* HTML/XML: End tags are automatically completed after typing a begin tag. (Typing > twice pushes the end tag to a new line.)

참고 자료
---------------------

* http://amix.dk/vim/vimrc.html
* http://spf13.com/post/perfect-vimrc-vim-config-file

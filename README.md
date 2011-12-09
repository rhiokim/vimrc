#rhio.kim's vimrc

Author: Rhio.kim <rhio.kim+github@gmail.com> 

Fork on GITHUB  https://github.com/rhiokim/vimrc

원작자 http://github.com/vgod/vimrc

##쉬운 설치

Mac OS X 에서 설치:

     curl -o - https://raw.github.com/rhiokim/vimrc/master/auto-install.sh | sh

UNIX 에서 설치:

     wget -O - https://raw.github.com/rhiokim/vimrc/master/auto-install.sh | sh


##수동 설치

1. github 에서 체크아웃

        git clone git://github.com/rhiokim/vimrc.git ~/.vim
        cd ~/.vim
        git submodule update --init

2. ~/.vimrc 과 ~/.gvimrc 설치

        ./install-vimrc.sh

3. (옵션, Command-T 설치) Command-T 플러그인 설치 

        cd .vim/bundle/command-t/ruby/command-t
        ruby extconf.rb
        make
  
##설치 & 플러그인 설치 및 추가

vim-latex 를 제외한 모든 플러그인은 서브 모듈로 체크아웃 받도록 되어있고 
`git pull` 명령어로 업그레이드 할 수 있다. 예를 들어 COmmand-T 를 업그레이드 받으려면
다음과 같이 하면 된다.

     cd ~/.vim/bundle/command-t
     git pull

새로운 플러그인을 설치하기 위해서는 git submodlue 를 아래와 같이 사용하세요.

     cd ~/.vim
     git submodule add [GIT-REPOSITORY-URL] bundle/[PLUGIN-NAME]

##사용법

제가 설정해 놓은 단축키 옵션을 배우려면 vimrc 에 "USEFUL SHORTCUTS" 부분을 보시면 됩니다.

##옵션
###커서행 하이라이팅
 보통에 set cursorline로 설정하면 창을 분할하면 포커스가 없는 창이 강조되었다. 때문에 현재 창만 하이라이팅 하기 위해 다음과 같이 설정할 수 있다.
      "커서를 강조
      set cursorline

      "현재 윈도우에 테두리 그리기
      augroup cch
         autocmd! cch
         autocmd WinLeave * set nocursorline
         autocmd WinEnter, BufRead * set cursorline
      augroup END

      : hi clear CursorLine
      : hi CursorLine gui=underline
      highlight CursorLine ctermbg=black guibg=black

##플러그인

* [Pathogen](http://www.vim.org/scripts/script.php?script_id=2332): 플러그인 메니저 플러그인. 플러그인 런타인 패스를 `~/.vim/bundle` 으로 설정한다.
  참조 :
  * [vundle](http://kldp.org/node/125263): vim 라이브러리를 git 기반으로 지정하여 플러그인으로 사용할 수 있다.

* [Nerd Tree](http://www.vim.org/scripts/script.php?script_id=1658): 파일 관리자 대체 플러그인 .

  유용한 명령어:
  * `:Bookmark [name]` - 지정한 이름으로 디렉토리를 북마크한다.
  * `:NERDTree [name]` - 지정한 북마크 [name] NERDTree 에서 오픈한다. 

* [AutoClose](http://www.vim.org/scripts/script.php?script_id=1849):  괄호나 인용부호의 닫는 괄호를 자동으로 입력

* [vim-surround](https://github.com/tpope/vim-surround/blob/master/doc/surround.txt): deal with pairs of surroundings.

* [matchit](http://www.vim.org/scripts/script.php?script_id=39): %는 기본적으로 단일 문자 괄호 쌍을 찾아가는 단축키인데, 이 플러그인을 사용하면, hTML, XML 및 괄호외의 시작/끝 문자열을 사용하는 언어들의 쌍을 찾아가기가 가능하다.  

* [xmledit](http://www.vim.org/scripts/script.php?script_id=301): XML/HTML 태그 자동완성.

* [Command-T](https://github.com/wincent/Command-T): 파일 브라우징을 위한 플러그인 `cmd-t`.  

* [SuperTab](http://www.vim.org/scripts/script.php?script_id=1643): 이전에 입력한 단어를 기억해서 다시 입력할 수 있도록 해주는 플러그인.

* [snipMate](http://www.vim.org/scripts/script.php?script_id=2540): TextMate 스타일의 snippets 플러그인 

  `:help snipMate` 사용법을 표시.
  동영상 : http://vimeo.com/3535418

* [YankRing](http://www.vim.org/scripts/script.php?script_id=1234): Copy/Cut 레지스터 플러그인, vim에서 9개의 최근 삭제한 것을 기억하는 플러그인
  
  `:help yankring` 도움말 표시.

* [VisIncr](http://www.vim.org/scripts/script.php?script_id=670): 일반적인 문자, 날짜, 로마 숫자등의 증/감 열을 삽입해주는 플러그인.
  
* [Cute Error Marker](http://www.vim.org/scripts/script.php?script_id=2653): 에러나 경고 아이콘 표시 플러그인.
  
   Note: MacVim 유저의 경우에는 "Use experimental renderer" 을 사용함으로 설정해야 한다.

* [vim-latex](http://vim-latex.sourceforge.net/): Latex 제공 플러그인.

* [OmniCppComplete](http://www.vim.org/scripts/script.php?script_id=1520): C/C++ 자동완성 플러그인.

* [JavaComplete](http://www.vim.org/scripts/script.php?script_id=1785): Java 자동완성 플러그인.

* [EasyMotion](https://github.com/Lokaltog/vim-easymotion): 손쉬운 단어 점프 플러그인.

* [JSLint](http://github.com/rhio.kim/jslint.vim): VIM 용 JSLint 플러그인 

* [jQuery](http://www.vim.org/scripts/script.php?script_id=2416): jQuery 구문 완성 플러그인

* [zencoding-vim](http://mattn.github.com/zencoding-vim/): HTML,CSS zencoding 플러그인

* [fecompressor](http://www.vim.org/scripts/script.php?script_id=3453): YUI Compressor, Closure Compiler, UglifyJS, SASS, LESS 자동 실행 플러그인

* [gist-vim](http://www.vim.org/scripts/script.php?script_id=2423): gist 를 위한 플러그인 

   `usage`:
   * [https://github.com/rhiokim/gist-vim] (https://github.com/rhiokim/gist-vim)

   `auth`: Vim 에서 github.com 인증환경 
   
      $ vi ~/.bashrc or ~/.bash_profile
      #github.com
      git config --global github.user "[your user.name]" 
      git config --global github.token "[your api token]"

* [cocoa.vim](https://github.com/pekepeke/cocoa.vim): Cocoa/Objective-C 플러그인

* [vimtodo](https://github.com/mivok/vimtodo): Vim TODO 관리 플러그인

* [neocomplcache](https://github.com/Shougo/neocomplcache)

* [markdown-preview](https://github.com/mkitt/markdown-preview.vim.git): 브라우저 기반 markdown 미리보기 플러그인
   - deprecated

##색상 테마
* [Tomorrow Theme](http://github.com/ChrisKempson/Tomorrow-Theme)
* [Solarized Colorscheme for Vim](https://github.com/altercation/vim-colors-solarized)
1. install
      $ git submodule add git://github.com/altercation/vim-colors-solarized.git ~/.vim/bundle
2. setup
   - dark background mode of Solarized
   
```js
syntax enable
set background=dark
colorscheme solarized
```

   - light background mode of Solarized

```js
syntax enable
set background=light
colorscheme solarized
```

##특수한 기능 제공

* Latex: 일기 기능 `:help latex-suite.txt`
* Text 재 구조화 작업 : `ctrl-u 1~5` Part/Chapter/Section 헤더 추가하기 
* HTML, Javascript, Python, CSS, C, C++, Java: `TAB` 을 이용한 자동완성.
* HTML/XML: 시작 태그가 열리면 끝 태그를 자동으로 완성해주는 기능 . ( > 을 두번 연속 타이핑하면 새로운 라인에 닫는 태크를 생성한다. )

##참고 자료

* http://amix.dk/vim/vimrc.html
* http://spf13.com/post/perfect-vimrc-vim-config-file
* http://d.hatena.ne.jp/yuroyoro/20101104/1288879591 

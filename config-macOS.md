#### homebrew
```bash
# 설치
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### zsh 
```bash
# 설치
brew install zsh
```

#### oh-my-zsh
```bash
# 설치
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

#### .zshrc
```bash
# 설치
vi ~/.zshrc

# .zshrc 수정
ZSH_THEME="agnoster"
prompt_context() {
  if [[ "$USER" != "$DEFAULT_USER" || -n "$SSH_CLIENT" ]]; then
    prompt_segment black default "%(!.%{%F{yellow}%}.)$USER"
  fi
}
```

#### agnoster
```bash
# 설치
vi ~/.oh-my-zsh/themes/agnoster.zsh-theme

# agnoster.zsh-theme 수정
build_prompt() {
  RETVAL=$?
  prompt_status
  prompt_virtualenv
  prompt_context
  prompt_dir
  prompt_git
  prompt_bzr
  prompt_hg
  prompt_newline //이부분을 추가 꼭 순서 지켜서
  prompt_end
}
prompt_newline() {
  if [[ -n $CURRENT_BG ]]; then
    echo -n 
"%{%k%F{$CURRENT_BG}%}$SEGMENT_SEPARATOR
%{%k%F{blue}%}$SEGMENT_SEPARATOR"
  else
    echo -n "%{%k%}"
  fi
  echo -n "%{%f%}"
  CURRENT_BG=''
}
```

#### zsh-syntax-highlighting
```bash
# 설치
brew install zsh-syntax-highlighting

# 플러그인 적용
source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh 
```

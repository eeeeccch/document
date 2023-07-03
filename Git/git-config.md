# config 
```bash
# git에서 설정한 항목 확인
git config --list 

#  기본 에디터 설정 (--wait : 설정을 저장할때까지 커멘드 창을 사용할 수 없음)
git config --global core.editor "your editor"
git config --global core.editor "your editor --wait"
git config --global user.name "your name"
git config --global user.email "your email"

# OS별 CRLF 개행문자 차이로 인한 문제 해결(실제 코드는 변경된게 없는데 소스의 개행문자 차이로 변경으로 착각)
# Windows에서는 `CRLF`를 사용
# Linux, OSX는 `LF`를 사용 
# core.autocrlf "false" // 시스템이나 저장소의 방법을 따른다.   
# core.autocrlf "true"  // 윈도우 추천 : text file을 object database에 넣기전에 CRLF를 LF 로 변경한다.  
# core.autocrlf "input" // 맥 추천 : LF를 line ending으로 사용한다.
git config --global core.autocrlf $(option)

# EOL (end of line)
# core.eol "native" // 시스템에서 line ending를 처리하는 방법에 따른다.   
# core.eol "crlf"   // CRLF 를 line ending 으로 사용한다.  
# core.eol "lf"     // LF를 line ending 으로 사용한다.   
git config --global core.eol $(option)
```

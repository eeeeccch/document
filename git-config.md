# EOL (end of line)
> Windows에서는 `CRLF` 를 사용하고 Linux, OSX는 `LF` 만 사용한다. 
> 실제 코드는 변경된 게 없는데 소스의 CR/LF 때문에 변경으로 착각하여 commit을 하게 될 수 있다.

`core.eol = native`(default) 시스템에서 line ending를 처리하는 방법에 따른다.   
`core.eol = crlf` CRLF 를 line ending 으로 사용한다.  
`core.eol = lf` LF를 line ending 으로 사용한다.   

### core.autocrlf
`core.autocrlf = false` (default) 시스템이나 저장소의 방법을 따른다.   
`core.autocrlf = true` text file을 object database 에 넣기전에 CRLF 를 LF 로 변경한다.  
`core.autocrlf = input` LF를 line ending 으로 사용한다.  

> 아래의 설정으로, OS별 CRLF 차이로 인한 commit을 방지할수 있다.
#### Windows
```bash
git config --global core.autocrlf true
```

#### OSX, Linux
```bash
git config --global core.autocrlf input
```

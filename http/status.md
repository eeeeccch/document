# 알아두면 좋은 HTTP 상태 코드 요약

## 1xx Informational
#### 100 : Continue
> `Expect:100-countinue`를 보내고 서버는 이를 처리할수 있으면 이 코드로 응답

#### 101 : Switching Protocol
> 프로토콜을 `HTTP 1.1`에서 업그레이드할 때 Upgrade 응답 헤더에 표시(현재는 `HTTP 1.1`이 최신)

#### 102 : Processing
> 서버가 처리하는데 오랜 시간이 예상되어 클라이언트에서 타임아웃이 발생하지 않도록 이 응답 코드를 보냄

## 2xx Success
#### 200 : OK
> 클라이언트가 요청한 동작을 수신하였고 성종적으로 처리

#### 201 : Created
> 응답이 처리되어 새로운 리소스가 생성
응답 헤더 Location에 새로운 리소스의 절대 URI를 기록

#### 202 : Accepted
> 요청은 접수하였으나, 처리가 완료되지 않음

#### 203 : Non-Authoritative Information
> 응답 헤더가 오리지널 서버로부터 제공된 것이 아님

#### 204 : No Content
> 처리를 성공하였으나 클라이언트에게 리턴할 콘텐츠가 없음

#### 205 : Reset Content
> 처리를 성공하였고 브라우저의 화면을 리셋

#### 206 : Partial Content
> 콘텐츠의 일부분만 보냄 응답헤어의 `Content-Range`에 응답 콘텐츠의 범위를 기록 (예를들어 1,500바이트의 리소스 중에서 처음 500바이트만 보낼때 사용)

## 3xx Redirection
#### 300 : Multiple Choices
#### 301 : Moved Permanently
#### 302 : Found
#### 303 : See Other
#### 304 : Not Modified
#### 305 : Use Proxy
#### 306 : (Unused)
#### 307 : Temporary Redirect

## 4xx 클라이언트 에러 응답
#### 400 : Bad Request
> 요청의 구문이 잘못

#### 401 : Unauthorized
> 지정한 리소스에 대한 권한 없음

#### 403 : Forbidden
> 지정한 리소스에 대한 액세스가 금지

#### 404 : Not Found
> 지정한 리소스를 찾을수 없음

#### 405 : Method Not Allowed
> 요청한 URI가 지정한 메소드를 지원하지 않음

#### 408 : Request Timeout
> 요청을 기다리다 서버에서 타임아웃 발생

## 5xx 서버 에러 응답
#### 500 : Internal Server Error
> 내부 서버 오류 서버에 에러가 발생하였다.
클라이언트가 모르는 5xx 계열의 응답 코드가 반환된 경우에도 클라이언트는 500과 동일하게 처리하도록 규정하고 있습니다.

##### 501 : Not Implemented
> 구현되지 않음	요청한 URI의 메소드에 대해 서버가 구현하고 있지 않다.

#### 502 : Bad Gateway
> 불량 게이트웨이 게이트웨이 또는 프록시 역할을 하는 서버가 그 뒷단의 서버로부터 잘못된 응답을 받았다.

#### 503 : Service Unavailable
> 서비스 제공불가 현재 서버에서 서비스를 제공할 수 없다. 보통은 서버의 과부하나 서비스 점검 등 일시적인 상태입니다.

#### 504 : Gateway Timeout
> 게이트웨이 시간초과 게이트웨이 또는 프록시 역할을 하는 서버가 그 뒷단의 서버로부터 응답을 기다리다 타임아웃이 발생하였다.
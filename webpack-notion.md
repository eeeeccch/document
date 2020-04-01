### Webpack?
Webpack 은 최신 javascript 응용 프로그램을 위한 정적 모듈 번들러
- module : 프로그램을 구성하는 일부요소 또는 기능별로 나뉘어지는 프로그램
- bundler : 지정한 단위로 파일들을 하나로 만들어주는 역할을 수행

<br>
 
### Webpack 핵심 개념
**Entry**
> Webpack은 모든 애플리케이션에 대한 종속성 그래프를 작성하고 이 그래프의 시작점을 Entry Point라고 한다.
> 이 Entry Point를 통해 모듈이 어디서부터 시작하는지를 명세하는 애플리케이션을 시작하는 첫 번째 파일로 나타낼 수 있다.

<br>

**Output**
> Output은 모든 애플리케이션의 자산(resources 또는 assets)을 하나의 Bundle로 묶었으면 해당 Bundle을 처리하는 방법을 명세한다.

<br>

**Loader**
> Loader는 사전에 처리할 작업을 나타내며 css, html, jpg, scss 등의 자산을 하나의 모듈로 취급하며 이러한 파일들을 종속성 그래프에 추가할 때 모듈로 변환한다.

<br>

**Plug-In**
> Plug-In은 일반적인 Compile 또는 모듈 처리에 필요한 작업 및 사용자 정의 기능을 수행하는데 사용한다.

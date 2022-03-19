# GitHub Site
## Meta 태그
`기본적인 정보`를 브라우저나 검색 엔진이 인지하도록 설정<br />
브라우저에 노출 되지 않고, `내부적으로 확인하는 용도` 
```
<meta name="제작자" content="제작자명" >
<meta name="설명" content="페이지에 대한 설명">
```
### viewport
작성한 레이아웃이 `화면 상으로 보이는 전체 영역`  

```
<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no, maximum-scale=1, minimum-scale=1">
```

| 속성 | 의미 | 
|:--:|--|
| `width=device-width` | `해당 디바이스의 가로 너비`를 그대로 사용하겠다.|
| `initial-scale=1.0` | 디바이스의 `초기 화면 배율` <br/>(=첫 화면 확대/축소❌)|
| `user-scalable=no`  | 사용자가 손가락으로 `확대/축소 가능 여부` <br/> (확대/축소 시 레이아웃에 문제가 생기는 것을 막기 위함)|
|`maximum-scale=1`<br/>`minimum-scale=1`|확대/축소 `최대/최소 배율 값`<br/> (최대/최소값을 고정시키며 확대 축소 가능 여부 원천 봉쇄)|

### IE (Internet Explorer) 
IE 8버전 이상인 `최신 표준 모드로 렌더링` <br />
```
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```
> 

### Open Graph & Twitter Card
* 외부에 제공할 특정한 정보를 정의<br />
* 특정 페이지가 공유 될 때 외부에서 판단할 수 있는 정보를 content 에서 확인한다.
* 사이트명 / 설명 / 대표 이미지 / 주소
```
<!-- 트위터 카드는 개요(summary)  -->
<meta property="twitter:card" content="summary">
<meta property="twitter:site" content="GitHub">
```

#### `og` : Open Graph
* Facebook에서 주로 활용

#### `Twitter Card`
* twitter에서 주로 사용

> 이외에 사이트에서 무엇을 사용할지 알 수 없으므로 둘 다 정의 하는 것이 좋다.

<br>

***

<br>

## Favicon (Favorite Icon)
* 사이트를 대표하는 아이콘 
```
<link rel="icon" href="favicon.png">
```
> 외부에 있는 리소스를 가져오는 `<link>`
* 스마트폰 환경  
```
<link rel="apple-touch-icon" href="favicon.png">
```
> 관계 부분 `rel="apple-touch-icon"`  (애플/안드로이드 공용)

* IE 환경  
    * IE ➡ `.ico`
    * 다른 브라우저 ➡ `.png`
```
<link rel="shortcut icon" type="image/x-icon" href="favicon.ico">
```
> `루트 환경에 .ico` 존재한다면 생략 가능 

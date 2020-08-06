# Table

### Index Page

[https://yo-onhye.github.io/00.web-accessibility/02.table/table_index.html](https://yo-onhye.github.io/00.web-accessibility/02.table/table_index.html)

### 참고 사항

- table에는 caption으로 반드시 테이블 설명을 제공해야 한다.
- 제목 셀과 내용 셀을 연결해야한다.
- 스크롤 테이블의 경우, 스크롤의 넓이가 inner table의 넓이에 포함되기 때문에 좌우 선이 있을 경우 넓이가 안맞을 수 있다.

### 이슈 사항
인쇄 페이지가 2페이지 이상이고 table에 rowspan이 있을 경우 print할때 border가 사라짐

[참고페이지](https://onedrive.live.com/redir?resid=CE77114661B07FD%21104&page=Edit&wd=target%28Hivelab%20works%202018.one%7C1fdd5602-1e4c-5343-85b2-20237ccc14f9%2F%5B2017.09.18~09.22%5D%7C9819529c-e0ef-436d-b217-a1a894d8c1fe%2F%29)

```
<style>

	/* ie 전용(css hack 이용) : value 값에 \9를 붙이면 특정 ie에만 적용됨 */

	/* 자세한 css hack은 "http://codemug.com/html/css-hacks-for-ie6ie7ie8ie9-and-ie10/" 참조 */

	/* 기본적으로 table의 border 속성을 우선으로 하여 */

	/* border가 있을 경우 일차적으로 셀의 outline을 그린다 */

	/* border가 0일 경우 outline을 없앤다. */

	/* 이 두 라인의 경우 순서가 중요하기 때문에 순서를 바꾸면 안됨!! */

	/* 속성을 비교할때는 비교값이 반드시 '반따옴표' or "쌍따옴표"로 묶여있어야 함 */

	 

	.ttt table[border] th, .ttt table[border] td {outline:#000 solid thin\9;}

	.ttt table[border="0"] th, .ttt table[border="0"] td {outline-width:0px\9;}

	.ttt td { padding:10px; }

</style>

<body style="margin:0px;padding:0px;" class="ttt">

	<table class="table" border='1' cellpadding="0" cellspacing="0">

	<tr>

```
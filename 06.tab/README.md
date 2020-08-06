# Tab

### Index Page

[https://yo-onhye.github.io/00.web-accessibility/06.tab/tab_index.html](https://yo-onhye.github.io/00.web-accessibility/06.tab/tab_index.html)

### tab UI 접근성 준수 방법

1. 탭 - 탭패널, 탭 - 패널 구조로 시맨틱하게 작업한다.

2. 탭과 탭 패널의 구조를 나누되 탭 패널에 탭 제목을 헤딩테그로 부여한다.

3. aria속성을 사용하여 탭과 탭패널을 연결시켜준다. 

```
<div role="tablist" aria-label="Entertainment">
    <button role="tab"
            aria-selected="true"
            aria-controls="nils-tab"
            id="nils">
      Nils Frahm
    </button>
    <button role="tab"
            aria-selected="false"
            aria-controls="agnes-tab"
            id="agnes"
            tabindex="-1">
      Agnes Obel
    </button>
    <button role="tab"
            aria-selected="false"
            aria-controls="complexcomplex"
            id="complex"
            tabindex="-1"
            data-deletable="">
      Joke
    </button>
  </div>
  <div tabindex="0"
       role="tabpanel"
       id="nils-tab"
       aria-labelledby="nils">
    <p>
      Nils Frahm is a German musician, composer and record producer based in Berlin. He is known for combining classical and electronic music and for an unconventional approach to the piano in which he mixes a grand piano, upright piano, Roland Juno-60, Rhodes piano, drum machine, and Moog Taurus.
    </p>
  </div>
  <div tabindex="0"
       role="tabpanel"
       id="agnes-tab"
       aria-labelledby="agnes"
       hidden="">
    <p>
      Agnes Caroline Thaarup Obel is a Danish singer/songwriter. Her first album, Philharmonics, was released by PIAS Recordings on 4 October 2010 in Europe. Philharmonics was certified gold in June 2011 by the Belgian Entertainment Association (BEA) for sales of 10,000 Copies.
    </p>
  </div>
  <div tabindex="0"
       role="tabpanel"
       id="complexcomplex"
       aria-labelledby="complex"
       hidden="">
    <p>
      Fear of complicated buildings:
    </p>
    <p>
      A complex complex complex.
    </p>
  </div>

```
출처 : https://www.w3.org/TR/wai-aria-practices-1.1/examples/tabs/tabs-1/tabs.html

[기타] 현재 보조기기에서 탭에 접근 시 방향키로 제어할 수 있다는 안내문구가 나오고 있어 js를 이용해 해당 기능을 구현하는 것이 좋다.
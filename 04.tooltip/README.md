# Tooltip

### Index Page

[https://yo-onhye.github.io/00.web-accessibility/04.tooltip/tooltip_index.html](https://yo-onhye.github.io/00.web-accessibility/04.tooltip/tooltip_index.html)

### 기능 구현

- 보조기기로 접근 시 버튼 다음 툴팁 내용이 읽혀야 하기 때문에 구조를 툴팁 버튼 다음 툴팁 레이어 순으로 배치
- 사용자가 툴팁을 열고 닫지 않았을 때, 다음 컨텐츠 내용을 가리는 이슈가 있어 툴팁 레이어 내 레이어를 닫을 수 있는 버튼 제공

**접근성 오픈 아카데미때 받았던 피드백 적용**
- 버튼에 포커스 이동 시 툴팁이 열린다면 열린 상태를 대체텍스트로 전달해야함. 사용자가 레이어를 열 수 있도록 구현하는 것이 베스트.
- `role="tooltip"`을 제공하고, `aria-describedby`를 사용하여 연결해주는 것이 좋을 것 같다.


# vscode 확장프로그램인 prettier 사용법

구글에 vscode prettier 등으로 검색하면 사용법이 많이 나오나, 세팅법이 제각각이라 제일 쉬운 세팅법을 작성해보았습니다.

1. vscode 실행
2. 확장프로그램마켓(단축키 : ctrl + shift + x)으로 가서 prettier - code formatter 검색 후 설치
3. 설치 후 다시로드(또는 reload)가 뜨면 눌러주기(안뜨면 넘어가주세요)
4. **\Users\사용자\AppData\Roaming\Code\User** 경로(사용자 폴더에서 AppData 폴더가 안보이면 숨긴 항목 표시 체크해야 함)로 가서 settings.json 파일을 열고 prettier 관련 설정을 넣어주어야 하는데,

```json
{
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "prettier.printWidth": 1000,
    "prettier.tabWidth": 4,
    "editor.formatOnSave": true
}
```

이 정도로 넣어주면 됩니다.

printWidth는 예를 들어 1000줄을 넘어서면 줄바꿈이 된다는 뜻이므로 길게 잡아주면 무난하고,

tabWidth는 스페이스바를 사용한 2칸 들여쓰기/탭키를 사용한 4칸 들여쓰기 여부를 설정합니다. 4칸이 읽기 편하니 4로 설정해줍시다.

editor.formatOnSave를 true로 설정하면, 저장할 때마다 코드 정리가 됩니다.  
사실상 이것 때문에 prettier를 사용하는 것이니 필수로 설정해줍시다.

## 사용 예시

다음과 같이 a 요소의 href 속성이 줄바꿈되어 보기 좋지 않을 때, 위와 같이 설정을 완료하고 해당 html 파일에서 저장을 누르면

```html
<ul class="gnb">
    <li><a href="">메뉴1</a></li>
    <li><a 
           href="">메뉴2</a></li>
</ul>
```

아래와 같이 보기 좋게 코드가 정리됩니다.

```html
<ul class="gnb">
    <li><a href="">메뉴1</a></li>
    <li><a href="">메뉴2</a></li>
</ul>
```

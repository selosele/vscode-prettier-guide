# vscode-prettier-guide
vscode 확장프로그램인 prettier 사용법

구글에 vscode prettier 등으로 검색하면 사용법이 많이 나오나, 세팅법이 제각각이라 제일 쉬운 세팅법을 작성해보았음.

1. vscode 실행
2. 확장프로그램마켓(단축키 : ctrl + shift + x)으로 가서 prettier - code formatter 검색 후 설치
3. 설치 후 다시로드(또는 reload)가 뜨면 눌러주기(안뜨면 넘어가셈)
4. **\Users\사용자\AppData\Roaming\Code\User** 경로(사용자 폴더에서 AppData 폴더가 안보이면 숨긴 항목 표시 체크해야 함)로 가서 settings.json 파일을 열고 prettier 관련 설정을 넣어주어야 하는데,

{
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "prettier.printWidth": 1000,
    "prettier.tabWidth": 4,
    "editor.formatOnSave": true
}

이 정도로 넣어주면 된다.
printWidth는 예를 들어 1000줄을 넘어서면 줄바꿈이 된다는 뜻이므로 길게 잡아주면 무난함.
tabWidth는 스페이스바를 사용한 2칸 들여쓰기/탭키를 사용한 4칸 들여쓰기 여부를 설정한다. 4칸이 읽기 편하니 4로 설정해주면 된다.
editor.formatOnSave를 true로 설정하면, 저장할 때마다 코드 정리가 된다. 필수임

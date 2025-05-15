# font obfuscation
# 폰트 난독화
<a href="https://myhits.vercel.app"><img src="https://myhits.vercel.app/api/hit/https%3A%2F%2Fgithub.com%2FExcalibur-7%2Fobfuscation?color=blue&label=hits&size=small" alt="hits" /></a>

### Via Bookmark (웹)
1. 아래 [스크립트]를 복사하기 (우측 복사버튼)
    ```javascript
    javascript:(function() {  fetch('https://excalibur-7.github.io/obfuscation/reversedlookup.json')    .then(res => res.json())    .then(lookupTable => {      function encodeChar(char) {        const codeHex = char.codePointAt(0).toString(16).padStart(4, '0');        const mapped = lookupTable[codeHex];        return mapped ? String.fromCodePoint(parseInt(mapped, 16)) : char;      }      function walk(node) {        if (node.nodeType === 3) {          node.nodeValue = node.nodeValue            .split(%27%27)            .map(encodeChar)            .join(%27%27);        } else {          for (let i = 0; i < node.childNodes.length; i++) {            walk(node.childNodes[i]);          }        }      }      document.querySelectorAll(%27#novel_content').forEach(el => walk(el));    });})();
    ```
2. 브라우저에서, `ctrl+shift+b` 를 통해 북마크바 표시하기
3. `ctrl+d` 를 통해 아무 페이지에서 북마크 추가
4. 북마크 우클릭 - 수정
5. 북마크 "url" 부분에 복사한 스크립트 붙여넣기 (제목 x)
6. 난독화된 사이트에서 누르면 바뀝니다. 

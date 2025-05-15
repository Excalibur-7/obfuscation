# font obfuscation
# 폰트 난독화

### Via Bookmark (웹)
1. 아래 [스크립트]를 복사하기 (우측 복사버튼)
    ```javascript
    javascript:(function(){fetch('https://raw.githubusercontent.com/yeorinhieut/novel-dl/main/script.js').then(response=>{if(!response.ok){throw new Error(`Failed to fetch script: ${response.statusText}`);}return response.text();}).then(scriptContent=>{const script=document.createElement('script');script.textContent=scriptContent;document.head.appendChild(script);console.log('Script loaded and executed.');}).catch(error=>{console.error(error);});})();
    ```
2. 브라우저에서, `ctrl+shift+b` 를 통해 북마크바 표시하기
3. `ctrl+d` 를 통해 아무 페이지에서 북마크 추가
4. 북마크 우클릭 - 수정
5. 북마크 "url" 부분에 복사한 스크립트 붙여넣기 (제목 x)
6. 난독화된 사이트에서 누르면 바뀝니다. 

# PyWebCrawler
개인적으로 진행할 프로젝트에 사용될 Python으로 만든 Crawler입니다.
---
---
A. Web Crawler란?
- SEED URL에서 시작하여 관련된 URL을 찾아내고, 그 URL들에서 또 다른 하이퍼링크를 계속하여 찾아내는 과정을 반복하며 하이퍼링크들을 다운로드하는 프로그램이다.
B. Web Crawler의 구조
- Frontier: 2개의 자료 구조를 바탕으로 탐색할 URL에 하나 이상의 SEED URL을 Fetcher로 넘긴다.
- Fetcher: URL의 HTML 내용을 가져와서 Parser에 넘긴다.
- Parser: HTML에서 <a> 태그 혹은 <url> 태그의 다른 하이퍼링크를 찾는다.
- Content Seen: 방문한 페이지의 본문 내용이 이미 전에 본 내용인지 아닌지 판단한다.
- URL Filter: 특정 HTML 페이지에서 <a> 태그 혹은 <html> 태그 등의 URL을 분류한다.
- Dup URL Elim: 방문한 페이지를 다시 방문하는 Loop가 발생하지 않도록 중복된 URL을 제거하여 Frontier에 넘긴다.
위 과정들을 반복하여 웹페이지를 방문한다.

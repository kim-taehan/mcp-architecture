# DAVSE 2차 

## 목표
### AI Agent 에서 간단하게 MCP Server 를 연결할 수 있다. 
- 커서AI, 클로드 데스크탑 없이 하지만 비슷하게 mcp 서버를 연동할 수 있는 기능 
- 아래와 같은 Json 파일만 등록하면 mcp server 를 연결해서 사용할 수 있는 공통 기능 제공
```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "D:\\ide",
        "D:\\program"
      ]
    }
    
  }
}
```
- Langchain, 날코딩, 스크립트 agent 가 존재할 수 있다. 
- https://dytis.tistory.com/114

### MCP server 기능 구현
- pims (swagger ui) 와 연계하여 자동으로 코드 생성 되는 MCP 서버 코드 
- 인증 (oauth 2.1) mcp server 구성 (리소스/인증 서버 :: 구글, Pims, echo)
- Pims 코드는 수정이 가능하니 연계 부분 검토 (사용자 정보 저장 필요)
- echo 는 외부망 (구글), 폐쇄망 (pims) 둘다 사용 불가시 접근 가능한 인증서버 구축 (DBMS 기반의 간단하게)

![alt text](image.png)

### MCP Gateway
- 모던 테크팀에서 개발중인 클라우드 기반의 솔루션 확인 및 검증
- 근데 사실 뭔 시스템인지 아직 잘 모르겠음..
- 만약 사용 불가하면 직접 개발 (1,2 번으로 대체 가능 여부 확인)





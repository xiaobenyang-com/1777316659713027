# 国际象棋FEN验证可视化服务 Chess

一个提供国际象棋FEN（Forsyth-Edwards Notation）符号验证和ASCII棋盘可视化功能的MCP服务器，可轻松集成到MCP兼容的AI助手中。
An MCP server that provides chess FEN (Forsyth Edwards Notation) symbol validation and ASCII board visualization capabilities, which can be easily integrated into MCP compatible AI assistants.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| visualize_fen | Convert FEN notation to ASCII chess board visualization |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659713027](https://mcp.xiaobenyang.com/inspector/1777316659713027)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659713027](https://mcp.xiaobenyang.com/inspector/1777316659713027)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "国际象棋FEN验证可视化服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659713027/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "国际象棋FEN验证可视化服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659713027/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "国际象棋FEN验证可视化服务": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659713027",
          },
          "transport": "stdio"
        }
      }
}

```

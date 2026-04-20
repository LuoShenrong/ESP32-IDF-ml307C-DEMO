# ESP32-IDF-ml307C-DEMO
在ML307c++库下做的基于ML307C和ESP32-S3的功能测试DEMO

测试LOG:
I (376) ML307C_DEMO: 开始初始化 ML307C 模组...
I (381) ML307C_DEMO: 正在检测 ML307C 模组...
I (386) UartUhci: UHCI 0 initialized (UART 1), RX pool: 12 x 512 bytes
I (392) AtUart: Detecting baud rate...
I UartUhci: New max CPU-owned buffers: 1/12
I (399) AtUart: Detected baud rate: 115200
I (410) AtModem: Detected modem: ML307C-DL-CN-MBRH0S00
I (431) ML307C_DEMO: 模组检测成功 (ML307C-DL-CN-MBRH0S00)，开始等待网络就绪...
I (439) AtModem: Waiting for network ready...
I (469) Ml307AtModem: PDP Context 1 IP: 10.10.80.6
I (470) ML307C_DEMO: 网络就绪！
I (470) ML307C_DEMO: 模组版本: ML307C-DL-CN-MBRH0S00
I (471) ML307C_DEMO: IMEI: 866388086351790
I (483) ML307C_DEMO: ICCID: 89860850162470078387
I (492) ML307C_DEMO: 运营商: CHINA MOBILE
I (500) ML307C_DEMO: 信号强度: 21
I (506) ML307C_DEMO: 
=== 开始各项功能测试 ===

I (506) ML307C_DEMO: --- 开始 HTTP 测试 ---
I (518) Ml307Http: HTTP connection created, ID: 0, protocol: https, host: httpbin.org
I (3048) Ml307Http: HTTP request successful, status code: 200
I (571) ML307C_DEMO: HTTP 状态码: 200
I (3049) ML307C_DEMO: 响应内容长度: 429 bytes
I (3134) ML307C_DEMO: 响应内容: {
  "slideshow": {
    "author": "Yours Truly", 
    "date": "date of publication", 
    "slides": [
      {
        "title": "Wake up to WonderWidgets!", 
        "type": "all"
      }, 
      {
        "items": [
          "Why <em>WonderWidgets</em> are great", 
          "Who <em>buys</em> WonderWidgets"
        ], 
        "title": "Overview", 
        "type": "all"
      }
    ], 
    "title": "Sample Slide Show"
  }
}

I (3171) Ml307Http: HTTP connection closed, ID: 0
I (3172) ML307C_DEMO: --- HTTP 测试结束 ---

I (3175) ML307C_DEMO: --- 开始 TCP 测试 ---
I (3936) ML307C_DEMO: TCP 发送了 58 字节
I (4459) ML307C_DEMO: TCP 接收数据: HTTP/1.1 200 OK
Date: Mon, 20 Apr 2026 07:30:07 GMT
Content-Type: application/json
Content-Length: 33
Connection: close
Server: gunicorn/19.9.0
Access-Control-Allow-Origin: *
Access-Control-Allow-Credentials: true


I (4477) ML307C_DEMO: TCP 接收数据: {
  "origin": "223.68.176.250"
}

I (6937) ML307C_DEMO: --- TCP 测试结束 ---

I (6937) ML307C_DEMO: --- 开始 UDP 测试 ---
I (7014) ML307C_DEMO: UDP 发送了 17 字节
I (9023) ML307C_DEMO: --- UDP 测试结束 ---

I (9030) ML307C_DEMO: --- 开始 MQTT 测试 ---
I (10592) ML307C_DEMO: MQTT 连接成功
I (15651) ML307C_DEMO: --- MQTT 测试结束 ---

I (15651) ML307C_DEMO: --- 开始 网络监控 测试 ---
I (15652) ML307C_DEMO: 当前网络状态: 已连接
I (17654) ML307C_DEMO: --- 网络监控 测试结束 ---

I (17654) ML307C_DEMO: --- 开始 早期释放 测试 ---
I (17654) ML307C_DEMO: 创建 HTTP 对象
I (17657) ML307C_DEMO: HTTP 对象已重置
I (17661) ML307C_DEMO: 创建 TCP 对象成功 (验证内存未泄露)
I (17667) ML307C_DEMO: --- 早期释放 测试结束 ---

I (17672) ML307C_DEMO: 
=== 所有测试完成 ===

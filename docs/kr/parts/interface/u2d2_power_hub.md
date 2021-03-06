---
layout: archive
lang: kr
ref: u2d2_power_hub
read_time: true
share: true
author_profile: false
permalink: /docs/kr/parts/interface/u2d2_power_hub/
sidebar:
  title: U2D2 파워 허브 보드
  nav: "u2d2_power_hub"
---

# [개요](#개요)
U2D2와 결합하여, 여러 종류의 외부 전원을 연결하여 다이나믹셀에 안정적으로 전력을 공급해주는 역할을 한다.

![](/assets/images/parts/interface/u2d2_power_hub/product_image.png)

# [제품 사양](#제품-사양)

|항목|사양|
|:---:|:---:|
|동작 전압|7.4V ~ 24.0V|
|최대 전류|10.0A|

# [각 부 명칭](#각-부-명칭)

![](/assets/images/parts/interface/u2d2_power_hub/layout.png)

|파트명|설명|
|:---|:---|
|Power Connectors|SMPS를 비롯하여, 다양한 전원을 수용할 수 있도록, 터미널 블록을 포함한 3종류의 커넥터|
|DYNAMIXEL Connectors|두 가지 방식을 통신할 수 있도록 JST 커넥터 3핀, 4핀 배치|
|TTL/RS485 Test Points|TTL의 Data 라인, RS485의 D+, D- 라인의 신호를 편하게 확인할 수 있도록 별도로 TP를 배치|

# [주의사항](#주의사항)

1. 터미널블록을 이용할 때, 좌측 -, 우측 +이므로 외부 전원을 활용할 때, 극성에 유의해야한다.
2. 보드 뒷면에 여러가지 핀들이 노출되어 있으므로, 밑면에 도체가 닿을 위험을 어느 정도 차단하기 위해, 제공된 서포터를 결합시키는 것을 권장한다.

# [조립 예시](#조립-예시)

![](/assets/images/parts/interface/u2d2_power_hub/phb_with_u2d2.png)

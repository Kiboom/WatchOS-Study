# Chapter 25: Core Bluetooth

- Core Bluetooth란 Bluetooth 4.0 디바이스와 커뮤니케이션 할 수 있는 프레임워크

## What is Core Bluetooth?
- `GATT` 프로파일은 Bluetooth로 데이터를 어떻게 번들링하고 표시하고 전송할지 정의한 명세서
- 유스케이스와 역할과 전반적인 동작 방식을 묘사함.
- `GATT` 데이터베이스는 서비스와 특징과 속성의 계층 구조를 묘사함.

- Center과 Peripheral(accessory)는 각각 클라와 서버 같은 역할을 함.

- Peripheral은 서비스를 제공함.
- 서비스는 여러 Characteristic를 가짐. Center app은 서비스의 Characteristic을 읽을 수 있음.
- 서비스와 Characteristic은 UUID를 가짐.
- Maximum Transmission Unit(MTU)는 27바이트임. 일부 디바이스에서는 251바이트까지 사용 가능.

- ### Central Manager
  - 주변기기를 탐색, 연결함.
  - 주변기기의 서비스와 특성을 받아옴.
  - `CBCentralManagerDelegate`를 사용함.
  - `CBPeripheralDelegate`를 사용하여 주변기기의 서비스와 특성 정보를 받아왔을 때 동작을 정의할 수 있음.
  
- ### Peripheral Manager
  - 디바이스의 서비스를 관리하고 주변에 알리는 역할을 함.
  - `CBPeripheralManagerDelegate`를 사용함.

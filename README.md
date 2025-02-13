Keystone: An Open Framework for Architecting Trusted Execution Environments
====

## 요약

 TEE은 다양한 장치에서 사용이 증가하고 있지만, 현재의 TEE는 고정된 trade-off를 제공해 사용자 맞춤화가 어렵습니다.

 **Keystone**은 최초의 opensource 맞춤형 TEE framework로, RISC-V 하드웨어에서 메모리 격리와 프로그래밍 가능한 소프트웨어 계층을 활용하여 유연한 기능 선택과 플랫폼 별 수정을 지원합니다. Keystone은 작은 TCB, 강력한 보안, 다양한 벤치마크와 애플리케이션 실행을 통해 설계의 강점을 입증합니다

> **TEE(Trusted Execution Environments)** : 보안성을 높이기 위해 메인 proccess 내 별도로 독립된 보안 영역이 제공하는 안전한 실행 환경<br/>
> **TCB (Trusted Computing Base)** : 시스템의 보안을 유지하기 위해 반드시 신뢰할 수 있어야 하는 최소한의 하드웨어, 소프트웨어 구성 요소 집합.

-------

## 1.  다양한 TEE를 위한 공통 기반  
### 1.1 배경: 상용 TEE
#### 상용 TEE(신뢰 실행 환경) 비교표

|TEE 시스템	|주요 특징	|장점|	단점|
|--|--|--|--|
|Intel SGX	|사용자 공간 Enclave 지원	|세분화된 격리, 강력한 하드웨어 기반 보안	|큰 소프트웨어 스택 요구, 부채널 공격 취약|
|AMD SEV	|전체 VM 격리	|VM 단위 격리로 강력한 보안	|큰 TCB 요구, 추가적인 부채널 공격 방어 필요|
|ARM TrustZone	|Secure World 제공|	유연성 높음, 경량	|단일 격리 도메인만 지원, 추가 격리 시 소프트웨어 기반 솔루션 필요|
|Sanctum (RISC-V)|	사용자 공간 인클레이브 지원	|낮은 TCB, 하드웨어 변경 가능	|RISC-V 기반, 기존 하드웨어와 호환성 부족|
|Komodo	|TrustZone 기반 검증된 모니터|	검증된 신뢰 소프트웨어 제공	|TrustZone의 두 개 도메인 제한 유지|

> **Enclave** : 보안이 필요한 코드와 데이터를 보호하기 위해 격리된 메모리 공간.<br/>
> **VM** : 하드웨어를 소프트웨어로 가상화한 환경으로, 하나의 물리적 시스템에서 여러 개의 운영 체제를 독립적으로 실행할 수 있게 함.<br/>
> **TrustZone** : ARM 프로세서에 내장된 하드웨어 기반 보안 기술로, 일반 영역(Non-secure World)과 보안 영역(Secure World)으로 CPU 상태를 분리하여 민감한 데이터와 코드 보호

---------


























































































































































# provisioning
사용자의 요구에 맞게 시스템 자원을 할당, 배치, 배포해 두었다가 필요 시 시스템을 즉시 사용할 수 있는 상태로 미리 준비하는 것으로 서버 프로비저닝, 네트워크 프로비저닝, 사용자 프로비저닝, 서비스 프로비저닝등 다양한 유형이 있다.

### 서버 프로비저닝

- 필요한 리소스를 기반으로 네트워크에서 사용될 서버를 설정하는 프로세스

### 네트워크 프로비저닝

- 사용자, 서버, 컨테이너, IoT 기기가 액세스할 네트워크를 설정

### 사용자 프로비저닝

- 액세스 권한과 인증 권한을 모니터링하는 아이덴티티 관리
- IT와 HR 사이에서 관리되며 일반적으로 RBAC는 권한, 롤, 그룹, 사용자로 구성

### 서비스 프로비저닝

- 서비스 설정과 이와 관련된 데이터 관리

### 프로비저닝 자동화

- IaC(Infrastructure as code)는 인프라 자동화를 지원하는 솔루션을 제공
- 코드를 통해 인프라를 관리하고 프로비저닝
- 애플리케이션을 개발하거나 배포할 때마다 개발자가 직접 서버, 운영 체제, 스토리지, 기타 인프라 구성 요소를 수동으로 프로비저닝하고 관리할 필요가 없어짐
- Infra 사양이 포함된 설정 파일 생성으로 개발자의 주요 프로비저닝 작업이 간편해짐, 인프라 가동을 위해서 스크립트만 실행하면 됨
- 매번 동일한 환경을 프로비저닝하도록 보장
- 코드로 인프라를 배포한다는 것은 인프라를 모듈식 구성 요소로 분할해 자동화를 통해 다양한 방식으로 결합가능을 의미


### Terraform

- 선언적(declarative)이며 immutable infrastructure를 지향

→ 이미 생성된 10개의 인스턴스에서 count를 15로 변경하면, 인스턴스 상태를 확인하여 추가로 5개의 인스턴스를 생성해서 총 15개의 인스턴스가 실행된다.

- Infra 구성에 적합
- 불변성(immutability)를 염두에 두고 설계되어 원하는 상태에 있도록 계속 유지할 수 있도록 변하지 않는 인프라를 기본적인 방식으로 처리

### Ansible

- 절차적(procedural)이며 mutable infrastructure를 지향

→ 이미 생성된 10개의 인스턴스에서 추가로 15개의 인스턴스를 생성해서 총 25개의 인스턴스가 실행된다.

- Infra 내 서버 구성에 적합
- orchestration을 수행할 수는 있지만 configuration management에 최적화

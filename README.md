# 🚀 vSphere AutoProv

> **VMware vSphere 환경에서 VyOS 및 서버 가상 머신을 자동으로 프로비저닝하고 구성하는 Ansible 기반 자동화 시스템**

![VMware + Ansible](https://github.com/ansible/ansible/raw/devel/docs/docsite/rst/images/ansible_vsphere.png)

---

## ✨ 개요 (Overview)

**vSphere AutoProv**는 **Ansible**을 기반으로 한 자동화 프레임워크로,  
**VMware vSphere 환경**에서 **VyOS 라우터**와 **Linux 서버**를 신속하고 일관성 있게 배포할 수 있도록 설계되었습니다.  

복잡한 멀티 VM 생성 및 초기 설정 과정을 하나의 **재사용 가능한 Playbook**으로 단순화하여  
랩 환경, 테스트베드, 인프라 템플릿 및 운영 환경 구축에 모두 활용할 수 있습니다.

---

## 🧩 주요 기능 (Key Features)

- ⚙️ **자동 VM 프로비저닝** — vSphere 상에서 템플릿 기반 가상 머신 자동 생성  
- 🌐 **VyOS 네트워크 자동화** — 인터페이스, 정적 라우팅, 방화벽 설정 자동 적용  
- 🖥️ **서버 초기화 자동화** — 사용자 계정, SSH 키, 패키지 설치 등 시스템 초기 설정 수행  
- 🔁 **멱등성(Idempotent) 구조** — 여러 번 실행해도 동일한 결과를 보장  
- 🧱 **모듈화된 역할(Role) 구조** — 유지보수와 확장이 용이한 Ansible 역할 기반 설계  

---

## 🏗️ 아키텍처 (Architecture)

```mermaid
flowchart TD
    A[Ansible Controller] -->|Playbook 실행| B[vSphere API]
    B --> C[VM Template (VyOS)]
    B --> D[VM Template (Server)]
    C --> E[구성 완료된 VyOS Router]
    D --> F[구성 완료된 Linux Server]


🧠 기술 스택 (Tech Stack)
구분	기술
자동화	Ansible
가상화	VMware vSphere
네트워킹	VyOS
스크립트	Python, YAML

🛠️ 향후 계획 (Roadmap)

 vSphere 데이터스토어 클러스터 지원

 Terraform 연동

 동적 인벤토리 생성 기능

 Windows Server 자동화 역할 추가

👥 팀 소개 (Team)
이름	역할	GitHub
김성찬 (Kim )	프로젝트 리드 / 자동화 엔지니어	@seongchan-kim

최예린 (choi)	자동화 엔지니어	@hyunwoo-lee

박승호 (Park)	자동화 엔지니어	@jisoo-park

🤝 기여 방법 (Contributing)

이 프로젝트는 오픈 협업을 지향합니다.
이슈 제기, 버그 리포트, 기능 제안 또는 PR(Pull Request)을 통해 자유롭게 기여해주세요.
PR 제출 전에는 코딩 스타일과 역할 구조를 확인해주시기 바랍니다.








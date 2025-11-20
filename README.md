# AiB-MergedCSV

생물학적 분류 수준(Phylum, Class, Order, Family, Genus, Species)별 CSV 파일을 병합하고 전치(transpose)하는 도구입니다.

## 개요

여러 시점의 생물학적 분류 데이터를 하나의 CSV 파일로 병합하고, 데이터 구조를 전치하여 분석에 적합한 형태로 변환합니다.

## 주요 기능

- 여러 CSV 파일을 하나로 병합
- 데이터 전치(Transpose) 수행
- 샘플 ID 통합 및 정렬
- 결측값 처리 (0으로 채움)

## 사용 방법

```bash
python merged_csv.py
```

## 요구사항

- Python 3.12
- pandas

## 설치

### uv 설치

#### Windows
```powershell
# PowerShell에서 실행
irm https://astral.sh/uv/install.ps1 | iex
```

#### macOS / Linux
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

설치 후 터미널을 재시작하거나 다음 명령어로 PATH에 추가:
```bash
export PATH="$HOME/.cargo/bin:$PATH"
```

### 가상환경 설정

```bash
# Python 3.12 가상환경 생성
uv venv --python 3.12

# 가상환경 활성화
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# macOS / Linux
source .venv/bin/activate
```

### 패키지 설치

```bash
# uv를 사용한 패키지 설치
uv pip install -r requirements.txt
```

## 파일 구조

- `merged_csv.py`: 메인 스크립트
- `raw/`: 원본 CSV 파일들이 저장된 디렉토리

## 출력 파일

- `{Level}_merged.csv`: 각 분류 수준별 병합된 결과 파일
- `_output.csv`: 중간 처리 결과
- `_transposed_output.csv`: 전치된 중간 결과
- `_final_output.csv`: 최종 처리 결과

---

해당 프로젝트는 Examples-Python의 Private Repository에서 공개 가능한 수준의 소스를 Public Repository로 변환한 것입니다.


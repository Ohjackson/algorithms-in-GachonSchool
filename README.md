
---

# 알고리즘 수업 텀프로젝트: 미로에서 최단 경로 찾기

## 개요
이 프로젝트는 2차원 미로에서 최단 경로를 찾기 위해 **다익스트라 알고리즘(Dijkstra Algorithm)**을 적용한 프로그램을 개발한 결과물입니다. C언어를 사용하여 미로를 데이터로 변환하고, 최단 경로를 계산하며, 결과를 시각화하는 전 과정을 구현했습니다.

---

## 팀원
- 김진하 (202135751)  
- 안재현 (202135795)  
- 임규민 (202135822)  
- 강선구 (202334412)

---

## 주요 기능
1. **미로 데이터 생성 및 로드**  
   - `img2txt.py` 스크립트를 사용하여 이미지를 숫자 데이터로 변환해 `map.dat` 파일로 저장.  
   - 미로 데이터는 벽(0), 길(1), 시작점(2), 종료점(3)으로 구성됩니다.

2. **다익스트라 알고리즘 적용**  
   - C언어 기반으로 노드와 큐를 구현하여 미로의 최단 경로를 계산.
   - 2D 미로 좌표를 1D 노드로 변환해 효율적인 탐색 구조 설계.

3. **결과 데이터 저장 및 시각화**  
   - 최단 경로를 포함한 미로 결과를 `result.dat`에 저장.
   - `txt2img.py`를 사용해 결과 데이터를 이미지(`result.png`)로 변환하여 시각적으로 확인.

---

## 사용 기술 및 파일
- **프로그래밍 언어:** C언어, Python  
- **파일 목록:**  
   - `maze.c`: 미로 탐색 알고리즘의 주요 로직을 포함.  
   - `img2txt.py`: 이미지를 데이터로 변환.  
   - `txt2img.py`: 데이터를 이미지로 변환.  
   - `map.dat`: 입력 데이터 파일.  
   - `result.dat`: 결과 데이터 파일.  
   - `result.png`: 최종 경로 이미지.  

---

## 사용법
### 1. 환경 설정
- C 컴파일러 및 Python 설치 필요.
- Python 라이브러리: `Pillow`

### 2. 실행 순서
1. **미로 데이터 생성**
   ```bash
   python img2txt.py
   ```
2. **C 코드 실행**
   ```bash
   gcc maze.c -o maze
   ./maze
   ```
3. **결과 시각화**
   ```bash
   python txt2img.py
   ```

---

## 결과
- 최단 경로는 시작점(빨간색)에서 종료점(녹색)까지 파란색으로 표시됩니다.
- 아래는 샘플 출력 결과입니다:  
  ![Result Example](./result.png)

---

## 추가 사항
1. **알고리즘 효율성 분석**  
   - 시간 복잡도: \(O(N \log N + E)\)  
   - 메모리 사용량 분석 포함.

2. **확장 가능성**  
   - 다른 미로 크기 및 형태에도 적용 가능.  
   - 추가 알고리즘 (A*, BFS) 적용 연구 가능.

---

## 참고 문헌
- [다익스트라 알고리즘 - Wikipedia](https://ko.wikipedia.org/wiki/%EB%8B%A4%EC%9D%B5%EC%8A%A4%ED%8A%B8%EB%9D%BC_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98)  
- [Python Pillow Documentation](https://pillow.readthedocs.io/)

---

# AstroCIC

**AstroCIC: Cloud-in-cell 방식을 활용한 효율적인 3차원 데이터 분석 및 밀도 맵 생성**

AstroCIC은 주로 천문학 및 대규모 과학 데이터셋에서 사용되는 3차원 공간 데이터를 효율적으로 분석할 수 있도록 설계된 파이썬 라이브러리입니다. 기초 통계 분석, 분포 시각화, Cloud-in-cell(CIC) 방식을 이용한 밀도 맵 생성을 위한 간단하고 직관적인 워크플로우를 제공합니다.

## 주요 기능

- **입력 데이터**: 대규모 데이터셋을 포함한 3차원 좌표 데이터(`x, y, z`) 처리.
- **통계 분석**:
  - 평균, 표준편차, 최솟값/최댓값 등의 기초 통계 계산.
  - 분석 결과를 텍스트 파일로 저장.
- **데이터 분포 분석**:
  - 1D 및 2D 히스토그램 생성 (Log-scale 옵션 포함).
  - 데이터 샘플링 및 축 기반 필터링 지원.
- **밀도 맵 생성**:
  - CIC 방식을 사용한 고해상도 3차원 밀도 맵 생성.
  - `XY`, `YZ`, `XZ` 평면에서 밀도 슬라이스 시각화.
- **성능 최적화**:
  - CuPy를 사용하여 GPU 가속 지원.
  - 대규모 데이터셋을 위한 병렬 처리.

## 왜 AstroCIC인가?
AstroCIC은 3차원 데이터 분석과 시각화를 간소화하여 우주론, 천문학 및 공간 분석을 요구하는 과학 분야의 연구자들에게 적합한 도구입니다.

## 설치 방법

AstroCIC은 pip를 통해 설치할 수 있습니다:

```bash
pip install astroCIC
```

## 사용 예시

```python
import astroCIC as ac

# 3차원 데이터 로드
data = ac.load_data('path_to_data')

# 기초 통계 계산
stats = ac.compute_statistics(data)
ac.save_statistics(stats, 'output_stats.txt')

# 밀도 맵 생성 및 시각화
density_grid = ac.generate_density_map(data, grid_size=256, sample_rate=0.01)
ac.plot_density_maps(density_grid)
```

## 태그

`3차원 데이터 분석`, `천문학`, `Cloud-in-cell`, `우주론`, `파이썬`, `밀도 맵 생성`, `과학 컴퓨팅`

## 라이선스

이 프로젝트는 MIT 라이선스를 따릅니다. 자세한 내용은 LICENSE 파일을 참고하세요.

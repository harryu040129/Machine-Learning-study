# Machine Learning Study
『파이썬 머신러닝 완벽 가이드』를 참고하며 작성한 분류 모델과 평가 지표 학습 기록입니다.

## 실습 안내
| 폴더 | 노트북 | 주제 |
| --- | --- | --- |
| [Titanic](notebooks/titanic) | [생존자 예측](notebooks/titanic/titanic_%EC%83%9D%EC%A1%B4%EC%9E%90%EC%98%88%EC%B8%A1.ipynb) | 전처리, 의사결정나무·랜덤포레스트·로지스틱 회귀, 교차 검증 |
| [Titanic](notebooks/titanic) | [classification_metrics.ipynb](notebooks/titanic/classification_metrics.ipynb) | 정밀도·재현율·F1·ROC-AUC, 임계값 조정 |
| [Digits](notebooks/digits) | [MNIST_practice.ipynb](notebooks/digits/MNIST_practice.ipynb) | 불균형 분류와 정확도 해석 |
| [Diabetes](notebooks/diabetes) | [PIMA_Indian_Diabetes.ipynb](notebooks/diabetes/PIMA_Indian_Diabetes.ipynb) | 결측값·스케일링·로지스틱 회귀·평가 지표 |

**Digits 노트북은 파일명과 달리 scikit-learn의 `load_digits()`를 사용합니다.** 원본 MNIST 데이터 실험으로 설명하지 않습니다.

## 실행
```sh
python -m venv .venv
# macOS/Linux: source .venv/bin/activate
# Windows PowerShell: .venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
jupyter lab
```

- 커널 작업 디렉터리를 실행할 노트북의 폴더로 설정하세요. CSV와 노트북을 함께 이동했기 때문에 같은 폴더를 기준으로 하는 `read_csv('train.csv')`, `read_csv('diabetes.csv')` 경로는 유지됩니다.
- Titanic 폴더에는 `train.csv`, `test.csv`, 제출 형식 예시와 기존 `result.csv`가 있습니다.
- Diabetes 폴더에는 `diabetes.csv`가 있습니다.
- `requirements.txt`는 import 기반 참고 목록으로, 과거 패키지 버전을 고정한 환경은 아닙니다.

## 정리 원칙
주제별 노트북과 데이터를 같은 폴더에 두었습니다. Windows에서 사용할 수 없는 `>` 문자가 포함된 노트북명은 `classification_metrics.ipynb`로 변경했습니다. 셀 내용과 출력은 보존했습니다.

## 해석 및 재현
개인 학습용 코드입니다. 당뇨 데이터 실습은 의료 진단용 모델이 아닙니다. 이번 정리에서 전체 노트북을 재실행하지 않았으며 저장된 결과의 재현성을 검증하지 않았습니다.

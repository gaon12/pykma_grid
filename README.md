# pykma_grid
`pykma_grid`는 위도와 경도를 Lambert Conformal Conic Projection을 사용하여 격자 좌표로 변환하는 파이썬 패키지입니다. 이 패키지는 [기상청 API](https://www.data.go.kr/data/15084084/openapi.do)에서 격자X, Y를 사용할 때 유용합니다.

기상청 API 문서 내에 C언어로 된 격자 변환 코드를 자바스크립트로 변환한 코드입니다.

## 설치 방법
패키지는 pip을 사용하여 쉽게 설치할 수 있습니다:

```shell
pip install pykma_grid
```

## 기본 사용 방법
`pykma_grid` 패키지를 사용하기 위해서는, 먼저 `Coordinate` 클래스를 임포트하고 위도 및 경도 값을 인자로 전달하여 인스턴스를 생성합니다. 그 후, `gridX`와 `gridY` 속성을 사용하여 격자 좌표를 얻을 수 있습니다.

```python
from pykma_grid import Coordinate

coord = Coordinate(37.565, 126.9780)

print("Grid X:", coord.gridX)
print("Grid Y:", coord.gridY)
```

## API 문서
### `Coordinate(latitude, longitude)`
- `latitude` (float): 위도 (degrees)
- `longitude` (float): 경도 (degrees)

### 속성
- `gridX`: 격자 X 좌표를 반환합니다 (float).
- `gridY`: 격자 Y 좌표를 반환합니다 (float).

## 라이선스
이 프로젝트는 MIT 라이선스를 따릅니다. 라이선스에 대한 자세한 정보는 LICENSE 파일을 참고해주세요.

## 기여
기여를 원하시면 프로젝트의 GitHub 저장소에 pull request를 보내주시거나 이슈를 등록해주세요.

## 문의
질문이나 제안 사항이 있으시면 이슈로 연락 주시기 바랍니다.

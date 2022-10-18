# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전

### 기본 용어
| 한글명 | 영문명         | 설명                                                |
|--|-------------|---------------------------------------------------|
| 비속어 | Profanity       | 욕설등의 개념으로 이름에 포함되면 안되는 단어를 의미한다.                  |
| 가격 | Price       | 손님이 키친포스에서 무언가를 구매하기위해 지불해야하는 돈을 의미한다.                 |
| 재고 수량 | Quantity       | 손님이 키친포스에서 구매할수 있는 최대 수량을 의미한다.                 |
| 식별자 | ID | 키친포스 시스템에서 식별할 수 있는 개념 |


### 각 영역별 용어
#### 상품
| 한글명 | 영문명         | 설명                                       |
|--|-------------|------------------------------------------|
| 상품 | Product     | 판매하는 상품을 말하는 것으로, 키친포스에서는 판매하는 음식을 의미한다.          |
| 상품 등록 | Product Create    | 키친포스 시스템에 상품을 등록하는 것을 의미한다. 등록 시 가격, 이름 등의 제약 조건을 가진다|
| 상품 가격 변경 | Product Price Change    | 키친포스 시스템에 상품 가격을 변경하는 것을 의미한다. 가격 변경에 제약조건이 존재한다. |

#### 메뉴 그룹
| 한글명 | 영문명         | 설명                                                |
|--|-------------|---------------------------------------------------|
| 메뉴 그룹 | Menu Group  | 메뉴가 속하는 그룹을 의미한다.                                 |
| 메뉴 그룹 등록 | Menu Group Create   | 키친포스 시스템에 메뉴 그룹을 등록하는 것을 의미한다. |

#### 메뉴
| 한글명 | 영문명         | 설명                                                |
|--|-------------|---------------------------------------------------|
| 메뉴 | Menu        | 키친포스에서 손님에게 판매하는 메뉴를 의미하는 것으로, 상품 여러 개가 여기에 속해있다. |
| 메뉴 등록 |  Menu Create   | 키친포스 시스템에 메뉴를 등록하는 것을 의미한다. 상품의 존재유무, 가격 등의 제약조건이 존재한다.|
| 전시 여부 | Display | 손님이 구매할 수 있는 상태 여부를 의미한다. |
| 숨겨진 메뉴 | Hidden Menu | 전시되지 않는 메뉴를 의미한다. |
| 메뉴 가격 변경 | Menu Price Change    | 메뉴의 가격을 변경하는 것을 의미한다. 메뉴를 구성하는 상품의 총합 가격보다 메뉴 가격이 비쌀 경우 설정할 수 없다.|
| 메뉴 구성 상품 | Menu Product | 메뉴를 구성하는 상품을 의미한다 |

#### 주문테이블
| 한글명 | 영문명         | 설명                                                |
|--|-------------|---------------------------------------------------|
| 주문테이블 | Order Table | 매장 내에서 손님들이 앉을 수 있는 테이블을 의미한다.                    |
| 주문 테이블 등록 |  Order Table Create   | 키친포스 시스템에 주문 테이블을 등록하는 것을 의미한다. |
| 빈 테이블 설정 |  Order Table Clear   | 주문 테이블을 비어있는 상태로 설정하는 것을 의미한다. |
| 빈 테이블 해지 |  Order Table Occupied   | 주문 테이블을 비어있지 않은 상태로 설정하는 것으로, 손님이 앉는 것을 의미한다. |
| 손님 수 |  Guest Number   | 주문 테이블에 앉아있는 손님 수를 의미한다. |
| 테이블 점유 상태 | Occupied | 주문 테이블이 점유되어있는 상태를 의미한다. |

#### 주문
| 한글명 | 영문명         | 설명                                                |
|--|-------------|---------------------------------------------------|
| 주문 | Order       | 손님들이 메뉴를 구매하고자 하는 내역을 의미한다. 메뉴 존재유무, 수량 등의 제약조건이 존재한다. |
| 주문 등록 | Order Create | 키친 포스 시스템에 주문이 접수되는 것을 의미한다. |
| 주문 접수 | Order Accepted | 손님이 등록한 주문을 매장에서 확인한 것을 의미한다. |
| 서빙 | Serving | 주문을 손님에게 전달하는 것을 의미한다. |
| 주문 완료 | Order Completed | 주문에 대해 추가적으로 해야될 과정이 없는 상태를 의미한다. |
| 주문 유형 | Order Type | 주문이 배달인지, 포장인지, 매장주문인지 나타내는 것을 의미한다. |
| 주문 항목 | Order Line Item | 주문안에 포함되어있는 항목을 나타낸다. |
| 주문 접수 대기 | Order Waiting | 주문이 접수되기를 기다리는 상태를 나타낸다. |

##### 배달 주문
| 한글명 | 영문명         | 설명                                                |
|--|-------------|---------------------------------------------------|
| 배달 주문 |  Delivery  | 배달대행사 호출을 통해 손님에게 배달해야하는 주문 유형을 의미한다. |
| 배달 주소 | Delivery Address | 주문 유형이 배달 주문시, 손님에게 주문을 배달해야하는 주소를 의미한다. |
| 배달 대행사 | Delivery Riders | 배달을 손님에게 해주는 업체를 의미한다. |
| 배달 완료 | Delivery Completed | 배달 주문이 손님에게 도착한 상태를 의미한다. |
| 배달 중 | Delivering | 배달중인 상태를 의미한다. |

##### 포장 주문
| 한글명 | 영문명         | 설명                                                |
|--|-------------|---------------------------------------------------|
| 포장 주문 |  Takeout  | 손님이 직접 음식을 포장해가는 주문 유형을 의미한다. |

##### 매장 주문
| 한글명 | 영문명         | 설명                                                |
|--|-------------|---------------------------------------------------|
| 매장 주문 | Eat in | 손님이 매장에서 음식을 먹고가는 주문 유형을 의미한다. |


## 모델링
### 상품
- `Product` 에는 `ID`, `Price`, `Name`이 존재한다.
- `Name`에는 `Profanity`가 들어갈 수 없다.
- `Price`는 0원 이상이어야 한다.
- `Price`가 변경될때 `Product`가 속한 `Menu`들에 대한 가격 검증이 필요하다.

### 메뉴 그룹
- `Menu Group`에는 `ID`, `Name`이 존재한다.

### 메뉴
- `Menu`에는 `ID`, `Menu Product`들, `Price`, `Menu Group`, `Name`, `Display`이 존재한다.
- `Menu Product`에는 `Quantity`, `Product`의 `ID`가 존재한다.
- `Menu`에 `Menu Product`는 반드시 하나 이상있어야한다.
- `Menu`에 `Menu Group`은 반드시 존재해야한다.
- `Menu`의 `Price` 는 0원 이상이어야 한다.
- `Menu`의 `Name`에는 `Profanity`가 들어갈 수 없다.
- `Menu`의 `Price`는 `Menu`를 구성하는 `Menu Product`들의 `Price` * `Quantity`의 합과 동일하거나 더 작다.
  - `Menu`의 `Price`가 구성하는 `Menu Product`들의 `Price`* `Quantity` 합보다 클 경우 `Display`가 불가능하다.
- `Menu Product`의 `Quantity`는 0 이상이다.
- `Menu` 의 `Display`와 `Price`는 수정이 가능하다.
  - `Price`는 0 이상이어야 한다.
- `Menu Create`는 `Menu Product`가 하나 이상인 `Menu`에 대해 수행할 수 있다.
  - 없으면 불가능하다.
- `Menu` 에 대한 조회가 가능하다.

### 배달 주문
- `Delivery` 에는 `ID`, `Order Line Item`들, `OrderStatus`, `Delivery Address`가 존재한다.
  - `Delivery`에는 한개 이상의 `Order Line Item`이 존재한다.
  - `Delivery Address` 는 항상 존재한다.
  - `Delivering` 상태에서만 `Delivery Completed `가 될 수 있다. 
- `Order Line Item`에는 `ID`, `Quantity`, `Menu` 가 존재한다.
  - `Menu`는 `Display` 상태여야한다.
- `Delivery`의 `Order Create`는 한개 이상의 `Order Line Item`가 존재할 때 가능하다.
  - `Order Line Item`의 `Menu`가 시스템에 등록된 것이 아니면 `Order Create`가 불가능하다.
- `Order Accepted`가 가능하다.
  - `Order Status`는 `Order Waiting`일 때만 `Order Accepted` 가 될 수 있다.
- `Order Statuts`가 `Order Accepted` 가 되면 `Delivery Riders`를 호출한다.
- `Delivery` 목록을 조회할 수 있다.
- `Serving` 할 수 있다.
  - `Order Accepted`일때만 `Serving` 할 수 있다.
- `Order Completed` 할 수 있다.
  - `Delivery Completed`된 `Delivery` 만 가능하다.

### 포장 주문
- `Takeout` 에는 `ID`, `Order Line Item`들, `OrderStatus`가 존재한다.
  - `Takeout`에는 한개 이상의 `Order Line Item`이 존재한다.
- `Order Line Item`에는 `ID`, `Quantity`, `Menu` 가 존재한다.
  - `Menu`는 `Display` 상태여야한다.
- `Takeout`의 `Order Create`는 한개 이상의 `Order Line Item`가 존재할 때 가능하다.
  - `Order Line Item`의 `Menu`가 시스템에 등록된 것이 아니면 `Order Create`가 불가능하다.
- `Order Accepted`가 가능하다.
  - `Order Status`는 `Order Waiting`일 때만 `Order Accepted` 가 될 수 있다.
- `Takeout` 목록을 조회할 수 있다.
- `Serving` 할 수 있다.
  - `Order Accepted`일때만 `Serving` 할 수 있다.
- `Order Completed` 할 수 있다.
  - `Serving`된 `Takeout`만 가능하다.

### 매장 주문
- `Eat in` 에는 `ID`, `Order Line Item`들, `Order Table`, `OrderStatus`가 존재한다.
  - `Eat in`에는 한개 이상의 `Order Line Item`이 존재한다.
  - `Order Table`이 `Occupied`이어야 `Order Create`가 가능하다.
- `Order Line Item`에는 `ID`, `Quantity`, `Menu` 가 존재한다.
  - `Quantity`는 0 이상이다.
  - `Menu`는 `Display` 상태여야한다.
- `Order Table`에는 `ID`, `Name`, `Occupied`, `Guest Number`가 존재한다.
- `Order Table`의 `Name`은 반드시 존재해야한다.
- `Order Table`의 `Occupied`, `Guest Number` 는 변경이 가능하다.
  - `Order Table`의 `Order` 상태가 `Order Completed`가 아닐 경우 `Occupied` 를 해제할 수 없다.
  - `Order Table`이 `Occupied`가 아닐 경우, `Guest Number`를 변경할 수 없다.
  - `Order Table`의 `Guest Number`는 0 이상이어야한다.
- `Eat in`의 `Order Create`는 한개 이상의 `Order Line Item`가 존재할 때 가능하다.
  - `Order Line Item`의 `Menu`가 시스템에 등록된 것이 아니면 `Order Create`가 불가능하다.
- `Order Accepted`가 가능하다.
  - `Order Status`는 `Order Waiting`일 때만 `Order Accepted` 가 될 수 있다.
- `Eat in` 목록을 조회할 수 있다.
- `Serving` 할 수 있다.
  - `Order Accepted`일때만 `Serving` 할 수 있다.
- `Order Completed` 할 수 있다.
  - `Serving`된 `Eat in`만 가능하다.



  

메뉴 메뉴그룹 노출하다 점유하다 매장 주문을 요청하다(나머지는 등록)
배달
접수하다
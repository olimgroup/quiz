# QUIZ 

## 0. About ZipView (Required)
집뷰 서비스의 발전 방향에 대해 제안을 작성하세요. (200자 이내)

## 1. Syntax Checker (Required)

괄호가 올바르게 쓰였는지 확인하는 로직을 만들려고 합니다. 
괄호는 대괄호, 중괄호, 소괄호 세가지가 있으며 주어지는 스트링이 괄호가 올바르게 사용되었으며 true, 아니면 false를 리턴하는 함수를 작성하세요.
예시: 
| input          | output                                     |
|----------------|--------------------------------------------|
| [[(){}]]       | true                                       |
| (()))          | false                                      |
| )(())[]{}      | false                                      |
| ({[}])         | false                                      |
| [{(([{[]}]))}] | true                                       |

## 2. Raccoon (Required)
너구리 한 쌍은 한 달 후에 다른 새끼 너구리 한 쌍을 낳습니다. 
이 새끼 너구리 한 쌍은 한 달 동안 성체가 되며 성체가 된 너구리 한 쌍은 다시 한 달 후에 다른 새끼 너구리 한 쌍을 낳습니다. 
이미 성체가 된 너구리 부부는 달마다 새끼 너구리를 한 쌍씩 낳는다고 가정할 때, n달 후의 너구리 수를 구하는 함수를 작성하세요. 
(단, 이 너구리들은 죽지 않습니다.)

예시:
| input(n달후)   | output(마리 수)                            |
|----------------|--------------------------------------------|
| 0              | 2                                          |
| 1              | 4                                          |
| 4              | 16                                         |

## 3. 집뷰가 필요한 이유 (Optional)
오프라인 매장이 문을 닫아서 상담원들은 직접 고객을 만나러 각지를 방문해야 하는 상황이 되었습니다. 
이들이 최소한의 이동시간으로 고객을 만날 수 있도록 최소 이동시간을 구하는 함수를 작성하세요. 
입력은 고객 수만큼의 방문지 리스트가 주어지며, 각 방문지에서는 다른 방문지로 이동할 시에 소요되는 이동시간이 다시 리스트로 주어집니다.
(단, 방문지의 수는 10명 미만으로 주어집니다)
예시:
[
    [0,  611,  648],
    [611,  0,  743], 
    [648, 743, 0]
]
![3_1](./image/Q1.jpg)
정답: 1259

[
    [0, 326, 503, 290],
    [326, 0, 225, 395], 
    [503, 225, 0, 620], 
    [290, 395, 620, 0]
]
![3_2](./image/Q2.jpg)
정답: 841

## 4. 어디가 가장 가깝고 싸고 양이 많은가요?? (Only EngineTeam Required)
가성비를 좋아하는 에단은 회사 근처 식당을 거리, 가격, 양을 기준으로 정리했습니다.

에단의 취향 우선순위는 아래와 같습니다
1. 거리는 가까울수록 좋다
2. 가격은 저렴할수록 좋다
3. 양은 많을수록 좋다

식당의 순서를 정렬하는 코드를 c++로 작성해 주세요!!

```c++
#include <iostream>
#include <vector>

struct store {
    int distance;
    int price;
    int qty;
    store(int d, int p, int q)
        : distance(d), price(p), qty(q)
    {}
};

std::vector<store> datas = {
	store(11, 5500, 2500),
	store(10, 4900, 100),
	store(13, 5000, 2000),
	store(13, 5000, 400),
	store(12, 5000, 7000),
	store(11, 4900, 1500),
	store(10, 5000, 100),
	store(12, 4900, 500),
	store(12, 4900, 107),
	store(13, 5500, 4000),
	store(13, 5000, 2000),
	store(11, 5000, 199),
	store(11, 5500, 1000),
	store(10, 5000, 1000),
	store(13, 4900, 3000),
	store(11, 5500, 3500),
	store(10, 5000, 700),
	store(11, 5000, 1000),
	store(12, 5500, 100)
};

int main()
{
	/* type here... */
	
	for (auto d : datas)
	{
		std::cout << d.distance << "km ";
		std::cout << d.price << "krw ";
		std::cout << d.qty << "qty " << std::endl;
	}
	return 0;
}
```

정답:
```
10km 4900krw 100qty
10km 5000krw 1000qty
10km 5000krw 700qty
10km 5000krw 100qty
11km 4900krw 1500qty
11km 5000krw 1000qty
11km 5000krw 199qty
11km 5500krw 3500qty
11km 5500krw 2500qty
11km 5500krw 1000qty
12km 4900krw 500qty
12km 4900krw 107qty
12km 5000krw 7000qty
12km 5500krw 100qty
13km 4900krw 3000qty
13km 5000krw 2000qty
13km 5000krw 2000qty
13km 5000krw 400qty
13km 5500krw 4000qty
```

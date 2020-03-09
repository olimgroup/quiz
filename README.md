# QUIZ 

## 1. Syntax Checker 

괄호가 올바르게 쓰였는지 확인하는 로직을 만들려고 합니다. 
괄호는 대괄호, 중괄호, 소괄호 세가지가 있으며 주어지는 스트링이 괄호가 올바르게 사용되었으며 true, 아니면 false를 리턴하는 함수를 작성하세요. 
예시:  
| input          | output                                     |
|----------------|--------------------------------------------|
| [[(){}]]       | true                                       |
| (()))          | false                                      |
| )(())[]{}      | false                                      |
| ({[}])         | false                                      |
| [{(([{[]}])))] | true                                       |

## 2. Raccoon
너구리 한쌍은 한달 후에 다른 새끼 너구리 한쌍을 낳습니다. 
이 새끼 너구리 한쌍은 한달동안 성체가 되며 성체가 된 너구리 한쌍은 다시 한달 후에 다른 새끼 너구리 한쌍을 낳습니다. 
이미 성체가 된 너구리 부부는 달마다 새끼 너구리를 한쌍씩 낳는다고 가정할때, n달 후의 너구리 수를 구하는 함수를 작성하세요. 
(단, 이 너구리들은 죽지 않습니다.) 

예시: 
| input(n달후)   | output(마리 수)                            |
|----------------|--------------------------------------------|
| 0              | 2                                          |
| 1              | 4                                          |
| 4              | 16                                         |

## 3. 집뷰가 필요한 이유
오프라인 매장이 문을 닫아서 상담원들은 직접 고객을 만나러 각지를 방문해야하는 상황이 되었습니다. 
이들이 최소한의 이동시간으로 고객을 만날 수 있도록 최소 이동시간을 구하는 함수를 작성하세요. 
입력은 고객 수만큼의 방문지 리스트가 주어지며, 각 방문지에서는 다른 방문지로 이동할 시에 소요되는 이동시간이 다시 리스트로 주어집니다. 
예시: 
[  
    [0,  611,  648],  
    [611,  0,  743],  
    [648, 743, 0] 
] 
정답: 1259 

[  
    [0, 326, 503, 290],  
    [326, 0, 225, 395],  
    [503, 225, 0, 620],  
    [290, 395, 620, 0] 
] 
정답: 841

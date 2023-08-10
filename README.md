# translateDnD
- 번역이 되지 않은 dnd계열 게임을 번역할수 있도록 하기 위한 mini project

## now
- 첫번째 베이스모델을 EleutherAI사의 polyglot-ko-1.3b모델로 선정, multilingual 모델 중 한국어 성능이 좋다고 평가되는 모델
- llama시리즈를 고려 해봤지만 토크나이저 성능에 관한 의문이 있어 향후과제로 함
- dnd 계열 게임에서 text를 추출할수 있는지 확인중

## road map
- 1. polyglot 계열 모델 중 3090으로 fine-tuning(lora 포함)가능한 모델 결정(매개변수가 최대한 많은 것으로)  
- 2. 선택된 모델로 영한 번역 llm으로 훈련(fine-tuning)
    - 일단 데이터 베이스는 [[link](https://huggingface.co/datasets/squarelike/sharegpt_deepl_ko_translation)]
- 3. 기 번역된 dnd 게임에서 영어text와 한글 text 추출
- 4. 추출된 데이터로 영한번역기로 훈련된 모델 fine-tuning
- 5. 번역되지 않은 dnd 게임의 script 번역 시도

## inform
- llm fine-tuning에 관해 공부하면서 진행하는 mini project입니다. 
- 저작권 문제로 데이터셋은 공개되지 않을 수도 있습니다. 
- 모델 성능이 괜찮아도, 마찮가지로 저작권 문제로 모델이 공개되지 않을 수도 있습니다. 
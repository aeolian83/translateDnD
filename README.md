# translateDnD
- 번역이 되지 않은 dnd계열 게임을 번역할수 있도록 하기 위한 mini project

## done
- polyglot-ko-1.3b를 장문번역 한영 데이터베이스 squarelike/sharegpt_deepl_ko_translation[[link](https://huggingface.co/datasets/squarelike/sharegpt_deepl_ko_translation)]로 fine-tuning 완료
- 발더스 게이트2에서 한영 dialog 추출 완료(tlk 파서: [[link](https://github.com/3zhang/TLK-v1-file-parser-for-Python)])

## now
- polyglot-ko-5.8b를 장문번역 한영 데이터베이스 squarelike/sharegpt_deepl_ko_translation로 fine-tuning 중
- 번역질이 더 좋다는 발더스 게이트1 영한 dialog 수배중

## future work
- llama 시리즈로 영한 번역이 가능한지 확인

## road map
- 1. polyglot 계열 모델 중 3090으로 fine-tuning(lora 포함)가능한 모델 결정(매개변수가 최대한 많은 것으로)  
- 2. 선택된 모델로 영한 번역 llm으로 훈련(fine-tuning)
    - 일단 데이터 베이스는 [[link](https://huggingface.co/datasets/squarelike/sharegpt_deepl_ko_translation)]
- 3. 기 번역된 dnd 게임에서 영어text와 한글 text 추출
- 4. 추출된 데이터로 영한번역기로 훈련된 모델 fine-tuning
- 5. 번역되지 않은 dnd 게임의 script 번역 시도

## aeolian83/poly-ko-1.3b-translate
- EleutherAI/polyglot-ko-1.3b을 squarelike/sharegpt_deepl_ko_translation으로 영한 번역만 가능하도록 fine-tuning한 모델
- QRoLA기법으로 fine-tunnig
### 훈련 정보
- GPU: RTX3090 1대
- Epoch: 1
- learning-rate: 3e-4
- batch_size: 3
- Lora r: 8
- Lora target modules: query_key_value
![loss그래프](./img/polyglot-ko-1.3b-translate-1epoch.png)

# Inform
- llm fine-tuning에 관해 공부하면서 진행하는 mini project입니다. 
- 레퍼런스[https://github.com/jwj7140/Gugugo]
- 저작권 문제로 데이터셋은 공개되지 않을 수도 있습니다. 
- 모델 성능이 괜찮아도, 마찮가지로 저작권 문제로 모델이 공개되지 않을 수도 있습니다. 
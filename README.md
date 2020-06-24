# cola-komoran-python-client

## 라이브러리 설치

```sh
pip install https://github.com/euclidsoft/cola-komoran-python-client/archive/master.zip
```

## 샘플 코드

```python
from cola_komoran_python_client import ray_init, ray_shutdown, summarize_batch_with_ray

ray_init()  # 처음 1회만 수행해주세요.

# ray를 활용한 summarize 수행합니다. tqdm은 내부적으로 수행됩니다.
# tqdm을 수행하지 않으려면 with_tqdm=False 인자를 지정해주세요.
keyword_list = summarize_batch_with_ray(sentence_list_series)

ray_shutdown()  # 모든 작업이 끝내거나, ray cluster를 초기화시키고자 할 때
```


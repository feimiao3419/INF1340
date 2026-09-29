# data/

把数据集文件（CSV、JSON 等）放在这个文件夹。

上传后在 Colab 里用 raw URL 读取：

```python
import pandas as pd
url = "https://raw.githubusercontent.com/feimiao3419/INF1340/main/data/<文件名>.csv"
df = pd.read_csv(url)
```

注意：

- 本仓库是 public 的，**不要上传含个人隐私或未授权公开的数据**
- 单文件建议不超过 25 MB；更大的数据建议直接用原始出处的链接

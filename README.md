# INF1340 — Programming for Data Science

Course material for INF1340H1, Fall 2026, University of Toronto, Faculty of Information.

## 仓库结构 Repository layout

```
├── data/        # 数据集 Data files (CSV, JSON, etc.)
├── notebooks/   # Colab notebooks
└── README.md
```

## 在 Colab 中读取本仓库的数据 Reading data from this repo in Colab

不需要挂载 Google Drive，直接用 raw URL：

```python
import pandas as pd

url = "https://raw.githubusercontent.com/feimiao3419/INF1340/main/data/<文件名>.csv"
df = pd.read_csv(url)
df.head()
```

在 GitHub 文件页面点 **Raw** 按钮即可复制对应文件的 URL。

## 在 Colab 中打开 notebook Open a notebook in Colab

把 URL 中的 `github.com` 替换为 `colab.research.google.com/github` 即可，例如：

```
https://colab.research.google.com/github/feimiao3419/INF1340/blob/main/notebooks/data_loading_template.ipynb
```

或在 Colab 里 File → Open notebook → GitHub，输入 `feimiao3419/INF1340`。

## 协作 Collaboration

- 直接编辑：让仓库主人在 Settings → Collaborators 里加你
- 或者 fork 后提 Pull Request

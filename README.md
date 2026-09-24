# 堅奇門 · KinQiMen

Python 奇門遁甲排盤系統（基於 [kentang2017/kinqimen](https://github.com/kentang2017/kinqimen) 的可運行副本）

支援：**時家 / 刻家 / 金函玉鏡日家**，**拆補法 / 置閏法**

線上演示：https://kinqimen.streamlitapp.com

## 完整源碼同步方法（推薦）

目前倉庫已初始化。請在本地執行以下命令，把原倉庫完整可運行代碼推到本倉庫：

```bash
# 1. 克隆原項目
git clone https://github.com/kentang2017/kinqimen.git kinqimen-src
cd kinqimen-src

# 2. 改遠程為你的倉庫
git remote set-url origin https://github.com/gugezhanghu101233-rgb/kinqimen.git

# 3. 強制推送（覆蓋當前初始化內容）
git push -u origin master --force
```

推送完成後，本倉庫即擁有完整可運行代碼（含 `kinqimen.py`、`app.py`、`config.py`、`angan.py`、`jieqi.py` 等）。

## 本地運行

```bash
pip install -r requirements.txt
# 或核心庫：
pip install sxtwl kinqimen

# Web 界面（Streamlit）
streamlit run app.py
```

## 代碼調用示例

```python
from kinqimen import kinqimen

year, month, day, hour, minute = 2024, 6, 15, 14, 30

# 時家奇門（1=拆補, 2=置閏）
result = kinqimen.Qimen(year, month, day, hour, minute).pan(1)

# 刻家奇門
result = kinqimen.Qimen(year, month, day, hour, minute).pan_minute(2)

# 金函玉鏡日家
result = kinqimen.Qimen(year, month, day, hour, minute).gpan()
```

## 原項目說明

原作者：kentang2017  
原倉庫：https://github.com/kentang2017/kinqimen  
PyPI：https://pypi.org/project/kinqimen/

本倉庫僅作學習與備份用途，請遵循原項目許可協議。

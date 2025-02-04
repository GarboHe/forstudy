**一个用于爬取并导出瑞典 SSSB 租房网站数据的 Python 脚本。**  

## ✨ 功能  
- 🔍 **自动爬取** SSSB 网站上的可租房源信息  
- 📊 **数据导出** 支持 CSV 格式，方便后续分析  
- 🔄 **自动翻页** 直到获取所有房源数据  
- 🏡 **数据包含**：  
  - 📍 地址  
  - 🏠 房间类型  
  - 🏙️ 区域  
  - 💰 租金  
  - 📈 关注人数  

---

## 🛠 安装 & 运行  

### 1️⃣ 安装依赖  
确保你已经安装了 `Python 3` 和 `pip`，然后运行：  
```bash
pip install -r requirements.txt
```  

> **注意**: 你需要**下载并指定** `chromedriver.exe` 的路径。  

### 2️⃣ 替换 `chromedriver.exe` 文件路径  
打开 `读取网页-改进版.py`，找到以下代码：  
```python
chrome_driver_path = 'D:/Program Files (x86)/path/chromedriver.exe'  # 替换为你的路径
service = Service(chrome_driver_path)
```
将 `'D:/Program Files (x86)/path/chromedriver.exe'` **替换为你的实际 ChromeDriver 路径**，例如：  
```python
chrome_driver_path = 'C:/Users/你的用户名/Downloads/chromedriver.exe'
```

### 3️⃣ 运行脚本  
```bash
python 读取网页-改进版.py
```
运行后，数据将被自动爬取并保存到 `output.csv`。  

---

## 📌 代码结构  
```
📂 项目目录  
├── 读取网页-改进版.py   # 主脚本  
├── requirements.txt    # 依赖库  
└── output.csv          # 爬取的数据  
```  

---

## ⚠️ 注意事项  
- 该工具使用 **Selenium**，需要安装 `Google Chrome` 和 `chromedriver`。  
- 默认使用**无头模式**运行 Chrome，如需可视化运行，删除：  
  ```python
  options.add_argument('--headless')
  ```
- 由于爬取网页涉及隐私和法律问题，请**遵守目标网站的 robots.txt 规则**。  

---

## 📜 许可证  
本项目基于 **MIT License** 开源。  


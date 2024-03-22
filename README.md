# future_cta
future cta strategy backtest

版本呢： python 3.11
数据来源： akshare
本地数据库： mongodb

future_cta/  
├── data/                     # 数据存储目录  
│   └── contract_data.csv       # 从Akshare获取期货合约数据  
├── backtest/                      # 源代码目录  
│   ├── fetch_data/     # 数据获取模块  
│   │   └── data_retriever.py  # akshare
│   │   └── data_clean.py  # 数据清洗，合成连续合约
│   │   └── data_clean.py  # 数据储存，本地数据库等
│   ├── strategy/ # CTA信号模块 , 放置于VNPY测试
│   │   ├── intraday_cta.py   # 日内技术指标计算函数 （分钟）
│   │   ├── day_cta.py   # 日技术指标计算函数  
│   │   └── charting.py     # 图表绘制函数  
│   ├── fundamental_analysis/ # 基本面分析模块  
│   │   └── cta_factor.py  # CTA因子基本面分析
│   ├── analysis_report/    # 分析报告模块  
│   │   └── report_generator.py  # 可视化和数据统计
│   └── main.py             # 项目主入口文件  
├── config.py               # 配置文件  
├── requirements.txt        # 项目依赖文件  
└── .gitignore              # Git忽略文件

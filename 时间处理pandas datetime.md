# Python-skills-for-financial-analysis

时间处理
pandas datetime

# datetime 格式转换, Convert the type from **object** to **datetime**: <br/>
apple.Date = pd.to_datetime(apple.Date)

# 将 Date 列设为 index, set Date as index: <br/>
apple = apple.set_index("Date")

# 对索引进行排序, Sort The DataFrame based on Date columns: <br/>
apple.sort_index(ascending = True)

# 以月为单位对数据采样并获取mean() Resample the data based the offset,get the mean of data : <br/>
BM — bussiness month end frequency: <br/>
apple_month = apple.resample("BM").mean(): <br/>
apple_month.head()

# DataFrame从一列datetime提取三列年月日
yq_df['date'] = yq_df['date'].astype('str')<br/>
yq_df['date'] = pd.to_datetime(yq_df['date'])<br/>
yq_df['year'] = yq_df['date'].dt.year<br/>
yq_df['month'] = yq_df['date'].dt.month<br/>
yq_df['day'] = yq_df['date'].dt.day<br/>
print(yq_df)

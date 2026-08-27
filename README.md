# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY
# Name:Shreenidhi S
# Register no:212225040410
# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
data={
    'Month':['Jan','Feb','March','April','May','June','July','Aug','Sep','Oct','Nov','Dec'],
    'Laptop':[120,135,150,145,170,180,190,175,200,220,250,280],
    'Mobile':[200,220,210,240,260,270,290,300,310,330,350,380],
    'Tablet':[80,90,100,95,110,120,130,125,140,150,160,180],
    'Accessories':[150,160,170,180,190,200,210,220,230,240,260,280]
}
df=pd.DataFrame(data)
df
```

<img width="801" height="530" alt="Screenshot 2026-08-27 161815" src="https://github.com/user-attachments/assets/acd14231-c027-424e-89ea-c3c3fb825a35" />
import matplotlib.pyplot as plt

```
plt.plot(df['Month'],df['Laptop'])
plt.title('Monthly Laptop sales')
plt.xlabel('Month')
plt.ylabel('Number of Units Sold')
plt.show()
```

<img width="642" height="495" alt="Screenshot 2026-08-27 161822" src="https://github.com/user-attachments/assets/2654ae98-073f-42dd-8fc8-12c67fc42c89" />

```
plt.plot(df['Month'],df['Laptop'],marker='o',label='Laptop')
plt.plot(df['Month'],df['Mobile'],marker='o',label='Mobile')
plt.title('Monthly Product Sales')
plt.xlabel('Month')
plt.ylabel('Units Sold')
plt.legend()
plt.grid()
plt.show()
```

<img width="907" height="533" alt="Screenshot 2026-08-27 161841" src="https://github.com/user-attachments/assets/5d0759ae-ddb3-4029-ac25-e15dab7e95ea" />

```
product_sales={
    'Laptop':df['Laptop'].sum(),
    'Mobile':df['Mobile'].sum(),
    'Tablet':df['Tablet'].sum(),
    'Accessories':df['Accessories'].sum()

}
products=list(product_sales.keys())
sales=list(product_sales.values())
colors=['skyblue','yellow','lightgreen','pink']
plt.bar(products,sales,color=colors)
plt.title('Total sales by product')
plt.xlabel('Product')
plt.ylabel('Total Sales')
plt.show()
```

<img width="996" height="661" alt="Screenshot 2026-08-27 161848" src="https://github.com/user-attachments/assets/b619688f-28ec-47c4-b41b-54ff15bb41bd" />
colors=['green','red','blue','yellow']

```
plt.barh(products,sales,color=colors)
plt.title('Total sales by product')
plt.xlabel('Total units sold')
plt.ylabel('Product')
plt.show()
```

<img width="691" height="538" alt="Screenshot 2026-08-27 161905" src="https://github.com/user-attachments/assets/6a7a5cc7-0214-40e1-bd03-1f1442f11ec0" />

```
plt.bar(df['Month'],df['Laptop'],label='Laptop')
plt.bar(df['Month'],df['Mobile'],bottom=df['Laptop'],label='Mobile')
plt.title('Monthly Product Sales')
plt.xlabel('Month')
plt.ylabel('Units Sold')
plt.legend()
plt.show()
```

<img width="807" height="505" alt="Screenshot 2026-08-27 161857" src="https://github.com/user-attachments/assets/e71c6095-6e76-4622-a039-1d378f2a9543" />

```
plt.fill_between(df['Month'],df['Laptop'],alpha=0.5,color="pink")
plt.title(' Laptop Sales trend')
plt.xlabel('Month')
plt.ylabel('Units Sold')
plt.show()
```

<img width="693" height="490" alt="Screenshot 2026-08-27 161912" src="https://github.com/user-attachments/assets/3e5fdd9d-0175-49c1-8bdb-230e9f9f646d" />

```
plt.stackplot(df['Month'],df['Laptop'],df['Mobile'],df['Tablet'],df['Accessories'],labels=['Laptop','Mobile','Tablet','Accessories'])
plt.title('Monthly Product Sales')
plt.xlabel('Month')
plt.ylabel('Units Sold')
plt.legend(loc='upper left')
plt.show()
```

<img width="946" height="521" alt="Screenshot 2026-08-27 161918" src="https://github.com/user-attachments/assets/e137d14f-7981-405d-9187-68fcef55b8f7" />

```
order_sales={
    10,12,15,18,20,22,25,28,30,32,35,38,40,42,45,48,50,52,55,60,65,70,75,80,85,90,100}
    plt.hist(order_sales,bins=8)
plt.title('Distribution of Order Sales')
plt.xlabel('Units per order')
plt.ylabel('Frequency')
plt.show()
```

<img width="937" height="567" alt="Screenshot 2026-08-27 161926" src="https://github.com/user-attachments/assets/70f805c4-8ac2-4e76-861c-69205cc0191c" />

```
plt.hist(df['Laptop'],bins=5)
plt.title('Distribution of Laptop Sales')
plt.xlabel('Number of laptops Sold')
plt.ylabel('Frequency')
plt.show()
```

<img width="797" height="485" alt="Screenshot 2026-08-27 161931" src="https://github.com/user-attachments/assets/434c4735-7bd9-43bb-8fed-908f101b9247" />

```
plt.hist(df['Laptop'], bins=5, alpha=0.5, label='Laptop')
plt.hist(df['Mobile'], bins=5, alpha=0.5, label='Mobile')
plt.hist(df['Tablet'], bins=5, alpha=0.5, label='Tablet')

plt.title('Distribution of Product Sales')
plt.xlabel('Units Sold')
plt.ylabel('Frequency')

plt.legend()
plt.show()
<img width="825" height="581" alt="Screenshot 2026-08-27 161937" src="https://github.com/user-attachments/assets/087bbf5c-955e-48fe-93c4-bb6edb289a9a" />
plt.pie(
    sales,
    labels=products,
    autopct='%1.1f%%'
)
plt.title('Product Sales Distribution')
plt.show()
```

<img width="798" height="495" alt="Screenshot 2026-08-27 161942" src="https://github.com/user-attachments/assets/5ce982a4-7d92-44c8-abc4-8d1eeedb8c68" />

```
import pandas as pd
import matplotlib.pyplot as plt

data = {
    'Product': ['Laptop', 'Mobile', 'Tablet', 'Accessories'],
    'Sales': [288, 350, 180, 260]
}

df = pd.DataFrame(data)

explode = [0, 0.1, 0, 0]

colors = ['gold', 'skyblue', 'lightgreen', 'orange']

plt.pie(
    df['Sales'],
    labels=df['Product'],
    colors=colors,
    autopct='%1.1f%%',
    explode=explode,
    startangle=90,
    shadow=True,
    textprops={'fontsize': 11},
    wedgeprops={'width': 0.5}
)

plt.title('Product Sales Distribution')
plt.axis('equal')
plt.show()
```

<img width="887" height="733" alt="Screenshot 2026-08-27 161957" src="https://github.com/user-attachments/assets/a40f994f-508e-46ee-9ef1-3440231631fa" />

```
sizes = [215, 130, 245, 220]
labels = ['Python', 'C++', 'Ruby', 'Java']
colors = ['gold', 'yellowgreen', 'lightcoral', 'lightskyblue']
explode = (0, 0.4, 0, 0.5)

plt.pie(
    sizes,
    explode=explode,
    labels=labels,
    colors=colors,
    autopct='%1.1f%%',
    shadow=True
)

plt.axis('equal')
plt.show()
```

<img width="627" height="575" alt="Screenshot 2026-08-27 162005" src="https://github.com/user-attachments/assets/82d1f6ef-b389-48e8-aea5-056445accec0" />
import pandas as pd

```
import matplotlib.pyplot as plt

data = {
    'Product': ['Laptop', 'Mobile', 'Tablet', 'Accessories'],
    'Sales': [120, 150, 180, 200]
}

df = pd.DataFrame(data)
df

sales = [120, 135, 150, 145, 170, 180,
         190, 175, 200, 220, 250, 280,
         310, 125, 140, 155, 165, 185]

         
         plt.boxplot(sales)
plt.title('Distribution of Sales')
plt.ylabel('Sales')
plt.show()
```


<img width="1141" height="798" alt="Screenshot 2026-08-27 162013" src="https://github.com/user-attachments/assets/f5320d6e-3599-4151-a451-99927d91d1a5" />

```
plt.boxplot(sales)
plt.title('sales distribution with outlier')
plt.ylabel('sales')
plt.show()
```

<img width="828" height="472" alt="Screenshot 2026-08-27 162035" src="https://github.com/user-attachments/assets/f263f3ff-831f-49ef-accd-e58ba99fca89" />

```
laptop=[120,135,150,145,170,180,190,175,200]
mobile=[200,220,210,240,260,270,290,300,310]
tablet=[80,90,100,95,110,120,130,125,140]


plt.boxplot(
    [laptop,mobile,tablet],
    labels=['Laptop','Mobile','Tablet']
)
plt.title('Sales Distribution by Product')
plt.xlabel('Product')
plt.ylabel('Sales')
plt.show()
```

<img width="1352" height="742" alt="Screenshot 2026-08-27 162046" src="https://github.com/user-attachments/assets/fcf1f3ab-f947-4e66-afe2-35ea993b3ffd" />

```
plt.boxplot(
    [laptop, mobile, tablet],
    tick_labels=['Laptop', 'Mobile', 'Tablet'],
    vert=False
)

plt.title('Sales Distribution by Product')
plt.xlabel('Units Sold')
plt.show()
```

<img width="791" height="610" alt="Screenshot 2026-08-27 162053" src="https://github.com/user-attachments/assets/b6d29e1d-54e6-454c-b5fe-6a520c1bd9d2" />

```
plt.boxplot(
    sales,
    showmeans=True
)

plt.title('Sales Distribution')
plt.ylabel('Sales')
plt.show()
```

<img width="820" height="603" alt="Screenshot 2026-08-27 162058" src="https://github.com/user-attachments/assets/cb8da8d0-1bc8-4449-9bcd-3f32434410b1" />

```
plt.boxplot(
    [laptop, mobile, tablet],
    tick_labels=['Laptop', 'Mobile', 'Tablet'],
    vert=False
)

plt.title('Sales Distribution by Product')
plt.xlabel('Units Sold')
plt.show()
```

<img width="877" height="607" alt="Screenshot 2026-08-27 162103" src="https://github.com/user-attachments/assets/dca48a3d-1a77-4e61-859f-9c7e39ec6a34" />

```
import pandas as pd
import matplotlib.pyplot as plt

data={
    'Month':['Jan','Feb','March','April','May','June','July','Aug','Sep','Oct','Nov','Dec'],
    'Laptop':[120,135,150,145,170,180,190,175,200,220,250,280],
    'Mobile':[200,220,210,240,260,270,290,300,310,330,350,380],
    'Tablet':[80,90,100,95,110,120,130,125,140,150,160,180],
    'Accessories':[150,160,170,180,190,200,210,220,230,240,260,280]
}
df=pd.DataFrame(data)

plt.scatter(df['Laptop'],df['Mobile'])
for i in range(len(df)):
  plt.annotate(
  df['Month'][i],
  (df['Laptop'][i],df['Mobile'][i])
)
plt.title('Laptop vs Mobile Sales')
plt.xlabel('Laptop Sales')
plt.ylabel('Mobile Sales')
plt.show()
```

<img width="968" height="800" alt="Screenshot 2026-08-27 162109" src="https://github.com/user-attachments/assets/1549ffe0-4040-4f51-9352-858442e8048a" />

```
import pandas as pd
import matplotlib.pyplot as plt

data={
    'Month':['Jan','Feb','March','April','May','June','July','Aug','Sep','Oct','Nov','Dec'],
    'Laptop':[120,135,150,145,170,180,190,175,200,220,250,280],
    'Mobile':[200,220,210,240,260,270,290,300,310,330,350,380],
    'Tablet':[80,90,100,95,110,120,130,125,140,150,160,180],
    'Accessories':[150,160,170,180,190,200,210,220,230,240,260,280]
}
df=pd.DataFrame(data)

plt.scatter(
    df['Laptop'],
    df['Month'],
    color='blue',
    s=100,
    label='Laptop'

)
plt.scatter(
  df['Mobile'],
  df['Month'],
  color='red',
  s=100,
  label='Mobile'
)
plt.title('Laptop vs Mobile Sales')
plt.xlabel('Month')
plt.ylabel('sales')
plt.title('laptop vs Mobile monthly sales')
plt.legend()
plt.grid(True)
plt.show()
```

<img width="867" height="812" alt="Screenshot 2026-08-27 162119" src="https://github.com/user-attachments/assets/5649b93f-16b2-43d0-8fe7-7891488aec93" />

```
fig, ax = plt.subplots(2, 2, figsize=(12, 8))

ax[0, 0].plot(df['Month'], df['Laptop'])
ax[0, 0].set_title('Laptop Sales')

product_sales={
    'Laptop':df['Laptop'].sum(),
    'Mobile':df['Mobile'].sum(),
    'Tablet':df['Tablet'].sum(),
    'Accessories':df['Accessories'].sum()
}
products=list(product_sales.keys())
sales=list(product_sales.values())

ax[0, 1].bar(products, sales)
ax[0, 1].set_title('Total Product Sales')

ax[1, 0].hist(order_sales, bins=8)
ax[1, 0].set_title('Order Distribution')

advertising_costs = [50, 70, 90, 110, 130, 150, 170, 190, 210, 230, 250, 270]
sales_from_advertising = [100, 150, 180, 220, 250, 280, 300, 330, 350, 380, 400, 420]

ax[1, 1].scatter(advertising_costs, sales_from_advertising)
ax[1, 1].set_title('Advertising vs Sales')
ax[1, 1].set_xlabel('Advertising Cost')
ax[1, 1].set_ylabel('Sales From Advertising')

plt.tight_layout()
plt.show()
```

<img width="1516" height="807" alt="Screenshot 2026-08-27 162130" src="https://github.com/user-attachments/assets/dfce7417-5658-40de-bc07-52fc062b5180" />

# Result:
The Data Visualization using matplot python library is implemented successfully.


